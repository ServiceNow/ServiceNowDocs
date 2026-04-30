---
title: Universal Task templates
description: Task templates help agents to create Universal Task records by auto-populating fields in a template.
locale: en-US
release: xanadu
product: Universal Task
classification: universal-task
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Universal Task, Universal Task, Employee Service Management]
---

# Universal Task templates

Task templates help agents to create Universal Task records by auto-populating fields in a template.

The task template \[sn\_uni\_task\_template\] table follows data separation. For more information, see [Domain separation and Universal Task](domain-sep-universal-task.md).

Using task templates, you can create templates for common use-cases. You can also set a schedule to periodically create records based on a template.

A task template can have static and dynamic mappings. In static mappings, the values of fields are individually specified and fixed. In dynamic mappings, the field values are updated and mapped from another table. You can create dynamic template mappings between the fields of the Universal Task table and any other parent table that uses Universal Task. Using the dynamic template mappings, you can do the following:

-   Map Universal Task fields to parent table fields.
-   Create text templates for fields in the parent table.
-   Offset date fields by specific durations.

-   **[Create a template using the Universal Task template form](../task/ut-create-task-template.md)**  
Create a template for any service table to automatically populate fields on a form. Creating templates for common use cases enables agents to create universal tasks faster and ensures uniformity of field values.
-   **[Create a task template by saving a form](../task/ut-tasktemplate-saveform.md)**  
Save a populated Universal Task form as a template. This is an alternative method for creating a task template.
-   **[Create dynamic template mapping](../task/ut-create-dynamic-tmplt-map.md)**  
Create dynamic templates to map fields on a Universal task form to corresponding fields on the parent table form. Dynamic templates help agents to map parent table fields to Universal task fields.
-   **[Use Task templates](../task/ut-use-task-template.md)**  
Use a task template to auto-populate a Universal Task form. Using a task template enables agents to create tasks faster.

**Parent Topic:**[Using Universal Task](use-universal-task.md)

