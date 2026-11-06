---
title: Remediation view
description: The Remediation view in the Security Exposure Management workspace provides remediation owners and vulnerability analysts with a consolidated view of remediation tasks, findings \(vulnerable items and configuration test results\), and assets \(configuration items\) that are associated with exposure findings. In addition, vulnerability analysts will also have a consolidated view of fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/sem-workspaces-ui-remediation-module.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Security Exposure Management Workspace, Explore, Unified Security Exposure Management, Security Operations]
---

# Remediation view

The Remediation view in the Security Exposure Management workspace provides remediation owners and vulnerability analysts with a consolidated view of remediation tasks, findings \(vulnerable items and configuration test results\), and assets \(configuration items\) that are associated with exposure findings. In addition, vulnerability analysts will also have a consolidated view of fixes.

## Accessing the Remediation view

Users can view fixes, remediation tasks and findings for all exposure types from a single location using filters. The data available on this page can help remediation owners prioritize their work, and vulnerability analysts can monitor overall remediation progress for specific types of exposure findings or fixes.

Navigate to **Workspaces** &gt; **Security Exposure Management** &gt; **Remediation**. What you can see and do in the view depends on your role and the applications you have installed.

## Features of the Remediation view

Following tabs are available:

-   Fix intelligence: Displays findings for all exposure types. Available only for vulnerability analysts.

    **Note:** It is available when both the Unified Exposure Pipeline \(sn\_vul\_int\_cmn\) and Fix Intel for Security Exposure Management \(sn\_vul\_fix\) applications are installed.

-   Remediation Tasks: Filter records by remediation status, state, or risk rating. Available for both remediation owners and vulnerability analysts. Remediation owners can filter for tasks assigned to them or their groups.
-   Findings: Filter records by impacted configuration items, by state, risk rating. Available for both remediation owners and vulnerability analysts. Remediation owners can filter for findings assigned to them or their groups.
-   Assets: Filter records by configuration items and their associated security exposures. Available for both remediation owners and vulnerability analysts. Remediation owners can filter for assets assigned to them or their groups.

**Note:** You can also filter remediation tasks and findings records by the type of security exposure, host findings \(VIT\), application findings \(AVIT\), and so on. These records are available based on the applications that you have installed and the roles you have assigned:

-   Application Vulnerability Response - AVITs and AVULs.
-   Container Vulnerability Response - CVITs and CVUL records.
-   Host Vulnerability Response VITs and VUL records.
-   Test results Configuration Compliance CTRs and CRG records.

