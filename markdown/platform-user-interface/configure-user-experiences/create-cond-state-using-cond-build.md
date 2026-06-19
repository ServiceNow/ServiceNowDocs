---
title: Create a condition statement using the condition builder
description: A condition builder constructs a condition statement with a series of contextually generated fields. Condition builders are used in many operations, such as creating filters, administering surveys, and administering access control.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/create-cond-state-using-cond-build.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a condition statement using the condition builder

A condition builder constructs a condition statement with a series of contextually generated fields. Condition builders are used in many operations, such as creating filters, administering surveys, and administering access control.

## Before you begin

Role required: admin

## About this task

A condition consists of three parts: field, operator, and value.

\[Omitted image "condition-builder.png"\] Alt text: Condition builder with the Active field, the is operator, and the true value highlighted.

|Part|Description|
|----|-----------|
|Field|A choice list based on the table and user access rights. The choice list can include fields on related tables by dot-walking.|
|Operator|A choice list based on the field type. For example, in the Incident \[incident\] table, the greater than operator does not apply to the **Active** field but it does apply to the **Priority** field.|
|Value|A text entry field or a choice list, depending on field type. For example, in the Incident \[incident\] table, the **Active** field offers a choice list with the values **true**, **false**, and **empty**, while the **Short Description** field offers a text entry field.|

## Procedure

1.  To add a dependent condition, select **AND** or **OR** next to the condition.

2.  To add a top-level condition, select **AND** or **OR** on the condition builder toolbar above the conditions.

3.  To remove a condition, select the delete icon \(X\) next to the condition.

    \[Omitted image "ExampleConditionActiveIsTrueAndCallerIsNotEmpty.png"\] Alt text: Example AND condition


-   **[Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/c_ConditionBuilder.md)**  
A condition builder constructs a condition statement with a series of contextually generated fields. Condition builders are used in many operations, such as creating filters, administering surveys, and administering access control.
-   **[Operators available for filters and queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/r_OpAvailableFiltersQueries.md)**  
The system provides a set of operators for use with filters, condition builders, and encoded queries. The data type of a field determines what operators are available for it.

**Parent Topic:**[Common UI elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/p_CommonUIElements.md)

