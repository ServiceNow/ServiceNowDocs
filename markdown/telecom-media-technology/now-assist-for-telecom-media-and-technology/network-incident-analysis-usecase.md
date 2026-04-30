---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection analyze network incidents agentic workflow
description: Use the Analyze network incidents agentic workflow to resolve incidents, helping customer agents to resolve network tickets by tracking them and creating an actionable task.
locale: en-US
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Customer Service Problem Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection analyze network incidents agentic workflow

Use the Analyze network incidents agentic workflow to resolve incidents, helping customer agents to resolve network tickets by tracking them and creating an actionable task.

## Analyze network incidents agentic workflow overview

Resolve the customer issues using a team of AI agents in the Analyze network incidents agentic workflow. It assists the customer agents in resolving a given incident.

Role required: sn\_tmt\_agentic\_ai.sn\_noc\_incident\_user

To modify the Analyze network incidents agentic workflow, [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Note:** You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Role masking

Required role: sn\_tmt\_agentic\_ai.sn\_noc\_incident\_user

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Application dependency

The Analyze network incidents agentic workflow has the following plugin dependencies:

-   Customer service with service management \(sn\_cs\_sm\)
-   Customer service \(sn\_customerservice\)
-   Customer service problem management
-   Telecommunications alarm management open API \(sn\_ind\_tmf642\)
-   Field service management for telecommunications \(sn\_fsmt\)
-   Major issue management

## Analyze network incidents agentic workflow

To access the use case:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Analyze network incidents**.

To create a new use case, see [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Testing the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Test use cases**.

To test the use case, see [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## AI agents used in the Analyze network incidents agentic workflow

The following AI agents are used to execute the instructions for the agentic workflow.

To create an AI agent, see [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

<table id="table_bjk_z5c_s2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Network ticket resolution AI agent

</td><td>

AI agent capable of providing overall incident and alert summary. It’s also capable of searching the knowledge base for relevant articles to provide resolutions if available.

</td></tr><tr><td>

Ticket readiness AI agent

</td><td>

AI agent capable of predicting the incident fields like category, subcategory, priority, description, short description, and estimated time to resolve the incident using GAF on historic incident data.

 To activate the GAF, see [Activate Group Action Framework for Now Assist for Telecommunications, Media and Technology \(TMT\)](../task/activate-group-action-framework.md).

</td></tr><tr><td>

Network correlation monitor AI agent

</td><td>

AI agent capable of identifying the impacted accounts and services and correlating cases opened in the last 15 minutes that could be impacted because of the incident, provide the list to the customers for review, and associate it to the incident.It’s also capable of notifying customers about the outages based on human confirmation by creating service problem cases and linking child cases if any.

</td></tr><tr><td>

Network ticket actionable steps generation AI agent

</td><td>

AI agent capable of generating actionable resolution steps for incoming incident using the Group Action Framework \(GAF\) and modifies the steps according to the human feedback.

 To activate the GAF, see [Activate Group Action Framework for Now Assist for Telecommunications, Media and Technology \(TMT\)](../task/activate-group-action-framework.md).

</td></tr><tr><td>

Network remediation generation AI agent

</td><td>

AI agent capable of consuming resolution steps for an incident and converting them to one of the following task types:-   Incident Task
-   Work Order
-   Change Request

</td></tr></tbody>
</table>