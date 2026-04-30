---
title: Create Security Incident from a Vulnerability Record
description: Create a security incident to track and manage remediation efforts for identified vulnerabilities. This process helps prioritize security responses and maintain audit trails.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Access Vulnerability Downstream actions, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create Security Incident from a Vulnerability Record

Create a security incident to track and manage remediation efforts for identified vulnerabilities. This process helps prioritize security responses and maintain audit trails.

## Before you begin

Role required:

-   sn\_sec\_tisc.analyst
-   sn\_si.analyst

## About this task

Before you begin, ensure that Security Incident Response \(SIR\) application is installed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Threat Intel Library** icon on the workspace.

3.  Go to **Vulnerability Artifacts** &gt; **All Vulnerabilities**.

4.  Open a vulnerability record.

5.  Select **Create Security Incident**.

6.  On the form, **Short description** is automatically populated \(required\) and optionally update category, priority, assignment group, and description as necessary.

    ![Create Security Incident dialog with form fields for short description, category, priority, and assignment group.](../image/tisc-create-security-incident.png)

7.  Select **Submit**.

    A confirmation message appears indicating that Security incident \{\*\*\*\*\*\*\*\*\} created successfully, and a link to the Security Incident record is provided.

    **Note:**

    -   When you click the link from the confirmation message, the Security Incident opens in read-only mode. The record includes a reference to the originating vulnerability, and relevant fields are automatically populated to maintain consistency.
    -   A corresponding work note is also added to the vulnerability record. To access it, go to the **Details** section of the vulnerability record.
    -   Additionally, the system records a work note on the activity stream of the Security Incident Response Workspace indicating that the incident record is originated from a TISC vulnerability and providing a link to the related vulnerability record.
    The **TISC Context** feature in the Security Incident Response Workspace provides analysts direct access to threat intelligence linked to vulnerabilities associated with incidents. For more information, see [Working with TISC Context](../../secops-analyst-workspace/concept/working-with-tisc-context.md).

    This capability allows analysts to view and investigate related threat objects without leaving the Security Incident Response Workspace, streamlining analysis and enhancing incident response efficiency.


**Parent Topic:**[Access Vulnerability Downstream actions](../concept/downstream-actions-from-the-vulnerability-form-view.md)

**Related topics**  


[TISC integration within SIR Workspace](../concept/tisc-sir-workspace.md)

