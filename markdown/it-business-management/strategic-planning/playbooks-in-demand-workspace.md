---
title: Playbooks in Next Experience for Demand Management
description: Playbooks in Next Experience for Demand Management provide a guided, structured approach to managing a demand from initiation to completion. Playbooks focus specifically on helping demand teams follow the standard demand life-cycle, confirming every demand progresses consistently and no critical steps are missed. You can define your playbooks according to your requirements.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Playbooks in Next Experience for Demand Management

Playbooks in Next Experience for Demand Management provide a guided, structured approach to managing a demand from initiation to completion. Playbooks focus specifically on helping demand teams follow the standard demand life-cycle, confirming every demand progresses consistently and no critical steps are missed. You can define your playbooks according to your requirements.

## Purpose of Playbooks in Demand Management

Playbooks provide a structured way to manage work by guiding teams through predefined steps. It shows what to do, when to do it, and where to find the tools or information required to complete each task. You can apply a playbook to processes such as managing a demand, resolving an issue, launching a product, onboarding new employees, or define key steps of a process. For more information on playbooks and how to create them, see [Workflow studio playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer.md).

In Next Experience for Demand Management, playbooks help demand managers and reviewers:

-   Understand exactly which activities must be completed at each demand stage.
-   Track required inputs, approvals, and validations for demand progression.
-   Confirm that demand evaluation, prioritization, and planning follow the organization’s standard governance.
-   Provide built‑in process guidance within the demand record, reducing the need to rely on informal or undocumented knowledge.
-   Maintain process consistency across all demands, regardless of the requester or manager.
-   Enable you to define multiple standardized governance processes across the organization.

## How Playbooks work for demands

When a playbook is applied to a demand:

-   Demand life-cycle stages such as ideation, assessment, prioritization, and planning are outlined.
-   Each stage contains activities and tasks tailored to demand requirements, such as defining scope, estimating effort, documenting benefits, or securing stakeholder approval.
-   Playbooks guide demand managers through dependencies before the demand can move forward.
-   Demand records automatically capture progress and trigger actions such as assessments and approvals as the tasks are completed.

For example, a demand about a Customer Self‑Service Portal enhancement uses a playbook to guide its progress as follows:

-   The ideation stage prompts the demand manager to capture objectives and benefits.
-   The assessment stage guides effort, cost, and risk evaluation.
-   Prioritization helps validate scoring and funding.
-   Planning finalizes the scope and links the demand to a potential work entity.

As each stage is completed, the playbook ensures that the demand follows the standard life-cycle without missing any required steps.

## Playbook benefits

Playbooks add value to demand management by:

-   Standardizing demand intake: Ensuring required information is captured early.
-   Providing step-by-step instructions: Useful for new demand managers or occasional users.
-   Supporting governance: Ensuring stage gating for evaluation and approval.
-   Improving visibility: Showing exactly where a demand sits in the life-cycle and what is blocking its progress.
-   Integrating workflows: Using Flow Designer to set up different business logic for each playbook flow.

## Types of Playbooks

-   Demand default playbook - The default demand playbook is a stage-gate playbook. In a stage-gate playbook, the stages and tasks must be completed in a linear order. Each stage must be finished before moving to the next one. The stages are visible only when all activities in the previous stage are completed or skipped. After completing a stage, demand managers can still return to previous stages if needed.
-   AI playbook - The AI playbook is available for a demand when the AI Control Tower plugin is installed and the investment type of the demand is set to artificial intelligence. This playbook has an additional AI checkpoint stage where you can associate new or existing AI systems to your demand.

**Note:**

-   You can use the demand default playbook and customize it according to your organization's requirements. For more information about the stages and activities of this playbook, see [Demand default playbook stages and activities](../reference/demand-default-playbook-stages.md).
-   You can also create a demand playbook according to your requirements. For more information, see [Create and configure playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/setting-up-process-automation-designer.md).

**Related topics**  


[Workflow Studio playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/workflow-studio-playbooks-landing.md)

[Create and customize playbooks](../task/playbooks-configuration-for-dmnd-wpc.md)

[Use Playbooks](../task/use-playbooks-in-dw.md)

[Demand default playbook stages and activities](../reference/demand-default-playbook-stages.md)

