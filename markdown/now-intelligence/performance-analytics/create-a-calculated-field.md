---
title: Create a calculated field for a Data snapshots source
description: Show the length of time that has passed between two date/time fields on a Data snapshots source table. For example, calculate Age as the difference between Created and Updated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/create-a-calculated-field.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [indicator, breakdown, performance analytics]
breadcrumb: [Bucket group mappings and calculated fields, Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a calculated field for a Data snapshots source

Show the length of time that has passed between two date/time fields on a Data snapshots source table. For example, calculate Age as the difference between Created and Updated.

## Before you begin

Read [Bucket groups and calculated fields in Data Snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/ds-bucket-groups-calculated-fields.md), particularly the Limitations section.

Role required: pa\_data\_collector or higher

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **Breakdowns** &gt; **Calculated Fields** and select **New**.

2.  In the **Name** field, enter a short, descriptive name.

3.  In the **Description** field, provide more details about the calculated field.

4.  In the **Table** field, select the table to which to add the calculated field.

    The table should be used as a Data snapshots source.

5.  In the **Formula** field, define a DATEDIFF function.

    The DATEDIFF function has three parameters, which you specify in a comma-separated list without spaces.

    -   Time unit, in the singular. Supported units include 'day', 'week', and 'second'.
    -   Name of the field with the start time
    -   Name of the field with the end time
    The format follows:

    ```
    DATEDIFF('unit',start_time_field,end_time_field)
    ```

    **Note:** Use the technical field name, not the human-readable label. For example, use sys\_created\_on, not Created.

    Both the name and the formula must be unique. If either duplicates an existing calculated field, an error message is displayed and the record is not saved.


## Result

If both fields in a calculated field formula are listed as dimensions of a Data snapshots source, the calculated field is listed as Eligible on that source.

## Incident Age calculated field

You want to sort the indicator scores for incidents by age. There is no one field on the Incident table that tracks this. However, you determine that the difference between the Created date stamp and the Updated date stamp provides a reasonable approximation. You can filter the scores by another condition if you want the ages of only active incidents, for example.

You create a calculated field with the following values:

-   Name: Age
-   Description: The age of each incident at the time of its last update
-   Table: Incident
-   Formula: DATEDIFF\('day',sys\_created\_on,sys\_updated\_on\)

The formula uses the technical names of the Created and Updated fields.

\[Omitted image "calculated-field-form.png"\] Alt text: Completed form for incident age calculated field.

Because the Created and Updated fields are both dimensions on the incident\_dataset data source, Age is listed there as an eligible calculated field.

\[Omitted image "eligible-calculated-field.png"\] Alt text: The Age calculated field shown in the Eligible Calculated fields related list of the incident\_dataset data snapshots source record.

## What to do next

To use the calculated field as a filter on KPI Details, map it to a bucket group.

You cannot delete a calculated field from the Calculated Fields list.

**Parent Topic:**[Bucket groups and calculated fields in Data Snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/ds-bucket-groups-calculated-fields.md)

**Related topics**  


[Data snapshots sources and collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/tables-unlimited-breakdowns.md)

