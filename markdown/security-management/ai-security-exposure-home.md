---
title: Viewing AI Exposures
description: Access the entire attack surface across various types of findings on the AI Security Exposure Management dashboard on the AI Exposures module. AI exposures as a dedicated module of the Security Exposure Management workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/ai-security-exposure-home.html
release: australia
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 5
breadcrumb: [Security Exposure Management Workspace, Explore, Unified Security Exposure Management, Security Operations]
---

# Viewing AI Exposures

Access the entire attack surface across various types of findings on the AI Security Exposure Management dashboard on the AI Exposures module. AI exposures as a dedicated module of the Security Exposure Management workspace.

## AI Exposures overview

See [Exploring AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/exploring-ai-security-exposure.md) for an overview and more information about the application.

See the [AI security exposure management](https://www.servicenow.com/community/secops-articles/reduce-ai-attack-surface-with-ai-security-exposure-management/ta-p/3563696) article in the Security Operations Community for more information about AI Security Exposure Management.

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

The totals displayed on the dashboard are aggregated \(totaled\) by a scheduled job that by default runs daily. When you open dashboard, these aggregated results from the scheduled jobs are displayed. For more information about scheduled jobs see [Components installed with AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/installed-with-aisecmanagement.md). To see data on-demand, select **Refresh**. This activates the background jobs that refresh the page with the aggregated results.

Select a tab to view visualizations for each category.

## Overview section

The Overview section displays the total counts of finding remediation status for AI vulnerabilities, AI validation findings, and AI posture findings of AI exposures for Open findings, Unassigned, Approaching Target, and Overdue.

Select a tab to filter your lists by category and select a tile to open the filtered lists.

|Overview tile|Description|
|-------------|-----------|
|Open findings|Total combined findings still in an open for all the vulnerabilities, validation, and posture findings.|
|Unassigned findings|Findings with no owner assigned.|
|Findings Approaching Target|Findings nearing their remediation-due date.|
|Overdue findings|Findings already past their due dates. A value of 0 means the queue reflects good remediation timing.|

## AI vulnerabilities tab

This is data about vulnerabilities that are discovered in open source AI models that are published in repositories.

-   **Scan metrics section**

    Select a card \(widget\) to open a list of records. Scanning happens at the file level, which is why the number of model files scanned far exceeds the number of models scanned.

    -   Open vulnerabilities - The number of open vulnerability findings discovered by scanning model files.
    -   Models scanned - How many distinct AI models AISEM has scanned.
    -   Model files scanned - How many individual files were scanned. One model can hold many files \(weights, config, tokenizer, Python modeling code\) so this value is much larger than models scanned.
-   **Findings**

    Select a card \(widget\) to open a list of records.

    -   By risk rating - Findings grouped by severity \(Critical to None\).
    -   By top 5 categories - Vulnerability types detected, for example, Unapproved, Knowledge Base Poisoning, Obfuscation vulnerability, Unauthorized, and so on. Each bar represents a class of unsafe model file behavior.
    -   By top 5 MITRE ATLAS techniques - Adversarial Threat Landscape for Artificial-Intelligence Systems \(ATLAS\) is a knowledge base of tactics and techniques attackers use against AI/ML systems — the AI-specific cousin of MITRE ATT&amp;CK. Findings are tagged to ATLAS techniques so an analyst can understand the adversarial behavior behind a finding, not just the symptoms.
    -   By open vs closed state - A trend line of findings opened vs. closed over time. Lets you see if the backlog is increasing or decreasing.

## AI validation findings tab

These findings are from third-party automated penetration testing or automated red-teaming done to verify the behavior of some of these models by scanning them against their prompt libraries.

-   **Validation metrics section**

    Select a card \(widget\) to open a list of records.

    -   Open validation findings - Open findings where a model produced an unsafe or undesired response under testing.
    -   Mitigated findings - Findings now covered by a guardrail that blocks them at runtime.
    -   Active guardrails - Runtime guardrails currently active and blocking.
    -   Models tested - Number of models put through validation attacks.
    -   Number of attacks - Total adversarial attempts run against those models. Each attack is one probe; findings are the attacks that succeeded in eliciting bad behavior.
-   **Findings section**

    Select a card \(widget\) to open a list of records for model vulnerability findings.

    Select a card to open a list of records for model validation findings. Refer to the Findings definitions in the previous sections for these definitions in the AI vulnerabilities tab.

    -   By risk rating
    -   By top 5 threat categories
    -   By top 5 attack techniques
    -   By MITRE ATLAS techniques
    -   By top 5 models

## AI posture findings tab

These are findings for configuration-related vulnerabilities to help you verify that your AI assets are in compliance with your policies and controls.

-   **Posture metrics**

    Select a card.

    -   Open AI posture findings - Total open governance/hygiene findings.
    -   Agents with findings - AI agents flagged with a posture issue.
    -   Tools with findings - Tools flagged that agents can call.
    -   System prompts with findings - System prompts flagged.
    -   MCP servers with findings - MCP servers flagged.
    **Note:**

    The last four tiles map to the **agentic AI stack** &gt; **agent** &gt; **tools** &gt; **prompts** &gt; **MCP servers**.

    They may read 0, but they show that AISEM monitors posture across the whole agent ecosystem, not just standalone models.

-   **Findings**

    Select a card for AI posture findings. Refer to the Findings definitions in the previous sections for these definitions in the AI vulnerabilities tab.

    -   By risk rating
    -   By top 5 platforms
    -   By top 5 AI posture rules
    -   By top 5 critical agents by platform
    -   By top 5 MITRE ATLAS techniques
    -   By top 5 OWASP LLM categories

## Inventory

AI models \(total count\) - A breakdown of AI inventory showing counts of different AI assets with findings reported. Inventory is the denominator. Before scanning, validation, or posture work has any meaningful data, AISEM has to discover the AI footprint. Every finding in the other three tabs traces back to an asset that was reported here first.

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

