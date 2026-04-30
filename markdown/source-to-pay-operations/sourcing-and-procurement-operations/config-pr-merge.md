---
title: Configure conditions for merging purchase requisitions
description: Configure the conditions under which the purchase requisitions \(PR\) should be merged.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure conditions for merging purchase requisitions

Configure the conditions under which the purchase requisitions \(PR\) should be merged.

## Before you begin

Role required: sn\_shop.shopping\_hub\_admin or sn\_shop.procurement\_administrator

## About this task

The conditions that you set determine when to merge the purchase requisitions.

**Note:** The existing default scenarios for merging purchase requisitions and purchase lines remain valid and function as they did previously. For more information, see [Purchase requisition merging](../concept/purchase-requisition-merging.md).

You cannot merge the PRs that are in any of the following states:

-   Closed Complete
-   Closed Canceled
-   Closed Rejected
-   Pending Submission
-   Pending Cancellation
-   Pending Revision
-   Pending Supplier Confirmation

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Administration** &gt; **ShoppingHub Configuration**.

2.  In the Configuration type column, select **Merge configuration**.

    The **Configuration type** field is set to **Merge configuration** by default.

    ![Purchase requisition merge conditions.](../image/pr-merge.png)

3.  The **Active** check box is selected by default.

    Deselect the **Active** check box if you want to deactivate the merge configuration.

4.  On the **Merge conditions** tab, fill in the fields.

<table id="table_jzv_bqw_ycc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Purchase table

</td><td>

Read-only field that shows the Purchase Requisition \[sn\_shop\_purchase\_requisition\] table.

</td></tr><tr><td>

Merge type

</td><td>

The type of merge that you want to allow. The options are:-   **Allow both**: Enables you to configure both auto merge and manual conditions.

Displays both the Auto merge conditions and Manual merge conditions sections.

-   **Allow only auto merge**: Enables you to configure only the auto-merge conditions.

Displays the Auto merge conditions section.

-   **Allow only manual merge**: Enables you to configure only the manual-merge conditions.

Displays the Manual merge conditions section.

</td></tr><tr><td>

Matching conditions

</td><td>

Include custom fields that you want as part of the condition builder.Move the required fields from the Available list to the Selected list.

Let’s consider a scenario with two PRs, PR1 and PR2. For these PRs to be merged, the values in the fields defined in the matching conditions must be identical in both PRs. For example, if the matching conditions contain the Cost center and Legal entity fields, PR1's cost center must match PR2's cost center, and the same goes for their legal entity values.

</td></tr><tr><td>

Auto merge conditions

</td><td>

Allows you to define conditions to automatically merge PRs, based on any of the fields available for a PR.This section becomes available after you select the **Allow only auto merge** option in the **Merge type** field.

</td></tr><tr><td>

Manual merge conditions

</td><td>

Allows you to define conditions to manually merge PRs, based on any of the fields available for a PR.This section becomes available after you select the **Allow only manual merge** option in the **Merge type** field.

</td></tr></tbody>
</table>5.  Select **Update**.


**Parent Topic:**[Configuring Sourcing and Procurement Operations](../concept/configuring-spo.md)

**Related topics**  


[Install Sourcing and Procurement Operations](activate-finance-spend-central.md)

[Setting up primary data for ShoppingHub](../reference/set-up-master-data-shopping-hub.md)

[Configure punchout for third-party site purchases](configure-supplier-punchout.md)

[Customize your top suppliers on Shopping Hub](customize-top-suppliers.md)

[Service portal configuration for ShoppingHub](../concept/service-portal-configuration-for-shoppinghub.md)

[Install ShoppingHub Mobile](install-shoppinghub-mobile.md)

[Advanced Work Assignment for Source-to-Pay Operations](../concept/awa-spo.md)

