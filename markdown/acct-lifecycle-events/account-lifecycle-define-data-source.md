---
title: Define the data source
description: Before calculating the health, product adoption, or product usage score, you must specify the source from which data is to be collected. Data can be collected either through key performance metrics and external sources, or can be calculated.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Set up the Data Context Engine, Customer success, Configure, Customer Success Management]
---

# Define the data source

Before calculating the health, product adoption, or product usage score, you must specify the source from which data is to be collected. Data can be collected either through key performance metrics and external sources, or can be calculated.

To define the data source, follow these steps:

1.  Login as a user with the `sn_acct_lc.customer_success_application_admin` role.
2.  Navigate to **All** &gt; **Data Context Engine** &gt; **Data Sources** &gt; **Create New**.
3.  Enter the following details:

<table id="table_gtm_2sk_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the data source.

</td></tr><tr><td>

Source

</td><td>

Select the source from which the data is to be collected from the list.-   **PA indicator**: Select this option to use a PA indicator to collect performance analytics data at regular intervals and create records in the Context Engine Data table.
-   **External**: Specify the external data source from which the data is to be collected. You must define how this data can be retrieved from the external source or use the [Table API](https://www.servicenow.com/docs/access?context=c_TableAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) to save this information in the Context Engine data table.
-   **Calculated**: Select this option to calculate the metric values dynamically using formulas based on a combination of existing base metrics. For more details, see [Define a calculated metric data source](../task/account-lifecycle-define-data-source-calculate.md).
-   **Table**: Select this data source type to retrieve and analyze data from internal and external tables. To retrieve data from external sources, you must install the Workflow Data Fabric Hub application and create data fabric tables. For more details, see [Define a table data source](../task/account-lifecycle-define-data-source-table.md).
**Note:** The sequence in which the metrics are calculated is based on the Execution order that defines which metrics are evaluated first. The Execution order is defined as follows:

-   PA Indicator and External: 0 \(Metrics from these data sources are calculated first\).
-   Calculated metrics: 1 + Max\(The child or dependent metrics associated with the parent metric are calculated first followed by the parent metric\).


</td></tr><tr><td>

Frequency

</td><td>

Select the frequency at which the data should be collected from the list.-   Daily
-   Weekly
-   Monthly
-   Quarterly
**Note:** If you select PA Indicator as your data source, you must select a frequency equal to or greater than the PA Indicator collection frequency. For example, if the PA Indicator is collecting data once a week, you can't select a frequency that is lower than Weekly here.

</td></tr><tr><td>

PA indicator

</td><td>

Select the metric for which the data is being collected.

</td></tr><tr><td>

Breakdown

</td><td>

Select the attribute or category by which the health or risk score is to be grouped. This can be account, product, and so on.

</td></tr><tr><td>

Breakdown table

</td><td>

Select the source table against which the score is calculated.**Note:** This field is applicable only if the Source type is **Calculated** See [Define a calculated metric data source](../task/account-lifecycle-define-data-source-calculate.md) for details.

</td></tr><tr><td>

Target table mapping

</td><td>

\(Optional\) If the Source type is **Calculated**, you can optionally specify the Target table, Target field, and Target query field. After data collection, the calculated score is written into the matching records where the context aligns with the Target query field. See [Define a calculated metric data source](../task/account-lifecycle-define-data-source-calculate.md) for more details.

</td></tr><tr><td>

Unit of measurement

</td><td>

Select the unit of measurement for the PA indicator that can be minutes, hours, days, months, and so on.

</td></tr><tr><td>

Aggregate

</td><td>

Select how the aggregate score should be calculated from the list.-   Average
-   Sum
-   Max
-   Min
-   Count \(This is applicable only if the Source type is **Table**\). See [Define a table data source](../task/account-lifecycle-define-data-source-table.md) for details.
The Aggregate score is useful if you select a Frequency that is different from the collection frequency of the PA indicator. For example, suppose the PA indicator collection frequency is set to Daily, and the Frequency is set to Weekly, and you want to calculate the aggregate score for the week. In this case, you can use the average or sum option to calculate the score.

</td></tr><tr><td colspan="2">

The following fields are applicable only if you select the **Source** as **Table**.

</td></tr><tr><td>

Source table

</td><td>

Select the table from which the source data is to be retrieved. This can be an internal ServiceNow table or an external table.

</td></tr><tr><td>

Group by fields

</td><td>

If you select the **Table** type data source, you must specify the fields by which the data should be grouped.**Note:** You can use up to two fields for grouping.

</td></tr><tr><td>

Conditions

</td><td>

Specify the conditions or filters that will be used while retrieving the data. For example, you can choose to retrieve records for a specified period of time.

</td></tr><tr><td>

Source value

</td><td>

Select the field on which the aggregation is to be performed.

</td></tr><tr><td>

Source reference

</td><td>

The source record used to resolve the **Group by** fields. This field is automatically populated if you selected a single reference type field in the **Group by fields** option.

 You must update the Source reference resolver script and specify the fields that are to be mapped if the **Group by fields** contains:

-   Two fields \(maximum allowed\)
-   A non-reference field.
-   An external field.


</td></tr></tbody>
</table>4.  Select **Submit** to create this data source.
5.  Navigate to the **Contexts** related list and select **New**.
6.  In the Context page, select the table for which this data source is applicable. This relationship enables the Data Content Engine to collect data from the specified table. Depending on the type of score being calculated, select the table as follows:

    -   Health score: Select the Engagement table.
    -   Success outcome: Select the Success Outcome table.
    -   Product adoption: Select the Sold Products table.
    -   Product capability: Select the Product Capability Usage table.
    **Note:** You can define multiple context tables for a single data source.

7.  Enable the **Active** check box and click **Submit** to create the data source. You can associate the data source with one or more context tables.
8.  Define color bands as necessary. See the [Setup the color banding table](../task/account-lifecycle-setup-color-banding.md) for details. The color banding is applied to the health metric data displayed in the [Health](account-lifecycle-view-engage.md#section_p2r_t43_qdc) tab on the Engagement home page.

After setting up the data source and the context, the next step is to configure the context engine mapper. See the [Configure the Context Engine Mapper](account-lifecycle-define-context-engine-mapper.md) for details.

-   **[Define a calculated metric data source](../task/account-lifecycle-define-data-source-calculate.md)**  
Define dynamic metrics using formulas based on other metrics.
-   **[Define a table data source](../task/account-lifecycle-define-data-source-table.md)**  
Use the **Table** data source to retrieve data from internal ServiceNow tables or from external sources using Workflow Data Fabric.

**Parent Topic:**[Set up the Data Context Engine](../task/account-lifecycle-setup-dce.md)

