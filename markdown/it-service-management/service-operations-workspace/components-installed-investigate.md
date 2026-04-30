---
title: Components installed with Agent Client Collector for Investigation
description: Several types of components are installed with activation of the Agent Client Collector for Investigation \(sn\_acc\_adapter\) application, including user roles and ServiceNow Store applications.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference, Service Operations Workspace for ITSM, IT Service Management]
---

# Components installed with Agent Client Collector for Investigation

Several types of components are installed with activation of the Agent Client Collector for Investigation \(sn\_acc\_adapter\) application, including user roles and ServiceNow Store applications.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Metrics user\[sn\_cimaf.sn\_cimaf\_read\]

</td><td>

Enables users to access and perform basic operations in the Metrics Collector Framework such as view metric definition.

</td><td>

None

</td></tr><tr><td>

Metrics admin\[sn\_cimaf.sn\_cimaf\_admin\]

</td><td>

Enables users to install the application, add, configure the tables, and also view the metric definition.

</td><td>

\[sn\_cimaf.sn\_cimaf\_read\]

</td></tr><tr><td>

Investigate Framework Admin\[sn\_invest\_fwk.sn\_investigate\_admin\]

</td><td>

Enables users to install the Investigation Framework application and manage the Investigate Framework modules.

</td><td>

\[sn\_cimaf.sn\_cimaf\_admin\]

</td></tr></tbody>
</table>## Store applications installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metrics and CI Actions Framework \[sn\_cimaf\]

</td><td>

Core framework capabilities and configurations for Agent Client Collector for Investigation application, including API data and CI actions framework. For more information on the roles and tables installed, see [Components installed with Metrics and CI Actions Framework](components-installed-metrics-ci-action-fw.md)

</td></tr><tr><td>

Investigation Framework \[sn\_invest\_fwk\]

</td><td>

Framework to analyze the affected CIs using the metrics information.

</td></tr><tr><td>

Remedial Actions Framework\[com.snc.sn\_reacf\]

</td><td>

Framework to remediate or resolve the CI related issues. For more information on the roles and tables installed, see [Components installed with Remedial Actions Framework](components-installed-with-remediation-fw.md).

</td></tr></tbody>
</table>**Parent Topic:**[Service Operations Workspace for ITSM reference](../concept/sow-reference.md)

**Related topics**  


[Service Operations Workspace for ITSM data model](sow-itsm-data-model.md)

[Components installed with Service Operations Workspace ITSM Applications](components-installed-with-sow.md)

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

[Components installed with Universal Task for Service Operations Workspace](components-installed-ut-sow.md)

[Password Reset Reference](pr-sow-reference.md)

