---
title: Viewing AI Exposures
description: Access the entire attack surface across various types of findings on the AI Security Exposure Management dashboard on the AI Exposures module. See AI exposures as a dedicated module of the Security Exposure Management workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/ai-security-exposure-home.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 3
breadcrumb: [Security Exposure Management Workspace, Explore, Unified Security Exposure Management, Security Operations]
---

# Viewing AI Exposures

Access the entire attack surface across various types of findings on the AI Security Exposure Management dashboard on the AI Exposures module. See AI exposures as a dedicated module of the Security Exposure Management workspace.

## AI Exposures overview

See [Exploring AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/exploring-ai-security-exposure.md) for an overview and more information about the application.

Roles required.

-   sn\_vul.vulnerability\_admin
-   sn\_vul.vulnerability\_analyst
-   sn\_vul.remediation\_owner
-   sn\_sec\_ai.vulnerability\_admin
-   sn\_sec\_ai.vulnerability\_analyst
-   sn\_sec\_ai.remediation\_owner

There are three categories of AI exposures that are displayed on the dashboard.

-   AI vulnerabilities
-   AI validation findings
-   AI posture findings

Navigate to **Workspaces** &gt; **Security Exposure Management** &gt; **AI Exposures**.

The totals displayed on the dashboard are aggregated \(totaled\) by a scheduled job that by default runs daily. When you open dashboard, these aggregated results from the scheduled &lt;name&gt; job are displayed. To see data on-demand, select **Refresh**. This activates the background job and the page refreshes with the aggregated result when the job completes.

Select a tab to view visualizations for each category.

## Overview section

The Overview section displays the total counts of finding remediation status for AI vulnerabilities, AI validation findings, and AI posture findings of AI exposures for Open findings, Unassigned, Approaching Target, and Overdue.

Select a tab to filter your lists by category and select a tile to open the filtered lists.

## AI vulnerabilities tab

This is data about vulnerabilities that are discovered in open source AI models that are published in repositories.

-   **Scan metrics section**

    Select a card \(widget\) to open a list of records.

    -   Open vulnerabilities
    -   Models scanned
    -   Model files scanned
-   **Findings**

    Select a card \(widget\) to open a list of records.

    -   By risk rating
    -   By top 5 categories
    -   By top 5 MITRE ATLAS techniques
    -   By open vs closed state

## AI validation findings tab

These findings are from third-party automated penetration testing or automated red teaming done to verify the behavior of some of these models by scanning them against their prompt libraries.

-   **Validation metrics section**

    Select a card \(widget\) to open a list of records.

    -   Open validation findings
    -   Mitigated findings
    -   Active guardrails
    -   Models tested
    -   Number of attacks
-   **Findings section**

    Select a card \(widget\) to open a list of records for Model vulnerability findings.

    Select a card to open a list of records for model validation findings.

    -   By risk rating
    -   By top 5 threat categories
    -   By top 5 attack techniques
    -   By MITRE ATLAS techniques
    -   By top 5 models

## AI posture findings tab

These are findings for configuration-related vulnerabilities to help you verify that your AI assets are in compliance with your policies and controls.

-   **Posture metrics**

    Select a card.

    -   Open AI posture findings
    -   Agents with findings
    -   Tools with findings
    -   System prompts with findings
    -   MCP servers with findings
-   **Findings**

    Select a card for AI posture findings.

    -   By risk rating
    -   By top 5 platforms
    -   By top 5 AI posture rules
    -   By top 5 critical agents by platform
    -   By top 5 MITRE ATLAS techniques
    -   By top 5 OWASP LLM categories

## Inventory

AI models \(total count\) - A breakdown of AI inventory showing counts of different AI assets with findings reported.

## Tables storing imported data and used for the dashboard

For scans of AI models, imported data is populated on the following tables and used for the dashboard. The data is aggregated, and the system currently runs daily aggregations.

For model vulnerabilities, imported data is populated on the following tables and used for the dashboard.

-   AI Scan Summaries \[sn\_sec\_ai\_scan\_summary\]
-   AI Scan Findings \[sn\_sec\_ai\_scan\_finding\]
-   Discovered AI Assets \[sn\_sec\_ai\_src\_ci\]
-   AI Vulnerability Entries \[sn\_sec\_ai\_vul\_entry\]
-   Model Files \[sn\_sec\_ai\_file\]

For model validations, imported data is populated on the following tables and used for the dashboard.

-   AI Validation Findings \[sn\_sec\_ai\_validation\_finding\]
-   AI Validation Threat \[sn\_sec\_ai\_validation\_threat\]
-   AI Threat Signatures \[sn\_sec\_ai\_threat\_signature\]

For AI posture findings, imported data is populated on the following tables and used for the dashboard.

-   AI Posture Finding \[sn\_sec\_ai\_posture\_finding\]
-   AI Posture Rule \[sn\_sec\_ai\_posture\_rule\]
-   Finding guardrail \[sn\_sec\_ai\_m2m\_finding\_guardrail\]

