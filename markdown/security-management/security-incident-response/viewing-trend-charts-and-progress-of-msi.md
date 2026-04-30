---
title: View Major Security Incident impact metrics
description: Provides up-to-date summary reporting of the impact and progress of major security incidents, which is an important aspect of managing a major security incident using the new workspace.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Use, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View Major Security Incident impact metrics

Provides up-to-date summary reporting of the impact and progress of major security incidents, which is an important aspect of managing a major security incident using the new workspace.

The **Overview** tab provides the relevant metrics to manage both the scope and progress of the incident, including a rollup of affected assets, users, locations, and team resources, as well as the timeline of significant incident milestones.

Timeline provides a horizontal view of key events and milestones that have occurred as part of the specific major security incident resolution. The timeline component is displayed on top of all the Major Security Incident Management workspace tabs with an ability to collapse and expand for viewing as required. The events data represented will be updated and refreshed whenever designated milestone events or milestones are added or updated.

Each event or milestone is indicated with a different timeline event type option to identify the number and type of events or milestones. For example NOW record updates, collaboration activities. In addition, the time range period for the different major security incident states is tracked automatically and displayed using color-coded ranges displayed along with the duration of each incident state.

![Summary, Incident impact, and Timeline details of the major security incident](../image/overview-tab-summary-msim.png "MSIM Overview tab")

<table id="table_gsv_2gt_gbc"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Executive Summary**

</td><td>

A brief summary of the major security incident along with the user name, user role, and timestamp details.-   You can modify the Executive Summary by selecting the **Edit** icon. After you make the required changes, select the **Update** option.
-   To copy the Executive Summary and paste it to a major security incident, select the **Copy** icon and paste the summary to the required major security incident.

</td></tr><tr><td>

**Incident Impact**

</td><td>

These components display the impacted resources based on a rollup of all active tasks and linked incidents with identified assets, users, locations, and assigned team members. The impacted resources are:-   **Affected assets**
-   **Affected users**
-   **Affected locations**

Selecting the number values enables you to drill down and navigate to the impacted assets, users, and location details and displays the related tasks on the **Incident Impact** tab of the workspace.

Based on your selected incident impact type link, the related incident details such as task type and its description, assignment group and incident state are displayed in the **Incident Impact** tab of the MSIM workspace.

</td></tr><tr><td>

**Duration counters**

</td><td>

These components display the duration of the major security incident. The impacted resources are:-   **Time elapsed**: Displays the time elapsed from the time that the major security incident is detected.
-   **Estimated resolution date**: Displays the estimated resolution date by when the major security incident is estimated to be resolved.
-   **Next update on**: The date and time of the next update for resolving the major security incident. For example, 5:00 pm EST on March 25, 2024.

You can modify the **Next update on** by selecting the **Edit** icon. Select the new date and time, and select **Update**.


</td></tr></tbody>
</table>You can enable or disable viewing of certain event types for both timeline indicators and timeline ranges accordingly using the filter toggle buttons.

![Timeline view](../image/msim-timline-view.png "Timeline")

Refer to the following table for additional capabilities available with the timeline component.

<table id="table_vz4_s3n_vrb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New Event

</td><td>

Creates new custom events and associates these events to the MSI record. This helps in creating events for both past and future dates that might not otherwise get captured via a labeled task, record state change, or labeled collaboration activity, which are displayed by default on the timeline.

</td></tr><tr><td>

Refresh

</td><td>

Refreshes the Timeline events to display the latest updates.

</td></tr><tr><td>

Timeline Indicators

</td><td>

Lists the various types of events such as Now Record field changes, Labeled Collaboration Activities, and Other \(custom\), along with the icons and total number of events that occurred with respect to each event type indicator.

The slide indicator enables you to enable or disable all events for a specific event type.

</td></tr><tr><td>

Show Legend

</td><td>

Select to display the drop-down legend with different types of timeline indicators.

</td></tr><tr><td>

Timeline progress bar

</td><td>

Displays the overall progress of the incident via designated timeline events or milestones that are occurred within the different timeline ranges displayed.You can also link an Event type to an Event category. After you link it, the Event details get updated at both places on the timeline.

</td></tr><tr><td>

Timeline ranges

</td><td>

Displays various incidents state types and duration as the incident progresses throughout the full major security incident life-cycle.

Enable or disable a specific event based on the incident state.

</td></tr></tbody>
</table>## Create a Timeline event

To create a new Timeline event, perform the following steps:

1.  In the Overview tab, navigate to the **Timeline** section.
2.  Select **+ New event**.
3.  On the Add a new timeline event pop-up, fill the fields.

    ![Add a new timeline event](../image/msim-add-timeline-event.png "New Timeline event")

<table id="table_nkh_pss_dcc"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Enter the title for the timeline event.

</td></tr><tr><td>

Category

</td><td>

Select a category for the timeline event.The following categories are provided as a part of the base system, and you can choose one based on your requirements.

-   **Custom**.
-   **Response**.
-   **Threat**.
To add or configure a Timeline event category, see [Configure timeline categories for major security incidents](configuring-msi-administration-settings.md#).

</td></tr><tr><td>

Timestamp

</td><td>

Select the date and time of the timeline event using the Timestamp calendar. You can add events to the Timeline before and after the start date.

</td></tr><tr><td>

Description

</td><td>

Provide a brief description about the timeline event.

</td></tr><tr><td>

Linked to

</td><td>

Option to link the timeline event to a major security incident record.

</td></tr></tbody>
</table>4.  Select **Create**.
5.  You can use **Zoom in** and **Zoom out** icons to zoom in or out on the timeline progress bar, which includes displaying individual events when numbers are displayed to represent several events in close time proximity.

    You can also add the default zoom level to show all events.

6.  Select the **Refresh** icon to display the latest timeline events.

**Parent Topic:**[Using Major Security Incident Management](../../security-incident-response/concept/major-security-incident-setup.md)

**Related topics**  


[Propose, promote, and link incident records](../../security-incident-response/concept/promoting-sir-to-msim.md)

[Using MSI List view in the MSIM workspace](../../security-incident-response/task/list-view-in-msim.md)

[View Major Security Incident trend charts](viewing-msi-impact-metrics.md)

[Update Major Security Incident details](msim-details-tab.md)

[Link additional records to Major Security Incident](../task/linking-additional-records-to-major-security-incidents.md)

[Unlink records from Major Security Incident](../task/unlinking-msi-records.md)

[Manage tasks in a Major Security Incident](tasks-tab.md)

[Track collaboration activity via MSIM workspace](collab-tab.md#)

[Create and distribute MSIM Status Reports](../task/creating-and-distributing-major-security-incident-status-reports.md)

