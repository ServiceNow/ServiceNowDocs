---
title: Generate regulatory action plans
description: Generate regulatory action plans by using the generate regulatory action plan agentic workflow in the Now Assist panel. This agentic workflow analyzes impacted areas and similar historical alerts to create change tasks and action tasks that help implement regulatory change.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/generate\_regulatory\_action\_plans.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Agentic workflows in Risk &amp; Sustainability, Use agentic AI, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Generate regulatory action plans

Generate regulatory action plans by using the generate regulatory action plan agentic workflow in the Now Assist panel. This agentic workflow analyzes impacted areas and similar historical alerts to create change tasks and action tasks that help implement regulatory change.

## Before you begin

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user

Impacted areas must be associated with the regulatory alert. If no impacted areas are associated with the alert, the workflow returns a validation message and no tasks are created. For more information on adding impacted areas, see [Add impacted areas manually to a regulatory alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-impacted-area-reg-alert.md).

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

## About this task

The generate regulatory action plan agentic workflow helps regulatory change management professionals create structured action plans for alerts in the New or In Progress state. The workflow analyzes impacted areas identified on the alert and references similar historical alerts to generate change tasks and action tasks. These tasks are grouped by type such as control update, citation amendment, and policy revision, and appear in the **Regulatory tasks** tab. You can accept or dismiss the proposed plan, and only tasks in the New state can be deleted manually.

**Note:**

When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly. To modify this workflow, duplicate it and adjust the settings according to your requirements. You can activate the workflow template by making the triggers active and setting the display settings to include the Now Assist panel. For more information, see [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md).

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Compliance Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Regulatory alerts**.
    -   **Workspaces** &gt; **Compliance Workspace** select the Regulatory Change Management dashboard icon \[Omitted image "reg-change-icon.png"\] Alt text: and then in the Activity overview, Tracking, or Trends section, select any segment or value in an Alerts related widget to open the list of regulatory alerts with that state.
2.  Select any regulatory alert in the New or In Progress state.

3.  Initiate the generate regulatory action plan agentic workflow by selecting one of the following:

    -   Open the Now Assist panel by selecting the Now Assist panel icon \(\[Omitted image "nap-icon.png"\] Alt text: and then select **Generate regulatory action plans**.
    -   Select **Ask NowAssist** and then **Generate action plan**.
    The Now Assist panel icon is available to select anywhere in the Compliance Workspace.

    The **Ask NowAssist** action menu is available when you are on a regulatory alert page.

4.  Review the proposed action plan and choose whether to accept or dismiss it.

<table id="choicetable_action_plan_options"><thead><tr><th align="left" id="d91731e242">

Option

</th><th align="left" id="d91731e245">

Description

</th></tr></thead><tbody><tr><td id="d91731e251">

**Accept action plan**

</td><td>

After initiating the generate regulatory action plan agentic workflow, it creates structured change tasks and action tasks based on the impacted areas identified in the alert and patterns from similar historical alerts.\[Omitted image "generate-regulatory-action-plan.png"\] Alt text: Details on initiating the get regulatory alerts workflow in the Now Assist panel.

 On the Now Assist panel, ask the agent to create regulatory change and action task records by selecting `Yes`.

\[Omitted image "generate-regulatory-action-plan-2.png"\] Alt text: Details on the get regulatory alerts workflow outcome in the Now Assist panel.

**Note:**

-   Each generated task is grouped by regulatory alert type such as control, citation, policy, and all tasks appear in the **Regulatory tasks** tab.
-   The "other" type is used to capture non-standard or cross-functional activities that don’t directly map to impacted areas such as citations, control objectives, controls, or policies. These tasks are typically broader in scope and can apply to the entire regulatory alert rather than specific impacted elements.


</td></tr><tr><td id="d91731e301">

**Dismiss action plan**

</td><td>

In the Now Assist panel, ask the agent to dismiss the regulatory change and action task record creation by entering `No`.

 \[Omitted image "generate-regulatory-action-plan-3.png"\] Alt text: Details on the get regulatory alerts workflow dismissal in the Now Assist panel.

 **Note:**

-   No tasks are created.
-   You can navigate to the **Regulatory tasks** tab and manually create change tasks and action tasks.


</td></tr></tbody>
</table>    In the Now Assist panel, the agent receives a notification when the interaction is generated, enabling your users to follow the on-screen instructions and complete the task.

    **Important:** Be sure to check AI-generated plans and task records for accuracy.


## What to do next

Navigate to the **Regulatory tasks** tab to review, assign, or delete the generated tasks. You can manage all tasks created by the workflow from this tab. Only change and action tasks in the New state can be deleted manually from a regulatory alert. You can assign tasks to users and update task details for tasks in the New and In Progress state.

For more information on tasks, see [Regulatory change tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/regulatory-change-tasks.md) and [Action tasks in Regulatory Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/action-tasks.md).

**Related topics**  


[Using agentic workflows in IRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/using-agentic-ai-workflows.md)

[Activate the generate regulatory action plan agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/activate-rcm-agent-actions-workflow.md)

[Add impacted areas manually to a regulatory alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-impacted-area-reg-alert.md)

[Accept or dismiss recommendations for regulatory alert impacted citations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/manage-recommendation-reg-alert.md)

