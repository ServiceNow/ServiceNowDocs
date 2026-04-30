---
title: Create a risk definition
description: Use the engagement risk definition to configure the metrics required to define the risk signals for an engagement.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage engagements, Customer success, Configure, Customer Success Management]
---

# Create a risk definition

Use the engagement risk definition to configure the metrics required to define the risk signals for an engagement.

## Before you begin

-   Role required: sn\_acct\_lc.customer\_success\_agent
-   Data source and data context engine mapping must be setup for metric based risk definitions. See [Data Context Engine](../concept/account-lifecycle-setup-metric-data.md) for details.
-   For table based risk definitions, an active context engine mapping with source table as Engagement must be defined.

## About this task

You can define the risk conditions, risk category, and threshold values for an engagement in two ways:

-   **Metric based risk definition**

    Use this option to create or update risks if the specified threshold is breached. The context engine data records are generated after the last scheduled job is run. The context in this case is the engagement table. If the threshold specified in the risk definition is breached, a risk is generated.

-   **Table based risk definition**

    Use this option to create or update risks for all records that match the condition in the selected table. When the scheduled job is run, if an active risk that matches the criteria is present, a new risk occurrence record is created. If no active risks are present for the source record+engagement+category combination, a new risk signal is generated for each record.


New risks are generated automatically when the Customer Success Risk Analyzer scheduled job is executed.

## Procedure

1.  Navigate to **All** &gt; **Success Configuration** &gt; **All Risk Definitions** &gt; **New**.

2.  Enter the following details:

<table id="table_i5y_ynt_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the risk definition.

</td></tr><tr><td>

Category

</td><td>

Select a category for the risk definition. The risk categories displayed here are defined in the [Create a customer success choice record](account-lifecycle-ale-choice.md).

</td></tr><tr><td>

Type

</td><td>

Select the type of risk definition. This can be:-   Metric
-   Table


</td></tr><tr><td>

Description

</td><td>

Enter a description for the risk definition.

</td></tr><tr><td colspan="2">

`Metric based:` This option is used to create or update risks if a risk threshold is breached. If you’re creating a metric based risk definition, select the metric, define the thresholds, set up the template, and specify conditions to define the list of applicable engagements.

</td></tr><tr><td>

Metric

</td><td>

Select the metric definition that has been configured in the Data Source table and mapped with the context engine mapper. See [Data Context Engine](../concept/account-lifecycle-setup-metric-data.md) for details.

</td></tr><tr><td>

Threshold condition

</td><td>

Specify the threshold condition for the risk definition. If this threshold condition is breached, a risk signal is generated. For example, for the Daily collection of CSAT, the metric threshold condition is set to be less than 50. If the value falls below 50, a risk is generated.

</td></tr><tr><td>

Threshold

</td><td>

Specify the base threshold for the metric definition.

</td></tr><tr><td>

Applicable engagements

</td><td>

If you select an applicable engagement, this risk definition will be evaluated for the engagements in the Applicable engagements list.

</td></tr><tr><td colspan="2">

`Table based:` This option is used to create or update risks in all records in the matching table and the specified condition. If you’re creating table based risk definition, you must select the table, specify the condition, and set up the template with fields and values to generate risks in the specified format.

</td></tr><tr><td>

Source table

</td><td>

Select the source table for which the risk definition is to be created.**Note:** A context mapper must have been defined that associates the source and the context tables. See [Data Context Engine](../concept/account-lifecycle-setup-metric-data.md) for details.

For example, if you want to define risk signals for a contract, and select Contract as your source table, a context mapping with a Contract to Engagement association must have been defined.

</td></tr><tr><td>

Conditions

</td><td>

Specify any conditions that must be used for the risk definition for the selected source table. Risks are generated for the records in the source table that satisfy the specified conditions.

</td></tr><tr><td>

Template

</td><td>

Select the Template tab to define the fields for the risk definition. The following are mandatory fields:-   Short description
-   Description
-   Reported by


</td></tr></tbody>
</table>3.  Select **Submit** to create the risk definition.

4.  If you want to define risk threshold overrides for a metric based definition, open the risk definition you have created, navigate to the `Risk Threshold Overrides` related list and select **New**.

    Enter the following details:

    -   Engagement risk definition: This is the engagement risk definition for which you’re creating an override condition.
    -   Threshold: Specify the override threshold value.
    -   Select **Add Filter Condition** or **Add Or Clause** to specify additional override conditions.
    -   Rank: Specify a rank for this override condition. 1 is highest rank. If an engagement matches multiple threshold overrides, the engagement with the highest rank is considered first.
5.  Select **Submit** to create the override condition.

6.  Select **Publish**.

    When the next scheduled job is run, the risk signals are generated. Navigate to **Data Context Engine** &gt; **Context Engine Data** to see the date and time the risk signals are generated.

    ![Context engine data](../image/account-lifecycle-context-engine-data.png)


-   **[Sample risk definitions](../concept/account-lifecycle-risk-demo-data.md)**  
These are sample risk definitions available with the base system and can configured based on your requirements.

**Parent Topic:**[Manage engagements](../concept/account-lifecycle-manage-engagement.md)

