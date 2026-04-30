---
title: Upgrade History Task form
description: You can update information about a skipped record task using the Upgrade History Task form.
locale: en-US
release: yokohama
product: Upgrade Center
classification: upgrade-center
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Skipped Records visual task board \(VTB\), Reviewing upgrade history, Using Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade History Task form

You can update information about a skipped record task using the Upgrade History Task form.

To make changes on a skipped record task, click a task number link on a task over VTB.

<table id="table_tht_fp2_clb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Description about the task

</td></tr><tr><td>

Priority

</td><td>

Prioritization of the skipped records based on the importance of the file types. The prioritization is done as follows:-   Priority 1 \(highest priority\): UI pages, UI macros, and more
-   Priority 2: Business Rules, Security ACLs, and more
-   Priority 3: Reports and more
-   Priority 4: Form Sections, Choice Sets, and more
-   Priority 5 \(lowest priority\): other

</td></tr><tr><td>

Disposition

</td><td>

Disposition is Skipped since the task board is only for skipped records. The system did not change this record in order to preserve customizations.

</td></tr><tr><td>

Type

</td><td>

Type of file which determines the priority level.

</td></tr><tr><td>

State

</td><td>

State of the files.-   Not reviewed: Tasks which have not been reviewed
-   Reviewed: Tasks which have been reviewed
-   Merged: Tasks which have both the old and new changes
-   Retained: Tasks which have retained the updates from the latest upgrade
-   Reverted: Tasks which have reverted its changes to the base system

</td></tr><tr><td>

Work notes

</td><td>

Notes about the skipped record task

</td></tr><tr><td>

Update

</td><td>

Button to update the skipped record task

</td></tr><tr><td>

Resolve Conflicts

</td><td>

Button to resolve conflicts by reviewing the differences

</td></tr><tr><td>

Revert to Base System

</td><td>

Button to revert the customizations

</td></tr><tr><td>

Delete

</td><td>

Button to delete the skipped record task

</td></tr></tbody>
</table>The Old Resolution Details related list shows the actions taken in the previous upgrade version.![Image showing the Old Resolution Details related list](../image/uc-old-resolution.png)

<table id="table_shg_xqf_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Task number of the skipped file where some actions were taken in the previous upgrade version.

</td></tr><tr><td>

Short description

</td><td>

Description about the task

</td></tr><tr><td>

Disposition

</td><td>

Action performed on this file during previous upgrade

</td></tr><tr><td>

Priority

</td><td>

Prioritization of the skipped records based on the importance of the file types. The prioritization is done as follows:1.  \(highest priority\): xml content
2.  script or script\_plain
3.  html content
4.  sys\_ui\_form\_section, sys\_ui\_related\_list, or sys\_choice\_set
5.  \(lowest priority\): other

</td></tr><tr><td>

State

</td><td>

State of the files.-   Not reviewed: Tasks which have not been reviewed
-   Reviewed: Tasks which have been reviewed
-   Reviewed and Merged: Tasks which have been reviewed and have both the old and new changes
-   Reviewed and Retained: Tasks which have been reviewed and have retained the updates from the latest upgrade
-   Reviewed and Reverted: Tasks which have been reviewed and have reverted its changes to the base system

</td></tr><tr><td>

Assigned to

</td><td>

Name of the assigned user

</td></tr><tr><td>

From

</td><td>

Past previous version

</td></tr><tr><td>

To

</td><td>

Past current version

</td></tr></tbody>
</table>