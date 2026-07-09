---
title: Customer Service Management Live Agent Assist for voice channel
description: Live Agent Assist \(LAA\) is an AI Agent capability within ServiceNow Customer Service Management \(CSM\) that provides real-time recommendations to human agents during live customer interactions. LAA analyzes the conversation transcript, retrieves relevant knowledge and customer context, and surfaces actionable recommendations in the agent workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/csm-live-agent-assist.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use agentic AI in CSM, Now Assist for CSM, Customer Service Management]
---

# Customer Service Management Live Agent Assist for voice channel

Live Agent Assist \(LAA\) is an AI Agent capability within ServiceNow Customer Service Management \(CSM\) that provides real-time recommendations to human agents during live customer interactions. LAA analyzes the conversation transcript, retrieves relevant knowledge and customer context, and surfaces actionable recommendations in the agent workspace.

Live Agent Assist reduces handle time, improves first-contact resolution, and helps agents deliver consistent, accurate responses throughout the interaction.

## How Live Agent Assist works

Live Agent Assist is an AI agent with a single tool: Analyze Interaction &amp; Generate Response. The tool is a subflow-based tool that internally invokes GenAI skills to analyze the transcript, generate Knowledge Graph queries and Generate Response. These skills work in sequence to process the conversation, retrieve information from multiple data sources, and generate a final recommendation with cited sources.

Live Agent Assist is triggered automatically when the customer call lands to a human agent and interaction record is created. The AI agent activates when a live agent begins handling a customer interaction. No manual initiation is required.

After it is triggered, Live Agent Assist performs the following tasks:

-   Transcript Analysis — continuously reads and processes the live conversation transcript to extract unanswered customer queries.
-   Customer Information Retrieval — fetches basic customer context such as install base, account details, and interaction history.
-   AI Search for Knowledge Articles — performs an AI-powered search against the KB \(Knowledge Base\) to identify relevant articles.
-   Knowledge Graph Queries — queries the Knowledge Graph \(KG\) to perform joins across multiple related data tables for enriched context.
-   Recommendation Generation — synthesizes results from KB and KG to generate actionable, cited recommendations for the agent.
-   Clarification Query Handling — manages scenarios where the transcript is ambiguous, presenting clarifying questions to the agent.
-   Follow-up Query Handling — addresses agent follow-up questions in the context of the ongoing voice interaction.

The preceding tasks are fulfilled through four dedicated GenAI skills, each with a specific responsibility in the pipeline:

|Skill|Responsibility|
|-----|--------------|
|Transcript Analyzer|Analyzes the live transcript to extract unanswered customer queries and evaluate resolution paths.|
|KG Query Generator|Generates Knowledge Graph queries to retrieve joined data across CSM entity types.|
|Response Generator|Synthesizes KB articles, customer info, and KG results into a final recommendation with source citations.|
|Follow-up Query Enhancer|Enriches agent follow-up queries with customer context and transcript history before re-initiating the recommendation pipeline.|

## Data sources

Live Agent Assist retrieves information from the following primary data sources:

-   **Customer Context Builder**

    The Customer Context Builder is an interface class that pre-fetches basic customer context directly from database tables. This direct query path provides faster access to high-priority fields — such as recent interactions and installed products for the current caller.

    The base system includes CustomerContextBuilder interface which contains CustomerContextBuilderImpl implementation, that fetch and aggregate customer context data from multiple  tables \(interactions, cases, contracts, assets, entitlements, and more\), anchored to an interaction record. The result is serialized into a pipe-delimited format suitable for LLM input.

    **Note:** The Customer Context Builder is a scripted customization. Extending it requires creating a custom implementation of the interface class. For most scenarios, adding tables to the Enterprise Knowledge Graph tag is an easier approach because it does not require scripting.

-   **AI Search Profile**

    A RAG \(Retrieval-Augmented Generation\) retrieval call queries the AI search profile to identify configured sources. In the base system, the Live Agent Assist Search Profile is scoped to the Knowledge \(kb\_knowledge\) table, so recommendations draw from knowledge articles. Source citations identifying the contributing articles appear at the bottom of each recommendation. Admins can extend the profile to include additional tables. For more information on how to add additional search sources, see [Create a search source for AI Search](https://www.servicenow.com/docs/r/platform-administration/ai-search/create-search-source-ais.html).

-   **Enterprise Knowledge Graph**

    The Enterprise Knowledge Graph retrieves customer-specific information such as contract details, recent cases, and asset data. A tag scopes queries to a defined set of tables so that retrieval stays targeted.

    In the base system, the tag covers the account, asset, case, consumer, contact contract, entitlement, Install base item, Installed product, Interaction, Product Model, and Sold Product tables. As an admin, you can edit the tag to include additional tables:

    1.  Navigate to **All** &gt; **Knowledge Graph** &gt; **Knowledge Graph Designer** &gt; **Enterprise Graph**.
    2.  From the **Enterprise Graph Tags**, select the **CSM Live Agent Assist Tag**.
    3.  In the **Selected Tables** section, add the desired tables.
    For more information on editing tags, see [Managing Knowledge Graph tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/managing-knowledge-graph-tags.md).


## Role masking

Required role: B2B agents \(sn\_customerservice\_agent\) and B2C agents \(sn\_customerservice.consumer\_agent\)

**Important:** To access data in the agentic workflow, the admin role must include the specified roles under **Contains roles**.

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to enable agents to resolve cases efficiently. For example, add the csm role to the agentic workflow's list of approved roles to enable access to case records.

## Configure Live Agent Assist for voice channel

Configure the Live agent Assist AI agent to generate recommendations for ongoing voice interactions in the Agent workspace.

Before you begin:

-   The Customer Service Management AI Agent Collection plugin must be activated on your instance.
-   Role required: now\_assist\_admin

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Live Agent Assist** in the AI agents tab.
3.  Activate the trigger.

    -   In the Add triggers section, select the **Live Agent Assist** trigger which is in inactive state by default.
    -   In the Edit trigger dialog, turn on the **Trigger is ON** radio button and select **Save**.
    For more information on modifying an AI agent, see [Modify an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-ai-agent.md)Modify an AI Agent.


Result: The Live Agent Assist trigger is active. The agent now runs automatically each time a voice call is accepted. When an agent accepts a call and opens the interaction record, Live Agent Assist starts and displays recommendations in the Otto panel.

## Access Control lists \(ACLs\)

ACLs \(Access Control Lists\) are preconfigured to support the Provide customer 360 insights use case, including AI agents and their associated flows and actions, such as the Customer insights Agent. By default, ACLs are configured for the sn\_esm\_agent role. Customers can modify these ACLs to align with their specific business requirements and security policies. For more information, [Configure security controls for a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nask-access-control.md).

When updating the agent role for the Provide customer 360 insights Agentic Workflow, it is important to also update the corresponding ACLs to ensure proper permissions. To manually update ACLs for custom roles:

1.  Go to the **sys\_security\_acl** table.
2.  Use filters to locate ACLs related to your use case, AI agent, and internal flows or actions.
3.  Add your custom role to each relevant ACL record.

## Use the Live agent Assist AI agent for voice channel

Get real-time recommendations from the conversations happening over a live voice interaction.

Before you begin:

-   SN and CCaaS provider integration must exist. Supported CCaaS providers are Genesys, Twilio, NICE, Five9, 3CLogic, and Amazon Connect.
-   Real-time transcription feature with CCaaS provider must be enabled.
-   The Live agent Assist trigger in the Live Agent Assist AI agent must be activated. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).
-   Role required: sn\_customerservice.consumer\_agent

When a customer calls the support channel, an interaction record is created and assigned to a human agent. Live Agent Assist is triggered automatically and displays a notification in the banner. Select the Otto icon to open the Otto panel and view the welcome message.

Procedure:

1.  When you're on a live call with a customer, select the Otto icon on the banner.
    -   The Otto panel appears with the interaction ID.
    -   The transcript of your live conversation with the customer appears in the Conversation pane.
2.  After you gather details about customer requirements, select the **Get Recommendations** button on the Otto panel.
    -   The AI agent analyzes the conversation and generates recommendations or asks more questions. The icon appears while the agent processes the conversation before generating the next steps. If the customer asks multiple queries, you will be asked to choose the query you want to address first. You can pick a query and address one after another based on the customer's priority. For more information on how the recommendations are generated from the sources, see [Live Agent Assist overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/csm-live-agent-assist.md).
    -   When the recommendations are generated for a query, the sources from which the recommendations are generated appear under the Sources section following the recommendations. You can open these sources for further details.
3.  As you progress through the conversation, select the **Get Recommendations** button to get the recommendations.
4.  Clarification handling: If the AI Agent needs additional context before generating a recommendation, it displays clarifying questions with rendered option buttons, then waits for user selection.

    When you select one of the option buttons, the final answer is displayed with cited sources and the **Get Recommendations** button for further queries.

5.  Follow-up query handling: After an initial recommendation is delivered, type any follow-up question in the text field and select the Enter icon to get the recommendations.

    You can ask natural language questions, such as `What products is this customer currently using?` The AI agent responds with accurate, contextually relevant answers and maintains conversational context across multiple questions.


The final response is rendered with cited sources and the **Get Recommendations** button.

