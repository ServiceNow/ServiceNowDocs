---
title: Create Inbound Data Exclusion Rules
description: Create inbound data exclusion rules in order to filter any type of data or any kind of incoming source records data.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [About Rules Engine in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# Create Inbound Data Exclusion Rules

Create inbound data exclusion rules in order to filter any type of data or any kind of incoming source records data.

## Before you begin

The application supports the integration of multiple threat intelligence feeds, including STIX data sources. To ensure that only relevant data is ingested, customizable exclusion rules must be applied.

Role required: sn\_sec\_tisc.admin

## About this task

Exclusion rules are created and applied on a source record to process further steps. The base system provides the **Sample Filtering Rule** for the users with a predefined rule to filter the ingested observables, indicators data, or entities/objects.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Drill down to **Rules Engine** &gt; **Inbound Data Exclusion Rules**.

3.  Click **New** to define exclusion rules.

    The Create New Inbound Data Exclusion Rules page is displayed.

4.  On the form, fill in the fields.

<table id="table_pvj_fv5_fyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new exclusion rule.

</td></tr><tr><td>

Description

</td><td>

Short description of the exclusion rule.

</td></tr><tr><td>

Order

</td><td>

The exclusion rule priority. This field indicates the order in which the exclusion rules are executed when two or more rules share the triggering conditions. The exclusion rule with the lowest number has the highest priority. To set the order of operation, enter a value. For example, 100, 200, 300, and so on.

The default value is 100 for the base system exclusion rule.

</td></tr><tr><td>

Data Sources

</td><td>

Select the feeds for which the exclusion rule should be applied.

</td></tr><tr><td>

Table

</td><td>

Select the type of table that you would want to apply the filter for. For example, Observable Source, Indicator Source, and Object Source.

</td></tr><tr><td>

Filter Type \(only when Table selected is Observables Source\)

</td><td>

Filter types contains two options based on which you can apply the filter.-   Filter based on Condition
-   Filter based on List


</td></tr><tr><td>

Filter Type \(Filter based on Condition\)

</td><td>

Filter conditions in the condition builder. These conditions are based on the source table. For example, Indicator Source and Object Source has only filter type: Filter based on Condition.To add more conditions, click **AND** or **OR**. If **AND** is selected, all conditions must be matched. If **OR** is selected, either condition can be matched. To set a second filter condition, click **New Condition set**.

</td></tr><tr><td>

Filter Type \(Filter based on List\)

</td><td>

If the inbound observables matches against the entries in the list selected will be filtered.**Note:** These exclusion rules doesn’t apply for Data Imports using the import Intelligence and the available options are Allow list, Deny list, and Watch list.

</td></tr></tbody>
</table>    The records excluded by the exclusion rule can be viewed in the following sections.

    1.  **Filtered Observable Records**: Filters and lists the observables records.
    2.  **Filtered Indicators Records**: Filters and lists the indicators records.
    3.  **Filtered Object Records**: Filters and lists the object records.
    **Note:** In order to apply the exclusion rules based on tags which are added to the source records, then select **TISC tags** option in the Filter conditions builder.


