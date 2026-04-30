---
title: Manually create an SRM template
description: Templates help you quickly create SRM services, alerts, incidents, or teams from existing forms.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [SRM interface, Get started with Service Reliability Management, Exploring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Manually create an SRM template

Templates help you quickly create SRM services, alerts, incidents, or teams from existing forms.

## Before you begin

Role required: Responder, Manager, or Administrator

## About this task

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You are taken to your SRM homepage.

    **Note:** If you have other SOW applications, and depending on your assigned roles, that homepage may not be the SRM homepage. It is the SOW homepage instead, with SRM alerts and incidents included in your metrics. In that case, to view SRM specific areas, select SRM modules from the left navigation pane.

2.  In the left navigation pane, select **Services**, **Teams**, **Alerts**, or **Incidents**.

3.  Open a service, team, alert, or incident.

4.  In the far right panel, select the Template icon ![Template icon](../image/icon-sr-template.png) and select **Create**.

5.  Fill in the fields on the **Create New Template** form, as appropriate.

<table id="template-fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the table. Keep or edit the default entry.

</td></tr><tr><td>

Domain

</td><td>

Select the SRM domain for the template.

</td></tr><tr><td>

Table

</td><td>

Table that this template applies to. Select Global to make the template available for use with all tables.**Note:** The table list shows only the tables and database views that are in the same scope as the template.

</td></tr><tr><td>

User

</td><td>

Individual who can configure and apply the template. If you define one, no one else can see the template unless you select the Global option. The individual creating the template is the default.

</td></tr><tr><td>

Assignment group

</td><td>

Select a team to work on the incident by typing or searching.

</td></tr><tr><td>

Active checkbox

</td><td>

State of the template. Active by default. Uncheck to deactivate.

</td></tr><tr><td>

Groups

</td><td>

Group whose members can configure and apply the template. If you define a group, no other groups can see the template unless you select the Global option.

</td></tr><tr><td>

Global checkbox

</td><td>

Read-only. Option for allowing any user who can access the templates to view and apply this template. Not implemented for SRM.

</td></tr><tr><td>

Short description

</td><td>

Add description of the template indicating use.

</td></tr><tr><td>

Template

</td><td>

Content that automatically populates records that are based on this template. Select a field from the specified table in the left column and then enter the data to automatically populate in the right column.

**Note:** Even though you can select dot-walked fields in the template, they do not apply to fields that are on the form.

 Select a field. Choices are:

-   Active: Check the box to activate.

A template must be active to be used.

-   Cost center
-   Default assignee
-   Description
-   Exclude manager
-   Group email
-   Include members
-   Manager
-   Name
-   Parent
-   Roles
-   Source
-   Type


</td></tr></tbody>
</table>    The template is created and you can see I in the template panel.


**Parent Topic:**[SRM interface](../concept/sr-navigate-interface.md)

