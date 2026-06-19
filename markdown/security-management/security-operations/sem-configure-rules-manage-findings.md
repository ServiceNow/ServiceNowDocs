---
title: Configure rules to manage findings
description: By configuring rules, you can automate, organize, and manage the lifecycle of findings. The rules help ensure scalability, data consistency, and faster response times by reducing manual intervention across large volumes of vulnerability data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-operations/sem-configure-rules-manage-findings.html
release: australia
product: Security Operations
classification: security-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Configure rules to manage findings

By configuring rules, you can automate, organize, and manage the lifecycle of findings. The rules help ensure scalability, data consistency, and faster response times by reducing manual intervention across large volumes of vulnerability data.

-   **[Configuring lookup rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-configure-lookup-rules.md)**  
By configuring lookup rules, you can map security exposure data to the correct configuration items \(CIs\) in the CMDB. This mapping is a critical function because associating exposure findings with the right assets is essential for proper risk assessment, assignment, and remediation workflows.
-   **[Configuring classification rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-configure-classification-rules.md)**  
By configuring classification rules, you can ensure consistent categorization and processing of vulnerabilities, discovered items and other finding related entities based on key attributes. This helps the system route findings to the correct tables, apply the appropriate grouping, assignment, and remediation rules, enhance reporting accuracy, and determine which business logic to use \(such as prioritization and remediation targets\).
-   **[Configuring roll-up calculator rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-configure-risk-rules.md)**  
Configure roll-up calculator rules to compute the cumulative risk score for remediation tasks and imported vulnerabilities.
-   **[Configuring assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-configure-assignment-rules.md)**  
By configuring assignment rules, you can automate the process of routing findings to the appropriate teams or individuals. By defining assignment criteria based on vulnerability attributes or affected assets, you can ensure timely and accurate ownership for remediation efforts.
-   **[Configuring remediation target rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-configure-remediation-target-rules.md)**  
By configuring remediation target rules, you can set the expected time frame for addressing findings, similar to how service level agreements \(SLAs\) set deadlines for fixing vulnerabilities.
-   **[Configuring an exception rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-configure-exception-rule.md)**  
You can request an exception for findings that can't be remediated or deferred immediately. By automating the finding deferral process, you can defer the matching findings based on the rule when the system identifies them.
-   **[Define fields and weights for the risk rule for Unified Security Exposure Management risk calculators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-vuln-calc-define-risk-rule-fields.md)**  
Customize risk rule parameters and weights to generate risk scores that reflect your organization's specific finding and asset data. By selecting relevant fields for the risk rule, you can create an effective risk scoring framework that meets your organization's unique needs.
-   **[Configuring remediation task rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-configure-remediation-task-rules.md)**  
By configuring remediation task rules, you can automatically group findings based on filter conditions.
-   **[Configuring auto-close rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-configure-auto-close-rules.md)**  
By configuring auto-close rules, you can automate the process of closing stale detections and findings associated with retired configuration items \(CIs\).
-   **[Configuring auto-delete rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-configure-auto-delete-rules.md)**  
By configuring auto-delete rules, you can automate the process of deleting older findings and remediation tasks.
-   **[Configuring exclusion rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-configure-exclusion-rules.md)**  
By configuring exclusion rules, you can filter or exclude detections from being converted into vulnerable items \(VITs\) during ingestion. This filtering helps streamline vulnerability management by reducing noise and prioritizing critical issues.
-   **[Approval workflow configurations for unassign request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/sem-unassign-approval-rules.md)**  
You can design the approval workflow for the removal of assignments from vulnerable items \(VIs, VITs\), remediation tasks, application vulnerable items \(AVITs\), and container vulnerable items \(CVITs\) for you and your group.

