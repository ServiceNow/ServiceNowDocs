---
title: Sales Cart integration with external ordering systems
description: External ordering systems can connect to the Sales Cart through the Sales Cart REST API, and can create, retrieve, update, and submit carts without depending on the Business Portal user interface. Carts created externally run the same pricing, validation, and order conversion logic as carts built in the Business Portal, so customers can view and work with them in either system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-cart-external-integration.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Configuring Sales Cart for Business Portal, Business Portal, Configure, Sales Customer Relationship Management]
---

# Sales Cart integration with external ordering systems

External ordering systems can connect to the Sales Cart through the Sales Cart REST API, and can create, retrieve, update, and submit carts without depending on the Business Portal user interface. Carts created externally run the same pricing, validation, and order conversion logic as carts built in the Business Portal, so customers can view and work with them in either system.

## Integration model

An external ordering system is a third-party consumer portal, partner portal, telecommunications self-service portal, or headless ordering application that calls the Sales Cart REST API on behalf of an account contact or consumer. The term describes a category of API client, not a specific certified product or vendor connector.

The external system provides the ordering experience. The ServiceNow instance remains the system of record for the cart and stores the cart header, lines, characteristics, and pricing adjustments in the following tables:

-   Sales Cart \(sn\_sales\_cart\)
-   Sales Cart Line Item \(sn\_sales\_cart\_line\_item\)
-   Sales Cart Line Characteristic \(sn\_sales\_cart\_line\_characteristic\)
-   Sales Cart Pricing Adjustment \(sn\_sales\_cart\_pricing\_adjustment\)

Carts created externally use the same records and cart processing as carts created in the Business Portal, so a cart can be viewed and worked with in either channel. This means the instance needs only one cart model: pricing, validation, and order conversion behave the same way whether the cart came from the Business Portal or an external system, so you don't rebuild that behavior for every external channel you connect.

For endpoint paths, parameters, request and response schemas, and error handling, see the [Sales Cart REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/sales-cart-api.md) reference.

## How the integration works

The following table summarizes what the external ordering system does at each stage, and how Sales Cart responds.

|Stage|External ordering system|Sales Cart|
|-----|------------------------|----------|
|Identify the customer|Sends either an account and contact, or a consumer.|Authorizes the caller and applies record-level access.|
|Build the cart|Creates a cart, sends product offerings and configurations, or adds lines to an existing Draft cart.|Stores the line hierarchy, validates that offerings exist, and resolves default values.|
|Maintain checkout|Retrieves the cart, updates existing lines, assigns supported line-level billing details, or removes top-level lines.|Enforces Draft-state rules and recalculates pricing unless pricing is suppressed.|
|Submit the order|Calls the submit-order operation when checkout is complete.|Validates top-level configurations, converts the cart to an order, and marks the cart Complete.|

## Access and cart ownership

Requests from an external system are authorized against the access control that protects the Sales Cart REST endpoints. The following roles are permitted to call them:

-   sn\_customerservice.customer for a caller acting on behalf of an account contact
-   sn\_customerservice.consumer for a caller acting on behalf of a consumer

A caller without either role can't reach the Sales Cart REST endpoints, regardless of the cart data requested.

If you have configured a CPQ instance, then Sales Cart installs a role hierarchy in which the cart integrator role contains the cart editor role, and the cart editor role contains the cart viewer role. These roles control access to the cart records themselves, separately from the access control on the REST endpoints.

Callers see only the carts their own access permits. When an integrated system retrieves a list of carts, the caller's record-level access is applied to the query, so the response contains only carts that the caller is permitted to read. A filter supplied by the caller narrows that result further, but it can't widen it. For a consumer caller, a query rule narrows that access further to carts opened by the consumer's own user record, so a consumer reaches only their own carts.

## Cart states and when a cart accepts changes

Draft is the only state in which a cart accepts changes. The following operations require the cart to be in the Draft state:

-   Adding line items to an existing cart.
-   Updating cart header attributes or line items.
-   Deleting the cart or one of its line items.
-   Submitting the cart to create an order.

A request against a cart in any other state is rejected and the cart is left unchanged. After a cart is submitted and the order is created, the cart state is set to Complete and the cart no longer accepts changes. A new cart is created for the next order.

## One draft cart per customer

A cart belongs to either an account contact or a consumer, never both. An integrated system provides an account and contact for an account cart, or a consumer for a consumer cart, and retrieving the cart afterward returns the same identity model it was created with.

An account contact or consumer can have only one Draft cart at a time. If a create request finds an existing Draft cart, the response identifies it. Include the draft cart's sysId in the request to add lines instead of creating a duplicate.

## Key values auto-resolved by the Sales Cart

An integrated system doesn't have to supply every cart header value. The Sales Cart derives common header information from the account or consumer data, as described in the following table.

|Value|Behavior|Admin action|
|-----|--------|------------|
|Currency|Resolved when omitted. Account carts use account data; consumer carts derive it from the consumer country.|Maintain the source data or provide currency where the API supports it.|
|Price list|Always resolved. Account carts use the default for account, currency, and contact; consumer carts use the default for currency. A caller-supplied price list is replaced.|Update the underlying default price-list or currency data to influence resolution.|
|Shipping and billing address|Resolved when omitted. When shipping location is omitted, addresses come from the account primary address or consumer data. Billing is set to the shipping address.|Maintain a usable address or supply supported address values.|
|State|Defaults to Draft when omitted.|Design the integration around the Draft life cycle.|

**Note:** Accounts used by the integration need currency, a usable address, and data from which a default price list can be resolved. Missing values can produce incomplete cart or pricing data.

## Line item structure and validation

Sales Cart checks every product offering against the product catalog. If an offering can't be found, the complete request is rejected and the response identifies the invalid offerings so the client can correct and resend them.

Line items form a hierarchy. A configured product creates a top-level line with child lines beneath it. Only top-level lines can be deleted directly, and deleting one also deletes its child lines. A request to delete a child line on its own is rejected. To change a configuration, the integrated system updates the top-level line instead of editing its children.

Adding a line, changing a line, and removing a line are three separate operations. The update operation changes lines that are already in the cart, matching each one by its sys\_id, and it applies to line attributes, characteristics, and pricing adjustments. It doesn't add or remove lines. An integrated system that sends a line the cart doesn't already hold has that line ignored rather than created, so adding a line uses the create operation and removing one uses the delete operation. Characteristics are replaced, not merged. When updating a line, include the complete characteristic set. A characteristic omitted from the request is removed from the line.

Price list is resolved by the ServiceNow pricing engine. Pricing is recalculated after cart changes are committed, so the client does not make a separate pricing call. Deleting a line recalculates the header totals. Changing any cart-header value reprices every line, even when the change only corrects an address.

Set skip\_pricing to true and send the supported pricing values. Sales Cart saves the supplied values but still resolves currency and price list.

The following table lists the fields that aren't saved to the database when skip\_pricing is set to true.

|Value when pricing is suppressed|Result|
|--------------------------------|------|
|Cumulative monthly recurring price on a line|Not saved because the pricing engine writes it.|
|Cumulative annual recurring price on a line|Not saved because the pricing engine writes it.|
|Periodicity on a line|Not saved.|
|Monthly, annual, and one-time header totals|Read as zero under the delivered suppressed-pricing behavior.|
|Header total amount|Rolls up from the caller-supplied cumulative net price.|
|Characteristics and pricing adjustments|Saved whether pricing runs or is suppressed.|

**Note:** Use skip\_pricing only when the external system owns price and downstream consumers can work with the documented persistence and total behavior.

## Carrying billing account and payment profile to a line item

Keep billing context attached to the product by assigning a billing account and payment profile to each cart line. Line-level storage supports a cart in which different products use different billing accounts, such as one product billed to a personal account and another to a business account.

|Field|Behavior|
|-----|--------|
|Billing account|If the line has an account, the billing account must belong to it. For a consumer cart without a line account, the billing account must belong to that consumer. If neither applies, any active billing account is allowed.|
|Payment profile|The payment profile must belong to the billing account already assigned to the line. Until a billing account is selected, any active payment profile is allowed. Assign the billing account first to maintain consistency.|

The billing account and payment profile are copied when a cart is cloned and carried to the matching order line when the cart is submitted. This preserves the supported billing selection for downstream order processing without manual re-entry.

The cart-line fields appear only when the Billing Account \(sn\_billing\_account\) application is installed. They carry to order line items only when Order Management is installed. Without these applications, the remaining cart integration continues to work and the two fields are absent.

## Submitting a cart to create an order

Submit a valid Draft cart to create an order. Before conversion, Sales Cart validates every top-level line against the configuration rules for its product. If a line fails validation, no order is created and the cart stays in the Draft state. Correct the affected lines and submit again. When validation succeeds, the records map as showing in the following table.

|Cart record|Order record|
|-----------|------------|
|Cart header|Order header|
|Cart line item|Order line item|
|Cart line characteristic|Order line characteristic|
|Cart pricing adjustment|Order pricing adjustment|

Line-level values, including billing account and payment profile, stay with their line. The sn\_l2c\_cart\_to\_order entity mapping governs the conversion. After the order is created, the cart becomes Complete.

**Related topics**  


[Components installed with Sales Cart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/components-installed-with-sales-cart-plugin.md)

