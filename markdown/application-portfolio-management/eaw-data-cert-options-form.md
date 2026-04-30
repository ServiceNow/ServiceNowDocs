---
title: Options form
description: The options that appear depends on whether they are relevant to the selected policy type. Therefore, some of the following options don't appear on your form.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Options form

The options that appear depends on whether they are relevant to the selected policy type. Therefore, some of the following options don't appear on your form.

<table id="table_gf3_fyh_khc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display fields

</td><td>

One or more fields that appear in list views in Data Certification tasks, that uniquely identify the records that require certification.

 The selected fields can't overlap fields in **Certification fields**.

</td></tr><tr><td>

Certification fields

</td><td>

One or more fields whose value requires verification and certification.

 The selected fields can't overlap fields in **Display fields**.

</td></tr><tr><td>

Allow field updates

</td><td>

Option to allow certification task reviewers to update field values while reviewing CIs.-   When selected, certification task reviewers can update field values in order to certify a CI.
-   When clear, certification task reviewer can't update field values, and therefore reject CIs that aren't compliant.

</td></tr><tr><td>

Allow empty field values

</td><td>

Option to allow users to certify CIs with empty attributes:

-   When selected, certification task reviewers can certify or fail certification of a CI with an empty attribute.
-   When clear, certification task reviewers can fail certification of a CI with an empty attribute but aren't able to certify that CI.

</td></tr><tr><td>

Days to complete

</td><td>

Maximum number of days that policy tasks must be completed by.

 If notifications are enabled for certification or attestation tasks, then this number is used to calculate the milestones for sending notifications. The full time \(100%\) interval starts when a task is created and ends when the number of days to complete the task arrives. Notifications are sent if a task isn't closed when 50%, 70%, and 90% of that interval passes.

</td></tr><tr><td>

Instructions

</td><td>

Any instructions to assigned users, to help them complete the tasks.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

