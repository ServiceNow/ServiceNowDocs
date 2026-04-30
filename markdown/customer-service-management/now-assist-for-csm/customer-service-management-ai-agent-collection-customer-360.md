---
title: Customer Service Management AI agent collection provide customer 360 insights
description: Provide Customer 360 insights agentic workflow is a GenAI-powered assistant that helps agents answer natural language questions about customers, cases, products, catalogs, and past interactions with a seamless multi-turn Q &amp; A experience.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-11-05"
reading_time_minutes: 6
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use agentic AI in CSM, Now Assist for CSM, Customer Service Management]
---

# Customer Service Management AI agent collection provide customer 360 insights

Provide Customer 360 insights agentic workflow is a GenAI-powered assistant that helps agents answer natural language questions about customers, cases, products, catalogs, and past interactions with a seamless multi-turn Q &amp; A experience.

This workflow enables agents to retrieve case details, customer information, and perform actions such as case creation, modification, escalation, and closure using natural language queries. It supports real-time context-aware responses and respects role-based access controls.

## Provide customer 360 insights agentic workflow overview

The Provide Customer 360 insights agentic workflow is a GenAI-powered assistant that helps agents to resolve cases more efficiently and effectively. By answering natural language questions about customers, cases, products, catalogs and past interactions, it provides contextual insights that enable agents to make informed decisions and solve issues faster. It provides a seamless, multi-turn Q&amp;A experience, helping agents to:

-   Ask follow-up questions and get context-aware responses in real time.
-   Access critical customer details and history to make informed decisions.

This feature consolidates scattered user and case data, providing agents with timely, accurate insights to make informed decisions, reducing Mean Time To Resolve \(MTTR\) and helping to solve issues. If something isn’t found, the GenAI responds clearly. For example, “I couldn’t find any recent catalog interactions for this customer". If the question is outside its scope, it redirects.

## Provide Customer 360 insights agentic workflow

Customer 360 insights agentic workflow is set up as a promoted asset in the Now Assist panel.

This workflow manages all case-related queries and actions, including retrieval of case details, history, timelines, assignments, status, customer information, sentiment analysis, related cases, knowledge articles, and case updates. It supports natural language requests for specific case numbers, aggregates comprehensive case and customer data, analyzes historical patterns and sentiment, and executes case management operations such as creation, modification, escalation, and closure.

## Role masking

Required role: B2B agents \(sn\_customerservice\_agent\) and B2C agents \(sn\_customerservice.consumer\_agent\)

**Important:** To access data in the agentic workflow, the admin role must include the specified roles under **Contains roles**.

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

In the data access settings, you must also add the necessary roles to helps agents to resolve cases more efficiently and effectively. For example, you can add the csm role to the agentic workflow's list of approved roles so that it can access case records.

## Setup Provide customer 360 insights Agentic Workflow

To configure the Provide customer 360 insights agentic workflow, perform the following steps:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Provide Customer 360 insights**.
3.  In **Define key requirements** the workflow’s purpose is clearly described and its steps with specific actions and criteria for each is outlined.
4.  In **Define security controls** you can set the access at user and data level.
    1.  **Define user access**: Specify which users can access and interact with the agentic workflow. Once you save your selections, the system automatically generates an Access Control List \(ACL\).
    2.  **Define data access**: Choose the user identity under which the Provide customer 360 insights agentic workflow will run. This determines the roles and associated data access permissions.

        **Note:** Choose the user identity this agentic workflow should run as to determine the roles and the data access permissions derived from them. Remember, when agentic workflows can access data, they can also share that data with the human user who interacts with them. Agent level role mask are: B2B agents \(sn\_customerservice\_agent\) and B2C agents \(sn\_customerservice.consumer\_agent\).

5.  In **Add triggers** you can set up optional triggers to launch the agentic workflow automatically without a user request. Triggers can be based on conditions or schedules you define and initiate agentic AI experiences.
6.  In **Select channels and status**, you can choose the channels where this agentic workflow will be available to engage with users who initiate interactions. Toggle the display for **Engage via the Now Assist panel** to see the agentic flow in the Now Assist panel.

    **Note:** To turn off the agentic workflow, toggle off **Engage via the Now Assist panel**.

7.  Select **Save and test**.

The agent executes the **testing** in AI Agent Studio for the agentic workflow.

![AI Agent Studio showing the testing output for Provide customer 360 insight agentic workflow](../image/customer-360-ai-agent.png "Example of Provide customer 360 insight agentic workflow testing in AI Agent Studio")

In the Now Assist panel, the agent receives a notification as soon as the interaction is generated, which enables them to follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in Customer Service Management by using the Now Assist panel](../task/request-gen-ai-capabilities-csm-now-assist-panel.md).

## Access Control lists \(ACLs\)

Access Control Lists \(ACLs\) are preconfigured to support the Provide customer 360 insights use case, including AI agents and their associated flows and actions, such as the Customer insights Agent. By default, ACLs are configured for the sn\_esm\_agent role. Customers can modify these ACLs to align with their specific business requirements and security policies. For more information, [Configure security controls for a skill](https://www.servicenow.com/docs/access?context=nask-access-control&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

When updating the agent role for the Provide customer 360 insights Agentic Workflow, it is important to also update the corresponding Access Control Lists \(ACLs\) to ensure proper permissions. To manually update ACLs for custom roles:

1.  Go to the **sys\_security\_acl** table.
2.  Use filters to locate ACLs related to your use case, AI agent, and internal flows or actions.
3.  Add your custom role to each relevant ACL record.

## AI agents used in Provide customer 360 insights agentic workflow

The following tables list the agents that are used in the Provide customer 360 insights agentic workflow.

|AI agent|Actions|
|--------|-------|
|Case action AI Agent|Perform customer-related actions, including case operations such as creating case tasks and updating work notes.|
|Customer insight AI Agent|Answer questions related to the record by retrieving comprehensive information, including customer details \(name, contact info, location, history, cases, orders\) and case data \(next steps, actions, assigned agent, notes, documents, tasks, resolutions\), along with other relevant attributes.|

## Use Provide customer 360 insights Agentic Workflow

The Provide customer 360 insights agentic workflow in Now Assist for Customer Service Management \(CSM\) gives agents contextual, GenAI-driven insights about customers directly within a case. By selecting the Now Assist icon ![Now assist icon.](../../../common/image/icon-ai-sparkle.png) in a case record, agents can access the Now Assist panel that delivers real-time insights based on customer data.

Agents can ask natural language questions, such as "What products is this customer currently using?" The AI agent responds with accurate, contextually relevant answers and maintains conversational context across multiple questions.

<table id="table_hlv_3ps_fhc"><thead><tr><th>

Feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Contextual Insights

</td><td>

AI retrieves and summarizes information from multiple sources, including:-   Case details \(status, priority, age, assignees, notes\).
-   Customer info \(account details, recent activity\).
-   Products and services they own.
-   Catalog items they interacted with.
-   Past interactions \(calls, chats, emails\).
-   Actions taken \(resolution steps, escalations, KBs shared\).

</td></tr><tr><td>

Handling

</td><td>

If data is unavailable or ambiguous, AI communicates clearly, for example, I couldn’t find any recent catalog interactions for this customer. For out-of-scope questions GenAI declines and redirects.

</td></tr><tr><td>

Security

</td><td>

GenAI respects role-based access controls and does not surface restricted information.

</td></tr><tr><td>

Feedback Loop

</td><td>

Agents can give thumbs up or thumbs down or flag inaccurate responses for retraining.

</td></tr></tbody>
</table>