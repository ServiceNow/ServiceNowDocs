---
title: Add additional reporting configuration filters for a Microsoft 365 configuration record in risk
description: Add additional reporting filters to specify at a granular level what data must be imported to the report from a table using the Management Reporting of Risk application.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating Microsoft 365 with Management Reporting of Risk, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Add additional reporting configuration filters for a Microsoft 365 configuration record in risk

Add additional reporting filters to specify at a granular level what data must be imported to the report from a table using the Management Reporting of Risk application.

## Before you begin

Role required: sn\_risk\_advanced.ara\_admin

## About this task

When you specify that you want to import data from a particular table, you must also specify from which exact record of the table you need the data. For example, assume that you specify that you want to fetch data from the sn\_risk\_risk table. This table may have multiple records. Therefore, you must specify the exact record from which you want to fetch the data. You can specify as many filters as you require.

## Procedure

1.  Navigate to **All** &gt; **Management Reporting of Risk** &gt; **Microsoft 365 Reporting Integration** &gt; **Reporting Configurations**.

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

Name of the field from which data must be fetched. For example, for the risks table, you can specify the **Name** field. If you select a name, then all the names of the risks are available for selection during data import.

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

The configuration data is ready to be imported in to your add-in.

