---
title: Create a release calendar
description: Create a release calendar to define release readiness targets within it.
locale: en-US
release: xanadu
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Digital Product Release, Digital Product Release, IT Service Management]
---

# Create a release calendar

Create a release calendar to define release readiness targets within it.

## Before you begin

Role required: sn\_dpr\_model.release\_admin

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

Name of the release calendar.

</td></tr><tr><td>

Release admin

</td><td>

Name of the release admin who will own the release calendar.

</td></tr><tr><td>

Description

</td><td>

Brief description of the release calendar.

</td></tr><tr><td>

Exclusion schedules

</td><td>

Schedules for blackouts, maintenance, or holidays are lists of dates for planned closures or business holidays. Add these schedules to the release calendar to avoid having release targets for certain dates.The blackouts and maintenance schedules are shown from the Schedule \[cmn\_schedule\] table. For more information, see [Define a schedule](https://www.servicenow.com/docs/access?context=t_DefineASchedule&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

To include user-defined exclusion schedules under **Others** category, you can configure the system property **sn\_dpr.release\_calendar\_exclusions**. For more information, see [Digital Product Release properties](../reference/digital-product-release-properties.md).

</td></tr></tbody>
</table>5.  Save the release calendar.

    -   Save a new release calendar by selecting **Create**.
    -   Save the changes to an existing release calendar by selecting **Save**.

## Result

The release calendar is saved and displayed in the calendar layout. Events for the exclusion schedules that are added to the release calendar are shown on specific dates on the calendar.

## What to do next

[Create a release readiness target](dpr-create-rls-readiness-target.md)

**Note:** Release readiness target and Release target are used interchangeably. Both terms refer to the same concept - release readiness target date.

