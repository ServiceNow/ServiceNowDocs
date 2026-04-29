---
title: Review and update a post incident report
description: Review a post incident report \(PIR\) using the Post Incident Report tab. A PIR helps you review and understand the cause of the major incident and the actions taken by the teams to resolve the incident. This helps prevent the issue in the future.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Managing a major incident record, Major Incident Management in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Review and update a post incident report

Review a post incident report \(PIR\) using the **Post Incident Report** tab. A PIR helps you review and understand the cause of the major incident and the actions taken by the teams to resolve the incident. This helps prevent the issue in the future.

## Before you begin

The major incident must be in the **Resolved** state. For more information, see [Resolve and close a major incident](resolve-close-mim-sow.md).

Role required:

-   For PIR review: sn\_incident\_read or sn\_incident\_write
-   For PIR update, generate and download: major\_incident\_manager or admin

## About this task

Reviewing the post incident report \(PIR\) also provides an opportunity to evaluate the incident response process and identify areas for improvement. The PIR can be reviewed and updated during the review process before it's shared with stakeholders.

After you resolve a major incident, you must publish the PIR for the major incident and share it with the stakeholders within a specified time duration as defined in the SLA. You can configure the SLA by specifying the value in hours in the **PIR publish hours** \(**sn\_sow\_inc.pir.publish.hours**\) system property.

The following events are captured in the timeline of the PIR:

-   Incident created
-   Incident proposed as major incident
-   Incident accepted as major incident
-   Incident resolved
-   Incident closed
-   Custom events
-   Incident task created
-   Incident task closed

## Procedure

1.  Open a major incident record that is in the **Resolved** state.

2.  Select the **Post incident report** tab.

3.  On the Incident Response Timing section, review the time duration for the following fields.

<table id="table_wnl_dhg_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time to identify

</td><td>

Duration of time taken to identify an incident as major incident.The **Time to identify** field is displayed based on this calculation:

```
Time to identify = (incident created time) - (incident proposed time)
```

or

```
Time to identify = (incident created time) - (incident promoted time)
```

</td></tr><tr><td>

Time to response

</td><td>

Duration of time taken to respond to the proposed major incident.The **Time to response** field is displayed based on this calculation:

```
Time to response = (incident proposed time) - (incident promoted time)
```

</td></tr><tr><td>

Time to resolve

</td><td>

Duration of time taken to resolve the major incident.The **Time to resolve** field is displayed based on this calculation:

```
Time to resolve = (incident promoted time) - (incident resolved time)
```

</td></tr></tbody>
</table>4.  On the Contributors section, add users to help with creating and publishing the PIR.

    1.  Select the **Edit Co-contributors** \(![Edit](../../configurable-workforce-optimization-itsm/image/edit-icon.png)\) icon to add users as contributors.

    2.  In the **Co-contributors** field, enter users or user groups.

    3.  Select the **Save Co-contributors** \( ![Save](../image/mim-save-icon.png)\) icon to save the changes.

5.  On the Incident summary section, review the incident summary information and edit as needed.

    **Note:**

    By default, this section retrieves the incident summary information from the **Overview** tab. You can modify the values.

    1.  Select the **Edit report** \(![Edit](../image/mim-edit-icon.png)\) icon to edit the incident summary field of this section.

    2.  Edit the following information.

        -   Summary
        -   Impact
        -   Resolution
    3.  Select the **Save report** \(![Save](../image/mim-save-icon.png)\) icon to save the changes.

6.  On the Timeline section, review the incident events timeline and edit as needed.

    1.  Select the **Edit Timeline** \(![Edit](../image/mim-edit-icon.png)\) icon to edit the event timeline.

    2.  Select the **Add event** option, enter the following information, and then select **Add** to add a new event to the timeline.

        |Field|Description|
        |-----|-----------|
        |Select date and time of the event|Date and time of the event.|
        |Enter short description of the event|Brief description of the event.|

    3.  Edit the event timeline with the following setting options.

<table id="table_h5b_rpg_1bc"><thead><tr><th>

Options

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide

</td><td>

Select the **Hide** \(![Hide](../image/mim-hide-icon.png)\) icon to hide an event from the timeline.

</td></tr><tr><td>

Show

</td><td>

Select the **Show** \(![Show](../image/mim-show-icon.png)\) icon to show a hidden event on the timeline.

</td></tr><tr><td>

Edit

</td><td>

Select the **Edit** \(![Edit](../image/mim-edit-icon.png)\) icon to edit the description or the date and time of an event. This option is available only for the events added using the **Add event** option.

</td></tr><tr><td>

Delete

</td><td>

Select the **Delete** \(![Delete](../image/mim-delete-icon.png)\) icon to delete an event from the event timeline. This option is available only for the events added using the **Add event** option.

</td></tr><tr><td>

Order of events

</td><td>

Option to set the chronological order of events. Possible options:

 -   Ascending – The event that occurred first is placed at the top, and the event that occurred last is placed at the bottom.

-   Descending – The event that occurred last is placed at the top, and the event that occurred first is placed at the bottom.

</td></tr><tr><td>

Event Grouping

</td><td>

Option to enable the grouping of the events that occur within a specified time duration.

</td></tr><tr><td>

Group events with--of each other

</td><td>

Time duration that groups events if the events occur within this value.

</td></tr><tr><td colspan="2">

Visibility settings

</td></tr><tr><td>

Show hidden events in edit view

</td><td>

Option to show the events that are hidden when the **Edit Timeline** \(![Edit](../image/mim-edit-icon.png)\) icon is selected.

</td></tr><tr><td>

Show manually events in edit view

</td><td>

Option to show the events that are added manually when the **Edit Timeline** \(![Edit](../image/mim-edit-icon.png)\) icon is selected.

</td></tr><tr><td>

Show time line events in edit view

</td><td>

Option to show the timeline events when the **Edit Timeline** \(![Edit](../image/mim-edit-icon.png)\) icon is selected.

</td></tr><tr><td>

Reset settings

</td><td>

Select the **Reset settings** \(![Reset settings](../image/mim-refresh-icon.png)\) icon to reset the settings back to the default settings.

</td></tr></tbody>
</table>    4.  Select the **Save settings** \(![Save](../image/mim-save-icon.png)\) icon to save the changes.

7.  On the Related records section, review the information of the records associated with the incident and update as needed.

    1.  Select **Edit**.

        You’re redirected to the Related records section of the **Details** tab in the major incident record.

    2.  On the Related records section, edit the following fields.

        |Fields|Description|
        |------|-----------|
        |Parent incident|Incident record that is associated as the parent to the incident record.|
        |Problem|Problem record associated with the incident record.|
        |Change request|Change request associated with the incident record.|
        |Caused by change|Change request for which the incident is created.|

    3.  Select **Save**.

        The information is updated in the fields of the Related records section of the Post incident report tab.

8.  Select **Preview**.

    **Note:** This option is available only if the **PIR SOW preview page** \(**sn\_sow\_inc.pir\_pdf\_preview\_sow\_page**\) system property is set to **true**.

9.  Select **Download**.

    A pop window displays the post incident report export in progress. Once the export process is completed, a **Download** option appears on the pop-up window.

10. Select **Download**.


## Result

The post incident report is downloaded to your system in PDF format. You can send the PDF file to the required stakeholders.

**Parent Topic:**[Managing a major incident record](../concept/managing-major-incident-sow.md)

