---
title: Add or remove entitlements for a contract renewal
description: Add or remove software entitlements that you want to include in the contract renewal process by using the Software assets selection task. You can also view the entitlements carried over to the new contract.
locale: en-US
release: australia
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contract renewal workflow, Contract Management, Asset Management, IT Service Management]
---

# Add or remove entitlements for a contract renewal

Add or remove software entitlements that you want to include in the contract renewal process by using the Software assets selection task. You can also view the entitlements carried over to the new contract.

## Before you begin

The Software Asset Management Professional \(com.snc.samp\) plugin must be activated.

Role required: contract\_system\_admin, sam\_user, contract\_manager

## About this task

The entitlements with the following license types are carried over to the new contract:

-   Perpetual and maintenance
-   Perpetual and software assurance
-   Only perpetual

## Procedure

1.  On the Contract Renewal Request Line form, select the Software assets selection task number.

2.  Create an entitlement if you don't have any entitlements carried over to the draft contract.

    1.  On the Contract Renewal Task form, select **Create Entitlement** in the **Planned Entitlements** tab.

    2.  On the Software Entitlement form, fill in the required fields.

        For more information, see [Software entitlement fields](https://www.servicenow.com/docs/access?context=software-entitlement-fields&version=australia&pubname=australia-it-asset-management&ft:locale=en-US).

    3.  Select **Save**.

        You can publish this entitlement after you complete the renewal request because this entitlement is associated with an existing renewal process.

    The entitlement is now listed in the Planned Entitlements list.

3.  Update the existing entitlements for the draft contract.

<table id="choicetable_ohx_k1c_qtb"><thead><tr><th align="left" id="d126611e134">

Interface

</th><th align="left" id="d126611e137">

Action

</th></tr></thead><tbody><tr><td id="d126611e143">

**Core UI**

</td><td>

1.  Select **Edit**.
2.  Indicate the entitlements that you want to cover by moving them to the **Planned Entitlements** or removing them.


</td></tr><tr><td id="d126611e167">

**Hardware Asset Workspace**

</td><td>

Add or remove entitlements to indicate the entitlements you want to cover.

 -   To add an entitlement, select **Add** and provide the required information.
-   To remove an entitlement, select it and select **Remove**.


</td></tr></tbody>
</table>4.  Select **Save**.

5.  Select **Close Task**.


## What to do next

[Update terms and conditions](update-terms-conditions.md)

