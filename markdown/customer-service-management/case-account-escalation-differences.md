---
title: Case and account escalation differences
description: An overview of the differences between case escalations and account escalations.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Case and account escalation, Administer, Customer Service Management]
---

# Case and account escalation differences

An overview of the differences between case escalations and account escalations.

-   **Case escalations**: A customer service agent typically manages a case escalation and performs most of the problem resolution work, which is recorded in the case record. For case escalations, the escalation record is used primarily for status reporting purposes. The escalation SLA is also associated with the case record rather than the escalation record because that is where the agent provides regular updates.
-   **Account escalations**: An account escalation manager typically manages an account escalation because it is associated with multiple underlying cases. An account manager works with multiple case owners to resolve the customer escalation and uses the escalation record to consolidate the status of the associated cases and provide regular updates. Therefore, the SLA is associated with the escalation record.

<table id="table_kvh_gkf_5bb"><thead><tr><th>

Feature

</th><th>

Case Escalation

</th><th>

Account Escalation

</th></tr></thead><tbody><tr><td>

Relationships

</td><td>

Corresponds one-to-one to a case.

</td><td>

Corresponds one-to-one to an account. Users can link specific cases to the escalation record to indicate which cases are causing the escalation.

</td></tr><tr><td>

Templates

</td><td>

Uses case escalation templates.**Note:** When you select Case Escalation in the **Type** field, an additional checkbox field appears for **Add Case Assignment Group Manager to Approvers**.

</td><td>

Uses account escalation templates.

</td></tr><tr><td>

Approval workflow

</td><td>

Includes an option to automatically add the manager of the case assignment group to the approver list when using the default approval workflow.

</td><td>

Does not include an option to automatically add the manager of the case assignment group to the approver list because an account escalation can be associated with multiple cases.

</td></tr><tr><td>

Escalation assignment

</td><td>

Does not include a separate assignment. A case escalation corresponds to an individual case and the customer service agent manages the escalation.

</td><td>

Includes a separate assignment. An account escalation can have multiple associated cases that are assigned to different agents so the escalation record includes an **Assigned to** field. An account escalation is typically assigned to an escalation manager because account escalations are typically more serious than case escalations.

</td></tr><tr><td>

Watch list

</td><td>

Does not include an option to automatically add an account team to the escalation watch list.

</td><td>

Includes an option to automatically add an account team to the escalation watch list.

</td></tr><tr><td>

Escalation updates added to case

</td><td>

Updates to the escalation record are also added to the **Work notes** field on the corresponding case record.

</td><td>

Updates to the escalation record are not added to the account record.

</td></tr><tr><td>

SLAs

</td><td>

The case escalation SLAs provided with the escalation feature are attached to the case.

</td><td>

The account escalation SLAs provided with the escalation feature are attached to the account.

</td></tr></tbody>
</table>