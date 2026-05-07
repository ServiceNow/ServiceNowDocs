---
title: Configure Forecast Model
description: The forecast model is a framework used to predict future sales based on historical data, current sales activities, and other relevant factors.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Sales Forecasting, Lead and opportunity management apps, Configure, Sales Customer Relationship Management]
---

# Configure Forecast Model

The forecast model is a framework used to predict future sales based on historical data, current sales activities, and other relevant factors.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Sales Forecast** &gt; **Forecast Model**.

2.  Select  **New**.

3.  On the form, fill in the fields.

<table id="table_wxs_pvw_h3c"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the forecast model that you want to create.

</td></tr><tr><td>

Description

</td><td>

Short description of the forecast model.

</td></tr><tr><td>

Forecast Source

</td><td>

Entity from which forecast data is generated. For example, Opportunity and Opportunity Allocation.

</td></tr><tr><td>

Filter By

</td><td>

Conditions that limit that records from the forecast source are included in the forecast.

</td></tr><tr><td>

Rollup Type

</td><td>

Select how forecast values roll up the hierarchy. For example, cumulative and single.

</td></tr><tr><td>

Measure Type

</td><td>

Data type of the forecast value.

</td></tr><tr><td>

Active

</td><td>

Option to activate the forecast model.

</td></tr><tr><td>

Measure

</td><td>

Parameter to calculate the forecast value.

</td></tr><tr><td>

Order

</td><td>

Display order of the forecast model.

</td></tr><tr><td>

Primary Hierarchy Type

</td><td>

Select **Sales Team** or **Territory** to select the hierarchy used to roll up the forecast values.

</td></tr><tr><td>

Sales Team Hierarchy

</td><td>

Conditions that restrict which sales teams are included in the rollup.

</td></tr><tr><td>

Territory Hierarchy

</td><td>

Territories that are included in the rollup.**Note:** This field is displayed when you select **Territory** from the Primary Hierarchy Type list.

</td></tr><tr><td>

Secondary Hierarchy Type

</td><td>

Select the secondary hierarchy that will be displayed within a territory or sales team, for example, Product Offering Family.

</td></tr><tr><td>

Base

</td><td>

Option to submit and adjust forecasts at base forecast source. **Note:** If you select this option, **Single** is the default option for Rollup Type field.

</td></tr></tbody>
</table>4.  Enter the configurations for forecast generation.

    1.  Select **Forecast Configuration Overrides** related list.

    2.  From the **Forecast Date Field** list, select the date from the forecast source to generate the forecast.

    3.  From the **Forecast Category Field** list, select the category to generate the forecast.

    4.  From the **Forecast Territory Field** list, select the field from the Forecast Source that contains the territory information.

    5.  From the **Product Offering Family Field** list, select the field from the Forecast Source table that contains product offering family information.

5.  Select the conditions to configure the forecast periods and submissions.

    1.  Select **Period and Submissions** related list.

    2.  From the **Primary Forecast Period** list, select the period for which you want to generate the forecast.

    3.  From the **Additional Forecast Period** list, you can select more granular periods from the Primary Forecast Period to generate forecasts.

    4.  Select the **Submission Required** check box to activate the submission period.

    5.  From the **Submission Frequency** list, select the frequency to submit forecasts.

6.  Configure the owner of the forecast.

    **Note:** This field is displayed only when you select **Territory** from **Forecast Hierarchy Type** list.

    1.  Select **Forecast Owner Configuration** related list.

    2.  From the **Forecast Owner Field** list, select the field that determines the owner of that forecast.

7.  Define the rolled‑up forecast at each level of the selected forecast hierarchy.

    **Note:** This field is displayed only when you select **Territory** from **Forecast Hierarchy Type** list.

    1.  Select **Rollup Owner Configuration** related list.

    2.  From **Rollup Owner Source** list, select the table that determines the rollup owner.

    3.  From the **Rollup Owner Field** list, select the table field that identifies the rollup owner on the selected rollup owner source.

    4.  In the **Rollup Owner Criteria** field, use **Add Filter Condition** or **Add OR Clause** to refine the rollup owner selection.

    5.  From the **Rollup Owner to Forecast Association** field, define how the rollup owner record is associated to the forecast record.![Roll Up Owner Configuration](../image/roll-up-owner-config-sf.png)

    6.  From the **Forecast to Rollup Owner Association** field, define how the forecast record is associated back to the rollup owner.

        **Note:** The values in the **Rollup Owner to Forecast Association** and **Forecast to Rollup Owner Association** fields should be identical.

8.  Select **Submit**.


## Result

The new forecast model is created. You can view it on the Forecast Models page.

