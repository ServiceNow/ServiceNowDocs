---
title: Approve or reject a workplace contract in Core UI
description: As a lease administrator or manager, you can approve or reject a workplace contract after it is submitted for review.
locale: en-US
release: zurich
product: Workplace Lease Administration
classification: workplace-lease-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with Workplace Lease Administration from the Core UI, Use, Workplace Lease Administration, Workplace Service Delivery, Employee Service Management]
---

# Approve or reject a workplace contract in Core UI

As a lease administrator or manager, you can approve or reject a workplace contract after it is submitted for review.

## Before you begin

Role required: sn\_wsd\_la.manager or sn\_wsd\_la.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Lease Administration** &gt; **Workplace Contracts**.

2.  Select a contract in the Requested state.

3.  Either approve or reject the contract.

    -   To approve the contract, select **Approve**.

        The contract substate changes to Approved.

    -   To reject the contract, select **Reject** and enter a rejection reason in the **Comments** field.

        The contract substate changes to Rejected.

4.  Select **Update**.


## Result

-   Contracts with the state set to Draft and a start date set in the future are kept in the Draft state until the start date is reached.
-   If the contract has a substate of Approved, the system changes the state to Active and removes the Substate value.
-   When a contract with a state of Draft and a start date set to a date in the past is approved, the State value is automatically set to Active and the Substate value is left empty.

**Parent Topic:**[Working with Workplace Lease Administration from the Core UI](../concept/use-lease-admin-core-ui.md)

**Related topics**  


[Create workplace contracts in Core UI](create-lease-contracts.md)

[Submit workplace contract for review in Core UI](submit-lease-contract-review.md)

