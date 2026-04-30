---
title: Open search results in IT Remediation Workspace
description: Set the application scope to IT Remediation Workspace to open your search results in the IT Remediation Workspace instead of classic UI by changing the application scope.
locale: en-US
release: yokohama
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using the IT Remediation Workspace, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Open search results in IT Remediation Workspace

Set the application scope to IT Remediation Workspace to open your search results in the IT Remediation Workspace instead of classic UI by changing the application scope.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## About this task

For example, if you search for a host vulnerable item with its number in the **Search** field by setting the application scope to IT Remediation Workspace, the VIT opens in its record view in the IT Remediation Workspace.

## Procedure

1.  In the unified navigation bar, select the globe icon ![Application scope icon](../../../reuse/icons/product-icons/globe-fill-24.svg).

2.  Select **Application Scope**, and then set the scope to **IT Remediation Workspace**.


## Result

When you search for records such as VITs, remediation tasks, state change approvals, and so on, in the **Search** field in the unified navigation bar, the records open in the IT Remediation Workspace.

When the scope is not Global, the globe icon displays with a red ring ![Application scope icon](../../vr-vulnerability-manager-workspace/image/icon-scope-change.png). Select it again to change the scope.

