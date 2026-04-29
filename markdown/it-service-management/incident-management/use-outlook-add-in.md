---
title: Use Microsoft Outlook to create incidents and VTB tasks
description: Create an incident or VTB task or chat with a virtual agent directly from within Microsoft Outlook using ServiceNow icons.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Use Microsoft Outlook to create incidents and VTB tasks

Create an incident or VTB task or chat with a virtual agent directly from within Microsoft Outlook using ServiceNow icons.

## Before you begin

You must activate and deploy the ServiceNow Add-in for Microsoft outlook. For more information, see [Configuring Microsoft Outlook to create incidents and VTB tasks](../concept/create-incident-outlook.md)

Role required: none

## Procedure

1.  On the Microsoft Outlook Home tab, click the **ServiceNow** icon \(![OutlookAddInIcon](../image/outlook-add-in-icon.png)\) and select **Create Incident** or **Create VTB Task**.

2.  In the ServiceNow IT Service Management pane, click **Login** and enter your ServiceNow credentials.

    You may need to reauthenticate if your session has expired.

3.  For an incident record, fill in the following fields and click **Submit**.

<table id="table_ssz_g5z_dgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated incident number.

</td></tr><tr><td>

Caller

</td><td>

Current logged in user \(default\).

</td></tr><tr><td>

Short description

</td><td>

Subject of the current email \(default\).

</td></tr><tr><td>

Additional comments

</td><td>

Email body in text format \(default\).

</td></tr><tr><td>

Category

</td><td>

Category of incident.-   Inquiry / Help
-   Software
-   Hardware
-   Network
-   Database


</td></tr></tbody>
</table>    You can add or remove fields directly on the Incident form for users with the itil role by customizing the Outlook view form layout.

    **Note:** For users that do not have the itil role, the configured Service Catalog form for creating new incidents is shown.

4.  For a task record, see fill in the following fields and click **Create**.

    |Field|Description|
    |-----|-----------|
    |Select Board|VTB board to which task belongs.|
    |Select Lane|Lane of the VTB board.|
    |Short Description|Short description of the task.|

5.  To chat with a virtual agent, select the **Chat with Virtual Agent** UI action to open the chat window.


