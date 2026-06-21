---
title: Condition field types
description: A condition field specifies when to run business logic such as a business rule or workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/condition-field-types.html
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Condition field types

A condition field specifies when to run business logic such as a business rule or workflow.

There are two types of condition field.

|Condition field type|Description|
|--------------------|-----------|
|Condition string|A text field that accepts a plain JavaScript condition statement. The system validates the condition syntax for correctness before an update.|
|Conditions|A field that adds a condition builder to a form. Condition builders require specifying a dependent field whose values the system uses to display choice list options. Typically, the dependent field is the **Table** field.|

The system evaluates both types of condition field to determine if the conditions are true or false. When true, the system runs the business logic. When false, the system ignores the business logic.

To find dictionary attributes that affect condition fields, see [Altering tables and fields using dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md).

-   **[Add the condition count to a condition field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/t_AddingTheConditionCountWidget.md)**  
The condition count widget can be activated on condition fields to display a preview of the records that would meet the current set of conditions. For fields where the condition count is activated, the number of records that match the conditions will automatically display. The count refreshes if the field the condition field depends on, such as Table, is changed. If the Table field is left empty, the widget is hidden.
-   **[Update a conditions field to use condition builder v2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/configure-condition-builder.md)**  
In Core UI, you can update a conditions field to display the version 2 condition builder.

**Parent Topic:**[Field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/r_FieldTypes.md)

