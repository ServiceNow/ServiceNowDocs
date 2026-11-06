---
title: Use Microsoft Outlook to create incidents and VTB tasks
description: Create an incident or a Visual Task Board \(VTB\) task, or chat with a virtual agent, directly from Microsoft Outlook by using the ServiceNow add-in.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/use-outlook-add-in.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Use Microsoft Outlook to create incidents and VTB tasks

Create an incident or a Visual Task Board \(VTB\) task, or chat with a virtual agent, directly from Microsoft Outlook by using the ServiceNow add-in.

## Before you begin

The ServiceNow Add-in for Microsoft Outlook must be activated and deployed. For more information, see [Configuring Microsoft Outlook to create incidents and VTB tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/create-incident-outlook.md)

Role required: none

## Procedure

1.  On the Microsoft Outlook Home tab, select the **ServiceNow** icon \(\[Omitted image "outlook-add-in-icon.png"\] Alt text: OutlookAddInIcon\) and select **Create Incident** or **Create VTB Task**.

2.  In the ServiceNow IT Service Management pane, select **Login** and enter your ServiceNow credentials.

    You may need to reauthenticate if your session has expired.

3.  For an incident record, fill in the following fields and select **Submit**.

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

Currently logged-in user \(default\).

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

Category of the incident.-   Inquiry / Help
-   Software
-   Hardware
-   Network
-   Database


</td></tr></tbody>
</table>    You can add or remove fields directly on the Incident form for users with the itil role by customizing the Outlook view form layout.

    **Note:** For users who don't have the itil role, the configured Service Catalog form for creating new incidents is shown.

4.  For a task record, fill in the following fields and select **Create**.

    |Field|Description|
    |-----|-----------|
    |Select Board|Visual task board to which the task belongs.|
    |Select Lane|Lane of the VTB board.|
    |Short Description|Short description of the task.|

5.  To chat with a virtual agent, select the **Chat with Virtual Agent** UI action to open the chat window.


