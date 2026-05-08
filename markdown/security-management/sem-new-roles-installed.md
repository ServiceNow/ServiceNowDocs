---
title: Security Exposure Management Workspace Roles
description: List of roles installed with Security Exposure Management, defining user permissions and access for Security Exposure Management-related tasks.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Security Exposure Management Workspace Roles

List of roles installed with Security Exposure Management, defining user permissions and access for Security Exposure Management-related tasks.

<table id="table_tvj_fyc_hgc"><thead><tr><th>

Application

</th><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Vulnerability Response Common

</td><td>

sn\_vul\_cmn.usem\_admin

</td><td>

Configures rules, integrations, and related settings for Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance.

</td><td>

-   sn\_vul.vulnerability\_admin
-   sn\_vul.app\_sec\_manager
-   sn\_vul\_container.vulnerability\_admin
-   sn\_vulc.admin

</td></tr><tr><td>

Administration for Security Exposure Management

</td><td>

sn\_sec\_wf.read\_admin\_rules

</td><td>

Read access to administration rules.

</td><td>

-   sn\_sec\_calculator.read
-   sn\_vul\_cmn\_ws.read\_admin\_rules
-   sn\_vul\_cmn.read\_auto\_close\_rules

</td></tr><tr><td>

Administration for Security Exposure Management

</td><td>

sn\_sec\_wf.manage\_admin\_rules

</td><td>

Create, read, update, and delete administration rules.

</td><td>

-   sn\_vul\_cmn.manage\_auto\_close\_rules
-   sn\_sec\_wf.read\_admin\_rules
-   sn\_vul\_cmn\_ws.write\_admin\_rules
-   sn\_sec\_calculator.admin

</td></tr><tr><td>

Exception Management for Unified Security Exposure Management

</td><td>

sn\_sec\_exception.approver

</td><td>

Approve or reject exception requests, false positive requests, and exception rules.

</td><td>

sn\_sec\_exception.read

</td></tr><tr><td>

Exception Management for Unified Security Exposure Management

</td><td>

sn\_sec\_exception.read

</td><td>

Read access to exception management configuration and exception rules.

</td><td>

None.

</td></tr><tr><td>

Exception Management for Unified Security Exposure Management

</td><td>

sn\_sec\_exception.admin

</td><td>

Create, read, update, and delete exception management configuration and exception rules.

</td><td>

sn\_sec\_exception.read

</td></tr><tr><td>

Risk Scoring for Security Exposure Management

</td><td>

sn\_sec\_calculator.read

</td><td>

Read access to records in the `sn_sec_calculator` scope.

</td><td>

None.

</td></tr><tr><td>

Risk Scoring for Security Exposure Management

</td><td>

sn\_sec\_calculator.admin

</td><td>

Create, read, update, and delete records in the `sn_sec_calculator` scope.

</td><td>

sn\_sec\_calculator.read

</td></tr></tbody>
</table>**Parent Topic:**[Security Exposure Management Workspace Components](../concept/sem-components-installed.md)

**Parent Topic:**[Unified Security Exposure Management reference](../concept/unified-security-exposure-management-reference.md)

