---
title: Workflow roles
description: Certain roles are required to use workflows.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow roles

Certain roles are required to use workflows.

**Important:** As of the Zurich release, new customers no longer receive the legacy workflows created and published by ServiceNow, Inc.. All legacy workflow functionality has been replaced by Workflow Studio content. Only customers who upgraded from prior versions retain the ability to use and edit existing legacy workflows. While all customers retain the ability to create legacy workflows, you are strongly encouraged to instead use Workflow Studio to create process automation content. Only Workflow Studio will receive new features and enhancements.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and contact your account representative.

<table id="table_g2t_fww_1r"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[snc\_required\_script\_writer\]

</td><td>

Provides access to the Workflow UI and allows scripting.

</td></tr><tr><td>

Activity creator

 \[activity\_creator\]

</td><td>

Creates and edits custom workflow activities, reuses custom activity data, and manages activity packs downloaded from the ServiceNow Store.

</td></tr><tr><td>

Web service administrator

 \[web\_service\_admin\]

</td><td>

Accesses and uses REST and SOAP messages in the [Orchestration activity designer](../../orchestration-activity-designer/concept/c_WorkflowActivityDesigner.md). Creates and edits custom activities that use the REST web service and SOAP web service templates.

</td></tr><tr><td>

Workflow administrator

 \[workflow\_admin\]

</td><td>

Checks out, creates, edits, publishes, and deletes graphical workflows.**Warning:** Granting this role to a user is equivalent to giving the user the admin role, because workflow Script activities bypass access controls and grant access to all tables and database operations. Script activities do not bypass application scope settings.

</td></tr><tr><td>

Workflow creator

 \[workflow\_creator\]

</td><td>

Checks out, creates, edits, and deletes graphical workflows.**Warning:** Granting this role to a user is equivalent to giving the user the admin role, because workflow Script activities bypass access controls and grant access to all tables and database operations. Script activities do not bypass application scope settings.

</td></tr><tr><td>

Workflow publisher

 \[workflow\_publisher\]

</td><td>

Checks out with force checkout option, validates, publishes, and deletes graphical workflows.

</td></tr></tbody>
</table>**Parent Topic:**[Workflow administration](../concept/c_WorkflowAdministration.md)

