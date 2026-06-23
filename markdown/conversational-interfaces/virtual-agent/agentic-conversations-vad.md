---
title: Agentic conversations in Virtual Agent
description: When you ask a question to the virtual agent, the agent understands the query. It can reason, plan, and execute across AI agents, virtual agent topics, conversational actions and subflows, catalogs, KB articles, custom skills, and any Now Assist in Virtual Agent supported skills to help you.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/conversational-interfaces/virtual-agent/agentic-conversations-vad.html
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-06-20"
reading_time_minutes: 4
keywords: [AI agent]
breadcrumb: [Exploring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Agentic conversations in Virtual Agent

When you ask a question to the virtual agent, the agent understands the query. It can reason, plan, and execute across AI agents, virtual agent topics, conversational actions and subflows, catalogs, KB articles, custom skills, and any Now Assist in Virtual Agent supported skills to help you.

-   If for the given assistant, specific agents are available to perform user tasks or sub tasks, they’re used.
-   If a specific agent isn’t available for the task or sub task, the system automatically employs the Search Agent to discover answers or appropriate skills within the system \(again based on the assistant scope\).
-   If skill execution is required, the system automatically executes the discovered skills.
-   The system can plan and orchestrate execution among multiple agents, skills, and QnA to accomplish complex tasks.

## Enable AI agents in Virtual Agent

Role required: admin or virtual\_agent\_admin

To enable AI agents in Virtual Agent:

1.  Create and configure multiple assistants with specific scope and map the assistants to one or more portals.

    The configuration consists of the following:

    -   Creating an assistant in Virtual Agent or using the default. To create an assistant, see [Create a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/now-assist-in-virtual-agent/create-assistant.md)
    -   Assigning specific assistants to a specific portal or portals. For more information, see [Display your chat assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/now-assist-in-virtual-agent/display-assistant-portal-channel.md).
    \[Omitted image "assistants.png"\] Alt text: Assistants in CI.

2.  Ensure that the **AI agents** skill is added to the assistant.

    \[Omitted image "assistant-skill.png"\] Alt text: AI agents skill.

3.  Map or publish an agent to one or more assistants on AI Agent Studio to make the agent available within a specific assistant. For more information, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/configure-next-best-action-agent.md).

    \[Omitted image "va-card-ai-agent.png"\] Alt text: Adding VA assistants to AI agent.


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

    \[Omitted image "utterance-qna.png"\] Alt text: Non-agentic response.

-   Agentic response: Breaks it into two questions and provides a better answer for each one of them.

    \[Omitted image "utterance-agentic1.png"\] Alt text: Agentic response part1.\[Omitted image "utterance-agentic2.png"\] Alt text: Agentic response part2.


**Scenario 2: Multiple skills with slot filling**

Utterance: `Hey, order a coffee for me, preferably dark roast and something to eat, maybe a pizza?`

-   Non-agentic response: Produces a single answer. Mostly listing all matching available skills. No auto-execution since it matched multiple skills.

    \[Omitted image "utterance2-qna.png"\] Alt text: Non-agentic response.

-   Agentic response: Breaks it into two distinct tasks, order coffee and order food/pizza. Executes one after another, completing the entire user request.

    \[Omitted image "utterance2-agentic1.png"\] Alt text: Agentic response part1.\[Omitted image "utterance2-agentic2.png"\] Alt text: Agentic response part2.\[Omitted image "utterance2-agentic3.png"\] Alt text: Agentic response part3.


**Scenario 3: Complex utterance with a combination of skills, agents, and QnA**

Utterance: `I am going on PTO tomorrow. Get my expense report and my IT ticket status. Send a summary of the expense report to John Jacob and the details on ticket status to Robert Williams, informing them of my PTO and requesting them to work on them.`

-   Non-agentic response: Produces a single answer. It lists all matching available skills. No auto-execution will take place since it matched multiple skills.

    \[Omitted image "utterance3-qna.png"\] Alt text: Non-agentic response.

-   Agentic response: Breaks it into multiple distinct tasks, reasons and plans, understands the dependencies, and executes one after another, completing the entire user request using output from prior actions as context as needed.

    \[Omitted image "utterance3-agentic1.png"\] Alt text: Agentic response part1.\[Omitted image "utterance3-agentic2.png"\] Alt text: Agentic response part2.\[Omitted image "utterance3-agentic3.png"\] Alt text: Agentic response part3.\[Omitted image "utterance3-agentic4.png"\] Alt text: Agentic response part4.\[Omitted image "utterance3-agentic5.png"\] Alt text: Agentic response part5.\[Omitted image "utterance3-agentic6.png"\] Alt text: Agentic response part6.


**Scenario 4: Complex utterance with a combination of QnA \(KB\) and agent**

Utterance: `What is the maximum contribution amount for espp? Send an email to Robert with the details.`

-   Non-agentic response: Produces a single answer and doesn’t complete or even suggest the second action since there’s no corresponding skill.

    \[Omitted image "utterance4-qna.png"\] Alt text: Non-agentic response.

-   Agentic response: Understands the two separate intents and executes them in sequence while using the output from the first intent to fulfill the second intent.

    \[Omitted image "utterance4-agentic1.png"\] Alt text: Agentic response part1.\[Omitted image "utterance4-agentic2.png"\] Alt text: Agentic response part2.


## Halting and restarting agentic conversations

If you want to stop an agentic conversation mid-query, hover over the send icon \[Omitted image "vad-send-icon.png"\] Alt text: Send icon. while the agent is researching a query. The icon becomes an interrupt flow icon \[Omitted image "vad-interrupt-flow-icon.png"\] Alt text: Interrupt flow icon.. Select the icon and the conversation stops. A message appears: `The current conversation has been stopped, but you can begin again`. Enter a new query to restart the agentic conversation.

