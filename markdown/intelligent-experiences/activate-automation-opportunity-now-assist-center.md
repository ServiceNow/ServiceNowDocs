---
title: Implement an automation opportunity from Now Assist Center
description: Deploy a matched AI agent or a new agent to automate a resolution for an identified automation opportunity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/activate-automation-opportunity-now-assist-center.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
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

2.  In the Automation opportunitiessection of the home page or in the automation opportunities list tab, select an automation opportunity to view its details.

    The Resolution Steps tab opens showing the opportunity details.

    The page displays summary information for the opportunity, a **Resolution steps**tab with editable implementation steps, and an **Example records**tab with example records from the data source.It also displays an **AI Agents** tab showing the agents created from the automation opportunity.

    \[Omitted image "now-assist-center-agent-advisor-opportunity-detail-3.png"\] Alt text: Resolution Steps tab showing the opportunity details.

    For more information on finding an automation opportunity, see [View your automation opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-center-view-automation-opportunities.md).

3.  Select the **Example Records** tab to review records from the source table.

    Select a record number to open the record and view its details.

4.  Select the **AI Agents** tab to view AI agents created from the automation opportunity.

5.  In the **Resolution Steps** tab, review the steps for accuracy and completeness in planning your AI agent.

    The **Resolution Steps** tab shows the implementation steps and the matched AI agents for each step.

6.  Adjust the steps as needed.

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

1.  Select the **Edit** icon \(\[Omitted image "icon-now-assist-center-edit.png"\] Alt text: Edit icon.\).
2.  Change the text as needed and select **Save**.


</td></tr><tr><td>

Delete a step

</td><td>

1.  1. Select the **Delete** icon \(\[Omitted image "icon-now-assist-center-delete.png"\] Alt text:\).
2.  2. Select **Delete** to confirm.


</td></tr><tr><td>

Reorder steps

</td><td>

Select the **Up** icon \(\[Omitted image "icon-now-assist-center-up.png"\] Alt text: Up icon.\) or **Down** icon \(\[Omitted image "icon-now-assist-center-down.png"\] Alt text: Down icon.\) to move the step in the list.

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
</table>7.  When the steps are ready to implement, select **Continue in AI Agent Studio**.

    The Continue building AI agent box opens.

    \[Omitted image "now-assist-center-agent-advisor-build-agent-2.png"\] Alt text: Continue building AI agent box showing steps for building an agent.

8.  Choose whether the AI agent will communicate as a **Chat Agent** or **Voice Agent**.

9.  Select **Continue in AI Agent Studio**.

    The Agent guided setup tab opens.

    \[Omitted image "now-assist-center-agent-advisor-opportunity-agent-setup-define.png"\] Alt text: Guided setup of the AI agent.

10. Complete the development of the new agentin the Agent guided setup tab using AI Agent Studio capabilities.

    The resolution steps are mapped to the set of instructions and added as tools for the new AI agent.

    For more information, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md).


**Parent Topic:**[Using AI Agent Advisor in Now Assist Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-center-using-ai-agent-advisor.md)

**Related topics**  


[View your automation opportunities]()

[Edit an AI agent from an automation opportunity]()

