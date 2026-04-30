---
title: Customize the dynamic related records for a playbook page
description: Customize the dynamic related records for a playbook page to display in the contextual side panel in CSM Configurable Workspace. These records dynamically change depending on the context of the current record or playbook activity.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Playbook pages, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Customize the dynamic related records for a playbook page

Customize the dynamic related records for a playbook page to display in the contextual side panel in CSM Configurable Workspace. These records dynamically change depending on the context of the current record or playbook activity.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

The definitions for the related records aren't active by default. You must activate these definitions if you want them to appear in the related records.

Any change made to the customer service case dynamic related record context applies to all extensions of the customer service case. For creating custom context, see [Configure related record contexts](configure-related-record-contexts.md).

You must define an EVAM \(Entity View Action Mapper\) view configuration for the tables in addition to setting up Dynamic Related Records. For more information, see [Define an EVAM view configuration](define-csm-evam-view-config.md).

## Procedure

1.  Navigate to **All** &gt; **Dynamic Related Records** &gt; **Related Record Contexts**.

2.  Select **Related Record Contexts** for either the Onboarding, Complaint, or Product Support table.

3.  Activate all the related record definitions for the Onboarding, Complaint, or Product Support case.

    For more information, see [Dynamic related records](../concept/csm-contextual-related-records.md).

4.  Select **Update**.

    The following table shows the Dynamic Related Record list for each case type.

<table id="table_ryz_p54_1xb"><thead><tr><th>

Case type

</th><th>

Dynamic related record

</th></tr></thead><tbody><tr><td>

Customer service case

</td><td>

-   Blocked By
-   Related Parties
-   Social Logs
-   Appointments
-   Requests
-   Special Handling Notes
-   Child Cases
-   Knowledge Gaps
-   Attached Knowledge
-   Task Skills
-   Emails
-   Draft Emails
-   Interactions
-   Tasks
-   Work Orders
-   Install base
-   Escalations
-   Service Level Agreement \(SLA\)


</td></tr><tr><td>

Complaint case

</td><td>

-   Emails
-   Blocked By
-   Involved Parties
-   Tasks
-   Sold Product
-   Active Contracts
-   Active Entitlement
-   Related Cases


</td></tr><tr><td>

Onboarding case

</td><td>

-   Emails
-   Blocked By
-   Related Cases
-   Additional members
-   Tasks
-   Sold Product
-   Active Contracts
-   Approvers


</td></tr></tbody>
</table>
**Related topics**  


[Configure dynamic related records](../concept/dynamic-related-records-configure.md)

[Configure related record definitions](configure-related-record-definitions.md)

