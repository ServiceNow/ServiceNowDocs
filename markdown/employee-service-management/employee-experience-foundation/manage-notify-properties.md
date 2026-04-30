---
title: Manage Notify Connector for Microsoft Teams properties
description: Manage the Notify connector for Microsoft Teams application properties to configure the calling capabilities.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Notify connector, Microsoft Teams integration for Agent Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Manage Notify Connector for Microsoft Teams properties

Manage the Notify connector for Microsoft Teams application properties to configure the calling capabilities.

## Before you begin

Role required: Notify admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Microsoft Teams** &gt; **Properties**.

    ![Notify connector for Microsoft Teams properties](../image/notify-ms-teams-properties02.png)

2.  On the form, fill the fields.

<table id="table_cr5_y2b_sqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Notify integration for Task table and extensions

</td><td>

Option to enable Notify integration for Task table and extensions

</td></tr><tr><td>

Enable Notify integration for Incident Communications Management

</td><td>

Option to use Notify connector for Microsoft Teams for incident and major incident-related records.

</td></tr><tr><td>

Specify a valid teams email field name

</td><td>

Option to provide the field name to initiate the call to the user defined in this field.

 **Note:** The custom field name must be defined in the sys\_user table.

</td></tr><tr><td>

Enable Mute participants capability for Notify Connector for Microsoft Teams

</td><td>

Option to mute the participants in a conference call.

</td></tr><tr><td>

Enable Bot calling to user when click **Join Call** instead of opening link in a new browser tab

</td><td>

Option to enable the bot call the user in a conference call.

</td></tr><tr><td>

Application ID of Meeting Extensibility app

</td><td>

Option to provide the app Id of Meeting Extensibility app. Provide the Meeting Extensibility app ID details to use Meeting Extensibility in your environment.

</td></tr></tbody>
</table>3.  Select **Save**.


**Parent Topic:**[Configure Notify connector for Microsoft Teams](../concept/config-notify-ms-teams.md)

