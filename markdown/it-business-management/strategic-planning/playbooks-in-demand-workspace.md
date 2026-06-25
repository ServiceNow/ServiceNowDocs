---
title: Playbooks in Next Experience for Demand Management
description: Playbooks in Next Experience for Demand Management provide a guided, structured approach to managing a demand from initiation to completion. Playbooks focus specifically on helping demand teams follow the standard demand life cycle, verifying every demand progresses consistently and no critical steps are missed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/playbooks-in-demand-workspace.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Playbooks in Next Experience for Demand Management

Playbooks in Next Experience for Demand Management provide a guided, structured approach to managing a demand from initiation to completion. Playbooks focus specifically on helping demand teams follow the standard demand life cycle, verifying every demand progresses consistently and no critical steps are missed.

## Purpose of Playbooks in Demand Management

Playbooks provide a structured way to manage work by guiding teams through predefined steps. They show what to do, when to do it, and where to find the tools or information required to complete each task. You can apply a playbook to processes such as managing a demand, resolving an issue, launching a product, onboarding new employees, or defining key steps of a process. For more information on playbooks and how to create them, see [Workflow studio playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer.md).

In Next Experience for Demand Management, playbooks help demand managers and reviewers in the following ways:

-   Understand which activities must be completed at each demand stage.
-   Track required inputs, approvals, and validations for demand progression.
-   Verify that demand evaluation, prioritization, and planning follow the organization’s standard governance.
-   Provide built‑in process guidance within the demand record, reducing the need to rely on informal or undocumented knowledge.
-   Maintain process consistency across all demands regardless of the requester or manager.
-   Define multiple standardized governance processes across the organization.

## How Playbooks work for demands

When a playbook is applied to a demand, the following processes take place:

-   Demand life-cycle stages such as ideation, assessment, prioritization, and planning are outlined.
-   Stages contain activities and tasks tailored to demand requirements, such as defining scope, estimating effort, documenting benefits, or securing stakeholder approval.
-   Demand managers are guided through dependencies before the demand can move forward.
-   Demand records automatically capture progress and trigger actions such as assessments and approvals as the tasks are completed.

For example, a demand about a Customer Self‑Service Portal enhancement uses a playbook to guide its progress as follows:

-   The ideation stage prompts the demand manager to capture objectives and benefits.
-   The assessment stage guides effort, cost, and risk evaluation.
-   Prioritization helps validate scoring and funding.
-   Planning finalizes the scope and links the demand to a potential work entity.

As each stage is completed, the playbook help verify that the demand follows the standard life cycle without missing any required steps.

In Demand Management, playbooks are triggered by record creation. A playbook is associated with demand records, and the Playbook page appears in the L-2 \(level 2\) menu when a demand meets the trigger condition.

## Playbook benefits

Playbooks add value to demand management in the following ways:

-   Standardizing demand intake: Establishing that required information is captured early.
-   Providing step-by-step instructions: Guiding new demand managers or occasional users.
-   Supporting governance: Providing stage gating for evaluation and approval.
-   Improving visibility: Showing exactly where a demand sits in the life cycle and what is blocking its progress.
-   Integrating workflows: Using Flow Designer to set up different business logic for each playbook flow.

## Types of Playbooks

Next Experience for Demand Management includes two predefined playbooks available in Workflow Studio: the demand default playbook and the AI playbook.

**Note:** These playbooks are ready to use without any additional configuration. Configure playbooks only when you must customize an existing playbook or create one for your organization's specific demand workflows.

-   Demand default playbook - The default demand playbook is a stage-gate playbook in which each stage must be finished before moving to the next one. Stages are visible only when all activities in the previous stage are completed or skipped. After completing a stage, demand managers can still return to previous stages.

    You can create a demand playbook or customize the default demand playbook. For more information about the stages and activities of this playbook, see [Demand default playbook stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/demand-default-playbook-stages.md). For information about creating one, see [Create and configure playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/setting-up-process-automation-designer.md).

-   AI playbook - This playbook has an additional AI checkpoint stage where you can associate new or existing AI systems to your demand. The AI Control Tower plugin must be installed. The investment type of the demand must be set to artificial intelligence.

**Note:**

-   You can activate a predefined playbook by defining an appropriate trigger condition. For more information, see [Activate Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/activate-process-automation-designer.md) and [Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer-triggers.md).
-   You can enable multiple playbooks at a time. Define trigger conditions so that each demand maps to only one playbook type. For more information, see [Create and configure playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/setting-up-process-automation-designer.md).

**Related topics**  


[Workflow Studio playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio-playbooks-landing.md)

[Building Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/building-a-process.md)

[Designing Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-experience-admins.md)

[Use Playbooks in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/use-playbooks-in-dw.md)

[Demand default playbook stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/demand-default-playbook-stages.md)

