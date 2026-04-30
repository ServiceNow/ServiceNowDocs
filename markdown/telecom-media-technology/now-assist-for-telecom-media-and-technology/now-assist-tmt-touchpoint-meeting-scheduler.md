---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection trigger risk mitigation touchpoint
description: Use the Trigger risk mitigation touchpoint agentic workflow to schedule and edit a touchpoint meeting for a specific user.
locale: en-US
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Customer Success Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection trigger risk mitigation touchpoint

Use the Trigger risk mitigation touchpoint agentic workflow to schedule and edit a touchpoint meeting for a specific user.

## Trigger risk mitigation touchpoint agentic workflow overview

The agentic workflow enables customer success agents to optimize meeting schedules within the customer success workflow by creating and managing meetings. It create and manage meetings based on key details such as invitees, agenda, meeting type, and scheduling preferences. With this agentic workflow, customer success managers can:

-   Take timely and contextual action.
-   Create a meeting with all required details.
-   Schedule draft meetings without manual coordination.

In the Trigger risk mitigation touchpoint agentic workflow, when the risk record's probability is very high or occurred, the customer success agent is assigned to that risk receives a Now Assist panel notification. From the risk record, the agentic workflow automates the creation of meeting and schedules the meeting.

To modify the Trigger risk mitigation touchpoint agentic workflow [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Note:** You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Role masking

Required role: sn\_acct\_lc.customer\_success\_agent

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Trigger risk mitigation touchpoint agentic workflow

This workflow does the following:

**Note:** Before running the workflow, you must configure the generic prompt as follows:

1.  Navigate to the OneExtend Capability \(sys\_one\_extend\_capability\) table by entering `sys_one_extend_capability.list` in the navigator.
2.  Search for `generic prompt` and open the record.
3.  In OneExtend Capability Attributes related list, set the **Default** to **True** for any of these definitions:
    -   Generic Prompt \(Azure OpenAI Chat\)
    -   Generic Prompt \(Now LLM Service\)
    -   Generic Prompt Vertex AI \(Google Cloud Chat Completion\)
    -   Generic Prompt \(Amazon Bedrock Chat Completions\)

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Trigger risk mitigation touchpoint**.

To create an agentic workflow, see [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Testing the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Test AI reasoning**.

To test the use case, see [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## AI agents used in the Trigger risk mitigation touchpoint agentic workflow

The following AI agents are used to execute the instructions for the agentic workflow.

To create an AI agent, see [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

<table id="table_wxl_gns_fgc"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Meeting draft creator AI agent

</td><td>

AI agent automates draft creation of meetings using context and history of the risk record.**Note:** The AI agent creates meeting inside a touchpoint.

</td></tr><tr><td>

Draft meeting scheduler AI agent

</td><td>

AI agent automates virtual meeting scheduling by collecting invite and details provided from the customer success agent.

</td></tr></tbody>
</table>**Parent Topic:**[Customer Success Management agentic workflows](now-assist-tmt-health-risk.md)

