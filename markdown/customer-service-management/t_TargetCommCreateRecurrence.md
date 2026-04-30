---
title: Create a recurring publication
description: Review publications to either accept or reject them. You must have the publication’s approval role to review the publication. If the publication is not reviewed before the Publish Date, the publication is rejected.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Targeted communications, Configure case management, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create a recurring publication

Review publications to either accept or reject them. You must have the publication’s approval role to review the publication. If the publication is not reviewed before the Publish Date, the publication is rejected.

## Before you begin

Role required: sn\_publications.author or sn\_publications.admin

## About this task

You can specify the recurrence interval and the recurrence start and end date. The number of copies that are created are based on these settings and appear in the **Publications** related list on the original publication form. Each copy has a different publish date, which is based on the interval. Each copy gets reset to the **Author** state and each one goes through its own workflow.

## Procedure

1.  Do one of the following:

    -   Navigate to **Targeted Communications** &gt; **Active Publications**, open the desired publication, and click the **Setup Recurrence** related link.
    -   Navigate to **Targeted Communications** &gt; **Recurrences** and click **New**.
2.  Fill in the fields on the Recurrence form.

<table id="table_mca_ftc_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short Description

</td><td>

A brief description or title of the publication.

</td></tr><tr><td>

Publication Template

</td><td>

The number of the publication being used as a template. -   If you clicked the **Setup Recurrence** related link, this field displays the original publication number.
-   If you clicked **Recurrences** in the Targeted Communications menu, select a publication from the Publications list.


</td></tr><tr><td>

Recurrence Start

</td><td>

Select a date for the first occurrence of the recurring publications.

</td></tr><tr><td>

Recurrence End

</td><td>

Select a date for the last occurrence of the recurring publications.

</td></tr><tr><td>

Recurrence Interval

</td><td>

Select an interval for the recurring publications:-   Daily
-   Weekly
-   Biweekly
-   Monthly
-   Custom


</td></tr><tr><td>

Custom Interval in Days

</td><td>

This field appears when you select **Custom** as the **Recurrence Interval**. Enter the number of days for the interval.

</td></tr></tbody>
</table>3.  Click **Submit**.

    The recurring publications are created based on the selected dates and the recurrence interval and the stage for each copy is set to **Author**. The copies appear on the **Publications** related list on the original publication form, as well as on the Active Publications and the Draft Publications lists. From any of these lists you can open each publication and change the information as necessary. Each copy lists the publication template number in the **Recurrence** field.

    A record of the recurrence appears on the Recurrences list.


