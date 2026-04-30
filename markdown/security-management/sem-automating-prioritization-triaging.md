---
title: Automating prioritization and triaging
description: Automate prioritization and triaging of findings using rules and severity mapping.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Automating prioritization and triaging

Automate prioritization and triaging of findings using rules and severity mapping.

-   **[Associating finding with a configuration item using lookup rules](sem-associate-finding-configuration-item-using-lookup-rules.md)**  
Unified Security Exposure Management uses lookup rules to associate imported third-party exposure findings with configuration items \(CIs\) in the Configuration Management Database \(CMDB\). These rules match asset data to existing CIs, enabling accurate remediation.
-   **[Categorizing findings and discovered items using classification rules](sem-categorizing-findings-discovered-items.md)**  
Classification groups automate the classification of entities or records based on the classification rules defined in the group. The condition for each rule is evaluated in order, and the first matching rule is used.
-   **[Prioritizing vulnerabilities and other findings using roll-up calculators](sem-prioritizing-vulnerabilities-other-findings.md)**  
After assessing risk calculators, use the roll-up calculators to configure how the cumulative risk scores are computed for remediation tasks and other higher entities.
-   **[Assigning findings to remediation teams using assignment rules](sem-assigning-findings-to-remediation-teams.md)**  
Assignment rules automatically assign findings, such as vulnerable items, application vulnerabilities, container vulnerabilities, and configuration test results, to the appropriate groups for remediation. This streamlined triage ensures that tasks are directed to the appropriate teams, and enhances consistency and visibility across security and compliance programs.
-   **[Defining your own service level agreements \(SLAs\) using remediation target rules](sem-defining-your-own-sla.md)**  
Remediation target rules set the expected time frame for addressing findings, similar to how service level agreements \(SLAs\) set deadlines for fixing vulnerabilities. You can also send notifications to users and groups when target dates are approaching and when they are past due.
-   **[Deferring findings automatically without manual intervention using exception rules](sem-exception-rules-overview.md)**  
Exception rules for Security Exposure Management Workspace enable you to automate the deferral process for findings. Request an exception for the findings that can't be remediated or deferred immediately, by identifying the impacted vulnerabilities, configuration items \(CIs\), or VIs. Defer the matching findings based on the rule when the system identifies them by automating the finding deferral process.
-   **[Grouping multiple findings as remediation tasks for easy processing using remediation task rules](sem-grouping-multiple-findings-remediation-tasks-processing.md)**  
Remediation tasks help vulnerability analysts and remediation teams manage findings in bulk. By configuring remediation task rules, you can automatically group findings into remediation tasks, eliminating the need for manual task creation and streamlining remediation efforts.
-   **[Closing stale detections and findings automatically using auto-close rules](sem-closing-stale-findings-automatically.md)**  
Auto-close rules automatically close stale detections and findings based on predefined criteria. These rules ensure that redundant or unwanted findings are marked as closed, helping to maintain an accurate and up-to-date record of the organization's security posture. By automating this process, the rules reduce manual effort and enable teams to focus on active and critical vulnerabilities.
-   **[Deleting stale findings automatically using auto-delete rules](sem-deleting-stale-findings-automatically.md)**  
Auto-delete rules automatically remove findings from the system based on predefined criteria. These rules help manage the life-cycle of vulnerabilities by ensuring that resolved or outdated findings are removed, reducing clutter and maintaining a clean, up-to-date database. This automation streamlines the vulnerability management process and ensures that teams focus on current and relevant issues.
-   **[Controlling the ingestion volume with automatic exclusion](sem-controlling-ingestion-volume-automatic-exclusion.md)**  
Exclusion rules provide a way to filter or exclude detections from getting converted into VITs during the ingestion process in Vulnerability Response.
-   **[Severity mapping for Unified Security Exposure Management](sem-severity-mapping.md)**  
Severity mapping is a critical feature that enables organizations to standardize and normalize the severity levels of findings detected across different sources. This process involves mapping the severity levels from various scanners and sources to a common severity scale used within Unified Security Exposure Management.
-   **[Creating CIs using the Identification and Reconciliation engine](sem-ci-creation-using-IRE.md)**  
You can create configuration items \(CIs\) in the Configuration Management Database \(CMDB\) using the Identification and Reconciliation engine \(IRE\) API. By using the IRE API to create CIs, you can prevent duplicate CIs from being created and you can reconcile CI attributes by allowing only authoritative data sources to write to CMDB.

