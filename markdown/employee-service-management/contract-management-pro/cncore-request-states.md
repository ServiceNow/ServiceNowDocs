---
title: Contract Management Pro states and status
description: Contract Management Pro requests follow a specific life cycle and move through a series of states.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Contract Management Pro reference, Contract Management Pro, Employee Service Management]
---

# Contract Management Pro states and status

Contract Management Pro requests follow a specific life cycle and move through a series of states.

The following field values change based on the progress of the approval.

-   **State**: State of the contract request.
-   **Contract status**: Additional info that describes the status based on the previous action.

## State

**State**: When an approval is in the requested state, the state of the contract reuqest is in **Awaiting approval**.

When an approvals are actioned, the state of the contract reuqest is in **Work in progress**.

## Contract status

**Contract status** \(For latest revision of the TPC\) In case of multiple document approval scenario, when the latest contract type revision or more than one contract type revision is sent for approval:

-   When for at least 1 document \(latest version\) revision approval status is **Requested**, the contract status is rolled up as **Awaiting approval**.
-   When none of the approvals is in the **Requested** status, with

    -   At least one approval is in the **rejected** state, the contract status is **Document approval rejected**.
    -   None of the approvals is in the rejected state with atleast one approval in **Approved** state, then the contract status is **Document approved**.
    -   None of the approvals is in the **rejected** state or the **approved** state, with one approval in the **Cancelled** state, then the contract status is **Document approval cancelled**
    -   None of the approvals is in the **rejected**, **cancelled**, or **approved** state with no new approvals, then the contract status is **Work in progress**
    **Note:** For single document scenario, the same status are applicable.


**Note:** For cumulative approvals in the multiple-document scenario, the approval status of latest revision is considered for populating the contract status.

**Parent Topic:**[Contract Management Pro reference](../concept/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro](cncore-comp-ccore.md)

[Components installed with Contract Workspace](cncore-comp-contract-workspace.md)

[Components installed with Analytics Pack for Contract Management Pro](cncore-comp-analytics-pack-cmpro.md)

[Clause Variation form](cncore-cv-form.md)

[Contract Configuration form](cncore-contract-config-form.md)

[Properties installed to configure expiry notifications](cncore-properties-installed.md)

[Properties installed to configure contracts integrations](cncore-properties.md)

[Expiring Contracts Condition form fields](cncore-email-notif-expcont-form.md)

[Action assignment form](cmpro-actn-assignment-form.md)

[UFX Add on Event mapping form](cmpro-ufx-event-map-form.md)

[Obligation form](cncore-obligation-form.md)

[Obligation Management notifications](cncore-ob-mgmt-notification.md)

