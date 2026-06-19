---
title: Bulk Fix code in real-time with Now Assist
description: As a ServiceNow developer, you can receive code fix suggestions when an error is detected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/fix-code-with-the-ai-agent.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 2
breadcrumb: [Fix code in real-time with Now Assist, Prevent and resolve technical debt, Platform Health, Using Impact, Impact]
---

# Bulk Fix code in real-time with Now Assist

As a ServiceNow developer, you can receive code fix suggestions when an error is detected.

## Before you begin

Complete the pre-requisites and setup steps in order to activate Fix code in real-time. See [Configure Fix code in real-time for Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-ai-code-fix-for-platform-health.md) for details.

Role required: sn\_impact\_gen\_ai\_fix\_user

## Procedure

1.  When an error eligible for AI resolution is detected, review the findings summary banner at the top of the form, then select **View finding details** to open the Findings panel.

    The Findings panel displays on the right side of the workspace and organizes findings into the following tabs: **All**, **Act**, **Recommend**, **Suggest**, and **Review**. Each finding card includes:

    -   **Finding level** and **impact level**: The severity and a link to the Scan Engine definition.
    -   **Details**: The exact line number in the code where the finding occurred.
    -   **Steps to resolve issue**: A description of the recommended resolution.
    -   **Supporting documentation**: A link to a knowledge base article or documentation explaining the recommended configuration.
    For Recommend level findings, a **Create exception** button is available directly on the finding card.

    \[Omitted image "real-time-code-fix-findings-panel.png"\] Alt text: The Findings panel displaying Act and Recommend level findings alongside the script editor.

2.  Select **Fix with Now Assist** from the menu bar to execute the remediation process.

    Review the Now Assist Panel with remediation suggestions.

    \[Omitted image "code-fix-ai-remediation.png"\] Alt text: The suggested fix for the finding.

    -   The Now Assist panel displays the reasoning, in steps, for the findings it provided resolutions for.
    -   At the same time, a code comparison view displays on the script itself, illustrating the suggested modifications. Updated code is displayed in green and the removed code has a pink background.
    -   The script editor is read-only until the Now Assist conversation closes, either by accepting or rejecting the proposed fix.

        **Note:** You can either accept the code fix as is, reject it, or provide revisions to the suggested fix. During the revision process, you can interact with the AI Agent panel to prompt it to make additional changes for each finding.

3.  Enter **Accept the solution** in the AI response prompt to make the change.

    -   The available prompts are displayed in the bulleted list for the proposed solution.
    -   If you reject the solution, the code will be editable.
    **Note:** Users with the executive role can access the Executive Dashboard which contains a module that displays all findings resolved using the Now Assist Agent. See [Scan Engine Executive dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/scan-engine-executive-dashboard.md) for additional information.


