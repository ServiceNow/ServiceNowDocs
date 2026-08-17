---
title: Transaction-level system fields
description: Reference for the system-provided fields at the transaction \(header\) level in Quote Experience, including variable names, descriptions, who can modify each field, and default values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-header-level-system-fields.html
release: australia
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 7
breadcrumb: [Fields, CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Transaction-level system fields

Reference for the system-provided fields at the transaction \(header\) level in Quote Experience, including variable names, descriptions, who can modify each field, and default values.

## Field naming conventions

Quote Experience uses a consistent prefix convention for field variable names.

-   System-generated header-level fields use the prefix `txn.` followed by the field name — for example, `txn.id`.
-   Custom header-level fields created by administrators use the prefix `txn.custom.` followed by the field name — for example, `txn.custom.quoteName`.

For line-level field naming conventions, see [Transaction line-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-line-level-system-fields.md).

## Modifiable by

The **Modifiable by** column in the field tables uses the following values.

-   **System**

    The field value is set only by the application. Users cannot edit system-modifiable fields on the quote layout, and administrators cannot set field values using determination rules.

-   **User**

    Any user with the appropriate permissions can update the field value. Determination rule actions can also modify user-modifiable fields.


## System-provided header-level fields

The following fields are available in all Quote Experience implementations.

|Variable name|Description|Default value|
|-------------|-----------|-------------|
|`txn.id`|UUID of the transaction. Uniquely identifies the transaction record.|Auto-generated on creation. Modifiable by: System|
|`txn.account.id`|ID of the account used when the transaction was created.|Empty. Expected to be passed in on create. Modifiable by: User|
|`txn.opportunity.id`|ID of the opportunity through which the transaction was created.|Empty. Expected to be passed in on create. Modifiable by: User|
|`txn.pricebook.id`|Pricebook associated with the products on the transaction.|Empty. A blank value is interpreted as the default pricebook. Modifiable by: User|
|`txn.pricing.currencyCode`|Currency code associated with the products on the transaction.|Empty. A blank value uses the base currency for the tenant. Modifiable by: User|
|`txn.created`|Timestamp of when the transaction was created.|Auto-generated on creation. Modifiable by: System|
|`txn.createdBy`|Name of the user who created the transaction.|Auto-generated on creation. Modifiable by: System|
|`txn.modified`|Timestamp of the most recent modification to the transaction.|Auto-generated on each update. Modifiable by: System|
|`txn.modifiedBy`|Name of the user who made the most recent modification to the transaction.|Auto-generated on each update. Modifiable by: System|
|`txn.externalId`|Unique identifier used to reference the transaction in external connections and integrations.|Empty. Expected to be passed in on create. Modifiable by: User|
|`txn.stage`|Current stage of the transaction in the quote lifecycle.|Auto-generated. Value depends on the stage configuration. Modifiable by: System|
|`txn.persona`|Persona of the user who performed the most recent request on the transaction.|Auto-generated. Value depends on the persona configuration. Modifiable by: System|

## ServiceNow SFA Fields

"The following fields are installed when ServiceNow SFA is enabled. Fields noted as "Set from opportunity" on create are populated automatically from the source opportunity when a quote is created.

|Variable name|Description|Default value|
|-------------|-----------|-------------|
|`txn.displayNumber`|Transaction display number. The user-facing quote number.|Empty. Set during create quote. Modifiable by: System|
|`txn.sysId`|ServiceNow system ID of the transaction.|Empty. Set during create quote. Modifiable by: System|
|`txn.shortDescription`|Short description of the transaction.|Empty. Set from opportunity on create. Modifiable by: System|
|`txn.contact`|Contact name associated with the transaction.|Empty. Set from opportunity on create. Modifiable by: System|
|`txn.assignedTo`|User assigned to the transaction.|Empty. Set from opportunity on create. Modifiable by: System|
|`txn.assignmentGroup`|Assignment group for the transaction.|Empty. Set from opportunity on create. Modifiable by: System|
|`txn.startDate`|Start date for the transaction.|Empty. Set from opportunity on create. Modifiable by: System|
|`txn.endDate`|End date for the transaction.|Empty. Set from opportunity on create. Modifiable by: System|
|`txn.term`|Contract term in months.|Empty. Set from opportunity on create. Modifiable by: System|
|`txn.channel`|Records the channel through which the transaction originated.|`agent_assist` Modifiable by: System|
|`txn.transactionType`|Type of transaction. Values: New, Amendment, Renewal.|Empty. Modifiable by: System|
|`txn.transactionAction`|Used to derive the transaction type. Values: Add, Change.|`add` Modifiable by: System|
|`txn.isAutoGeneratedForRenewal`|Indicates whether this transaction was automatically generated for a renewal based on the expiry of the original contract.|`false` Modifiable by: System|
|`txn.isAutoRenewContract`|Indicates whether the contract resulting from this transaction should trigger automatic renewal workflows.|`false` Modifiable by: System|
|`txn.source.quote`|Reference to the quote from which this transaction was consolidated, if applicable.|Empty. Modifiable by: System|
|`txn.source.contract`|Reference to the contract used in the amendment or renewal workflow that this transaction is part of.|Empty. Modifiable by: System|

## ServiceNow Pricing fields

The following fields are installed when ServiceNow Pricing is enabled.

|Variable name|Description|Default value|
|-------------|-----------|-------------|
|`txn.pricing.extendedPrice`|Total One-Time price. An aggregate of the one-time price across all lines.|Empty. Modifiable by: System|
|`txn.pricing.cost`|Total One-Time Cost. An aggregate of the one-time cost across all lines.|Empty. Modifiable by: System|
|`txn.pricing.margin.amount`|Total One-Time Margin. Calculated as Total One-Time Price minus Total One-Time Cost.|Empty. Modifiable by: System|
|`txn.pricing.margin.percentage`|Total One-Time Margin %. Calculated as Total One-Time Margin divided by Total One-Time Price × 100.|Empty. Modifiable by: System|
|`txn.pricing.netCost`|Total Cost. An aggregate of the cumulative net cost across all lines.|Empty. Modifiable by: System|
|`txn.pricing.margin.total.amount`|Total Margin Amount. Calculated as Total Amount minus Total Cost.|Empty. Modifiable by: System|
|`txn.pricing.margin.total.percentage`|Total Margin %. Calculated as Total Margin Amount divided by Total Amount × 100.|Empty. Modifiable by: System|
|`txn.pricing.annualPriceRecurring`|Total Annual Price. An aggregate of the cumulative annual recurring price across all lines.|0 Modifiable by: System|
|`txn.pricing.netPriceRecurring`|Total Monthly Price. An aggregate of the cumulative monthly recurring price across all lines.|0 Modifiable by: System|
|`txn.pricing.costRecurring`|Total Monthly Cost. An aggregate of the cumulative monthly recurring cost across all lines.|0 Modifiable by: System|
|`txn.pricing.marginRecurring.amount`|Total Monthly Margin. Calculated as Total Monthly Price minus Total Monthly Cost.|0 Modifiable by: System|
|`txn.pricing.marginRecurring.percentage`|Total Monthly Margin %. Calculated as \(Total Monthly Price minus Total Monthly Cost\) divided by Total Monthly Price.|Empty. Modifiable by: System|
|`txn.pricing.netNew.amount`|Total Net New Amount. An aggregate of the cumulative net price from new root lines.|0 Modifiable by: System|
|`txn.pricing.source.contract.amount`|Original Contract Amount. An aggregate of the renewal amount from lines. Represents the contract value from the original transaction being renewed.|0 Modifiable by: System|
|`txn.pricing.delta.upsellDownsellAmount`|Total Upsell/Downsell Amount. An aggregate of the upsell or downsell amount from lines.|0 Modifiable by: System|
|`txn.pricing.adjustment.renewalBasis`|Renewal Adjustment Basis. The starting renewal price from which to apply adjustments.|`list_price` Modifiable by: System|
|`txn.pricing.adjustment.renewalType`|Renewal Adjustment Type. The type of adjustment for renewal. Options: Markup %, Markdown %. Read-only when Renewal Adjustment Basis is List Price.|Empty. Set from opportunity on create. Modifiable by: System|
|`txn.pricing.adjustment.renewalValue`|Renewal Adjustment Value. The amount of adjustment to apply to the renewal price, interpreted according to the Renewal Adjustment Type.|Empty. Modifiable by: System|
|`txn.costbook`|Reference to the cost book associated with the transaction. Set in the Pricing Service response.|Empty. Modifiable by: System|

## Approvals fields

The following field is installed when ServiceNow Approvals is enabled.

|Variable name|Description|Default value|
|-------------|-----------|-------------|
|`txn.approvalState`|Approval state of the transaction.|Empty. Modifiable by: System|

## PDF Document Generation fields

The following fields are installed when ServiceNow PDF Document Generation is enabled.

|Variable name|Description|Default value|
|-------------|-----------|-------------|
|`txn.docGen.template`|Document template selection for document generation.|Empty. Modifiable by: User|
|`txn.docGen.internalSigner`|Internal signer selection for document generation.|Empty. Modifiable by: User|
|`txn.docGen.externalSigner`|External signer selection for document generation.|Empty. Modifiable by: User|

## Partner Management fields

The following fields are installed when ServiceNow Partner Management is enabled.

|Variable name|Description|Default value|
|-------------|-----------|-------------|
|`txn.dealType`|Route to market / deal type of the transaction.|`direct` Modifiable by: User|
|`txn.routeToMarket`|Route to market of the transaction.|`direct` Modifiable by: User|
|`txn.channelPartner`|Channel partner associated with the transaction.|Empty. Modifiable by: User|

## Sync Quote to Opportunity fields

The following field is installed when ServiceNow Sync Quote to Opportunity is enabled.

|Variable name|Description|Default value|
|-------------|-----------|-------------|
|`txn.opportunity.isSynced`|Indicates whether the quote is synced to the source opportunity.|Empty. Modifiable by: System|

**Related topics**  


[Quote transaction fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-fields.md)

[Transaction line-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-line-level-system-fields.md)

[Date and time field fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-date-time-field-behavior.md)

