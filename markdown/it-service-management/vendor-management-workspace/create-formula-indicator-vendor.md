---
title: Add a formula indicator to track vendor score
description: Create a custom formula indicator to add to your calculation for the vendor score. Add the indicator to your KPI group to analyze the score.
locale: en-US
release: zurich
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Vendor Management Workspace, IT Service Management]
---

# Add a formula indicator to track vendor score

Create a custom formula indicator to add to your calculation for the vendor score. Add the indicator to your KPI group to analyze the score.

## Before you begin

Role required: pa\_contributor, pa\_data\_collector, pa\_power\_user, or pa\_admin

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Indicators** &gt; **Formula Indicators**.

2.  Select **New**.

3.  Fill in the fields on the form.

    1.  In the **Name** field, enter a descriptive name for the formula indicator.
    2.  Fill in the **Indicator properties** section.

<table id="table_tr5_ncg_n1c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Direction

</td><td>

-   Select **Maximize** if an increase in score is desired.
-   Select **Minimize** if a decrease in score is desired.


</td></tr><tr><td>

Unit

</td><td>

Select the percentage \(%\) value.

</td></tr><tr><td>

Precision

</td><td>

Rounding of the fractional results.

</td></tr></tbody>
</table>    3.  In the **Formula** section, select **Browse for an indicator**.

        The **Add an indicator to a formula** appears.

    4.  In the **Indicator** field, select the indicator you want to add to the formula.
    5.  Click **Select**.
    6.  Add any mathematical operators such as +, -, \*, or %.
    7.  If you need to add more indicators, select the **Browse for an indicator** link and add more indicators to the formula based on the score you want to calculate.
4.  Select and hold \(or right-click\) the form header and select **Save**.

5.  Add a vendor breakdown for the indicator.

    1.  In the Breakdowns related list, select **Edit**.
    2.  Select **Vendors** from the Collection list and add it to the Breakdowns list.
    3.  Select **Save**.
6.  Add the indicator to the vendor KPI group.

    1.  Navigate to **All** &gt; **Vendor Management** &gt; **Configuration** &gt; **KPI Groups**.
    2.  Select the KPI group to which you want to add the formula indicator.
    3.  In the KPIs related list, select **New**.

        The KPIs form appears.

    4.  In the **KPI** field, select the formula indicator you've created.
    5.  In the **Order** field, set the order number.
    6.  Select **Submit**.

        **Note:** In the KPI Group form, make sure the combined weight of all KPIs in the KPIs related list adds to 100. If the combined weight is over 100, then the weight will be proportionately readjusted to 100.


## Result

The formula indicator is added to the KPI group and is used for calculating the vendor score in Vendor Management Workspace.

For detailed information on creating a formula indicator, see [Create a formula indicator](https://www.servicenow.com/docs/access?context=t_CreateAFormulaIndicator&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

