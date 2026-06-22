---
title: Help resolve tuition requests agentic workflow for Now Assist for HRSD
description: Use the Help resolve tuition requests agentic workflow for faster mean time to repair \(MTTR\) cases that require validation based on policies that are built for tuition reimbursement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-ai-agents-policy-resolving-tr-usecase.html
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Help resolve tuition requests agentic workflow for Now Assist for HRSD

Use the Help resolve tuition requests agentic workflow for faster mean time to repair \(MTTR\) cases that require validation based on policies that are built for tuition reimbursement.

## Help resolve tuition requests overview

The Help resolve tuition requests agentic workflow can help to collect requested information, check all the policy content, and evaluate the information to resolve a case.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Agentic workflows** &gt; **Help resolve tuition requests**.

    The Define key requirements workflow is displayed. For more information, see [Help resolve tuition requests AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-ai-agents-policy-resolving-tr-usecase.md).

3.  Select **Add a preferred trigger** to review the trigger factors for this agentic workflow. For more information, see [Triggers for the Help resolve tuition requests agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-ai-agents-policy-resolving-tr-usecase.md).
4.  The **Select a UI display** option enables the Now Assist panel. For more information, see [Select display](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-ai-agents-policy-resolving-tr-usecase.md).

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

**Parent Topic:**[Using agentic workflows in Now Assist for HRSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-ai-agents-use-cases.md)

**Related topics**  


[Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/na-ai-agents.md)

[Install Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/install-ai-agents-plugins.md)

[AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/ai-agent-studio.md)

