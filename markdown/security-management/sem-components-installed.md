---
title: Security Exposure Management Workspace Components
description: When you activate the Unified Security Exposure Management \(USEM\) and Security Exposure Management Workspace applications, the system installs specific key components including tables, user roles, and scheduled jobs to support the operations required for assessing and managing security exposures.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-07-28"
reading_time_minutes: 3
breadcrumb: [Reference, Unified Security Exposure Management, Security Operations]
---

# Security Exposure Management Workspace Components

When you activate the Unified Security Exposure Management \(USEM\) and Security Exposure Management Workspace applications, the system installs specific key components including tables, user roles, and scheduled jobs to support the operations required for assessing and managing security exposures.

The following applications install Security Exposure Management-specific components:

-   Unified Security Exposure Management
-   Security Exposure Management Workspace
-   Administration for Security Exposure Management
-   Risk Scoring for Security Exposure Management
-   Remediation for Attack Surface Management
-   Exception Management for Unified Security Exposure Management

USEM also depends on components provided by some existing security operations applications. For details of those existing components, see:

-   [Components installed with Vulnerability Response](../../vulnerability-response/reference/installed-with-vr.md)
-   [Components installed with Application Vulnerability Response](../../vulnerability-app-vuln-mgmt/reference/installed-with-avm.md)
-   [Components installed with Container Vulnerability Response](../../container-vulnerability-response/reference/installed-with-cvr-data.md#)
-   [Components installed with Configuration Compliance](../../vulnerability-config-compliance/reference/installed-with-config-compliance.md)

To view the full list of installed components, use the Application Files table. For instructions, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Deprecated Components

Some tables and scheduled jobs from the existing security operations applications are not included in USEM, as they have been deprecated.

The following tables from the existing applications have been deprecated and have corresponding replacements or references in USEM.

|Deprecated Tables|Mapped Table in Security Exposure Management|
|-----------------|--------------------------------------------|
|Security Calculator Group \[sn\_sec\_cmn\_calculator\_group\]|Risk Calculator \[sn\_sec\_calculator\_group\]|
|Vulnerability Calculator \[sn\_vul\_calculator\_group\]|
|Risk Calculators \[sn\_vulc\_calculator\_group\]|
|Security Calculator \[sn\_sec\_cmn\_calculator\]|Risk Calculator Rule \[sn\_sec\_calculator\_rule\]|
|Vulnerability Risk Rule \[sn\_vul\_calc\_risk\]|
|Calculator \[sn\_vulc\_calculator\_risk\_score\]|
|Configuration Compliance Risk Rule \[sn\_vulc\_risk\_rule\]|
|Security Classification Group \[sn\_sec\_cmn\_classification\_group\]|Classification Group \[sn\_sec\_wf\_classification\_group\]|
|Classification Group \[sn\_vul\_classification\_group\]|
|Security Classification Rule \[sn\_sec\_cmn\_classification\_rule\]|Classification Rule \[sn\_sec\_wf\_classification\_rule\]|
|Classification Rule \[sn\_vul\_classification\_rule\]|
|Exception Management Configuration \[sn\_sec\_cmn\_exception\_config\]|Exception Management Configuration \[sn\_sec\_exception\_config\]|
|Exception Management Configuration \[sn\_vul\_exception\_config\]|
|Questionnaire Configuration \[sn\_sec\_cmn\_questionnaire\_config\]|Questionnaire Configuration \[sn\_sec\_exception\_questionnaire\_config\]|
|Policy Exception Reason Mapping \[sn\_sec\_cmn\_policy\_reason\_mapping\]|Policy Exception Reason Mapping \[sn\_sec\_exception\_policy\_reason\_mapping\]|
|Policy Exception Reason Mapping \[sn\_vul\_policy\_reason\_mapping\]|
|Vulnerability Assignment Rule \[sn\_vul\_assignment\_rule\]|Assignment Rule \[sn\_sec\_wf\_assign\_rule\]|
|Assignment Rule \[sn\_vulc\_assignment\_rule\]|
|Vulnerability Calculator Rule \[sn\_vul\_calculator\]|Remediation Target Rules \[sn\_sec\_wf\_ttr\_rule\]|
|Remediation Target Rule \[sn\_vul\_ttr\_rule\]|
|Remediation Target Rule \[sn\_vulc\_ttr\_rule\]|
|Risk rule field \[sn\_vul\_risk\_field\]|Risk rule field \[sn\_sec\_calculator\_risk\_field\]|
|Risk rule field \[sn\_vulc\_risk\_rule\_field\]|
|Vulnerability Remediation Status \[sn\_vul\_m2m\_ttr\_status\]|Remediation Status \[sn\_sec\_wf\_m2m\_ttr\_status\]|
|Test Result Remediation Status \[sn\_vulc\_m2m\_ttr\_status\]|
|Vulnerability Rollup Calculator \[sn\_vul\_rollup\]|Rollup Config \[sn\_sec\_wf\_rollup\_config\]|
|Risk Score Rollup Calculator \[sn\_vulc\_risk\_score\_rollup\]|
|Exception Rule \[sn\_vul\_auto\_exception\_rule\]|Exception Rule \[sn\_sec\_exception\_rule\]|
|Auto Exception Rules \[sn\_vulc\_auto\_exception\_rule\]|
|Vulnerability State Change Approval \[sn\_vul\_change\_approval\]|Change Approval \[sn\_sec\_exception\_change\_approval\]|
|State Change Approval \[sn\_vulc\_state\_change\_approval\]|
|Vulnerability Compensating Control relationship \[sn\_vul\_m2m\_entry\_compensating\_control\]|Vulnerability Compensating Control relationship \[sn\_vul\_cmn\_m2m\_entry\_compensating\_control\]|
|Auto-Close stale Test Results \[sn\_vulc\_auto\_close\_stale\_config\]|Auto-close Rule \[sn\_vul\_cmn\_auto\_close\_rule\]|

|Deprecated Scheduled Jobs|
|-------------------------|
|Populate risk fields for risk rules|
|Rerun calculators|
|Reapply all vulnerability assignment rules|
|Send unassignment notification|
|Run severity calculator after vulnerability entry promotion|
|Evaluate remediation targets|
|Reassignment count for assignment rules|
|Remove Duplicate VI Remediation Status|
|Copy customized request exception questionnaire to compensating control|
|Rolldown until date from vulnerability group to vulnerable item|
|Check Vulnerable Item and Groups Deferment Expiration|
|Check Risk Mitigation Expiration|
|Associate existing AVIs with Auto Exception Rule|
|Associate existing VIs with Auto Exception Rule|
|Migrate the background jobs|
|Update Risk Rating for Test Results|
|Evaluate and notify remediation targets|
|Associate existing TRs with Auto Exception Rule|
|Check Remediation Tasks and Test Result Deferment Expiration|
|Associate existing Container VIs with Auto Exception Rule|
|Check Container Vulnerable Item Deferment Expiration|

-   **[Security Exposure Management Workspace Roles](../reference/sem-new-roles-installed.md)**  
List of roles installed with Security Exposure Management, defining user permissions and access for Security Exposure Management-related tasks.
-   **[Security Exposure Management Workspace Tables](../reference/sem-new-tables-installed.md)**  
The following are the tables installed with Security Exposure Management. These tables store Security Exposure Management-related configuration, rules, findings, and other data required for exposure assessment, remediation, scoring, and exception management.
-   **[Security Exposure Management Workspace Scheduled Jobs](../reference/sem-new-scheduledjobs-installed.md)**  
The following are the scheduled jobs installed with Security Exposure Management. These jobs automate Security Exposure Management operations to ensure that exposure data is kept current and accurate.

**Parent Topic:**[Unified Security Exposure Management reference](unified-security-exposure-management-reference.md)

