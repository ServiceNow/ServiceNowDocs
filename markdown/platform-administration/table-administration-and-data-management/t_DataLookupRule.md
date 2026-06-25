---
title: Create an assignment data lookup rule
description: Automatically assign a record using Data Lookup and Record Matching.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/table-administration-and-data-management/t\_DataLookupRule.html
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Assignment rules, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an assignment data lookup rule

Automatically assign a record using Data Lookup and Record Matching.

## Before you begin

Role required: assignment\_rule\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Assignment Lookup Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Category|The category the data lookup matches against.|
    |Subcategory|The subcategory the data lookup matches against.|
    |Configuration item|The configuration item the data lookup matches against.|
    |Location|The location the data lookup matches against.|
    |Assignment group|The assignment group to assign the incident to.|
    |Assigned to|The user to assign the incident to.|
    |Active|Option to run the rule or deactivate the rule.|
    |Order|Order in which the rule runs compared to other rules on the same table. The Data Lookup Plugin runs the rule with the lowest order and matching values.|

4.  Select **Submit**.


## Result

The rule assigns incidents to the values in the Assignment Group and Assigned To fields based on the values selected in the **Category**, **Subcategory**, **Configuration Item**, or **Location** fields. A valid assignment lookup rule requires at least one matcher field and one setter field.

## Assignment Data Lookup

In this example, the Assignment Data Lookup rule automatically assigns any incident with the Category of Inquiry/Help and Subcategory of Email to Fred Luddy.

\[Omitted image "Assignment\_Data\_Lookup.png"\] Alt text: Assignment data lookup

**Parent Topic:**[Defining assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DefineAssignmentRules.md)

**Related topics**  


[Assignment rules module]()

[Data lookup rules]()

[Precedence between data lookup, assignment, and business rules]()

[Workflow assignments]()

[Baseline assignment rules example]()

[Create an assignment rule]()

