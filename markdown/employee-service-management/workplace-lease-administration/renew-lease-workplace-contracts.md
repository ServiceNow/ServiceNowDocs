---
title: Renew workplace contract in Core UI
description: Renew a workplace contract after you have created it, when it is approaching expiration, or when it has expired.
locale: en-US
release: australia
product: Workplace Lease Administration
classification: workplace-lease-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage workplace contracts from Core UI, Manage workplace contracts, Workplace Lease Administration, Workplace Service Delivery, Employee Service Management]
---

# Renew workplace contract in Core UI

Renew a workplace contract after you have created it, when it is approaching expiration, or when it has expired.

## Before you begin

Role required: sn\_wsd\_la.manager or sn\_wsd\_la.admin

## About this task

You will receive an email notification when contracts are close to their expiration date.

You can renew a contract that meets the following conditions:

-   The state is Active or Expired
-   The substate is None or Rejected

## Procedure

1.  Navigate to **All** &gt; **Workplace Lease Administration** &gt; **Workplace Contracts**.

2.  Select a contract in the Active or Expired state.

3.  Select **Renew**.

4.  On the form, fill in the fields.

<table id="table_l2j_qkr_gr"><thead><tr><th>

Field

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Approver

</td><td>

User to approve or reject the contract.

</td></tr><tr><td>

Options

</td><td>

Length of time for the renewal in years.

</td></tr><tr><td>

Renewal Start Date

</td><td>

Date on which the renewed contract takes effect.

</td></tr><tr><td>

Renewal End Date

</td><td>

Date on which the renewed contract expires.

</td></tr><tr><td>

Cost Adjustment Type

</td><td>

Type of cost adjustment applied to the renewed contract. The available values are None, Fixed, Manual, or CPI.

</td></tr><tr><td>

Cost adjustment amount

</td><td>

Numerical increase or decrease in price of the renewed contract. A negative number indicates a decrease in price.

 You can specify a value for **Cost Adjustment** or **Cost Adjustment Percentage** but not both.

</td></tr><tr><td>

Cost Adjustment Percentage

</td><td>

Percentage increase or decrease in the price of the renewed contract. A negative percentage indicates a decrease in price.

 You can specify a value for **Cost Adjustment** or **Cost Adjustment Percentage** but not both.

</td></tr></tbody>
</table>5.  Save your changes.

    -   To save all entered data, select **Submit for Review**.

        The contract is sent to the specified approver and the substate is changed to Under Review.

    -   To save all entered data, select **Save**.

        You can submit the contract for renewal later. The substate is changed to Awaiting Review.

6.  Change any information on the Contract form.

7.  Select **Update**.


## What to do next

If you selected the **Save** option, ensure that you select **Renew** when you’re ready to submit the contract renewal for approval.

**Parent Topic:**[Manage workplace contracts from Core UI](../concept/manage-contracts-from-core-ui.md)

**Related topics**  


[Adjust workplace contract in Core UI](adjust-lease-contract.md)

[Cancel workplace contract in Core UI](cancel-lease-contract.md)

