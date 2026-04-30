---
title: AI capabilities for enhancing custom applications
description: Learn about the AI capabilities available with Now Assist for App Engine that you can use to enhance custom applications, including skills, AI agents, and agentic workflows.
locale: en-US
release: zurich
product: Now Assist for App Engine
classification: now-assist-for-app-engine
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, AI capability, AI feature, AI product, AI agent, skill, generative AI, genAI, Now Assist for App Engine, App Engine, custom app]
breadcrumb: [Explore, Now Assist for App Engine, AI in custom applications, Developing your application, Building applications]
---

# AI capabilities for enhancing custom applications

Learn about the AI capabilities available with Now Assist for App Engine that you can use to enhance custom applications, including skills, AI agents, and agentic workflows.

There are several types of AI capabilities that you can add to custom applications with Now Assist for App Engine:

-   Skills
-   AI agents
-   Agentic workflows

The following sections describe what each capability is and how you can use it to enhance a custom application. To learn about which AI capability might be best for your custom application use case, see [Choosing the right AI capability](choosing-the-right-ai-capability.md).

## Skills

On the ServiceNow AI Platform, a skill is a generative AI capability that contains instruction on how to complete a specific task for a use case, such as generating a summary.

There are several important components of a skill.

-   The input is the data that the skill analyzes to generate an output. Typically on the ServiceNow AI Platform, inputs are records in tables.
-   The prompt is the instruction to the underlying large language model \(LLM\) that tells the skill what to do with the input. Prompts define the task, tone, and structure of the output.
-   The output is the generated response from the LLM based on the prompt and input. Outputs can be plain text, structured data, or even formatted responses depending on how the skill is configured.

Skills also contain activation methods, which define how the skill can be accessed on the ServiceNow AI Platform. Skills can be called conversationally in the Now Assist panel, through UI actions such as buttons, and through conversations with Virtual Agent. To learn more about activating skills, see [Activate a skill](https://www.servicenow.com/docs/access?context=activate-skill&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Note:** Some skills might need to be reviewed and approved by a data steward before you can activate them.

## Now Assist Platform skills and custom skills

With Now Assist for App Engine, you have access to several kinds of skills: Now Assist Platform skills and custom skills. While both are able to be used in custom applications, the following table provides more information about each skill type and the ease of using the skill in custom applications.

<table id="table_o3m_tn4_xgc"><thead><tr><th>

Skill type

</th><th>

Description

</th><th>

Ease of use in custom applications

</th><th>

More information

</th></tr></thead><tbody><tr><td>

Now Assist Platform skills

</td><td>

Preconfigured skills that are designed for existing use cases,such as document extraction and dashboard and visualization export

</td><td>

Must be duplicated and reconfigured significantly for use within custom apps

</td><td>

[Now Assist skills in the Platform workflow](https://www.servicenow.com/docs/access?context=now-assist-on-now-platform&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

</td></tr><tr><td>

Custom skills

</td><td>

Skills that you create custom for your use case with Now Assist Skill Kit

</td><td>

Can be designed to work within custom apps during the creation process, when you define the skill inputs and outputs

</td><td>

-   [General guidelines for Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=na-skill-kit-guidelines&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
-   [Create a skill](https://www.servicenow.com/docs/access?context=create-new-skill&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

</td></tr></tbody>
</table>## Now Assist for App Engine custom app record summarization skill

Starting with version 28.2.4 of Now Assist for App Engine, you can also use the custom app record summarization skill, which is a template skill available with Now Assist for App Engine. The skill enables you to generate AI summaries of records within custom apps and tables. You can configure the skill to summarize the tables and fields that you need, and you can choose how your app users interact with the skill through in-product UI or conversation in the Now Assist panel. For more information about the custom app record summarization skill, see [Custom app record summarization skill](custom-app-record-summarization-na-for-app-engine.md).

## AI agents

An AI agent is a generative AI capability that contains a set of large language model \(LLM\) instructions with the tools to perform specific tasks. On the ServiceNow AI Platform, AI agents are often part of agentic workflows and can be orchestrated to perform complex tasks. More information about agentic workflows is included in the following section.

There are several important components of an AI agent.

-   The AI Agent role defines the capabilities and responsibilities for the AI agent. Roles enable the AI agent to perform its required actions.
-   The list of steps are the instructions are sent to the large language model \(LLM\) that describe the necessary steps the AI agent follows while carrying out its role.
-   The tools are the additional resources, such as skills, and data sources that you can provide your AI agent to accomplish its role.
-   The trigger defines how the AI agent is activated.
-   The availability determines how your AI agent is displayed, either in the Now Assist panel or Virtual Agent.

For more information about AI agents, see [AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Agentic workflows

An agentic workflow contains a set of large language model \(LLM\) instructions with one or more AI agents that can execute an objective. Agentic workflows are tailored to achieve specific business outcomes, such as classifying tasks or processing emails for tasks.

An agentic workflow is controlled by an AI Agent Orchestrator that coordinates the flow of work between AI agents. Additionally, an AI Agent Communicator helps to facilitate communication between the AI Agent Orchestrator and AI agents in the workflow.

For more information about agentic workflows, see [General guidelines for creating AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=gg-creating-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Now Assist AI agents, Platform agentic workflows, and custom AI agents and agentic workflows

With Now Assist for App Engine, you enhance custom applications with Now Assist AI agents and Platform agentic workflows, in addition to custom AI agents and agentic workflows. Like with Now Assist skills, configuring Now Assist AI agents and Platform agentic workflows to fit custom applications often takes more time than just building custom AI agents and agentic workflows. The following table provides additional information about Now Assist AI agents, Platform agentic workflows, custom AI agents, and custom agentic workflows.

<table id="table_ykz_ws4_xgc"><thead><tr><th>

 

</th><th>

 

</th><th>

Ease of use within custom applications

</th><th>

More information

</th></tr></thead><tbody><tr><td>

Now Assist AI agents and agentic workflows

</td><td>

Preconfigured AI agents and agentic workflows that are designed for existing use cases, such as incident resolution

</td><td>

Must be duplicated and modified significantly for use in custom applications

</td><td>

-   [Explore Now Assist AI agents](https://www.servicenow.com/docs/access?context=exploring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
-   [Platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

</td></tr><tr><td>

Custom AI agents and agentic workflows

</td><td>

AI agents that you create custom for your use case using AI Agent Studio

</td><td>

Can be designed to work within custom apps during the creation process, when you define the AI agent and agentic workflow

</td><td>

-   [General guidelines for creating AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=gg-creating-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
-   [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
-   [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

</td></tr></tbody>
</table>