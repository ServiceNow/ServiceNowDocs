---
title: Results of canceling a contract renewal process
description: Cancelling a contract renewal process results in a change in the state of Contract, Contract Renewal Request, Contract Renewal Request Lines, and Contract Renewal tasks.
locale: en-US
release: yokohama
product: Contract Management
classification: contract-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Contract renewal workflow, Contract Management, IT Asset Management]
---

# Results of canceling a contract renewal process

Cancelling a contract renewal process results in a change in the state of Contract, Contract Renewal Request, Contract Renewal Request Lines, and Contract Renewal tasks.

<table id="table_cnw_jrt_mtb"><thead><tr><th>

Canceled item

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Contract Renewal Request

</td><td>

-   The entire renewal request is canceled.
-   The substate of the contract that is being renewed is cleared.
-   All the draft contracts are canceled.

</td></tr><tr><td>

Contract Renewal Request Line

</td><td>

-   The Contract Renewal Request Line is canceled.
-   When all Contract Renewal Request Lines are canceled, the Contract Renewal Request is canceled.
-   The renewal of immediate child draft contracts is canceled.

</td></tr><tr><td>

Contract Renewal Task

</td><td>

-   The Contract Renewal Task and the Contract Renewal Request Line are canceled.
    -   If the Contract Renewal Request has only one Contract Renewal Request Line, the stage of the Contract Renewal Request changes to Canceled.
    -   If the Contract Renewal Request has multiple Contract Renewal Request Lines, the stage of the Contract Renewal Request doesn’t change.
-   The renewal of immediate child draft contracts is canceled.
-   The state of the draft contract changes to Canceled.
-   The state of the tasks that are already closed does not change.
-   The state of the open tasks changes to Closed Incomplete.
-   Rate cards are attached to the draft contract become inactive.
-   The state of the contract that was being renewed moves to the original state and the substate is cleared.
-   The associated entitlements with the Contract Renewal Task are removed.

</td></tr><tr><td>

Contract

</td><td>

-   The renewal of immediate child contracts is canceled when child contracts are included in the Contract Renewal Request.
-   The Contract Renewal Request Line is canceled.
-   Any initiated Contract Renewal Request by this contract is canceled.
-   The purchase order of the contract and immediate child contracts is canceled.

</td></tr></tbody>
</table>