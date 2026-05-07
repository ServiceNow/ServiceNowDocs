---
title: Implement an automation opportunity from Now Assist Center
description: Deploy a matched AI agent or a new agent to automate a resolution for an identified automation opportunity.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Now Assist Center, Gen AI, Generative AI]
breadcrumb: [Using AI Agent Advisor in Now Assist Center, Use, Now Assist Center, Enable AI experiences]
---

# Implement an automation opportunity from Now Assist Center

Deploy a matched AI agent or a new agent to automate a resolution for an identified automation opportunity.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to implement an automation opportunity with AI Agent Advisor.

Each automation opportunity includes a set of recommended resolution steps that describe how to automate the identified opportunity. AI Agent Advisor also maps each resolution step to an existing AI agent on your platform when a match is available. Review the details of an opportunity before deciding whether to deploy an agent for it.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Center** or **Workspaces** &gt; **Now Assist Center**.

2.  In the AI Agent Advisor section of the home page or in the automation opportunities tab, select an automation opportunity to view its details.

    The Resolution Steps tab opens showing the opportunity details. The page displays summary information for the opportunity, a **Resolution Steps** tab with editable implementation steps, and an **Example Records** tab with example records from the data source.

    ![Resolution Steps tab showing the opportunity details.](../image/now-assist-center-agent-advisor-opportunity-detail-2.png "Opportunity details page")

    For more information on finding an automation opportunity, see [View your automation opportunities](now-assist-center-view-automation-opportunities.md).

3.  Select the **Example Records** tab to review records from the source table.

    Select a record number to open the record and view its details.

4.  In the **Resolution Steps** tab, review the steps for accuracy and completeness in planning your AI agent.

    The **Resolution Steps** tab shows the implementation steps and the matched AI agents for each step.

5.  Adjust the steps as needed.

<table id="table_aj1_mrr_v3c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add a step

</td><td>

1.  Select **Add new step** under the steps.
2.  Enter the text and select **Save**.


</td></tr><tr><td>

Edit a step

</td><td>

1.  Select the **Edit** icon \(![Edit icon.](../image/icon-now-assist-center-edit.png)\).
2.  Change the text as needed and select **Save**.


</td></tr><tr><td>

Delete a step

</td><td>

1.  1. Select the **Delete** icon \(![](../image/icon-now-assist-center-delete.png)\).
2.  2. Select **Delete** to confirm.


</td></tr><tr><td>

Reorder steps

</td><td>

Select the **Up** icon \(![Up icon.](../image/icon-now-assist-center-up.png)\) or **Down** icon \(![Down icon.](../image/icon-now-assist-center-down.png)\) to move the step in the list.

</td></tr><tr><td>

Restore all

</td><td>

Select **Revert all** to restore the original steps before changes.

</td></tr><tr><td>

Expand all

</td><td>

Select **Expand all** to see the available assets for each step.

 In each applicable step, the description provides the tool name, context, confidence level, and rationale for matching the asset to the step.

 Select **Collapse all** to hide the details.

</td></tr></tbody>
</table>6.  When the steps are ready to implement, select **Continue in AI Agent Studio**.

    The Continue building AI agent box opens.

    ![Continue building AI agent box showing steps for building an agent.](../image/now-assist-center-agent-advisor-build-agent.png "Continue building AI agent box")

7.  Select **Continue in AI Agent Studio**.

8.  Complete the development of the new agent in AI Agent Studio.

    The resolution steps are mapped to the set of instructions and added as tools for the new AI agent.

    For more information, see [Create an AI agent](../../now-assist-ai-agents/task/configure-next-best-action-agent.md).


**Parent Topic:**[Using AI Agent Advisor in Now Assist Center](../concept/now-assist-center-using-ai-agent-advisor.md)

**Related topics**  


[View your automation opportunities](now-assist-center-view-automation-opportunities.md)

