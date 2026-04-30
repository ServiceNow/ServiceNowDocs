---
title: Help resolve tuition requests agentic workflow for Now Assist for HRSD
description: The Help resolve tuition requests agentic workflow evaluates employee-submitted course information against company tuition policies found in knowledge articles to help employees understand whether their proposed course meets reimbursement requirements and directs them through the pre-approval flow.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Help resolve tuition requests agentic workflow for Now Assist for HRSD

The Help resolve tuition requests agentic workflow evaluates employee-submitted course information against company tuition policies found in knowledge articles to help employees understand whether their proposed course meets reimbursement requirements and directs them through the pre-approval flow.

## Help resolve tuition requests overview

The Help resolve tuition requests agentic workflow streamlines the tuition pre-approval process by evaluating the course information an employee submits against company policies found in knowledge articles.

**Note:** This agentic workflow is designed for employees to receive pre-approval before enrolling in a course. The [Help resolve tuition requests](resolve-tuition-reimbursement-requests.md) agentic workflow helps employees request reimbursement for pre-approved and completed courses.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Agentic workflows** &gt; **Help resolve tuition requests**.

    The Define key requirements workflow is displayed. For more information, see [Help resolve tuition requests AI agents](now-assist-hrsd-ai-agents-policy-resolving-tr-usecase.md#section_kgq_whk_h2c).

3.  Select **Add a preferred trigger** to review the trigger factors for this agentic workflow. For more information, see [Triggers for the Help resolve tuition requests agentic workflow](now-assist-hrsd-ai-agents-policy-resolving-tr-usecase.md#section_chn_zlf_j2c).
4.  The **Select a UI display** option enables the Now Assist panel. For more information, see [Select display](now-assist-hrsd-ai-agents-policy-resolving-tr-usecase.md#section_bc5_ykn_x2c).

## Help resolve tuition requests AI agents

The following table lists the agents that are part of the Help resolve tuition requests agentic workflow.

|AI agent|Description|
|--------|-----------|
|Tuition reimbursement policy based HR case evaluation AI agent|Evaluates the HR case details against the company policy.|
|Tuition reimbursement case closure AI agent|Adds work notes with the resolution steps taken and moves the case to awaiting approval/close complete.|
|Tuition reimbursement preapproval task generation AI agent|Checks if the manager has approved a pre-approval request or creates a new pre-approval request.|

## Triggers for the Help resolve tuition requests agentic workflow

In the Help resolve tuition requests workflow, the agentic workflow begins executing when the case is assigned and in the Ready or WIP state.

|Trigger|Description|
|-------|-----------|
|Manager approves/rejects tuition reimbursement pre-approval case|The workflow is triggered when the employee's manager approves or rejects the pre-approval request for tuition reimbursement.|
|Tuition Reimbursement Pre- Approval Case Created/Updated|The workflow is triggered when the case is created \(employee submits the request\) or when the case is updated.|

## Select display

In the **Select a UI display** workflow, you can enable the Now Assist panel display, which sends notifications to HR agents for the triggered case. When the Now Assist panel option is enabled, the AI agent output or notifications are displayed in the Now Assist panel.

Select this option to receive and review notifications by AI agents in the Now Assist panel. AI agents notify HR agents in the Now Assist panel with the case resolution and summarization notes.

**Related topics**  


[Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

