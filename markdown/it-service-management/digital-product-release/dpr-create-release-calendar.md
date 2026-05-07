---
title: Create a release calendar
description: Create a release calendar to define release readiness targets within it.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Digital Product Release, IT Service Management]
---

# Create a release calendar

Create a release calendar to define release readiness targets within it.

## Before you begin

Role required: sn\_dpr\_model.release\_calendar\_admin orsn\_dpr\_model.release\_admin

## About this task

A release calendar provides you with a layout to manage and track release readiness targets, and view and manage releases and change requests. The release calendar also contains blackout, maintenance, and other user-defined schedules to avoid overlap of release targets on those dates. Each event type is color-coded and can be filtered using the hierarchical filter panel.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the release calendar icon \(![Release calendar icon.](../image/dpr-icon-rls-target.png)\).

3.  Create a release calendar or update an existing one.

    -   To create a release calendar, select the release calendar actions button \(![Release calendar actions button.](../image/dpr-icon-more-actions-v.png)\), and then select **Create release calendar**.
    -   To modify an existing release calendar, open the release calendar from the drop-down list, select the release calendar actions button, and then select **Edit release calendar**.
4.  In the dialog box, fill in the fields.

<table id="table_wdl_bcc_lyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the release calendar.For example, `Q3 2026 Platform Releases`.

</td></tr><tr><td>

Release admin

</td><td>

Name of the release admin who will own the release calendar.

</td></tr><tr><td>

Description

</td><td>

Brief description of the release calendar.For example, `Tracks all platform release readiness targets and deployment windows for Q3 2026`.

</td></tr><tr><td>

Exclusion schedules

</td><td>

Schedules for blackouts, maintenance, or holidays are lists of dates for planned closures or business holidays.Add your organization's schedules to the release calendar to avoid having release targets scheduled on those dates.

The blackouts and maintenance schedules are shown from the Schedule \[cmn\_schedule\] table. For more information, see [Define a schedule](https://www.servicenow.com/docs/access?context=t_DefineASchedule&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

To include user-defined exclusion schedules under **Others** category, you can configure the system property **sn\_dpr.release\_calendar\_exclusions**. For more information, see [Digital Product Release properties](../reference/digital-product-release-properties.md).

</td></tr></tbody>
</table>5.  Save the release calendar.

    -   Save a new release calendar by selecting **Create**.
    -   Save the changes to an existing release calendar by selecting **Save**.

## Result

The release calendar is saved and displayed in the calendar layout. Events for the exclusion schedules that are added to the release calendar are shown on specific dates on the calendar.

![Release calendar showing a monthly view with scheduled change requests, release targets, and schedules.](../image/dpr-release-calendar.png "Release calendar")

## What to do next

[Create a release readiness target](dpr-create-rls-readiness-target.md)

**Note:** Release readiness target and Release target are used interchangeably. Both terms refer to the same concept - release readiness target date.

You can perform the following tasks to manage and visualize your release activities:

-   Select an event \(release target, release, or change request\) from the release calendar to see a popover with the key details of the event. Select the edit icon \(![Edit icon.](../image/dpr-icon-edit.png)\) to view and edit the event record if you have the required roles.
-   Use the side panel to view all event details for the selected day, or search for an event.
-   Use filters to view calendar entries by event type \(release target, release, change request\) or by exclusion schedules \(blackouts, holidays, maintenance\).
-   Change the timezone to view events on the calendar for the selected timezone.
-   Switch between Week and Month views for better visibility of upcoming events.

**Related topics**  


[Digital Product Release - POST /sn\_dpr/digital\_product\_release/release\_calendar](https://www.servicenow.com/docs/access?context=digital-product-release-api&version=australia&pubname=australia-api-reference&section=dpr-POST-release_calendar&ft:locale=en-US)

