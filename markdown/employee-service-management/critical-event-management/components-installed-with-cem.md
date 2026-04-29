---
title: Components installed with Critical Event Management
description: Several types of components are installed with the Critical Event Management application, including tables and user roles.
locale: en-US
release: australia
product: Critical Event Management
classification: critical-event-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Critical Event Management, Health and Safety, Employee Service Management]
---

# Components installed with Critical Event Management

Several types of components are installed with the Critical Event Management application, including tables and user roles.

## Store applications installed

<table id="table_ulz_4tw_llba"><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety Core

</td><td>

Installs core data model for Health and Safety. This data model includes common components such as Health and Safety user profile and actions that are used in the Health and Safety applications.

 For more information on store applications, roles, and tables installed with Health and Safety Core, see [Components installed with Health and Safety Core](../../hs-core/reference/components-installed-hs-core.md).

</td></tr><tr><td>

Workplace Core \[sn\_wsd\_core\]

</td><td>

Enables workplace locations for Health and Safety applications.**Important:** The application installation doesn’t install the location demo data for the Workplace Core location model. As a workaround, repair the Workplace Core plugin with the **Load demo data** option.

</td></tr></tbody>
</table>## Roles installed

<table id="table_hjq_5kf_ldc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Critical event admin\[sn\_critical.admin\]

</td><td>

Administrator role. Configures the Critical Event Management application properties.

</td><td>

-   sn\_critical.agent
-   sn\_critical.responder
-   sn\_comm\_management.comm\_plan\_admin
-   sn\_critical.user
-   sn\_critical.manager

</td></tr><tr><td>

Critical event agent\[sn\_critical.agent\]

</td><td>

Works on critical event records from initiation to resolution.

</td><td>

-   sn\_comm\_management.comm\_plan\_manager
-   task\_editor
-   canvas\_user
-   sn\_ohs\_im.workspace\_user
-   sn\_critical.read

</td></tr><tr><td>

Critical event manager\[sn\_critical.manager\]

</td><td>

Oversees all critical events and guides agents and responders to resolve them.

</td><td>

sn\_critical.agent

</td></tr><tr><td>

Critical event reader\[sn\_critical.read\]

</td><td>

Has read-only access to critical event records.

</td><td>

sn\_comm\_management.comm\_plan\_viewer

</td></tr><tr><td>

On-site responder\[sn\_critical.responder\]

</td><td>

Assists on-site personnel during critical events.

</td><td>

sn\_critical.read

</td></tr><tr><td>

Critical event user\[sn\_critical.user\]

</td><td>

Reports emergency as an employee.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_ljq_5kf_ldc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Critical event communication plan\[sn\_critical\_comm\_plan\]

</td><td>

Stores information about detailed communication strategies during critical events.This table is an extension to the Communication Plan \[comm\_plan\] table.

</td></tr><tr><td>

Critical event communication task\[sn\_critical\_comm\_task\]

</td><td>

Tracks individual tasks related to the communication plan for critical events.This table is an extension to the Communication Task \[comm\_task\] table.

</td></tr><tr><td>

Critical event\[sn\_critical\_event\]

</td><td>

Contains records of critical events.This table is an extension to the Task \[task\] table.

</td></tr><tr><td>

Impacted people\[sn\_critical\_impacted\_people\]

</td><td>

Lists individuals impacted by critical events.

</td></tr><tr><td>

On-site responder mapping\[sn\_critical\_on\_site\_responder\_mapping\]

</td><td>

Maps responders to on-site locations during critical events.

</td></tr><tr><td>

Critical event task\[sn\_critical\_task\]

</td><td>

Stores tasks related to Critical Event Management.This table is an extension to the Task \[task\] table.

</td></tr></tbody>
</table>## Plugins installed

<table id="table_e5t_txn_ldc"><thead><tr><th>

Plugins

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notify \[com.snc.notify\]

</td><td>

Provides the ability to set SMS preferences to receive messages from different providers.

</td></tr><tr><td>

Task Communication Management \[com.snc.task\_communication\_management\]

</td><td>

-   Activates the base system.
-   Includes demo data and activates related plugins if they aren’t already active.

</td></tr></tbody>
</table>## Store applications installed

|Store applications|Description|
|------------------|-----------|
|Health and Safety|Allows you to report Health and Safety incidents.|
|Task Communications Management UI Components for Configurable Workspace|Stores bundle of UI components required to leverage Task Communications Management core capabilities in workspaces.|

## Optional applications

<table id="table_zfg_t11_hdc"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Geo Map componentsn\_geo\_map

</td><td>

Enables the map component on the Critical Event Management dashboard.

</td></tr></tbody>
</table>**Parent Topic:**[Critical Event Management reference](../concept/critical-event-management-reference.md)

