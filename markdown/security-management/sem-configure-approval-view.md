---
title: Configure Approval List and Form View
description: Optimize the review and approval process by configuring list views and form layouts for unified exception and approval management.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Unified Approvals View, Use, Unified Security Exposure Management, Security Operations]
---

# Configure Approval List and Form View

Optimize the review and approval process by configuring list views and form layouts for unified exception and approval management.

## Before you begin

Role required: Admin

## About this task

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **Approvals**.

2.  The default list displays all approvals in the Approvals list view.

3.  Select application type such as: Application vulnerabilities \(AVR\), Container vulnerabilities \(CVR\), Infra Vulnerabilities \(VR\), and Misconfigurations \(CC\) to filter approvals by category.

4.  or Select the 3-menu option to group requests by Approval Name, Record reference, Request Type, Number, Risk Rating, Remediation Status, Approval Assignment group, and state.

    **Note:** You can select the filter icon to view requests by status and list icon or gear icon to reset the columns according to your requests or to reset the widths.

5.  Select any request to view the form and request details such as:

    1.  **State**, **Approval Due Date** and **Approver**.
    2.  **Overview tab** consists of details such as:
        -   Approval Status: Provides an overview of the Change approval \(CA\) request.
        -   Request details: Provides Change approval\(CA\) request details.
        -   Remediation details: Provides remediation details for the Change approval \(CA\) request.
        -   Impact summary: Provides approvers the visibility of the impacted count information such as, Impacted CIs, Total Findings, and Total Vulnerabilities on the Change Approval for a Remediation Task.
        -   Vulnerability Intelligence: Provides vulnerability intelligence data such as CISA KEV information, Known ransomware indicators, and EPSS percentile. This tile is visible only when Intelligence and App-Vuln NVD plugins are installed.
    3.  **Approvers tab** consists of details such as:
        -   Approver name
        -   Email ID
        -   State
    4.  **Impacted services tab** consists of details such as Name, Business criticality, Used for, Service classification, Managed by, Owned by, Approval group, Location, Operational status.

        **Note:** Admins can see additional filtering options and widgets such as: **Pending approvals**, **Today's approvals**, **Exception Approvals**, **False Positive Approvals**


**Parent Topic:**[Unified Approvals View](../concept/sem-approval-view.md)

