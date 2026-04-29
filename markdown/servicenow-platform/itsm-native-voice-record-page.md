---
title: Enable native voice control in Service Operations Workspace
description: Enable the native voice control to allow the agents to manage the calls using the Interaction Controls Component and the Customer History tab component.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ServiceNow Voice with ITSM, Integrating Voice with other applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable native voice control in Service Operations Workspace

Enable the native voice control to allow the agents to manage the calls using the Interaction Controls Component and the Customer History tab component.

## Before you begin

Role required: admin

## About this task

This page variant is available to users when:

-   The Interaction Controls Component plugin \(com.app\_interaction\_control\) is installed.
-   Interaction controls in the OpenFrame configuration are enabled.

When the following conditions are met, the agent sees the SOW voice interaction record page with the Interaction Controls Component and the Customer History tab component.

-   The interaction is of type phone.
-   The **Enable interaction controls** field on the OpenFrame Configuration record is enabled.
-   The agent belongs to the **User Group** selected on the OpenFrame Configuration record.

The agent can switch between phone interactions and chat interactions. If an interaction is of type chat, the agent sees the CSM default record page.

## Procedure

1.  Navigate to **All** &gt; **OpenFrame** &gt; **Configurations**.

2.  Select a configuration record.

    For example, select **CTI**.

3.  Select the **Enable interaction controls** check box to enable interaction controls for OpenFrame.

4.  Select a group from the available **User Group** column and move it to the **Selected** column.

    This is the group of users to whom the OpenFrame configuration applies.

5.  Unlock the URL field, and add a third-party URL.

    You can get this URL from your contact center provider admin.

6.  Select **Update**.


**Parent Topic:**[Integrating ServiceNow Voice with ITSM](../concept/integrate-ccc-itsm.md)

