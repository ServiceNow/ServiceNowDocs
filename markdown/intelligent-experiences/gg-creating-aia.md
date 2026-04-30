---
title: General guidelines for creating AI agents and agentic workflows
description: By following some general guidelines for creating AI agents and agentic workflows, you can create clear and effective instructions that help maximize their efficiency and effectiveness.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-09-19"
reading_time_minutes: 6
breadcrumb: [Exploring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
---

# General guidelines for creating AI agents and agentic workflows

By following some general guidelines for creating AI agents and agentic workflows, you can create clear and effective instructions that help maximize their efficiency and effectiveness.

Discussing when to create a flow, conversational topic, AI agent, or agentic workflow to accomplish a task on the Now Platform 

## Creating AI agents and agentic workflows overview

AI agents and agentic workflows rely on large language models \(LLMs\), so the language that you use for their instructions is important. There are many steps that you can take to help improve the quality and consistency of your agentic AI solutions.

Follow these guidelines when writing AI instructions for an AI agent or agentic workflow.

-   **Clarity**
    -   Use instructions that are concise, clear, and precise. Simple language can help remove ambiguous situations that could stall or disrupt an agent's progress. Example: "You’re an assistant tasked with helping the caller or requester by suggesting answers to survey questions." instead of "You help callers with questions."
    -   Use specific action verbs. Example: "Analyze" instead of "look at."
    -   Add explicit conditions when a certain step must be completed. Example: "If priority = High, then escalate immediately" instead of "escalate urgent issues."
    -   Clarify boundaries and limitations. Example: "NEVER modify incident status without supervisor approval."
    -   Limit technical jargon. Technical jargon can limit applicability because it may not be accessible or universal.
-   **Context**
    -   Embed requirements within context. Specify when certain requirements should be used within the task. Example: "When generating answers to present to the user, apply standard quality controls."
    -   Only include the context that affects decision making. Avoid extraneous information to help prevent the AI agent or agentic workflow from incorporating unwanted details.
    -   Define what good outcomes look like. Include examples. Missing or vague descriptions of results could result in AI agents or agentic workflows exiting before the end state is achieved. Example: "Present the user with a report that includes a minimum of 3 relevant graphs pertaining to the list of records."
-   **Constraints**
    -   Denote hard requirements. Use strong language to insist on the importance of the requirements. While output cannot be guaranteed to follow these requirements, being specific about standards can help reduce deviations.
    -   Describe preferences that can be adjusted based on context.
    -   Add conditional restraints. Example: "If more than one record is returned, present the results to the user in order of creation date. If more than five records are returned, present the results to the user in order of relevance."
-   **Coherence**
    -   Create steps that flow logically. Each step should build on the results of the previous step. Example: "Step 1 gathers a list of incident records. Step 2 performs record operations on those list of records."
    -   Use consistent terminology throughout.
    -   Design instructions that serve the overall objective. All of your tools and AI agents work together to solve problems.
    -   Break complex goals into individual pieces. Example: "Step 1: Analyze customer data systematically. Step 2: Check priority and validation permissions. Step 3: Generate and format comprehensive report."
-   **Structure**
    -   Use consistent formatting. Similar instructions should use similar language patterns.
    -   Group related steps together.
    -   Create a smooth flow from instruction to instruction. Along with grouped instructions and logical step progression, this provides a systematic and structured process for the AI agent or agentic workflow to follow.

## Guidelines for creating AI agents

The description, AI agent role, and list of steps are the sections that give the LLM the context and instructions to perform a task. Together, they form the blueprint that's necessary for the LLM to complete its role in a complex workflow. Follow these guidelines to improve the accuracy, adaptability, and optimization of the AI agent:

-   **AI agent description**
    -   Specify the key areas or tasks that you want the agent to handle. Example: "Specializes in handling inquiries and resolving customer issues."
    -   Use clear, focused language and avoid vague terminology.
    -   Define the agent's inputs, outputs, and context.
    -   Differentiate the agent's unique role from other agents. Provide distinct and detailed descriptions of what that specific agent should do that is different than other agents.
-   **AI agent role**
    -   Clearly state the primary function of the AI agent in one or two sentences. Example: "The AI agent acts as a customer service assistant."
    -   State the specific business challenge that you want the AI agent to address. Example: "Reducing customer wait times by 50%."
    -   Provide a brief scenario of how the AI agent is to be used. Example: "Automating responses to common queries and escalating complex issues to human agents."
-   **AI agent list of steps**
    -   Create a logical progression from step to step.
    -   Use action-oriented language. Use verbs like the following:
        -   Fetch
        -   Retrieve
        -   Filter
        -   Analyze
        -   Extract
        -   Parse
        -   Update
        -   Send
        -   Notify
        -   Generate
        -   Validate
    -   Include outputs for each step to measure the task completion. Example: "Return the total incident count to other agents or processes that need it."
    -   Add contingencies to account for unexpected scenarios. Example: "If you encounter an error while looking up records, try again. If you still get an error, report that an error occurred."
    -   Define success and completion. Provide end states so that the AI Agent Orchestrator can determine whether an AI agent has finished its objective.
    -   If you've created a tool for your AI agent, refer to the tool by name. However, you should make sure that the instructions change if the tool is ever renamed. If you don't, then the AI agent could be unable to complete its task.
-   **Tools**
    -   Write detailed tool descriptions to help the AI agent learn what the tool is and how best to use it.
    -   Create tools that work together. Build your tools around achieving the list of steps for the AI agent itself.
    -   Use the output transformation strategy field to define what the output of a tool should look like. Specifying how a tool should present its output can help the AI agent use that output when employing other tools or when sharing information between other agents.

## Guidelines for creating agentic workflows

Follow these agentic workflow guidelines to provide the detailed information and the steps needed to accomplish a task:

-   **Agentic workflow list of steps**
    -   Write each step sequentially and number each step so that there’s a logical and actionable flow.
    -   Account for as many possibilities as you can to avoid gaps. Provide enough detail that the agentic workflow can adapt if it encounters an edge case.
    -   Define the starting conditions, actions, decision points, and end states.
    -   Refer to end users as "the user."
    -   Use verbs like "show," "display," or "inform" to describe steps where the user needs to be shown something but they do not need to provide input.
-   **Additional tips**

    Associate a maximum of 10 agents per agentic workflow. Adding more agents doesn’t necessarily mean that you get better or faster results. Instead, use small, well-defined scopes.

    **Note:** You can assign up to 100 agents to an agentic workflow. However, not all 100 agents may be involved in resolving the agentic workflow because the AI Agent Orchestrator decides which agents should execute the plan. For example, an incident resolution gets impacted by the size of the agentic workflow and the number of agents that are assigned to it.


When creating agentic workflows with more than one assigned agent, make sure that you clearly define the agents with non-overlapping responsibilities. Include explicit limitations in the agents' roles. For example, one agent could handle user record details while another agent handles the incident record details.

## Common issues

-   **Problem: Agent consistently uses the wrong tool**

    Potential solutions:

    -   Create clear, specific instructions with action keywords.
    -   Write detailed tool descriptions that specify when and why to use each tool.
    -   Include explicit input and output guidance in tool descriptions.
    -   Evaluate tool selection logic by testing against various scenarios.
-   **Problem: Inconsistent output quality**

    Potential solutions:

    -   Embed standards as actionable requirements.
    -   Use phrases such as "implementing professional standards."
    -   Add quality verification steps.
-   **Problem: Quality checks or other steps skipped**

    Potential solutions:

    -   Convert checklists to actionable steps.
    -   Use phrases such as "analyze completion against criteria."
    -   Add conditional progression logic.

## Additional resources

For more prompting recommendations, see the Community [Now Assist AI Agents prompting guide](https://www.servicenow.com/community/now-assist-articles/now-assist-ai-agents-prompting-guide/ta-p/3386242).

