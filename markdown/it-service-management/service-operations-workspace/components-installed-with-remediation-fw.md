---
title: Components installed with Remedial Actions Framework
description: Several types of components are installed with activation of the Remedial Actions Framework \(com.snc.sn\_reacf\) application, including user roles and tables.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference, Service Operations Workspace for ITSM, IT Service Management]
---

# Components installed with Remedial Actions Framework

Several types of components are installed with activation of the Remedial Actions Framework \(com.snc.sn\_reacf\) application, including user roles and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Remedial action user\[sn\_reacf.sn\_remedial\_action\_read\]

</td><td>

Enables users to access and read the Remedial Action Execution table and remediate CI related issues using remedial actions.**Note:** itil role contains this role.

</td><td>

cmdb\_read

</td></tr><tr><td>

Remedial action admin\[sn\_reacf.sn\_remedial\_action\_admin\]

</td><td>

Enables users with read and write access to all Remedial Action configuration tables.

</td><td>

-   sn\_reacf.sn\_remedial\_action\_read
-   flow\_operator

</td></tr></tbody>
</table>## Tables installed

<table id="table_ics_vsk_xsb"><thead><tr><th>

Tables

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remedial action\[sn\_reacf\_remedial\_action\]

</td><td>

List of remedial actions \(definitions\) such as End Process - Device, Restart Service - Server and so on.

</td></tr><tr><td>

Remedial action parameter\[sn\_reacf\_remedial\_action\_parameter\]

</td><td>

List of parameters required to execute the remedial actions such as process ID, assigned to and so on.

</td></tr><tr><td>

Remedial action role\[sn\_reacf\_remedial\_role\]

</td><td>

List of roles required to access and execute the remedial actions.

</td></tr><tr><td>

User criteria action inclusion\[sn\_reacf\_remedial\_user\_criteria\_mtom\]

</td><td>

List of user criteria which are allowed to execute the Remedial Action.

</td></tr><tr><td>

User criteria action exclusion\[sn\_reacf\_remedial\_user\_criteria\_no\_mtom\]

</td><td>

List of user criteria which aren't allowed to execute the Remedial Action.

</td></tr><tr><td>

Remedial action type\[sn\_reacf\_remedial\_action\_type\]

</td><td>

List of remedial action types such as CI action and standard change.

</td></tr><tr><td>

Remedial action origin\[sn\_reacf\_remedial\_action\_origin\]

</td><td>

List of applications where the Remedial Action Framework is used.

</td></tr><tr><td>

Remedial action execution\[sn\_reacf\_remedial\_action\_execution\]

</td><td>

List of execution records that are created for each remedial action when executed. The record is used to track the progress and maintain the information. The record includes information such as executed remedial action, parameter values, action execution record, parent record, target record, current state, user who executed the remedial action and origin.**Note:** This table is read only.

</td></tr></tbody>
</table>**Parent Topic:**[Service Operations Workspace for ITSM reference](../concept/sow-reference.md)

**Related topics**  


[Service Operations Workspace for ITSM data model](sow-itsm-data-model.md)

[Components installed with Service Operations Workspace ITSM Applications](components-installed-with-sow.md)

[Components installed with Agent Client Collector for Investigation](components-installed-investigate.md)

[Components installed with Microsoft Endpoint Configuration Manager for Investigation](components-installed-mecm-adapter.md)

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

