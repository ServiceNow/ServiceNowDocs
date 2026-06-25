---
title: Use the AI guardrails helper agentic workflow
description: Use the AI agent to ask about the guardrails that were identified by the AI skill component in the AI Guardrails Helper, automatically defer findings with existing mitigations in the form of guardrails, or create exception rules to auto-defer future findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/ai-security-exposure-use-agent.html
release: australia
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 2
breadcrumb: [Using the AI guardrails helper skill and agentic workflow, AI Security Exposure Management, Use, Unified Security Exposure Management, Security Operations]
---

# Use the AI guardrails helper agentic workflow

Use the AI agent to ask about the guardrails that were identified by the AI skill component in the AI Guardrails Helper, automatically defer findings with existing mitigations in the form of guardrails, or create exception rules to auto-defer future findings.

## Before you begin

The Now Assist panel must be activated. For more information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

Roles required: sn\_vul.vulnerability\_admin or sn\_vul.vulnerability\_analyst admin

## About this task

Because the agentic workflow uses AI to generate responses, review all output before acting on it and apply human judgment to any remediation decisions.

Before providing the agent with instructions, use the AI guardrails helper skill to collect guardrail suggestions for findings that have associated vulnerabilities.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  If the **AI validation findings** tab is not displayed, select it.

3.  Select **Ask Now Assist** to invoke the agent.

    A new panel opens. The agent displays the following options:

    -   **Find mitigated validation findings**

        Locate mitigated findings by threat categories to help you see more about the AI behavior threats identified by automated red teaming or validation.

    -   **Defer validation findings**

        Defer findings returned by the Guardrail Detector skill, or a subset of the returned results, using AI-generated justifications for deferral.

    -   **Create exception rule**

        Create exception rules to automatically defer future AI validation findings that have guardrails as mitigations already present in the AI security platform. See [Configure Exception Management for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-configure-exp-mngmt-vr.md) for more information about exception management.

    -   **Learn about guardrails**

        View how active mitigations in your environment help defer findings and reduce risk.

        **Note:** For deferred findings, associated threats are imported and stored for potential reconsideration.

4.  Select a prompt in the panel.

    For example, if you select **Defer validation findings**, you can defer all findings for a specific criterion: risk rating, assignment group, and so on.

    The system displays a justification for the deferral for your review. You can approve or reject the justification. If you approve it, a calendar is displayed so you can choose an end date for the deferral. After you select **Submit**, the finding state transitions from **Open** to **Deferred**.

    The system displays the number of findings associated with your deferral request and prompts you to create an exception rule.

    If you select **Yes**, a rule is created. Select the link to view your new rule. The system displays the record for review. You can modify the conditions of the rule and select **Save** to preserve your changes. Select **Submit** to send your new rule for approval based on your approval hierarchy and approval rules described in &lt;link to Exception Management.&gt;

    Select the **Approvals** tab on the approval rule record to view the status of your requests.


**Parent Topic:**[Using the AI guardrails helper skill and agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/ai-security-exposure-skill-agent.md)

