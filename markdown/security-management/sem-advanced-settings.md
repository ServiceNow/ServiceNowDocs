---
title: Configure advanced Settings in Security Exposure Management Workspace
description: The Advanced Settings section allows administrators to configure system-level behavior for vulnerability processing, remediation workflows, compliance handling, and service impact calculations across Unified Security Exposure Management products.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-09"
reading_time_minutes: 1
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Configure advanced Settings in Security Exposure Management Workspace

The Advanced Settings section allows administrators to configure system-level behavior for vulnerability processing, remediation workflows, compliance handling, and service impact calculations across Unified Security Exposure Management products.

## Before you begin

Role required: System Administrator \(admin\)

## About this task

You can configure advanced settings for exclusion rules and lookup rules using the **Configure advanced auto-exclude settings** option under **Administration** &gt; **Exclusion Rules** and the **Configure advanced lookup settings** option under **Administration** &gt; **Lookup Rules**, respectively. After selecting either option, you are redirected to a new page displaying the Advanced Settings configuration for that rule type, where you can update fields and select **Save** to apply the changes. You can also select **View all settings** to view and update all advanced settings properties.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  In the navigation pane, select **Administration**.

3.  Under the **Others** section, locate **Advanced Settings**.

4.  Select **Review** to open the Advanced Settings configuration page.

5.  Review and configure the Advanced Settings fields as needed.

    |Field|Description|
    |-----|-----------|
    |Auto-resolve duplicate vulnerable items|Automatically marks duplicate vulnerable items \(VITs\) as resolved, reducing noise and improving reporting accuracy.|
    |Add policy as key in configuration test|Automatically adds **Test Group** as a key in configuration tests.|
    |Set remediation fields as mandatory|Automatically makes the **Remediation plan** and **Remediation commitment date** fields mandatory to ensure proper remediation documentation.|
    |Auto-update the state of findings|Automatically sets the finding status to **Awaiting Implementation** when both Remediation state and Plan are defined. Applies to Host findings, Container findings, Configuration test results, and Application findings.|
    |Calculate age of findings|Calculates the age of findings based on the selected date. For Vulnerability Response, Application Vulnerability Response, and Container Vulnerability Response: Opened at, First found, Created at, Last opened. For Configuration Compliance: Created on, First seen, Last opened date time.|
    |Auto-close vulnerable item with excluded detections|Automatically marks vulnerable items as **Closed - Excluded** when all associated detections are excluded using exclusion rules.|
    |Ignore configuration item \(CI\) classes|Specifies CI classes and CI model profiles to exclude from lookup rules.|
    |Ignore configuration item \(CI\) classes for service|Specifies CI classes to exclude from impacted service computation.|

6.  Select **Save** to apply the changes.


