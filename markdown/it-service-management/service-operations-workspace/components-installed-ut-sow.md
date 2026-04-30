---
title: Components installed with Universal Task for Service Operations Workspace
description: Several types of components are installed with activation of the Universal Task application, including tables, and user roles.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference, Service Operations Workspace for ITSM, IT Service Management]
---

# Components installed with Universal Task for Service Operations Workspace

Several types of components are installed with activation of the Universal Task application, including tables, and user roles.

## Roles installed

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|Admin \[sn\_uni\_task.admin\]|View and configure the Universal Task application|None|
|Report view \[sn\_uni\_task.report\_view\]|Access and view Universal Task reports|None|
|Employee form admin \[sn\_uni\_task.emp\_form\_admin\]|Create and manage Employee forms|survey\_admin|
|Employee form creator \[sn\_uni\_task.emp\_form\_creator\]|Create and modify employee forms|survey\_creator|
|sn\_uni\_task.template\_admin|Create and manage Universal Task templates|None|

## Tables installed

<table id="table_fbz_123"><thead><tr><th>

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
</table>**Parent Topic:**[Service Operations Workspace for ITSM reference](../concept/sow-reference.md)

**Related topics**  


[Service Operations Workspace for ITSM data model](sow-itsm-data-model.md)

[Components installed with Service Operations Workspace ITSM Applications](components-installed-with-sow.md)

[Components installed with Agent Client Collector for Investigation](components-installed-investigate.md)

[Components installed with Microsoft Endpoint Configuration Manager for Investigation](components-installed-mecm-adapter.md)

[Components installed with Remedial Actions Framework](components-installed-with-remediation-fw.md)

[Components installed with Metrics and CI Actions Framework](components-installed-metrics-ci-action-fw.md)

[Recommendation rules for an incident in Service Operations Workspace](recommendation-rules.md)

[Recommended Actions for ITSM reference](../concept/recommended-actions-for-itsm-reference.md)

[Reference section for Problem Management in Service Operations Workspace](../concept/reference-problem-management-sow.md)

[Features of the Investigation tab](features-of-investigation-tab.md)

[Extension points for batch processing in Service Operations Workspace](mra-extension-points-batch-processing-sow.md)

[Quick start tests for Incident Management in Service Operations Workspace](../../../administer/atf-quick-start-tests/reference/quick-start-tests-im-sow.md)

[Components installed with Universal Request for Service Operations Workspace](components-installed-ur-sow.md)

[Password Reset Reference](pr-sow-reference.md)

