---
title: Configure extreme repetition
description: Configure an extreme repetition definition to view a pattern where a transition repeats more than the usual repetition range between the steps.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting Automated improvement opportunities, Setting improvement opportunities, Use, Process Mining, Platform Analytics]
---

# Configure extreme repetition

Configure an extreme repetition definition to view a pattern where a transition repeats more than the usual repetition range between the steps.

## Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

Extreme repetitions finding definition surfaces transitions that are repeated significantly more than the median repetition. This helps uncover potential repetition anomalies.

![Extreme repetition](../image/extreme-repetition.png)

## Procedure

1.  Navigate to Improvement opportunity definition page.

    For information about the Improvement opportunity definition page, see [Set improvement opportunities](improve-opportunities.md).

2.  Select **Create** on the Extreme repetitions card.

    For a particular type of automated finding, you can create a maximum of two automated findings.

3.  Provide details in the **Define** section.

<table id="table_gyh_kjk_wbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Specify a name for your automated finding definition.

</td></tr><tr><td>

Pattern type

</td><td>

This field is auto-populated. The automated finding definition that you chose to create is displayed here.You can change it if necessary.

</td></tr><tr><td>

Field to detect the pattern on

</td><td>

Select any field from the table on which you want to detect this pattern. The entire finding definition works on this field.

</td></tr><tr><td>

Category

</td><td>

Specify a category to which the automated finding definition belongs. The available options are:-   Quality
-   Automation
-   Conformance
-   Performance


</td></tr><tr><td>

Active

</td><td>

Select the field if you want this finding definition to be active. By default, it’s selected.

</td></tr><tr><td>

Table

</td><td>

Displays the table name that you have selected. This field is non-editable.

</td></tr><tr><td>

Apply to process/project

</td><td>

Displays the table name that you have selected. This field is non-editable.

</td></tr><tr><td>

Impacted KPIs

</td><td>

Select the KPIs most likely impacted by the findings. Choosing the affected KPIs enables you to assess the business impact. You can view the KPI-related findings in the insights panel of the Process Mining workspace.

</td></tr></tbody>
</table>4.  Select **Configure**.

    The **Configure** tab is displayed.

5.  Fill the details on the form.

    Default values are provided. You can edit them if needed.

    ![Extreme repetition configuration](../image/extreme-repetition-config.png)

    According to the example, records that meet the following conditions are available as improvement opportunities in the Summary and insights page:

    -   The minimum repetition is calculated as multiplier x median repetition for transition. In this example, records must meet or exceed 20 times the median repetition.
    -   A transition must contain at least 20 records.
    -   The top percentage of records in the extreme high repetition category that can qualify. Prevents too many records from being included and focuses on true outliers. In this case it is 2%.
    -   A maximum of 5 improvement opportunities will be generated in the Summary and insights page.
6.  Select **Save and exit**.


**Parent Topic:**[Setting Automated improvement opportunities](../concept/automated-findings.md)

