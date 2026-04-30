---
title: Generate regulatory action plans
description: Generate regulatory action plans by using the generate regulatory action plan agentic workflow in the Now Assist panel. This agentic workflow analyzes impacted areas and similar historical alerts to create change tasks and action tasks that help implement regulatory change.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-10-15"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Agentic workflows, Use agentic AI, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Generate regulatory action plans

Generate regulatory action plans by using the generate regulatory action plan agentic workflow in the Now Assist panel. This agentic workflow analyzes impacted areas and similar historical alerts to create change tasks and action tasks that help implement regulatory change.

## Before you begin

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Role required: sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user

Impacted areas must be associated with the regulatory alert. If no impacted areas are associated with the alert, the workflow returns a validation message and no tasks are created. For more information on adding impacted areas, see [Add impacted areas manually to a regulatory alert](add-impacted-area-reg-alert.md).

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## About this task

The generate regulatory action plan agentic workflow helps regulatory change management professionals create structured action plans for alerts in the New or In Progress state. The workflow analyzes impacted areas identified on the alert and references similar historical alerts to generate change tasks and action tasks. These tasks are grouped by type such as control update, citation amendment, and policy revision, and appear in the **Regulatory tasks** tab. You can accept or dismiss the proposed plan, and only tasks in the New state can be deleted manually.

**Note:**

When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly. To modify this workflow, duplicate it and adjust the settings according to your requirements. You can activate the workflow template by making the triggers active and setting the display settings to include the Now Assist panel. For more information, see [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Compliance Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Regulatory alerts**.
    -   **Workspaces** &gt; **Compliance Workspace** select the Regulatory Change Management dashboard icon ![](../../grc-rcm/image/reg-change-icon.png) and then in the Activity overview, Tracking, or Trends section, select any segment or value in an Alerts related widget to open the list of regulatory alerts with that state.
2.  Select any regulatory alert in the New or In Progress state.

3.  Initiate the generate regulatory action plan agentic workflow by selecting one of the following:

    -   Open the Now Assist panel by selecting the Now Assist panel icon \(![](../../grc-common/image/nap-icon.png) and then select **Generate regulatory action plans**.
    -   Select **Ask NowAssist** and then **Generate action plan**.
    The Now Assist panel icon is available to select anywhere in the Compliance Workspace.

    The **Ask NowAssist** action menu is available when you are on a regulatory alert page.

4.  Review the proposed action plan and choose whether to accept or dismiss it.

<table id="choicetable_action_plan_options"><thead><tr><th align="left" id="d82229e238">

Option

</th><th align="left" id="d82229e241">

Description

</th></tr></thead><tbody><tr><td id="d82229e247">

**Accept action plan**

</td><td>

After initiating the generate regulatory action plan agentic workflow, it creates structured change tasks and action tasks based on the impacted areas identified in the alert and patterns from similar historical alerts.![Details on initiating the get regulatory alerts workflow in the Now Assist panel.](../image/generate-regulatory-action-plan.png)

 On the Now Assist panel, ask the agent to create regulatory change and action task records by selecting `Yes`.

![Details on the get regulatory alerts workflow outcome in the Now Assist panel.](../image/generate-regulatory-action-plan-2.png)

**Note:**

-   Each generated task is grouped by regulatory alert type such as control, citation, policy, and all tasks appear in the **Regulatory tasks** tab.
-   The "other" type is used to capture non-standard or cross-functional activities that don’t directly map to impacted areas such as citations, control objectives, controls, or policies. These tasks are typically broader in scope and can apply to the entire regulatory alert rather than specific impacted elements.


</td></tr><tr><td id="d82229e297">

**Dismiss action plan**

</td><td>

In the Now Assist panel, ask the agent to dismiss the regulatory change and action task record creation by entering `No`.

 ![Details on the get regulatory alerts workflow dismissal in the Now Assist panel.](../image/generate-regulatory-action-plan-3.png)

 **Note:**

-   No tasks are created.
-   You can navigate to the **Regulatory tasks** tab and manually create change tasks and action tasks.


</td></tr></tbody>
</table>    In the Now Assist panel, the agent receives a notification when the interaction is generated, enabling your users to follow the on-screen instructions and complete the task.

    **Important:** Be sure to check AI-generated plans and task records for accuracy.


## What to do next

Navigate to the **Regulatory tasks** tab to review, assign, or delete the generated tasks. You can manage all tasks created by the workflow from this tab. Only change and action tasks in the New state can be deleted manually from a regulatory alert. You can assign tasks to users and update task details for tasks in the New and In Progress state.

For more information on tasks, see [Regulatory change tasks](../../grc-rcm/concept/regulatory-change-tasks.md) and [Action tasks in Regulatory Change Management](../../grc-rcm/concept/action-tasks.md).

**Related topics**  


[Using agentic workflows in Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/concept/using-agentic-ai-workflows.md)

[Activate the generate regulatory action plan agentic workflow](activate-rcm-agent-actions-workflow.md)

[Add impacted areas manually to a regulatory alert](add-impacted-area-reg-alert.md)

[Accept or dismiss recommendations for regulatory alert impacted citations](manage-recommendation-reg-alert.md)

