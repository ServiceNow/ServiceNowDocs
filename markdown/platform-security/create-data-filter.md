---
title: Add a data filter for your data filtration rule
description: You can optionally use a data filter to narrow the scope of your data filtration rule to apply only to specific records on a table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/create-data-filter.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create data filtration rules, Data filtration, Access Management]
---

# Add a data filter for your data filtration rule

You can optionally use a data filter to narrow the scope of your data filtration rule to apply only to specific records on a table.

## Before you begin

Role required: admin

## Procedure

1.  On your data filtration record, open the **Data Filter** tab.

2.  Use the condition builder to filter the table records their field values.

    The data filter uses the same condition builder used in other parts of the platform. For details on using this interface, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/c_ConditionBuilder.md).

    **Important:** The **Data Filter** tab appears empty until you select a table in the **Table** field.

3.  Use the **Preview** button to see a count of how many records match your data filter.

4.  Select the number of records to open a list of the matching records.

    \[Omitted image "df-conditions-1-2.png"\] Alt text: Data filter showing matching records

5.  Select **Save**.


## Example

This example shows a data filtration rule for the Incident\[incident\] table. The data filter is set to select all active records that are not in the **Security** category. With this rule active, users can see these records. See the section below to further using criteria outside the contents of the record.

\[Omitted image "df-example-1-2.png"\] Alt text: Data filtration rule for security incidents

**Important:**

The **not** operation in your conditions may return unexpected results, depending on the type of database your instance uses. For example, take the following condition:

For this condition, the expected result would be that the result set would be all records where the company is not `ServiceNow` and all records that do not have a value in the **company** field. Instances using databases other than MySQL and Maria do not return values records with an empty **company** field. When using **not** queries for these instances, include conditions to ensure empty values are returned.

