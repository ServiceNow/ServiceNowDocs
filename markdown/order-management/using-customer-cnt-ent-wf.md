---
title: Using Contracts and Entitlements Workflows
description: Learn how contracts and entitlements using workflows enable you to create and manage service contracts, service contract lines, and entitlements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/using-customer-cnt-ent-wf.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Using Contracts and Entitlements Workflows

Learn how contracts and entitlements using workflows enable you to create and manage service contracts, service contract lines, and entitlements.

You can manage the life cycle of customer service contracts and entitlements from offer creation to contract generation using contracts and entitlements workflows. Using workflows you can suspend, resume, cancel, and renew multiple entities at once. You can also perform the following functions using workflows:

-   Create, suspend, resume, cancel, and renew service contracts.
-   Create, modify, suspend, resume, cancel, and renew service contract lines, and entitlements.

## Automatic renewal of service contracts

While creating service contracts from quote or orders, you can select the **Auto-renew contract** option on a quote or order to automatically renew the contracts. ​When you add or delete a contract line from these service contracts, the renewed quotes and opportunities are updated. You can configure the auto-renewal date of the contract in the Customer Life Cycle Workflows Policy decision table. By default, you can choose to initiate the auto-renewal 90, 60, or 30 days before the contract end date, or on the contract creation date. For more info, see [Creating contracts and entitlements using workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/create-cont-ent-workflows-csm.md).

\[Omitted image "auto-renew-quote.png"\] Alt text: Auto-renew option

In the Renewal adjustment basis field, you can select **List price** or **Contracted price**. Selecting List price renews the contract at the market price of the contract at the time of the renewal date.

\[Omitted image "renewal-adjustment.png"\] Alt text: Renewal adjustment basis

Selecting Contracted price gives you the option to renew the contract at Markdown % or Markup % of the current contract price. For example, if you select **Markup %** field and you enter 10 in **Renewal adjustment value**, the service contract is renewed at 10% above the current contract price.

\[Omitted image "renewal-adjustment-quote.png"\] Alt text: Renewal adjustment type

That exact renewal date and the renewal adjustments for that service contract will be visible on the service contract form in the **Auto renewal date** field.

\[Omitted image "service-contract-auto-renew.png"\] Alt text: Auto renewal date on service contract

You cannot modify the renewal adjustment fields on the service contract. You can only modify the renewal adjustment values on the quote and orders.

## Updating contract end date

During quote processing, the system alerts you when the contract end date is exceeding the product offering end date. When you submit quotes for approval, a dialog box appears alerting you. You can select the option **update contract end dates to match offering end dates** to match the contract end date to the product offering end date.

\[Omitted image "end-of-life-check.png"\] Alt text: Matching end dates.

If you do not select this option and approve the quote, the contract end date remains the same.

## Co-terminate quote lines

You can assign the same start and end dates to multiple quote lines while creating or renewing a quote. On the **Line items** tab on the quote details page, select multiple quote lines and then select **Co-terminate**. All the selected quote lines have the same start and end date.

\[Omitted image "co-terminate-quotes.png"\] Alt text: Co-terminate option.

## Viewing price ramps

Customers can scale their purchases by adjusting the pricing and quantity throughout the contract or subscription term by using Ramps feature. For more info, see [Add price ramps on a quote line item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/add-price-ramps-on-a-quote-line-item.md). You can view the price ramp details on the contract line. Only the active price ramp segment is displayed on the contract line. Select a contract line and select **Ramps** to view all the details of the price ramp for that contract line. You can view start and end date, term period, ramp type \(yearly or quarterly\), ramp segments, and Annual percentage increase \(API%\).

-   **[Suspend a service contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-suspend-service-contract.md)**  
Suspend a service contract and its child service contract lines by creating an order on the CSM Configurable Workspace. Suspending a service contract suspends or disables the services specified in that service contract.
-   **[Modify a service contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-modify-service-contract.md)**  
Modify a service contract so that you can update its existing configurations.
-   **[Resume a service contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-resume-service-contract.md)**  
Resume a service contract and its child service contract lines by creating an order on the CSM Configurable Workspace. By resuming a service contract, you are restarting the services specified in that service contract.
-   **[Renew a service contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-renew-service-contract.md)**  
Renew a service contract on the CSM Configurable Workspace before the service contract expires.
-   **[Cancel a service contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-cancel-service-contract.md)**  
Create an order to cancel a service contract and its child service contract lines on the CSM Configurable Workspace. By canceling a service contract, you are terminating the services specified in that service contract.
-   **[Suspend a service contract line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-suspend-service-contract-line.md)**  
Suspend a service contract line and its child service contract lines by creating an order on the CSM Configurable Workspace. By suspending a service contract line, you are suspending or disabling the services and characteristics associated with that service contract line.
-   **[Modify a service contract line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-modify-service-contract-line.md)**  
Modify a service contract line so that you can update its existing configurations.
-   **[Resume a service contract line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-resume-service-contract-line.md)**  
Create an order to resume a service contract line and its child service contract lines on the CSM Configurable Workspace. By resuming a service contract line, you are restarting the services specified in that service contract line.
-   **[Renew a service contract line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-renew-service-contract-line.md)**  
Renew a service contract line on the CSM Configurable Workspace. You can renew the services specified in the service contract line and its associated child service contract lines and entitlements.
-   **[Cancel a service contract line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-cancel-service-contract-line.md)**  
Create an order to cancel a service contract line and its child service contract lines on the CSM Configurable Workspace. By canceling a service contract line, you are canceling or disabling the services and characteristics associated with that service contract line.
-   **[Upsell or Downsell a service contract line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-upsell-downsell-service-contract.md)**  
Upsell or downsell a service contract line on the CSM Configurable Workspace. You can reduce or increase the quantities of the products specified in the service contract line.
-   **[Modify an entitlement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-modify-entitlement.md)**  
Modify an entitlement associated to an account so that you can update its existing configurations.
-   **[Suspend an entitlement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-suspend-entitlement.md)**  
Suspend an entitlement by creating an order on the CSM Configurable Workspace. By suspending an entitlement, you are suspending or disabling the services and characteristics associated with that entitlement.
-   **[Resume an entitlement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-resume-entitlement.md)**  
Resume an entitlement by creating an order on the CSM Configurable Workspace. By resuming an entitlement, you are restarting the services and the characteristics specified in that entitlement.
-   **[Renew an entitlement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-renew-an-entitlement.md)**  
Renew an entitlement on the CSM Configurable Workspace.
-   **[Cancel an entitlement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-cancel-entitlement.md)**  
Cancel an entitlement by creating an order on the CSM Configurable Workspace. By canceling an entitlement, you are canceling or disabling the services and characteristics associated with that entitlement.
-   **[Add contract lines to a service contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/cce-add-contract-lines.md)**  
Add one or more contract lines to a service contract on the CSM Configurable Workspace.
-   **[Add Covered Products using Contracts and Entitlement Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/adding-cov-prod-cceworkflows.md)**  
Covered products refers to specific products or order line items that are included in a service contract. These items are linked to the contract to define what is covered for service or maintenance. Covered products can be directly tracked through the contract records, facilitating changes and visibility of what is covered.

**Parent Topic:**[Using Customer Contracts and Entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/using-post-sales-support.md)

