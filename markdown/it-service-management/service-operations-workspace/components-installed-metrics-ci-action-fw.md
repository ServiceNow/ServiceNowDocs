---
title: Components installed with Metrics and CI Actions Framework
description: Several types of components are installed with activation of the Metrics and CI Actions Framework \(sn\_cimaf\) application, including user roles and ServiceNow Store applications.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Incident Management in Service Operations Workspace reference, Incident Management in Service Operations Workspace, Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# Components installed with Metrics and CI Actions Framework

Several types of components are installed with activation of the Metrics and CI Actions Framework \(sn\_cimaf\) application, including user roles and ServiceNow Store applications.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Metrics and CI Actions user\[sn\_cimaf.sn\_cimaf\_read\]

</td><td>

Enables users to access and read Metric, Action Request and Action Output tables.**Note:** itil role contains this role.

</td><td>

cmdb\_read

</td></tr><tr><td>

Metrics and CI Actions admin\[sn\_cimaf.sn\_cimaf\_admin\]

</td><td>

Enables users with read and write access to all Metrics and CI Actions configuration tables.

</td><td>

-   sn\_cimaf.sn\_cimaf\_read
-   flow\_operator

</td></tr></tbody>
</table>## Tables installed

<table id="table_n3m_3yq_gxb"><thead><tr><th>

Tables

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider\[sn\_cimaf\_provider\]

</td><td>

List of providers such as Agent Client Collector \(ACC\) or Microsoft Endpoint Configuration Manager \(MECM\).

</td></tr><tr><td>

Metric Definition \[sn\_cimaf\_metric\_definition\]

</td><td>

List of metric definitions such as Asset usage, Running processes and so on.

</td></tr><tr><td>

Adapter Configuration \[sn\_cimaf\_adapter\_config\]

</td><td>

List of configurations for the adapter. You can define the provider such as Agent Client Collector \(ACC\) or Microsoft Endpoint Configuration Manager \(MECM\), query and transform flows or scripts.

</td></tr><tr><td>

Adapter Applicability Rule\[sn\_cimaf\_adapter\_applicability\_rule\]

</td><td>

List of adapter applicability rules that enables you to configure on which CIs, the selected adapter configuration is applicable.

</td></tr><tr><td>

Provider Specific Adapter Configuration\[sn\_cimaf\_provider\_specific\_adapter\_config\]

</td><td>

List of adapter configuration for a specific provider such as Agent Client Collector \(ACC\) or Microsoft Endpoint Configuration Manager \(MECM\).

</td></tr><tr><td>

Collection Rule\[sn\_cimaf\_collection\_rule\]

</td><td>

List of collection rules that enables you to configure when the metrics should be auto-collected.

</td></tr><tr><td>

Collection Rule Metric Association \[sn\_cimaf\_collection\_rule\_metric\_asscn\]

</td><td>

List of records that are created for the association of the collection rules with metric definitions.

</td></tr><tr><td>

Metric\[n\_cimaf\_metric\]

</td><td>

List of metrics fetched. The metric record contains the information such as metric definition, CI, timestamp and the actual metric payload.

**Note:** This table is read only.

</td></tr><tr><td>

Action\[sn\_cimaf\_action\]

</td><td>

List of CI actions such as End Process or Restart service and so on.

</td></tr><tr><td>

Action Role\[sn\_cimaf\_action\_role\]

</td><td>

List of roles required to access and execute the CI actions.**Note:** One CI action can be mapped to multiple roles.

</td></tr><tr><td>

User Criteria Action Inclusion\[sn\_cimaf\_action\_user\_criteria\_mtom\]

</td><td>

List of user criteria which are allowed to execute the CI Action.

</td></tr><tr><td>

User Criteria Action Exclusion\[sn\_cimaf\_action\_user\_criteria\_no\_mtom\]

</td><td>

List of user criteria which aren’t allowed to execute the action.**Note:** This table is prioritized over the Action Role and User Criteria Action Inclusion configuration tables.

</td></tr><tr><td>

Action Configuration\[sn\_cimaf\_action\_config\]

</td><td>

List of action configurations applicable to CI. You can create multiple configurations for a CI action based on different providers or CI class.

</td></tr><tr><td>

Action Parameter\[sn\_cimaf\_action\_parameter\]

</td><td>

List of parameters required to execute the CI action.

</td></tr><tr><td>

Action Configuration Step\[sn\_cimaf\_provider\_specific\_action\_config\]

</td><td>

List of sequential steps to be executed for any Action Configuration.

</td></tr><tr><td>

Action Request\[sn\_cimaf\_action\_request\]

</td><td>

List of the CI action execution records. The record includes information such as parameters, CI details, and CI action and current status.**Note:** This table is read only.

</td></tr><tr><td>

Action Output\[sn\_cimaf\_action\_output\]

</td><td>

List of the CI action output records. Each record is linked to the record in action request table. The record includes information such as action request record, action configuration step, payload, state, and request ID.**Note:** This table is read only.

</td></tr></tbody>
</table>**Note:** Deny unless ACLs are added to all the tables. The Deny unless ACLs restrict access for a non-authenticated user, such as a public role user. Without access, the user can't perform any actions on the tables related to the mentioned applications, such as reading, writing, deleting, creating, or accessing the report view. For more information on Deny-Unless ACLs and enhanced security model adoption features, see [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) and [Features of enhanced security model adoption for incident tables](../../incident-management/reference/comp-instal-itsm-enhanced-sec-features.md).

**Parent Topic:**[Incident Management in Service Operations Workspace reference](../concept/sow-im-reference.md)

