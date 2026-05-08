---
title: Using Contracts and Entitlements Workflows
description: Learn how contracts and entitlements using workflows enable you to create and manage customer contracts, customer contract lines, and entitlements.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer Contracts and Entitlements, Customer management, Use, Customer Service Management]
---

# Using Contracts and Entitlements Workflows

Learn how contracts and entitlements using workflows enable you to create and manage customer contracts, customer contract lines, and entitlements.

You can manage the life cycle of customer contracts and entitlements from offer creation to contract generation using contracts and entitlements workflows. Using workflows you can suspend, resume, cancel, and renew multiple entities at once. You can view customer contract lines as a hierarchical list that helps to view the parent and child relationship between line items. Customer Contracts and Entitlements supports variable and derived pricing models. Contracts and entitlements correctly reflect dynamically calculated prices, ensuring consistency with underlying pricing logic and improving accuracy across contract‑driven workflows. For more info, see Configuring derived pricing. You can also perform the following functions using workflows:

-   Create, suspend, resume, cancel, and renew customer contracts.
-   Create, modify, suspend, resume, cancel, and renew customer contract lines, and entitlements.

## Automatic renewal of customer contracts

While creating customer contracts from quote or orders, you can select the **Auto-renew contract** option on a quote or order to automatically renew the contracts. ​When you add or delete a contract line from these customer contracts, the renewed quotes and opportunities are updated. You can configure the auto-renewal date of the contract in the Customer Life Cycle Workflows Policy decision table. By default, you can choose to initiate the auto-renewal 90, 60, or 30 days before the contract end date, or on the contract creation date. For more info, see [Creating contracts and entitlements using workflows](create-cont-ent-workflows-csm.md).

![Auto-renew option](../images/auto-renew-quote.png "Automatic renewal for customer contracts on quotes")

In the Renewal adjustment basis field, you can select **List price** or **Contracted price**. Selecting List price renews the contract at the market price of the contract at the time of the renewal date.

![Renewal adjustment basis](../images/renewal-adjustment.png "Renewal adjustment basis")

Selecting Contracted price gives you the option to renew the contract at Markdown % or Markup % of the current contract price. For example, if you select **Markup %** field and you enter 10 in **Renewal adjustment value**, the customer contract is renewed at 10% above the current contract price.

![Renewal adjustment type](../images/renewal-adjustment-quote.png "Renewal adjustment type")

That exact renewal date and the renewal adjustments for that customer contract will be visible on the customer contract form in the **Auto renewal date** field.

![Auto renewal date on customer contract](../images/service-contract-auto-renew.png "Automatic renewal of customer contracts")

You cannot modify the renewal adjustment fields on the customer contract. You can only modify the renewal adjustment values on the quote and orders.

## Updating contract end date

During quote processing, the system alerts you when the contract end date is exceeding the product offering end date. When you submit quotes for approval, a dialog box appears alerting you. You can select the option **update contract end dates to match offering end dates** to match the contract end date to the product offering end date.

![Matching end dates.](../images/end-of-life-check.png "Matching the contract and product offering end dates")

If you do not select this option and approve the quote, the contract end date remains the same.

## Co-terminate quote lines

You can assign the same start and end dates to multiple quote lines while creating or renewing a quote. On the **Line items** tab on the quote details page, select multiple quote lines and then select **Co-terminate**. All the selected quote lines have the same start and end date.

![Co-terminate option.](../images/co-terminate-quotes.png "Co-terminate quote lines")

## Viewing price ramps

Customers can scale their purchases by adjusting the pricing and quantity throughout the contract or subscription term by using Ramps feature. For more info, see Add price ramps on a quote line item. You can view the price ramp details on the contract line. Only the active price ramp segment is displayed on the contract line. Select a contract line and select **Ramps** to view all the details of the price ramp for that contract line. You can view start and end date, term period, ramp type \(yearly or quarterly\), ramp segments, and Annual percentage increase \(API%\).

