---
title: Create a metric
description: Create a metric to perform calculations on your data.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Environmental, Social, and Governance Management]
---

# Create a metric

Create a metric to perform calculations on your data.

## Before you begin

Role required: sn\_esg.metric\_manager

## About this task

To create a metric, you need a metric definition and an entity. A metric definition defines the method for collecting the score for an entity. When a metric definition gets associated with an entity, it creates a metric.

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **ESG Workspace** &gt; **Metrics**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_lrv_yw4_brb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the metric. For example, `Number of incidents- ACME Asia`.

</td></tr><tr><td>

Description

</td><td>

Brief description of the metric.

</td></tr><tr><td>

Active

</td><td>

Option to mark the metric definition as active.

</td></tr><tr><td>

Key metric

</td><td>

Option to mark the metric definition as a key metric.

</td></tr><tr><td>

Metric definition

</td><td>

Metric definition associated with the metric.

</td></tr><tr><td>

Type

</td><td>

Method used to determine if the score is collected manually or in an automated manner. This field is automatically set to **Automated** but the value changes when you select the metric definition and gets updated to the type of the metric definition.

</td></tr><tr><td>

Entity

</td><td>

Entity associated with the metric.

</td></tr><tr><td>

Enterprise Owner Type

</td><td>

Enterprise owner type who is responsible for the metric. This field is automatically set.

</td></tr><tr><td>

Enterprise owner

</td><td>

Enterprise owner of the metric definition. This field is automatically set.

</td></tr><tr><td class="sub-head" colspan="2">

Metric Properties

</td></tr><tr><td>

Direction

</td><td>

Direction of the automated metric definition. The choices are as follows:-   **None**: If you don’t want any change in the metric direction, select this option.
-   **Minimize**: If the desired metric direction is downward or descending, select this option. For example, you want to minimize the fuel consumption.
-   **Maximize**: If the desired metric direction is upward or ascending, select this option. For example, you want to maximize the use of natural resources in your organization.
-   **Milestone**: When the metric direction isn’t applicable, but the metric is tracked against a milestone, select this option. For example, if your organization is going to launch a new renewable energy product in the market, the upcoming launch date is considered as a milestone.


</td></tr><tr><td>

Precision

</td><td>

Number of decimal places after the decimal point on a score.

 When an indicator has a Precision of 0, the indicator rounds the result to the nearest even, whole number. For example, if an indicator with Precision 0 calculates the values 7 + \(5 / 2\), the indicator rounds the result up to 10. However, if the formula calculates 2 + \(5 / 2\), the indicator rounds the result down to 4.

 When an indicator has a Precision greater than 0, the indicator rounds to the nearest decimal point for the given precision. For example, an indicator with Precision 1 rounds a result of 4.45 as 4.5.

</td></tr><tr><td>

Unit

</td><td>

Unit for the automated metric definition. You can define the units in which the scores are shown. The most commonly used units are provided by default.

</td></tr><tr><td>

Nature

</td><td>

Nature of the automated metric definition. The choices are as follows:-   **None**
-   **Leading**: If the metric is an indicator of future events, select this option. For example, consider the number of sales that a store makes on new solar batteries. This number is a leading indicator for the support requests that the store may receive in the future.
-   **Lagging**: If the metric is an indicator of past events, select this option. For example, consider the number of sales that a store has made in the previous year. This number is a lagging indicator for the support requests that the store has received in the past year.
-   **Current**: If the metric is an indicator of the current state of the events, select this option. For example, consider the number of sales that a store has made in the current year. This number is an indicator of the current support requests received by the store.


</td></tr><tr><td class="sub-head" colspan="2">

Method

</td></tr><tr><td>

Table

</td><td>

Table that is queried for creating the metric definition. This field is automatically set.

</td></tr><tr><td>

Method Type

</td><td>

Type of automated metric. The choices are as follows:-   **Basic**
-   **Scripted**
 **Note:** If you select **Scripted**, you must save the form and select **Add script** to add your script. Only users with the sn\_grc.developer role can add scripts.

</td></tr><tr><td>

Table

</td><td>

Table that is queried for creating the metric definition. This field is automatically set.

</td></tr><tr><td>

Criteria

</td><td>

Condition for the record from which a score is obtained. Build a filter by adding conditions that contain a field, operator, and values and then select **Set**.**Note:** Select a value for the **Table** field before modifying this field.

</td></tr><tr><td>

Aggregate

</td><td>

Method to aggregate the automated metric definition score. When an option is selected in the **Aggregate** field, a new **Aggregation Field** is displayed next to the **Aggregate** field. The **Aggregation Field** displays the selected record. The choices for the **Aggregate** field are as follows:

 -   **Count**: Count of the number of records that are rendered by the table query that is set in the filter criteria.
-   **Sum**: Sum of the values of the parameters based on the selected value in the **Aggregation Field**.
-   **Average**: Average of the values of the parameters based on the selected value in the **Aggregation Field**.
-   **Maximum**: Maximum of the values of the parameters based on the selected value in the **Aggregation Field**.
-   **Minimum**: Minimum of the values of the parameters based on the selected value in the **Aggregation Field**.
-   **Count Distinct**: Number of groups in the result set that is grouped by the **Aggregation Field**.
 **Note:** The **Aggregation Field** is displayed for all the options except **Count**.

</td></tr><tr><td>

Reference field

</td><td>

Field based on which the metric data can be segregated. This field connects the entity to the selected scoring table and it calculates a score that is specific to an entity. **Note:** Ensure that the table that the reference field points to matches with the table of the records that the associated entities point to, through the **Applies to** field in the entity form.

 **Note:** It’s the user's responsibility to validate the criteria mentioned in the note as the system doesn’t validate it. Select a table before modifying this field.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Calendar

</td><td>

Calendar to use for metric collection. Only the configured calendar options are available. This field is automatically set to **Standard Calendar**. Standard calendar refers to the Gregorian calendar. This field can be modified only if the metric definition for this metric doesn’t use the standard calendar.

</td></tr><tr><td>

Frequency

</td><td>

Collection frequency for the metric definition. This field is automatically set based on the frequency of the selected metric definition.

</td></tr><tr><td>

First run date

</td><td>

Date the metric is run the first time.

</td></tr><tr><td>

Due date offset

</td><td>

Number of days after the schedule end date when the metric data task becomes overdue. For example, if the frequency of a metric definition is monthly and if the you enter `15` in this field, then the due date for metric data task will be overdue 15 days after the month ends. This field only appears when the metric definition associated with the metric is of type Manual.

</td></tr><tr><td>

Next run date

</td><td>

Date when the metric going to be executed.

</td></tr><tr><td>

Period date

</td><td>

Date used to specify the start and end dates for the data collection period.

</td></tr><tr><td class="sub-head" colspan="2">

Data Collection Details

</td></tr><tr><td>

Data owner type

</td><td>

Data owner type, such as User.

</td></tr><tr><td>

Data owner

</td><td>

Name of the user as the data owner.

</td></tr><tr><td class="sub-head" colspan="2">

Approval**Note:** This section appears only when the Metric approval property is set to Simple. For more information see, [Components installed with ESG Management](../../esg-management-reporting/reference/components-installed-with-esg.md).

</td></tr><tr><td>

Approval required

</td><td>

Option to indicate if an approval is required.

</td></tr><tr><td>

Approver type

</td><td>

Type of the approver of the metric definition. The choices are as follows:-   **User**
-   **User group**


</td></tr><tr><td>

User

</td><td>

Approver user or approver group that is responsible to approve the metric definition. The choices are as follows:-   **Approver**: Displayed when the User option is selected.
-   **Approver group**: Displayed when the User group option is selected.
**Note:** By default, the approver is the user specified in the metric definition, but this can be overridden at the metric level.

</td></tr><tr><td class="sub-head" colspan="2">

Classification

</td></tr><tr><td>

Group

</td><td>

Area that the metric relates to.

</td></tr><tr><td>

Reporting classification

</td><td>

Tag used to categorise the metric.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup that the metric relates to.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td colspan="2">

**Note:** This section only appears when:

-   The **sn\_grc.enable\_record\_confidentiality** property is enabled under GRC properties.
-   The record is in **Draft** state.


</td></tr><tr><td>

Allowed users

</td><td>

Users who can view the record.**Note:** By default, the logged in user is added to the list of confidential users.

</td></tr><tr><td>

Allowed groups

</td><td>

Groups that can view the record.

</td></tr></tbody>
</table>4.  Click **Save**.

    **Note:** After a new metric is created, the related lists along with the **Details** tab are displayed on the form. You can view the metric data overview in the **Overview** tab. The Metrics overview page displays the metrics data details when you execute a metric along with the duration for which the data is collected.


## Result

The metric is saved in the Metrics list.

**Parent Topic:**[Configuring GRC: Metrics](../concept/configuring-grc-metrics.md)

