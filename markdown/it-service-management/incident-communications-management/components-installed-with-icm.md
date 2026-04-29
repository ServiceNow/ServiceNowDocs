---
title: Components installed with Incident Communications Management
description: Several types of components are installed with activation of the Incident Communications Management plugin \(com.snc.iam\), including tables and user roles.
locale: en-US
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Incident Communications Management reference, Incident Communications Management, IT Service Management]
---

# Components installed with Incident Communications Management

Several types of components are installed with activation of the Incident Communications Management plugin \(com.snc.iam\), including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

ia\_admin

</td><td>

Can create, edit, or cancel incident communication plan, incident communication task, and manage contact information. **Note:** The role is available when you activate the Notify plugin.

</td><td>

-   contact\_admin
-   sn\_comm\_management.comm\_plan\_manager
-   notify\_view

</td></tr><tr><td>

sn\_iam\_admin

</td><td>

Configure all Incident Communications Management features including creating, editing, or canceling incident communication plan, communication task, and managing contact information. Additionally, this role can administer all Incident Communications Management capabilities.

</td><td>

ia\_admin

</td></tr><tr><td>

contact\_user

</td><td>

Can view contacts, contact definitions, contact responsibilities, and default overrides.

</td><td>

NA

</td></tr><tr><td>

contact\_admin

</td><td>

Can create and edit contact definitions and contact responsibilities.

</td><td>

contact\_user

</td></tr><tr><td>

sn\_contact\_admin

</td><td>

Configure all Contact Management features including creating and editing contact definitions, contact responsibilities, configuration of major incident \(MI\) users, recipient lists, and groups.

</td><td>

contact\_admin

</td></tr><tr><td>

sn\_tcm\_admin

</td><td>

Configure all Task Communications Management features including communication plans and tasks. For more information, see [Components installed with Task Communications Management](https://www.servicenow.com/docs/access?context=components-installed-with-tcm&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td><td>

-   comm\_plan\_admin
-   comm\_plan\_mgr

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Impacted CI \[impacted\_ci\]

</td><td>

The CIs impacted by the source CI in the incident communication plan.

</td></tr><tr><td>

Incident Communication Plan \[incident\_alert\]

</td><td>

The Incident Communication Plan table extends from the Communication Plan table \[comm\_plan\] so that the incident communication plan inherits any future enhancements made to the communication object.

</td></tr><tr><td>

Incident Communication Task\[incident\_alert\_task\]

</td><td>

The Incident Communication Task table extends the Communication Task table \[comm\_task\].

</td></tr></tbody>
</table>**Parent Topic:**[Incident Communications Management reference](reference-section-inci-comm-mngmt.md)

