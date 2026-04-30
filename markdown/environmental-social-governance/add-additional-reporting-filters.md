---
title: Add additional reporting configuration filters for a Microsoft 365 configuration record
description: Add additional reporting filters to specify at a granular level what data must be imported to the disclosure report from a table.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrating Microsoft 365 with ServiceNow reporting, Integrating ESG Management with other applications, Environmental, Social, and Governance Management]
---

# Add additional reporting configuration filters for a Microsoft 365 configuration record

Add additional reporting filters to specify at a granular level what data must be imported to the disclosure report from a table.

## Before you begin

Role required: \(per product\)

-   In Environmental, Social, and Governance Management: sn\_esg\_msoff\_intg.admin
-   In Audit Management: sn\_audit.admin

## About this task

When you specify that you want to import data from a particular table, you must also specify from which exact record of the table you need the data. For example, assume that you specify that you want to fetch data from the sn\_gf\_goal table. This table may have multiple records. Therefore, you must specify the exact record from which you want to fetch the data. You can specify as many filters as you require.

## Procedure

1.  Navigate to once of the following locations:

    -   **All** &gt; **Environmental, Social, and Governance** &gt; **Microsoft 365 Reporting Integration** &gt; **Reporting Configurations**
    -   **All** &gt; **Audit** &gt; **Audit report** &gt; **Reporting Configurations**
2.  Open the record for which you want to add the additional reporting configuration filters.

3.  On the Microsoft 365 reporting configuration filters related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_ehy_kb2_vvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reporting configuration

</td><td>

Name of the configuration to which you're adding additional filters. This field is automatically set.

</td></tr><tr><td>

Field name

</td><td>

Name of the field from which data must be fetched. For example, for the goals table, you can specify the **Name** field. If you select name, then all the names of the goals are available for selection during data import.

</td></tr><tr><td>

Related fields

</td><td>

Fields in the add-in pane that are dependent on the selected **Field name**. Only records relevant to the selected **Field name** will be displayed as choices. For example, only entities related to a selected metric definition will be available as a choice. For more information, see [Add related fields to a Microsoft 365 configuration record](add-related-fields-0365.md).

</td></tr><tr><td>

Order

</td><td>

Order of the field as it would appear on the add-in pane of the document.

</td></tr><tr><td>

Aggregate on time dimension

</td><td>

Option to aggregate the report configuration source table data based on the chosen time dimension. For more information about this option, see the example in the procedure. This field only appears when the **Field name** has **Time dimension**.

</td></tr><tr><td>

Time dimension

</td><td>

Time dimension for which data must be aggregated. The list of time dimensions are:-   Year
-   Semi-annual
-   Quarter
-   Month
-   Week
-   Date
Select the dimensions according to your requirement and move them from the Available list to the Selected list. **Note:** This field only appears when the **Aggregate on time dimension** option is selected.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

The configuration data is now ready to be imported in to your add-in.

## Data aggregation for entities

If an ESG reporting disclosure manager wants to understand the total emissions for an entire year for a particular location and if the location has sub-locations, you can also aggregate the data and use it for reporting purposes. For example, consider that your organization has a location Japan. Japan, in turn, has two sub locations, Tokyo and Kyoto. Assume that you want to find your total yearly Scope 1 emissions for the year 2022 for Japan. Using the time dimensions feature, you can aggregate your data and get a view of your total emissions for a year. You can also aggregate the data for a quarter, week, or a month depending on your reporting requirements. The metric data is aggregated at frequencies higher than the metric data collection frequency. To achieve this, in the **Source table** field, select **Metric data by entity \[sn\_grc\_metric\_data\_by\_entity\]** and select the **Aggregate on time dimension** option, and select the time dimension field from the source table.

-   **[Add related fields to a Microsoft 365 configuration record](add-related-fields-0365.md)**  
Add related fields to filter values based on the chosen primary field. These filter values will automatically adjust according to the selected filter criteria.

**Parent Topic:**[Integrating Microsoft 365 with ServiceNow reporting](../concept/integrating-o365-with-servicenow.md)

