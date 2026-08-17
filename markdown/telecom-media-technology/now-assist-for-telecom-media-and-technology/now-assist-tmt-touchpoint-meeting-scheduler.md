---
title: ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) draft and schedule touchpoint meetings agentic workflow
description: Use the Draft and schedule touchpoint meetings agentic workflow to schedule and edit a touchpoint meeting for a specific user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-touchpoint-meeting-scheduler.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer Success Management, Use agentic workflows, ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) draft and schedule touchpoint meetings agentic workflow

Use the Draft and schedule touchpoint meetings agentic workflow to schedule and edit a touchpoint meeting for a specific user.

## Draft and schedule touchpoint meetings agentic workflow overview

The agentic workflow enables customer success agents to optimize meeting schedules within the customer success workflow by creating and managing meetings. It create and manage meetings based on key details such as invitees, agenda, meeting type, and scheduling preferences. With this agentic workflow, customer success managers can:

-   Take timely and contextual action.
-   Create a meeting with all required details.
-   Schedule draft meetings without manual coordination.

The meeting AI plugin \(app-meeting-ai-ag\) installs automatically with the Customer Success AI agent.

**Important:** In the Now Assist skills page, make sure to Activate the meeting proposal generator skill to trigger the agentic workflow. See [Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-skill.md) for more details.

When the risk record's probability is very high or occurred, the customer success agent assigned to that risk receives a Now Assist panel notification. The agentic workflow automates the creation and scheduling of the meeting.

The Meeting AI plugin supports these tables:

-   Touchpoint \(sn\_acct\_lc\_touchpoint\)
-   Account Onboarding Case \(sn\_acct\_lc\_onb\_case\)
-   Engagement \(sn\_acct\_lc\_engagement\)
-   Customer Account \(customer\_account\)
-   Risk Signal and Issue \(sn\_acct\_lc\_risk\_signal\_issue\)

**Note:** To create the meeting AI plugin extensible to other business units, see [KB3119608](https://support.servicenow.com/kb?sys_kb_id=696e678cc37d8fd4a9ea601bb0013170&id=kb_article_view).

To modify the Draft and schedule touchpoint meetings agentic workflow [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Note:** You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md).

## Role masking

Required role: sn\_acct\_lc.customer\_success\_agent

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

## Draft and schedule touchpoint meetings agentic workflow

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
2.  Select **Draft and schedule touchpoint meetings**.

To create an agentic workflow, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md).

## Testing the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Test AI reasoning**.

To test the use case, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

## AI agents used in the Draft and schedule touchpoint meetings agentic workflow

The following AI agents are used to execute the instructions for the agentic workflow.

To create an AI agent, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md).

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
</table>