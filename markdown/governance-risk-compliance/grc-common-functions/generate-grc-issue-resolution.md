---
title: Optimize a GRC issue resolution
description: Optimize a GRC issue resolution plan by using the Optimize GRC issue resolution agentic workflow in the Now Assist panel. This agentic workflow generates an action plan for the issue and suggests remediation tasks to resolve the issue.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Agentic workflows, Use agentic AI, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Optimize a GRC issue resolution

Optimize a GRC issue resolution plan by using the Optimize GRC issue resolution agentic workflow in the Now Assist panel. This agentic workflow generates an action plan for the issue and suggests remediation tasks to resolve the issue.

## Before you begin

Role required: sn\_grc\_genai.issue\_user or sn\_irm\_gen\_ai.user

## About this task

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

To modify the Optimize GRC issue resolution workflow [duplicate it](https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-ai-agents/task/clone-aia-usecase.html), and adjust the settings according to your requirements. You can activate the workflow template by making the triggers active and setting the display settings to include the Now Assist panel.

## Procedure

1.  Navigate to Risk Workspace and select any issue in the Analyze state.

2.  Open the issue that you want to resolve by using the agentic workflow.

3.  Select the Now Assist \(![Now Assist panel icon.](../image/nap-icon.png)\) icon.

    The Now Assist panel is displayed.

4.  Resolve the GRC issue by generating an issue action plan and generating recommended remediation tasks.

<table id="table_apz_1dc_w2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Issue action plan AI agent

</td><td>

On the Now Assist panel, ask the agent to optimize the GRC issue resolution workflow in natural language by entering `Generate action plan` or selecting **Generate GRC issue resolution**.**Note:**

-   If you provide an issue number, such as `Generate action plan for the issue: IPT0020240`, the workflow acts on the suggested issue and generates an action plan that is based on previous similar issues.
-   You can generate an action plan for any issue from the Now Assist panel by providing the suggested issue number.
-   You can accept the action plan.
-   You can edit the generated action plan by providing inputs like `Delete 1, 2`, `Add <text>`, or `Combine 1,4`.
-   You can discard the generated action plan and instead create an action plan manually.


</td></tr><tr><td>

Remediation tasks AI agent

</td><td>

If you accept the action plan, the Now Assist virtual agent can suggest remediation tasks, You can do one of the following actions:-   Accept the remediation tasks.

**Note:** Check for duplicate remediation tasks.

-   Edit the suggestions. Provide inputs like `Delete 1, 2`, `Add <text>`, or `Merge 1,4`. You can update the recommended remediation tasks.
-   Discard the recommendations and create remediation tasks manually.


</td></tr></tbody>
</table>    ![Now Assist panel for issue resolution.](../image/nap-issue-resolution.png)

    In the Now Assist panel, the agent receives a notification when the interaction is generated, enabling your users to follow the on-screen instructions and complete the task.


