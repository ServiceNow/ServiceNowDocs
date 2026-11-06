---
title: Playbooks in Next Experience for Demand Management
description: Playbooks in Next Experience for Demand Management provide a guided, structured approach to managing a demand from initiation to completion. Playbooks focus specifically on helping teams follow the demand life cycle for different governance processes, so every demand progresses consistently and critical steps aren't missed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/strategic-planning/playbooks-in-demand-workspace.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 10
breadcrumb: [Manage demands, Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Playbooks in Next Experience for Demand Management

Playbooks in Next Experience for Demand Management provide a guided, structured approach to managing a demand from initiation to completion. Playbooks focus specifically on helping teams follow the demand life cycle for different governance processes, so every demand progresses consistently and critical steps aren't missed.

\[Omitted video\] Description: Benefits of playbooks, the default demand workflow playbook in Next Experience for Demand Management and how to customize playbooks for your governance processes.

## Purpose of playbooks in demand management

Playbooks provide a structured way to manage work by guiding teams through predefined steps. They show what to do, when to do it, and where to find the tools or information required to complete each task. You can apply a playbook to processes such as managing a demand, resolving an issue, launching a product, onboarding new employees, or defining key steps of a process. You can also have different playbooks for different governance processes, such as IT and marketing. The stages and activities required for an IT demand may not be the same as those required for marketing demands. In such cases, with the relevant playbook, users can see and interact with only those stages and activities that are relevant for their processes. For more information on playbooks, see [Workflow Studio playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio-playbooks-landing.md).

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

For example, a demand about a customer self‑service portal enhancement uses a playbook to guide its progress as follows:

-   The ideation stage prompts the demand manager to capture objectives and benefits.
-   The assessment stage guides effort, cost, and risk evaluation.
-   Prioritization helps validate scoring and funding.
-   Planning finalizes the scope and links the demand to a potential work entity.

As each stage is completed, the playbook helps verify that the demand follows the standard life cycle without missing any required steps.

## Playbook benefits

Playbooks add value to demand management in the following ways:

-   Standardizing demand intake: Establishing that required information is captured early.
-   Providing step-by-step instructions: Guiding new demand managers or occasional users.
-   Supporting governance: Providing stage gating for evaluation and approval.
-   Improving visibility: Showing exactly where a demand sits in the life cycle and what is blocking its progress.
-   Integrating workflows: Using Flow Designer to set up different business logic for each playbook flow.

## Demand workflow playbook

Next Experience for Demand Management includes a predefined playbook, Demand workflow, available on the **Playbooks** tab in Workflow Studio. The playbook is active by default and is ready to use without any additional configuration. You can customize this playbook by duplicating it or create one for your organization's specific demand workflows.

In Next Experience for Demand Management, the default demand workflow playbook is triggered by record creation. When triggered, a playbook is associated with the demand, and the Playbook page appears in the navigation menu of a demand.

The default playbook works as follows:

-   The playbook runs when a demand is created. It has no additional conditions, so it applies to every new demand, including records in tables that extend the Demand \[dmn\_demand\] table.
-   A stage appears only if at least one of its activities is available for the demand.
-   The AI checkpoint stage, where you associate AI systems with the demand, appears only when the AI Control Tower Core plugin \(com.sn.ai\_governance\) is installed.

For more information on the stages and activities in the default playbook, see [Demand workflow playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/demand-default-playbook-stages.md).

\[Omitted image "demand-playbook.png"\] Alt text: Stages and activities of the default demand playbook

**Note:** More than one playbook can be applicable for a demand based on the trigger conditions. In this scenario, these playbooks are displayed one after another. You can also nest one playbook within another. For more information, see [Nested Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/nested-playbooks.md).

## Activities for demand playbooks

Demand playbooks commonly use the following platform activities and demand-specific custom activities. The examples come from a playbook for IT investment governance. For the complete example, see [Creation example for a demand playbook for IT governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/example-it-investment-governance-playbook.md).

|Activity|Use it to|Example|
|--------|---------|-------|
|Record Form|Display fields of the demand for users to fill in.|A Capture business case activity displays the business case, financial benefit, and planned dates of the demand.|
|New Record Form|Create a related record that is linked to the demand.|An Add a benefit plan activity creates a benefit plan for the demand.|
|Instruction|Display a message that guides users, for example to another tab of the demand.|A Request resources activity sends users to the **Resources** tab to create resource assignments.|
|Update Record|Update a field of the demand automatically, such as its state, without user input.|A Submit for architecture review activity moves the demand to Screening.|
|Ask For Ad Hoc Approval|Request an approval from a user or a group.|An Investment approval activity asks the CIO to approve or reject the investment.|
|Demand State Transition Checker|Check the conditions for a state change before an Update Record activity changes the state.|See [Transition checker to move a demand to the next state automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/playbooks-in-demand-workspace.md).|
|Demand Related List|Display a related list of the demand so that users can add or remove related records.|See [Show the related lists of a demand in an activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/playbooks-in-demand-workspace.md).|
|Check if plugin is active|Check whether a plugin is installed, so that a stage or activity appears only when it is.|See [Show a stage only when a plugin is installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/playbooks-in-demand-workspace.md).|

## Demand components for custom playbooks

The demand workflow playbook uses custom actions, a custom activity, and a playbook experience that are built for demands. If you customize the demand workflow playbook or create a playbook for demands, reuse these components so that your playbook works the same way as the default one.

The examples in this section follow the IT investment governance playbook. Business teams submit demands for new technology, and the playbook runs only for demands where the category is Strategic and the type is Project. For the complete example, see [Creation example for a demand playbook for IT governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/example-it-investment-governance-playbook.md).

## Transition checker to move a demand to the next state automatically

Use the Demand State Transition Checker custom activity to validate the demand before moving it to the next state after users finish a stage. The automated activity at the end of a stage in the demand workflow playbook uses this action. For example, when you complete all the activities in the Create demand brief stage, the playbook moves the demand from Draft to Submitted.

When users complete all the activities in the stage, the playbook moves the demand to Screening. Before it changes the state, the playbook checks the same conditions that apply when you change the state of a demand manually. If a condition is not met, the state does not change. For example, the demand is already in a later state. For example, if a demand was moved to Approved outside the playbook, completing the Create demand brief stage does not move it back to Submitted.

The conditions for each state change are defined in the `DemandPlaybookUtils` script include that the action uses. If you use custom states or roles, update this script include. For example, if your governance process requires an Architecture review state that only users with an enterprise architect role can complete, add the state and role to `DemandPlaybookUtils`. If you must make many changes, create your own action instead of changing the predefined one. For more information, see [Building actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/actions.md).

## Show the related lists of a demand in an activity

Use the Demand Related List custom activity when you want users to add or remove related records, such as goals or cost plans, without leaving the playbook. The demand playbook experience includes an activity override that displays a related list of the demand in the playbook. In the demand workflow playbook, activities such as Add secondary goals and Estimate financial cost use it.

For example, to let the demand manager add investment goals during the Intake stage, add an Add investment goals activity. Use the Demand Related List activity definition. Set the activity to start after the Capture business case activity. Verify that the playbook uses the Demand Playbook Experience. For more information, see [Demand playbook experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/playbooks-in-demand-workspace.md).

Users see the goals of the demand as a list in the activity. They select **New** to add a goal, **Delete** to remove one, or a goal in the list to view its details. For more information, see [Activity definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/activity-definitions.md).

## Show a stage only when a plugin is installed

Use the Check if plugin is active custom activity when a stage applies only to instances where a specific plugin is installed. The activity checks whether a plugin ID is active. In the demand workflow playbook, this activity controls the AI checkpoint stage, which appears only when the AI Control Tower Core plugin \(com.sn.ai\_governance\) is installed.

For example, you want to show a Security review stage in your investment governance playbook only when a security plugin is installed. To achieve this, add this activity as the first activity in this stage. Enter the plugin ID in the activity. Set the other activities in the stage to run only when the activity finds that the plugin is active.

A stage appears only if at least one of its activities is available.

## Demand playbook experience

The Demand Playbook Experience controls what users see in the playbook and which activities they can select. It does not change the stages, activities, or logic of the playbook. It provides the following demand-specific customizations:

-   Activity overrides and customizations to existing actions.
-   Activities display the **Mark Complete**, **Save**, and **Skip** actions.

These customizations are available only when the playbook uses the Demand Playbook Experience. If the playbook opens with a different experience, such as the global playbook experience, activities display the default platform lists and declarative actions. For example, the Add investment goals activity in your investment governance playbook would not display the declarative action buttons.

If you create or customize a playbook for demands:

1.  Add any activity overrides to the Demand Playbook Experience.
2.  When you test the playbook, select Demand Playbook Experience as the experience, and verify that the related lists and actions appear as they will for users.

**Related topics**  


[Workflow Studio Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio-playbooks-landing.md)

[Building Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/building-a-process.md)

[Designing Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-experience-admins.md)

[Use playbook for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/use-playbooks-in-dw.md)

[Demand workflow playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/demand-default-playbook-stages.md)

[Customize and create playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/playbooks-configuration-for-dmnd-wpc.md)

[Creation example for a demand playbook for IT governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/example-it-investment-governance-playbook.md)

