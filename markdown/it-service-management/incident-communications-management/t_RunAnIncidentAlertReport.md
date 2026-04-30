---
title: Run an incident communication plan report
description: Run an incident communication plan report to view the status of communication plans. You can track the progress of the plan and intervene to improve the overall efficiency and effectiveness of the communication process.
locale: en-US
release: zurich
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, Incident Communications Management, IT Service Management]
---

# Run an incident communication plan report

Run an incident communication plan report to view the status of communication plans. You can track the progress of the plan and intervene to improve the overall efficiency and effectiveness of the communication process.

## Before you begin

Role required: ia\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Core UI artifacts** &gt; **Reports**.

2.  Select **New**.

3.  In the Data section, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Report name|Unique name for the report.|
    |Source type|Source from which the data is populated. The default value is Table.|
    |Table|Table from which the data is retrieved.|

4.  In the Type section, select the required visualization from the following sections:

    -   Bars
    -   Pies and Donuts
    -   Time series
    -   Multidimensional reports
    -   Scores
    -   Others
5.  In the Configure section, select the values for the following options:

    -   Column: Select the column that must be displayed in the report.
    -   Group By: Select the field based on which the data in the report is grouped.
    -   Configure the function field: Select to configure the function field for the report.
6.  In the Style section, select the title related values for the following options:

    -   Show chart title: Select to add a custom report name. Possible values:
        -   Never
        -   Report only
        -   Always
    -   Chart title: Custom title for the report.

        **Note:** This field is available only if the **Show chart title** field is set to `Always` or `Report only`.

    -   Size of the chart title: Font size of the report title.

        **Note:** This field is available only if the **Show chart title** field is set to `Always` or `Report only`.

    -   Chart title color: Color of the report title.

        **Note:** This field is available only if the **Show chart title** field is set to `Always` or `Report only`.

    -   Title horizontal alignment: Alignment of the report title. Possible values:

        -   Left
        -   Center
        -   Right
        **Note:** This field is available only if the **Show chart title** field is set to `Always` or `Report only`.

7.  Select **Run**.

    ![Incident communication plan report](../image/IAReportResolved.png)

    **Note:** You can also choose a graphical representation for the report or narrow down the result using the **Type** and **Configure** options.


**Parent Topic:**[Managing Incident Communications](../concept/working-with-inci-comm-mgmt.md)

