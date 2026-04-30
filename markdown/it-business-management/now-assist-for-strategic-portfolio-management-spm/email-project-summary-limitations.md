---
title: Additional information on Email project summary skill
description: View the additional information about email project summary skill such as column restrictions, date criteria, and so on.
locale: en-US
release: xanadu
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: reference
last_updated: "2024-10-22"
reading_time_minutes: 1
keywords: [Limitations, Email project summary skill limitations, Column restriction, Date selection criteria]
breadcrumb: [Reference, Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Additional information on Email project summary skill

View the additional information about email project summary skill such as column restrictions, date criteria, and so on.

## Column restrictions

The columns that are considered for generating the project summary for each table are listed in the following table.

<table id="table_unj_r43_ddc"><thead><tr><th>

Tables

</th><th>

Columns

</th></tr></thead><tbody><tr><td>

Project

</td><td>

-   State
-   Short description
-   Status
-   Planned start date
-   Planned end date
-   Project level EAC \(Estimate at Completion\)
-   Project budget
-   Percent complete

</td></tr><tr><td>

Milestone

</td><td>

-   Short description
-   State
-   Status
-   Planned start date
-   Planned end date
-   Milestone
-   Key milestone

</td></tr><tr><td>

Project task

</td><td>

-   Short description
-   State
-   Status
-   Planned start date
-   Planned end date

</td></tr><tr><td>

Resource assignment

</td><td>

-   Resource
-   Start date
-   End date
-   Resource status
-   Group
-   Role
-   Skill

</td></tr></tbody>
</table>## Date selection criteria

-   The planned start or end date of the milestone should fall within the same month as the snapshot.
-   The planned start date or end date of the resource assignment should fall within the same month as the snapshot.
-   The planned start date or end date of the project task should fall within the same month as the snapshot.

## Email cadence criteria for scheduling an email

-   Emails are scheduled to be sent at regular intervals.
-   Emails are sent consistently until the process is paused.
-   Once unpaused, the cadence resumes, with the next email sent at the next scheduled interval.
-   A new snapshot is created at the time of cadence change or when it’s unpaused.

