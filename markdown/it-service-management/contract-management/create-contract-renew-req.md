---
title: Create a contract renewal request
description: Create a contract renewal request for contracts that are nearing their expiry date or are already expired.
locale: en-US
release: australia
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Contract renewal workflow, Contract Management, Asset Management, IT Service Management]
---

# Create a contract renewal request

Create a contract renewal request for contracts that are nearing their expiry date or are already expired.

## Before you begin

Role required: contract\_system\_admin, asset, contract\_manager\(core UI and Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## About this task

You can create a renewal request only for Maintenance, Warranties, Subscriptions, and Software Licenses. If you have installed only the Software Asset Management application, you can renew Subscriptions, Maintenance, and Software Licenses contracts. If you have installed only the Hardware Asset Management application, you can renew Maintenance and Warranties contracts.If you have installed only the Enterprise Asset Management application, you can renew Maintenance and Warranties contracts.

## Procedure

1.  Open the list of contracts that you want to renew.

    -   If you are using the core UI, navigate to **All** &gt; **Contracts** &gt; **Contract Renewal**.
    -   If you are using the Hardware Asset Workspace, open the Contract management view and then select the **Overview** tab. In the Contract overview section, locate the Expiring contract widget.

        Alternatively, open the Contract management view and then select a tab for a contract type, such as **All** or **Maintenance**.

    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view and then select the **Overview** tab. In the Contract overview section, locate the Expiring contract widget.

        Alternatively, open the Contract and lease management view and then select a tab for a contract type, such as **All** or **Maintenance**.

2.  Select the contract that you want to renew with a type of either Maintenance, Warranties, Subscriptions, Software Licenses, or Service.

3.  Click **Renew** for the selected contract.

4.  Submit the contract renewal request.

    -   If you are using the core UI or Hardware Asset Workspace,click **OK**.

        The contract renewal request includes the following information:

        -   An auto-generated unique number
        -   The Stage indicating the type of task in the contract renewal process
        -   Reference to the contract for which you have requested the renewal
        -   Date and time when the request was created
    -   If you are using the Enterprise Asset Workspace, the Renew the Contract dialog box appears. In the dialog box, fill in the fields and then click **Submit for review**.

<table id="table_lw3_mbh_2xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approver

</td><td>

User who approves or rejects the contract renewal request.

</td></tr><tr><td>

Options

</td><td>

Duration of the contract renewal.

</td></tr><tr><td>

Renewal start date

</td><td>

Date on which the contract renewal begins.

</td></tr><tr><td>

Renewal end date

</td><td>

Date on which the contract renewal ends.

</td></tr><tr><td>

Cost adjustment type

</td><td>

Type of cost adjustment that is applied to the contract. The options are **Fixed**, **Manual**, and **CPI** \(consumer price index\).

</td></tr><tr><td>

Cost adjustment percentage

</td><td>

Percentage increase or decrease in the contract price. To indicate a decrease in price, enter a negative percentage.**Note:** You can specify either a cost adjustment percentage or cost adjustment amount on a contract renewal request. You cannot specify both.

</td></tr><tr><td>

Cost adjustment amount

</td><td>

Numerical increase or decrease in the contract price. To indicate a decrease in price, enter a negative number.**Note:** You can specify either a cost adjustment percentage or cost adjustment amount on a contract renewal request. You cannot specify both.

</td></tr></tbody>
</table>5.  Select the **Contract Renewal Request Lines** tab to view the parent Contract Renewal Request Line or existing and valid child contracts under the parent contract.

    A contract renewal request line is created for each contract that is being renewed.

6.  View all open contract renewal flow tasks and the details of each contract renewal task by selecting the **Open Tasks** tab.

7.  View all contract renewal flow tasks and the details of each contract renewal task by selecting the **All Tasks** tab.


## Result

The substate of the contract that is being renewed is set to **Renewal in process**.

## What to do next

If the parent contract doesn't have child contracts, select the [Build renewal task](fill-cont-renew-info.md).

If the parent contract has child contracts, select the [Contract selection task](select-contract.md).

