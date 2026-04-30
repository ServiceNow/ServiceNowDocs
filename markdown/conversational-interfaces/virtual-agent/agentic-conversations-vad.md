---
title: Agentic conversations in Virtual Agent
description: When you ask a question to the virtual agent, the agent understands the query. It can reason, plan, and execute across AI agents, virtual agent topics, conversational actions and subflows, catalogs, KB articles, custom skills, and any Now Assist in Virtual Agent supported skills to help you.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [AI agent]
breadcrumb: [Explore, Virtual Agent, Conversational Interfaces]
---

# Agentic conversations in Virtual Agent

When you ask a question to the virtual agent, the agent understands the query. It can reason, plan, and execute across AI agents, virtual agent topics, conversational actions and subflows, catalogs, KB articles, custom skills, and any Now Assist in Virtual Agent supported skills to help you.

-   If for the given assistant, specific agents are available to perform user tasks or sub tasks, they’re used.
-   If a specific agent isn’t available for the task or sub task, the system automatically employs the Search Agent to discover answers or appropriate skills within the system \(again based on the assistant scope\).
-   If skill execution is required, the system automatically executes the discovered skills.
-   The system can plan and orchestrate execution among multiple agents, skills, and QnA to accomplish complex tasks.

## Enable AI agents in Virtual Agent

Role required: admin or virtual\_agent\_admin

**Note:** You must manually enable agents to make them discoverable in Virtual Agent. For more information about changing the settings, see [Conversational settings for Assets in the Asset library](asset-lib-conv-settings.md).

To enable AI agents in Virtual Agent:

1.  Create and configure multiple assistants with specific scope and map the assistants to one or more portals.

    The configuration consists of the following:

    -   Creating an assistant in Virtual Agent or using the default. To create an assistant, see [Create a chat assistant](../../now-assist-in-va/task/create-assistant.md)
    -   Assigning specific assistants to a specific portal or portals. For more information, see [Display your chat assistant on a portal, channel, or mobile app](../../now-assist-in-va/task/display-assistant-portal-channel.md).
    ![Assistants in CI.](../images/assistants.png)

2.  Ensure that **Agentic support** is enabled. For more information about using agentic support, see [Use agentic support for a chat assistant](../../now-assist-in-va/task/use-agentic-support.md).

    ![AI agents skill.](../images/assistant-skill.png)

3.  Map or publish an agent to one or more assistants on AI Agent Studio to make the agent available within a specific assistant. For more information, see [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

    ![Adding VA assistants to AI agent.](../images/va-card-ai-agent.png)


During execution, only the configured AI agents are considered for the current assistant and dynamically makes them available to the Orchestrator for planning.

## Examples of AI agent behavior for user utterances

The examples will consider the following available example resources in the system:

<table id="table_llk_4dq_hfc"><thead><tr><th>

Agents

</th><th>

Skills/Topics

</th><th>

KB Articles

</th></tr></thead><tbody><tr><td>

Check IT Ticket status agent

 Email Agent

 Meeting scheduling Agent

</td><td>

Order coffee

 Order food

 Order laptop

 Order accessories

</td><td>

Spam

 ESPP policy

</td></tr></tbody>
</table>**Scenario 1: Multiple questions from KB articles**

Utterance: `How do I avoid spam? How do I detect it?`

-   Non-agentic response: Produces a single mixed answer.

    ![Non-agentic response.](../images/utterance-qna.png)

-   Agentic response: Breaks it into two questions and provides a better answer for each one of them.

    ![Agentic response part1.](../images/utterance-agentic1.png)![Agentic response part2.](../images/utterance-agentic2.png)


**Scenario 2: Multiple skills with slot filling**

Utterance: `Hey, order a coffee for me, preferably dark roast and something to eat, maybe a pizza?`

-   Non-agentic response: Produces a single answer. Mostly listing all matching available skills. No auto-execution since it matched multiple skills.

    ![Non-agentic response.](../images/utterance2-qna.png)

-   Agentic response: Breaks it into two distinct tasks, order coffee and order food/pizza. Executes one after another, completing the entire user request.

    ![Agentic response part1.](../images/utterance2-agentic1.png)![Agentic response part2.](../images/utterance2-agentic2.png)![Agentic response part3.](../images/utterance2-agentic3.png)


**Scenario 3: Complex utterance with a combination of skills, agents, and QnA**

Utterance: `I am going on PTO tomorrow. Get my expense report and my IT ticket status. Send a summary of the expense report to John Jacob and the details on ticket status to Robert Williams, informing them of my PTO and requesting them to work on them.`

-   Non-agentic response: Produces a single answer. It lists all matching available skills. No auto-execution will take place since it matched multiple skills.

    ![Non-agentic response.](../images/utterance3-qna.png)

-   Agentic response: Breaks it into multiple distinct tasks, reasons and plans, understands the dependencies, and executes one after another, completing the entire user request using output from prior actions as context as needed.

    ![Agentic response part1.](../images/utterance3-agentic1.png)![Agentic response part2.](../images/utterance3-agentic2.png)![Agentic response part3.](../images/utterance3-agentic3.png)![Agentic response part4.](../images/utterance3-agentic4.png)![Agentic response part5.](../images/utterance3-agentic5.png)![Agentic response part6.](../images/utterance3-agentic6.png)


**Scenario 4: Complex utterance with a combination of QnA \(KB\) and agent**

Utterance: `What is the maximum contribution amount for espp? Send an email to Robert with the details.`

-   Non-agentic response: Produces a single answer and doesn’t complete or even suggest the second action since there’s no corresponding skill.

    ![Non-agentic response.](../images/utterance4-qna.png)

-   Agentic response: Understands the two separate intents and executes them in sequence while using the output from the first intent to fulfill the second intent.

    ![Agentic response part1.](../images/utterance4-agentic1.png)![Agentic response part2.](../images/utterance4-agentic2.png)


## Halting and restarting agentic conversations

If you want to stop an agentic conversation mid-query, hover over the send icon ![Send icon.](../images/vad-send-icon.png) while the agent is researching a query. The icon becomes an interrupt flow icon ![Interrupt flow icon.](../images/vad-interrupt-flow-icon.png). Select the icon and the conversation stops. A message appears: `The current conversation has been stopped, but you can begin again`. Enter a new query to restart the agentic conversation.

## Error handling and fallback options

When the AI agent cannot understand a request, encounters a system error, or a session becomes inactive, it displays a message and presents options to help you continue.

-   When Now Assist cannot find an answer:

    Depending on how your administrator has configured the assistant, these options may include:

    -   Requesting a live agent
    -   Creating a support request
    -   Viewing office hours
    For example, if you ask about a topic the AI agent cannot find information on, you might see a message such as: “I can’t find anything on that directly but I can help you explore other options.” Select one of the displayed options to continue.

-   Session timeout due to inactivity:

    If you stop responding during a conversation, the AI agent waits for a set period before ending the session. When a session is about to time out, you will receive a warning message. For example: “Looks like you’ve left this conversation. Would you like to keep going?”. If you want to continue, respond to resume the conversation.

    If there is no response to the warning, the session ends with a session end message. For example, “Our chat has timed out due to inactivity. Just start a new conversation whenever you’re ready. I’ll be here to help!”. You can start a new chat to continue getting help.

-   Technical errors and system timeout:

    If the AI agent encounters a backend error or cannot complete a request due to a technical issue, it displays a message and presents fallback options. For example: “It looks like I’m having trouble completing your request right now because of a technical failure. But I can help you explore other options.” You can select one of the available fallback options to continue.

-   Errors during agentic tasks:

    When you ask the AI agent to complete a multi-step task on your behalf, it plans and carries out the steps automatically. If a step in the plan cannot be completed, it lets you know and offers fallback options so you can decide how to proceed.

    For example, if the AI agent is creating an expense report and encounters a problem, it displays a message such as: “Unfortunately that didn’t work. But I can help you explore other options.” The fallback options available depend on your configuration.


**Note:** Review AI generated responses for accuracy before taking action.

