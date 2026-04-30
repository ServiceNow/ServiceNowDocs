---
title: Workflow roles
description: Certain roles are required to use workflows.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-05-30"
reading_time_minutes: 1
breadcrumb: [Workflow administration, Classic Workflow, Build workflows]
---

# Workflow roles

Certain roles are required to use workflows.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and contact your account representative.

<table id="table_g2t_fww_1r"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity creator

 \[activity\_creator\]

</td><td>

Creates and edits custom workflow activities, reuses custom activity data, and manages activity packs downloaded from the ServiceNow Store.

</td></tr><tr><td>

Web service administrator

 \[web\_service\_admin\]

</td><td>

Accesses and uses REST and SOAP messages in the [Orchestration activity designer](https://www.servicenow.com/docs/access?context=c_WorkflowActivityDesigner&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). Creates and edits custom activities that use the REST web service and SOAP web service templates.

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

