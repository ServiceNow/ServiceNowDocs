---
title: Release readiness target form
description: Release admins can create release readiness targets on a release calendar to define the dates by which the releases must be ready for deployment.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Digital Product Release, IT Service Management]
---

# Release readiness target form

Release admins can create release readiness targets on a release calendar to define the dates by which the releases must be ready for deployment.

**Note:** Release readiness target and Release target are used interchangeably. Both terms refer to the same concept - release readiness target date.

For more information, see [Create a release readiness target](../task/dpr-create-rls-readiness-target.md).

<table id="table_wdl_bcc_lyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the release readiness target.You can create multiple release targets with the same name if they are scheduled for different days in a release calendar.

The target names are displayed along with the date.

</td></tr><tr><td>

Release admin

</td><td>

Name of the release admin who manages the release process.Your name is pre-populated by default; however, you can select another user with appropriate role as the release admin for the readiness target.

</td></tr><tr><td>

Description

</td><td>

Brief description of the release readiness target.

</td></tr><tr><td>

Date

</td><td>

Date by when the product or service must be ready for release.**Note:** This field isn’t available for release readiness targets that have a release associated.

The **Date** field is replaced by the **Start date** field when you select the **Recurring** option.

</td></tr><tr><td>

Recurring

</td><td>

Option to set the recurring target.Select an option from **Repeat**, choose the start date, recurrence options, and end date to set the recurring targets.

</td></tr><tr><td>

Schedules excluded from target

</td><td>

Schedules when the release readiness targets are excluded from creation that overlaps with blackout, maintenance, or other schedules.These schedules are auto-populated from the selected calendar.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Product Release reference](../concept/dpr-reference.md)

