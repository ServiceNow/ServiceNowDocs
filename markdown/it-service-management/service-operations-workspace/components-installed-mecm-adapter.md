---
title: Components installed with Microsoft Endpoint Configuration Manager for Investigation
description: Several types of components are installed with activation of the Microsoft Endpoint Configuration Manager for Investigation \(sn\_mecm\_adapter\) application, including user roles and ServiceNow Store applications.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Incident Management in Service Operations Workspace reference, Incident Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Components installed with Microsoft Endpoint Configuration Manager for Investigation

Several types of components are installed with activation of the Microsoft Endpoint Configuration Manager for Investigation \(sn\_mecm\_adapter\) application, including user roles and ServiceNow Store applications.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

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
</table>## Tables installed

<table id="table_jcb_wxf_bfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Adapter Configuration\[sn\_mecm\_adapter\_config\]

</td><td>

List of configurations for the MECM adapter.

</td></tr><tr><td>

Action Configuration\[sn\_mecm\_action\_config\]

</td><td>

List of action configurations applicable to CI.

</td></tr></tbody>
</table>**Note:** Deny unless ACLs are added to all the tables. The Deny unless ACLs restrict access for a non-authenticated user, such as a public role user. Without access, the user can't perform any actions on the tables related to the mentioned applications, such as reading, writing, deleting, creating, or accessing the report view. For more information on Deny-Unless ACLs and enhanced security model adoption features, see Deny-Unless ACL and [Features of enhanced security model adoption for incident tables](../../incident-management/reference/comp-instal-itsm-enhanced-sec-features.md).

## Store applications installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metrics and CI Actions Framework \[sn\_cimaf\]

</td><td>

Core framework capabilities and configurations for Microsoft Endpoint Configuration Manager for Investigation application, including API data and CI actions framework. For more information on the roles and tables installed, see [Components installed with Metrics and CI Actions Framework](components-installed-metrics-ci-action-fw.md).

</td></tr><tr><td>

Investigation Framework \[sn\_invest\_fwk\]

</td><td>

Framework to analyze the affected CIs using the metrics information.

</td></tr><tr><td>

Remedial Actions Framework\[com.snc.sn\_reacf\]

</td><td>

Framework to remediate or resolve the CI related issues. For more information on the roles and tables installed, see [Components installed with Remedial Actions Framework](components-installed-with-remediation-fw.md).

</td></tr></tbody>
</table>**Parent Topic:**[Incident Management in Service Operations Workspace reference](../concept/sow-im-reference.md)

