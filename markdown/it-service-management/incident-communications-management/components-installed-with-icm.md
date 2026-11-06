---
title: Components installed with Incident Communications Management
description: Activating the Incident Communications Management plugin \(com.snc.iam\) installs several types of components, including tables and user roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-communications-management/components-installed-with-icm.html
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Incident Communications Management reference, Incident Communications Management, IT Service Management]
---

# Components installed with Incident Communications Management

Activating the Incident Communications Management plugin \(com.snc.iam\) installs several types of components, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

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

Can create, edit, or cancel incident communication plans and incident communication tasks, and manage contact information. **Note:** The role is available when you activate the Notify plugin.

</td><td>

-   contact\_admin
-   sn\_comm\_management.comm\_plan\_manager
-   notify\_view

</td></tr><tr><td>

sn\_iam\_admin

</td><td>

Can configure all Incident Communications Management features, including creating, editing, or canceling incident communication plans and communication tasks, and managing contact information. This role can also administer all Incident Communications Management capabilities.

</td><td>

ia\_admin

</td></tr><tr><td>

contact\_user

</td><td>

Can view contacts, contact definitions, contact responsibilities, and default overrides.

</td><td>

N/A

</td></tr><tr><td>

contact\_admin

</td><td>

Can create and edit contact definitions and contact responsibilities.

</td><td>

contact\_user

</td></tr><tr><td>

sn\_contact\_admin

</td><td>

Can configure all Contact Management features, including creating and editing contact definitions and contact responsibilities, and configuring major incident \(MI\) users, recipient lists, and groups.

</td><td>

contact\_admin

</td></tr><tr><td>

sn\_tcm\_admin

</td><td>

Can configure all Task Communications Management features including communication plans and tasks. For more information, see [Components installed with Task Communications Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/components-installed-with-tcm.md).

</td><td>

-   comm\_plan\_admin
-   comm\_plan\_mgr

</td></tr><tr><td>

sn\_comm\_management.comm\_plan\_viewer

</td><td>

Can read Task Communications Management tables.

</td><td>

-   notify\_view
-   sn\_publications\_recipients\_list\_user
-   email\_client\_template\_read
-   contact\_user
-   sn\_publications\_recipients\_user
-   sn\_dex\_desktop.notification\_template\_admin

**Note:** Starting with the Brazil release, on zBoot instances, the sn\_dex\_desktop.notification\_template\_admin role is removed from the communication plan viewer \[sn\_comm\_management.comm\_plan\_viewer\] role and added to the sn\_incident\_write role when the ITSM Roles plugin \(com.snc.itsm.roles\) is installed. If the ITSM Roles plugin \(com.snc.itsm.roles\) isn't installed, the sn\_dex\_desktop.notification\_template\_admin role is added to the itil role.


</td></tr></tbody>
</table>**Note:** For the comm\_channel create and write ACLs, access to create communication channel definitions in incident communication tasks depends on the `commTaskGr.state.canWrite` script and on whether you have one of the following roles:

-   Communication Plan Manager \[sn\_comm\_management.comm\_plan\_mgr\]
-   Communication Plan Admin \[sn\_comm\_management.comm\_plan\_admin\]
-   Task communication management admin \[sn\_tcm\_admin\]
-   ITSM granular roles such as sn\_incident\_write and the user assigned to the incident communication task and plan.

## Tables installed

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

The Incident Communication Plan table extends the Communication Plan table \[comm\_plan\] so that the incident communication plan inherits any future enhancements made to the communication object.

</td></tr><tr><td>

Incident Communication Task\[incident\_alert\_task\]

</td><td>

The Incident Communication Task table extends the Communication Task table \[comm\_task\].

</td></tr></tbody>
</table>**Parent Topic:**[Incident Communications Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/reference-section-inci-comm-mngmt.md)

