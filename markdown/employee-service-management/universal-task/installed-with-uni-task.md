---
title: Components installed with Universal Task
description: Several types of components are installed with activation of the Universal Task application, including tables, user roles, and scheduled jobs.
locale: en-US
release: xanadu
product: Universal Task
classification: universal-task
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install Universal Task, Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Components installed with Universal Task

Several types of components are installed with activation of the Universal Task application, including tables, user roles, and scheduled jobs.

Demo data is available for this feature.

## Roles installed

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|Admin \[sn\_uni\_task.admin\]|View and configure the Universal Task application|None|
|Report view \[sn\_uni\_task.report\_view\]|Access and view Universal Task reports|None|
|Employee form admin \[sn\_uni\_task.emp\_form\_admin\]|Create and manage Employee forms|survey\_admin|
|Employee form creator \[sn\_uni\_task.emp\_form\_creator\]|Create and modify employee forms|survey\_creator|
|sn\_uni\_task.template\_admin|Create and manage Universal Task templates|None|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Universal Task \[sn\_uni\_task\_universal\_task\]

</td><td>

Store the Universal Task record details for a department-specific table.

</td></tr><tr><td>

Universal Task Configuration \[sn\_uni\_task\_config\]

</td><td>

Store the list of task types for each department-specific table.

</td></tr><tr><td>

Catalog Task Configuration \[sn\_uni\_task\_catalog\_task\_config\]

</td><td>

Stores the catalog items details of the department-specific table.

</td></tr><tr><td>

Base Task Configuration \[sn\_uni\_task\_base\_task\_config\]

</td><td>

Serves as the base table for the configuration tables for all task types.

</td></tr><tr><td>

Employee Form \[sn\_uni\_task\_employee\_form\]

</td><td>

Stores the employee form records that were created for the Collect employee input task type.

</td></tr><tr><td>

Employee Input Task Configuration \[sn\_uni\_task\_emp\_input\_task\_config\]

</td><td>

Stores the roles that can view the responses of completed employee forms for each department-specific table.

</td></tr><tr><td>

Universal Task Template \[sn\_uni\_task\_template\]

</td><td>

Stores the universal task templates with predefined field values that can be applied on Universal Task forms.

</td></tr><tr><td>

Universal Task Dynamic Template Mapping \[sn\_uni\_task\_dynamic\_template\_mapping\]

</td><td>

Stores the dynamic template mappings between Universal Task fields and parent table fields.

</td></tr></tbody>
</table>**Parent Topic:**[Install Universal Task](../task/install-universal-task.md)

