---
title: Condition field types
description: A condition field specifies when to run business logic such as a business rule or workflow.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Condition field types

A condition field specifies when to run business logic such as a business rule or workflow.

There are two types of condition field.

|Condition field type|Description|
|--------------------|-----------|
|Condition string|A text field that accepts a plain JavaScript condition statement. The system validates the condition syntax for correctness before an update.|
|Conditions|A field that adds a [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) to a form. Condition builders require specifying a dependent field whose values the system uses to display choice list options. Typically, the dependent field is the **Table** field.|

The system evaluates both types of condition field to determine if the conditions are true or false. When true, the system runs the business logic. When false, the system ignores the business logic.

To find dictionary attributes that affect condition fields, see [Altering tables and fields using dictionary attributes](../../reference-pages/concept/c_DictionaryAttributes.md).

