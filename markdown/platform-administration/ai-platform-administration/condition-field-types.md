---
title: Condition field types
description: A condition field specifies when to run business logic such as a business rule or workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/condition-field-types.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Condition field types

A condition field specifies when to run business logic such as a business rule or workflow.

There are two types of condition field.

|Condition field type|Description|
|--------------------|-----------|
|Condition string|A text field that accepts a plain JavaScript condition statement. The system validates the condition syntax for correctness before an update.|
|Conditions|A field that adds a [condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/c_ConditionBuilder.md) to a form. Condition builders require specifying a dependent field whose values the system uses to display choice list options. Typically, the dependent field is the **Table** field.|

The system evaluates both types of condition field to determine if the conditions are true or false. When true, the system runs the business logic. When false, the system ignores the business logic.

To find dictionary attributes that affect condition fields, see [Altering tables and fields using dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md).

