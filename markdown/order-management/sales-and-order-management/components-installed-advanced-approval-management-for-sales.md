---
title: Components installed with Advanced Approval Management
description: Several types of components are installed with activation of the Advanced Approval Management plugin, including tables, scheduled jobs, and user roles.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-21"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management reference, Configure, price, quote, Reference, Sales and Order Management]
---

# Components installed with Advanced Approval Management

Several types of components are installed with activation of the Advanced Approval Management plugin, including tables, scheduled jobs, and user roles.

## Roles installed

<table id="table_yvf_2vh_g3c"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Approval rule admin\[sn\_adv\_appr\_mgmt.approval\_rule\_admin\]

</td><td>

Manages all aspects of approval workflows. Creates, updates, and deletes approval configurations, chains, approval trigger conditions, approval rules, and approval users and groups.

</td><td>

sn\_adv\_appr\_mgmt.approval\_rule\_writer

</td></tr><tr><td>

Approval rule writer\[sn\_adv\_appr\_mgmt.approval\_rule\_writer\]

</td><td>

Creates, updates, and views approval configurations, approval chains, approval trigger conditions, approval rules, and approval users and groups. An approval rule writer can't delete approval-related items.

</td><td>

sn\_adv\_appr\_mgmt.approval\_rule\_viewer

</td></tr><tr><td>

Approval rule viewer\[sn\_adv\_appr\_mgmt.approval\_rule\_viewer\]

</td><td>

Views approval configurations, approval chains, approval trigger conditions, approval rules, and approval users and groups.

</td><td>

None

</td></tr><tr><td>

Approval request approver\[sn\_adv\_appr\_mgmt.approval\_request\_approver\]

</td><td>

Views approval steps and approves approval requests for which they are an approver.

</td><td>

-   sn\_adv\_appr\_mgmt.approval\_request\_viewer
-   approver\_user \(if using My Approvals\)

</td></tr><tr><td>

Approval request writer\[sn\_adv\_appr\_mgmt.approval\_request\_writer\]

</td><td>

Creates and views approval requests.

</td><td>

\[sn\_adv\_appr\_mgmt.approval\_request\_viewer\]

</td></tr><tr><td>

Approval request viewer\[sn\_adv\_appr\_mgmt.approval\_request\_viewer\]

</td><td>

Views approval requests.

</td><td>

sn\_adv\_appr\_mgmt.approval\_rule\_viewer

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_ej2_glz_q3c"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approval Reminder Daily Processor

</td><td>

Sends reminders to approvers to accept or reject an approval request.

</td></tr></tbody>
</table>## Tables installed

<table id="table_cwf_2vh_g3c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approval Configurations\[sn\_adv\_appr\_mgmt\_approval\_configuration\]

</td><td>

Details of an approval workflow entity, for example quotes that need approvals.

</td></tr><tr><td>

Approval Trigger Conditions\[sn\_adv\_appr\_mgmt\_approval\_trigger\_condition\]

</td><td>

Conditions that trigger one or more approval requests. Conditions map to one or more approval rules.

</td></tr><tr><td>

Approval Rules\[sn\_adv\_appr\_mgmt\_approval\_rule\]

</td><td>

One or more approval rules associated to an approval trigger condition. Rules define steps in an approval process. A rule can have multiple users or groups as approvers, as well as dynamic approvers.

</td></tr><tr><td>

Approval Chains\[sn\_adv\_appr\_mgmt\_approval\_chain\]

</td><td>

A group of approval rules that run in a specified order sequentially. A chain can run one or more rules in sequence. Chains can run in parallel or sequentially.

</td></tr><tr><td>

Approval Users\[sn\_adv\_appr\_mgmt\_approval\_user\]

</td><td>

A list of users who can approve requests.

</td></tr><tr><td>

Approval Groups\[sn\_adv\_appr\_mgmt\_approval\_group\]

</td><td>

A list of groups that can approve requests.

</td></tr><tr><td>

Approval Reminders\[sn\_adv\_appr\_mgmt\_approval\_reminder\]

</td><td>

A list of reminder durations for an approval workflow entity.

</td></tr><tr><td>

Approval Rule Reminders\[sn\_adv\_appr\_mgmt\_approval\_rule\_reminder\]

</td><td>

A list of reminder durations for approval rules.

</td></tr><tr><td>

Approval Requests\[sn\_adv\_appr\_mgmt\_approval\_request\]

</td><td>

The approval request records created when an approval request is submitted.

</td></tr><tr><td>

Approval Steps\[sn\_adv\_appr\_mgmt\_approval\_step\]

</td><td>

The approval step records created for an approval request. The records contain the relevant approval rules, conditions, and chain details defined for an approval configuration. The Approval Steps table is extended from the Task \[task\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Advanced Approval Management reference](advanced-approval-management-reference.md)

