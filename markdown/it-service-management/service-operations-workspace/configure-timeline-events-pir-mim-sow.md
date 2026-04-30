---
title: Configure the timeline events for a Post Incident Report
description: Configure the incident information displayed as the event on the post incident report that is generated after a major incident is resolved. You can configure what information a post incident report must contain and how the information is arranged.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Major Incident Management in Service Operations Workspace, Setting up Major Incident Management in Service Operations Workspace, Getting started, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the timeline events for a Post Incident Report

Configure the incident information displayed as the event on the post incident report that is generated after a major incident is resolved. You can configure what information a post incident report must contain and how the information is arranged.

## Before you begin

The Major Incident Management plugin must be activated in Service Operations Workspace. For more information, see [Activate Major Incident Management in Service Operations Workspace](install-mim-sow.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  On the Admin Center page, navigate to the configuration page for Major Incident Management through either the **Overview** tab or the **Configurations** tab.

    -   In the **Overview** tab, select **Configure** for Major Incident Management.
    -   In the **Configurations** tab, select **Major Incident Management**.
    The configuration page displays all configurable features in Major Incident Management.

3.  On the Timeline configuration section, select **Configure**.

4.  On the Timeline configuration page, configure the options.

    Review the sample timeline events displayed on the Preview \(sample timeline\) section. Based on the data, you can use the following options to modify the default settings of the timeline.

<table id="table_vkw_q4w_y1c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incident Milestones

</td><td>

Option to include the following critical incident milestones in the timeline events of the post incident report:-   Incident accepted as a Major Incident by an MI manager
-   Incident marked as Resolved


</td></tr><tr><td>

Order of events

</td><td>

Option to arrange the order of the incident events in a post incident report. Available options:

-   Ascending – Order of events where the first event is placed at the top of the post incident report and the last event is displayed at the bottom of the post incident report.
-   Descending – Order of events where the last event is placed at the top of the post incident report and the first event is placed at the bottom of the post incident report.
 **Note:** The first and last event displays the date along with the time.

</td></tr><tr><td>

Event grouping

</td><td>

Option to group the events, which are within a short time interval. This option enables you to have a more concise post incident report.

</td></tr><tr><td>

Group events within

</td><td>

Time duration within which events that exist must be grouped.

</td></tr></tbody>
</table>
