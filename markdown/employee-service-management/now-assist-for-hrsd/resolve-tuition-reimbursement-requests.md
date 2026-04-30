---
title: Help resolve tuition reimbursement requests agentic workflow
description: The Help resolve tuition reimbursement requests agentic workflow streamlines the reimbursement process by evaluating employee course reimbursement submissions against company policies and returning a decision of approval, denial, or request for additional information.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-11-24"
reading_time_minutes: 2
breadcrumb: [Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Help resolve tuition reimbursement requests agentic workflow

The Help resolve tuition reimbursement requests agentic workflow streamlines the reimbursement process by evaluating employee course reimbursement submissions against company policies and returning a decision of approval, denial, or request for additional information.

## Help resolve tuition reimbursement requests overview

The Help Resolve Tuition Reimbursement Requests agentic workflow automates the evaluation of employee tuition reimbursement submissions using the Policy-based HR evaluator skill to compare course information provided through the Employee Center against company policies documented in knowledge articles. For each request, the workflow collects the submitted course details, analyzes them against policy requirements, and returns a case analysis with one of three decisions: approval if the request meets all policy requirements, denial with explanation if requirements are not met, or a request for additional information if the submission is incomplete.

**Note:** This agentic workflow is designed for reimbursement requests for courses that were pre-approved and completed. The [Help resolve tuition requests](now-assist-hrsd-ai-agents-policy-resolving-tr-usecase.md) agentic workflow helps employees evaluate whether a course meets company requirements before the employee enrolls.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Agentic workflows** &gt; **Help resolve tuition reimbursement requests**.

    The Define key requirements workflow is displayed. For more information, see [Help resolve tuition reimbursement requests AI agents](resolve-tuition-reimbursement-requests.md#section_kgq_whk_h2c).

3.  The **Select a UI display** option enables the Now Assist panel. For more information, see [Select display](resolve-tuition-reimbursement-requests.md#section_bc5_ykn_x2c).
4.  Enable the business rule that triggers the agentic workflow. For more information, see [Triggers for the Help resolve tuition reimbursement requests agentic workflow](resolve-tuition-reimbursement-requests.md#section_chn_zlf_j2c)

## Help resolve tuition reimbursement requests AI agents

The following table lists the agents that are part of the agentic workflow.

|AI agent|Description|
|--------|-----------|
|Tuition reimbursement request evaluator AI agent|Evaluates the HR case details against the company policies described in knowledge articles.|
|Tuition reimbursement request closure AI agent|Adds work notes with the resolution steps taken and moves the case to awaiting approval/close complete.|

## Select display

In the **Select a UI display** workflow, you can enable the Now Assist panel display, which sends notifications to HR agents for the triggered case. When the Now Assist panel option is enabled, the AI agent output or notifications are displayed in the Now Assist panel.

Select this option to receive and review notifications by AI agents in the Now Assist panel. AI agents notify HR agents in the Now Assist panel with the case resolution and summarization notes.

## Triggers for the Help resolve tuition reimbursement requests agentic workflow

In the Help resolve tuition reimbursement requests workflow, the agentic workflow begins executing when the case is assigned and in the Ready or Work in progress state. The agentic workflow utilizes system business rules instead of agentic triggers. To enable the business rule, do the following steps:

1.  Navigate to **System definition** &gt; **Business Rules**.
2.  Locate and open **TR Case Created or Updated**.
3.  Select the **Active** option to enable the business rule.

