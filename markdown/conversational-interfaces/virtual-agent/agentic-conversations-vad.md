---
title: Agentic conversations in Virtual Agent
description: When you ask a question to the virtual agent, the agent understands the query. It can reason, plan, and execute across AI agents, virtual agent topics, conversational actions and subflows, catalogs, KB articles, custom skills, and any Now Assist in Virtual Agent supported skills to help you.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-05-12"
reading_time_minutes: 3
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

    -   Creating an assistant in Virtual Agent or using the default. To create an assistant, see [Create an assistant](../../now-assist-in-va/task/create-assistant.md)
    -   Assigning specific assistants to a specific portal or portals. For more information, see [Display your assistant on a portal or channel](../../now-assist-in-va/task/display-assistant-portal-channel.md).
    ![Assistants in CI.](../images/assistants.png)

2.  Ensure that the **AI agents** skill is added to the assistant.

    ![AI agents skill.](../images/assistant-skill.png)

3.  Map or publish an agent to one or more assistants on AI Agent Studio to make the agent available within a specific assistant. For more information, see [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

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


