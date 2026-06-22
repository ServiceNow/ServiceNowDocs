---
title: Use the AI guardrails helper skill
description: This AI skill can help you identify finding types, understand the guardrails that might be already mapped to findings, and see why they were selected by the skill to map to specific findings. This information can help you determine which findings might be already mitigated or deferred for later review or remediation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-operations/ai-security-exposure-use-aiskill.html
release: australia
product: Security Operations
classification: security-operations
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 1
breadcrumb: [Using the AI guardrails helper skill and agentic workflow, AI Security Exposure Management, Use, Unified Security Exposure Management, Security Operations]
---

# Use the AI guardrails helper skill

This AI skill can help you identify finding types, understand the guardrails that might be already mapped to findings, and see why they were selected by the skill to map to specific findings. This information can help you determine which findings might be already mitigated or deferred for later review or remediation.

## Before you begin

The Now Assist panel must be activated. For more information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/activate-now-assist-panel.md).

Roles required: sn\_vul.vulnerability\_admin or sn\_vul.vulnerability\_analyst admin

## Procedure

1.  Navigate to **All** &gt; **Security Exposure Management** &gt; **AI Exposures**.

2.  Select the **AI validation findings** tab.

    The AI guardrails helper panel is displayed.

    **Note:** This panel is displayed only if you have installed the Now Assist for Vulnerability Response application.

3.  If you're using the application for the first time, select **Detect guardrails**.

4.  Respond to the prompt asking whether the AI guardrails helper should run periodically.

    -   **Yes** — Run the job on the scheduled time and frequency. You can choose how often the job runs.
    -   **No, only manually \(on-demand\)** — Run the skill manually when needed.
    To view these options after you initially set them, select the menu icon \[Omitted image "icon-menu.png"\] Alt text:

5.  Select **Confirm and run**.

    Run time scales with the number of newly imported findings. The first run may take a few moments to display results. Subsequent runs process only delta findings. You can activate a notification to trigger when the job completes.

    -   N \(number of findings\) for deferral — The number of findings that can use detected matching guardrails. These findings can be deferred because the risks can be mitigated by the guardrails.
    -   Mitigated findings by threat category, for example:
        -   Social Division and Polarization
        -   Violence and Public Safety
        -   Hate Speech
        -   Harassment
    Select a value from the categories to open a list of findings by category \(AIVUL\).

    You can now use the Guardrail Detector agentic workflow to create exception rules to automatically defer findings that match your criteria.


**Parent Topic:**[Using the AI guardrails helper skill and agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/ai-security-exposure-skill-agent.md)

