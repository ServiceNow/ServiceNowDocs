---
title: Provide data for a metric data task
description: Use the metric data task to provide data for a manual metric. Metric data helps you analyze your progress toward your goals.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using GRC: Metrics to provide data, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Provide data for a metric data task

Use the metric data task to provide data for a manual metric. Metric data helps you analyze your progress toward your goals.

## Before you begin

-   To enable support for data estimation refer to [Set up estimation for manual metric definition](set-up-estimation-for-manual-metric-definition.md).
-   Role required: sn\_esg.data\_owner

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Metrics** &gt; **My metric data tasks**.

2.  Open the task for which you want to provide the data.

3.  Select **Move to In Progress**.

4.  On the Metric information form, under the Metric input section, fill in the following fields.

<table id="table_h2g_242_dgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type of Data

</td><td>

Indicates whether the data provided is actual or estimated.

</td></tr><tr><td>

Estimation method

</td><td>

Estimation value for the data. You can choose from the following options:-   **Manual**: Enter a custom estimated value manually.
-   **Average**: Calculate the estimated value based on the average of historical data.
-   **Same period as last year**: Use the value from the same period in the previous year as the estimated value.
This field appears only when **Estimate** is selected in the **Type of Data** field in the metric form.

</td></tr><tr><td>

Number of past periods

</td><td>

Number of past periods data to be included in the average calculation. This field appears only when **Average** is selected in the **Estimation method** field in the metric form.**Note:** The maximum past period limit varies by frequency, confirm that your selection is within these limits:

-   Daily: Up to 180 days
-   Weekly: Up to 52 weeks
-   Monthly: Up to 36 months
-   Quarterly: Up to 12 quarters
-   Semiannually: Up to 6 semi-annual periods
-   Yearly: Up to 3 years


</td></tr><tr><td>

Same period last year

</td><td>

Specifies the period from the previous year to use as the estimated value. This field appears only when **Same period as last year** is selected in the **Estimation method** field in the metric form.

</td></tr><tr><td>

Metric data

</td><td>

Value for the metric. This field appears only when **Quantitative** is selected in the **Category** field in the metric form.**Note:** When **Estimate** is selected in the **Type of Data** a refresh icon is available on **Metric data** field. Selecting that calculates the estimated metric data value.

</td></tr><tr><td>

Unit

</td><td>

Unit of the data. For example, US gallon.**Note:** You can provide the data in any unit and it gets converted to the reporting unit specified in the metric definition.

</td></tr><tr><td>

Variance \(%\)

</td><td>

The variation between the current period and the previous period's metric data.

</td></tr><tr><td>

Response

</td><td>

Response for the metric. This field appears only when **Qualitative** is selected in the **Category** field in the metric form.

</td></tr><tr><td>

I certify and acknowledge that the response I have submitted is accurate.

</td><td>

Option to certify data accuracy.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Additional information for the metric data.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  To provide evidence or supporting information, in the Related documents, related list, select **New**.

7.  On the Related Document form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Provide a name for the supporting information.|
    |Url|Select the lock icon to add a supporting URL.|
    |Metric data task|This field is automatically set to the name of the metric data task for which you’re providing information.|

8.  Select **Submit**.


**Parent Topic:**[Using GRC: Metrics to provide data](../concept/using-grc-metrics.md)

