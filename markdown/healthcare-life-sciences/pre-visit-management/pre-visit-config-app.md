---
title: Configuring Pre-Visit Management
description: Set up the Pre-Visit Management application to complete pre-visit activities associated with a procedure.
locale: en-US
release: yokohama
product: Pre-Visit Management
classification: pre-visit-management
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 3
breadcrumb: [Pre-Visit Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configuring Pre-Visit Management

Set up the Pre-Visit Management application to complete pre-visit activities associated with a procedure.

**Important:**

Starting with the Yokohama release, Pre-Visit Management is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

The following table provides an overview of the configuration tasks required for Pre-Visit Management.

**Note:** The Pre-Visit Management application is based on the [Healthcare and Life Sciences data model](hcls-serv-mgmt-core.md) and stores all procedure requests in the Procedure request \[sn\_previsit\_procedure\_request\] table.

<table id="table_ksw_gpr_4nb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Install Pre-Visit Management](../task/install-pre-visit-mgmt.md).

</td><td>

Install the Pre-Visit Management application to work on procedure requests.

</td></tr><tr><td>

[Assign roles for Pre-Visit Management users](../task/pre-visit-assign-roles.md).

</td><td>

Assign roles to control access to features, capabilities, and data in the Pre-Visit Management application.

</td></tr><tr><td>

[Approve restricted caller access privileges for Pre-Visit Management.](pre-visit-approve-rca.md)

</td><td>

Approve restricted caller access \(RCA\) privileges for accessing document templates from the Pre-Visit Management application.

</td></tr><tr><td>

[Determine who can work on the appointment booking task for a procedure](../task/pre-visit-proc-scheduler-grp.md).

</td><td>

Add users who can work on the appointment booking task for a procedure to the Procedure scheduler assignment group.

</td></tr><tr><td>

[Configure when to send the procedure consent form to a patient](../task/pre-visit-config-proc-consent-time.md).

</td><td>

Configure the Pre-Visit Management application to when to send the procedure consent document for review and signature to a patient before the procedure appointment date.

</td></tr><tr><td>

[Specify a to-do item for patients](pre-visit-config-to-do-items.md).

</td><td>

Add a to-do item that patients must complete as part of their pre-visit planning.

</td></tr><tr><td>

[Configure the auto-generation of documents for a procedure request](pre-visit-config-doc-decisions.md).

</td><td>

Define the conditions for auto-generating documents for a procedure request.

</td></tr><tr><td>

[Configure the patient portal to add a to-dos menu item for procedure request tasks](pre-visit-config-to-do.md).

</td><td>

Configure the patient portal to add a menu item that lists all to-do items for patients.

</td></tr><tr><td>

[Configure a playbook for Pre-Visit Management](pre-visit-config-playbook.md).

</td><td>

Configure a playbook to provide step-by-step guidance for resolving procedure request cases.

</td></tr><tr><td>

[Configure a Pre-Visit Management email notification](pre-visit-config-emails.md).

</td><td>

Configure the Pre-Visit Management email notifications sent to patients about pre-visit activities for procedure requests.

</td></tr><tr><td>

[Determine additional user profiles](pre-visit-connector-contributor.md).

</td><td>

Determine who can act as an agent connector or contributor for procedure request cases.

</td></tr><tr><td>

[Set up the process for contributors to create a procedure request case](pre-visit-case-contributor.md).

</td><td>

Set up the process for creating procedure request cases on a service portal.

</td></tr></tbody>
</table>