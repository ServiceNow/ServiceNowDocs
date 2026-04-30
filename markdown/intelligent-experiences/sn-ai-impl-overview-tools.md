---
title: Now Assist organization and tools
description: The Now Assist experience includes generative AI skills, agentic AI, and conversational user engagement layer. A good AI experience depends on quality data and a coherent AI policy that functions as its guiding star. AI Search capabilities and other tools help connect the pieces.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-10-22"
reading_time_minutes: 15
keywords: [Now Assist, agentic AI, AI readiness]
breadcrumb: [ServiceNow AI implementation, Enable AI experiences]
---

# Now Assist organization and tools

The Now Assist experience includes generative AI skills, agentic AI, and conversational user engagement layer. A good AI experience depends on quality data and a coherent AI policy that functions as its guiding star. AI Search capabilities and other tools help connect the pieces.

The following infographic illustrates the components of the Now Assist experience. You can think of each area as a layer, with AI policy as the basis for your implementation. Data plays an important role, since poor data will lead to poor outcomes, and the search experience drives both generative and agentic AI capabilities. The conversational engagement layer allows your users to communicate with AI and perform tasks and self-serve more easily.

![The Now Assist experience includes a policy layer, a data layer, a content layer, a generative AI and agentic AI layer, and a conversational engagement layer.](../images/mmasset0021424.png "Components of the Now Assist experience")

## AI policy

AI governance is defined by your organization and then implemented on the platform using AI Control Tower. AI Control Tower is designed to scale with your organization’s AI maturity. It enables end-to-end life cycle management of AI agents and models, from intake and evaluation to deployment and optimization. It also acts as a bridge between governance committees and implementation teams, ensuring that policy decisions are translated into technical configurations and operational controls. The platform includes the AI Risk and Compliance application, which comes with pre-built content aligned to the EU AI Act and NIST AI Risk Management Framework \(AI RMF\), helping organizations accelerate compliance and implement responsible AI practices from day one. For more information, see [AI governance for Now Assist on the ServiceNow AI Platform](sn-ai-impl-governance.md).

For real-time guardrail enforcement for AI interactions, you can use Now Assist Guardian to monitor and mitigate risks related to offensive content, sensitive topics, and security threats in generative AI outputs. Admins can configure these guardrails directly in the Now Assist Admin console, and logs are available to track detection events and guide decisions about blocking or escalation.

Roles and responsibilities:

-   **[AI steward \[sn\_ai\_governance\_ai\_steward\]](../../ai-governance-workspace/concept/aict-health-tab.md)**

    The AI steward role manages the platform's data assets and AI capabilities, ensuring data quality, integrity, and ethical use. The steward also implements governance policies to maintain compliance, security, and responsible AI practices across ServiceNow applications and workflows.

-   **[AI asset/product owner \[ sn\_ai\_asset\_mgmt.ai\_asset\_owner\]](../../ai-governance-workspace/reference/roles-installed-with-ai-control-tower.md)**

    The AI asset \(or product\) owner is responsible for driving the development and delivery of AI-powered products, ensuring alignment with business goals and user needs. They define product vision, manage feature prioritization, and translate business requirements into technical deliverables.

-   **[AI Risk and Compliance Manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\]](https://www.servicenow.com/docs/access?context=roles-installed-with-ai-risk-and-compliance&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The AI Risk and Compliance Manager is tasked with identifying, assessing, and mitigating risks related to AI use within the enterprise. This role ensures AI compliance with laws, regulations, and internal standards while addressing issues such as bias, privacy, and transparency.

-   **[Now Assist Admin \[sn\_nowassist\_admin.nsa\_admin\]](../../now-assist-admin/reference/roles-installed-with-now-assist-admin.md#)**

    The Now Assist admin is responsible for enabling and managing the Now Assist Guardian guardrails within the Now Assist Admin console. This includes configuring detection settings for offensiveness, prompt injection, and sensitive topics, as well as monitoring logs to assess harmful or malicious AI outputs. The admin can toggle guardrails on or off, choose actions like “Block and Log,” and tailor the configuration to match organizational risk tolerance and use cases.


For more information about these tools, see:

-   [AI Control Tower](../../ai-governance-workspace/concept/ai-control-tower-landing.md)
-   [AI Risk and Compliance](https://www.servicenow.com/docs/access?context=ai-risk-and-compliance&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist Guardian](../../now-assist-platform/concept/now-assist-guardian.md)

## Data management

You know the old saying, "Garbage in, garbage out?" Poor, incomplete, or unstructured data can lead to poor AI outcomes. To prepare your data for AI implementation, see [Data readiness for implementing Now Assist on the ServiceNow AI Platform](sn-ai-impl-data-readiness.md).

Now Assist provides several tools to help you manage data and provide user context on your instance. The Now Assist Data Kit helps organizations manage AI training data on their ServiceNow instance. It provides a centralized workspace to curate, generate, cleanse, and evaluate datasets, including importing data from tables, adding ground truth, and creating derived datasets. It supports synthetic data generation—up to 1,000 records at a time—and includes tools to anonymize sensitive information for privacy compliance. Integrated with the Now Assist Skill Kit, it enables teams to test custom AI skills and measure performance.

Knowledge Graph makes AI in Now Assist more personal by using structured enterprise data to tailor responses to each user. It helps AI understand context, such as a user’s role, location, or assigned assets, making answers more relevant and accurate. It also supports intelligent slot-filling, automatically pulling in known information to streamline conversations and reduce repetitive questions. This results in faster, more personalized, and trustworthy AI interactions.

Roles and responsibilities:

-   **[Now Assist Data Kit admin \[sn\_data\_kit.admin\]](../../now-assist-data-kit/reference/data-kit-admin-role.md)**

    This role is required to create, update, and publish datasets in Now Assist Data Kit.

-   **[Knowledge Graph admin \[kg\_admin\]](../../knowledge-graph/Reference/knowledge-graph-roles.md)**

    This role is required to design, manage, and audit Knowledge Graph schemas, including configuring nodes \(tables\), properties \(columns\), and relationships.


For more information about these tools, see:

-   [Now Assist Data Kit](../../now-assist-data-kit/concept/now-assist-data-kit-landing.md)
-   [Knowledge Graph](../../knowledge-graph/concept/knowledge-graph-landing.md)
-   [Now Assist Readiness Evaluation](../../now-assist-readiness-evaluation/concept/now-assist-readiness-evaluation-landing-page.md)

## Internal and external content search

Now Assist in AI Search is the primary tool used to find content on your instance, whether it's in the form of knowledge articles, Service Catalog items, system users, Knowledge Graph schemas, or content in enhanced chats using Now Assist in Virtual Agent.

Now Assist in AI Search is a plugin that enhances your existing AI Search configuration, adding support for Now Assist Genius Result answers.

You can expand the amount of content available to Now Assist in AI Search by using External Content Connectors. With this tool, AI Search applications can search content and metadata from external content repositories such as Atlassian Confluence Cloud and Microsoft SharePoint Online.

Roles and responsibilities:

-   **[AI Search admin \[ais\_admin\]](https://www.servicenow.com/docs/access?context=components-installed-ais&version=zurich&pubname=zurich-platform-administration&section=ais-admin-role&ft:locale=en-US)**

    This role is required to manage configuration settings for the AI Search application.

-   **[External Content Connectors admin \[sn\_ext\_conn.xcc\_admin\]](https://www.servicenow.com/docs/access?context=installed-with-ext-content-connectors&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    This role is required to manage configuration and crawl settings for the External Content Connectors application.


For more information about these tools, see:

-   [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

## Generative AI skills

Now Assist product plugins provide workflow-specific, generative AI skills that are tailored to specific use cases. For example, a skill might summarize a customer chat, suggest next steps in a workflow, or generate resolution notes for a task. For a list of available skills by product, see [Now Assist skills](../../now-assist-skills/concept/now-assist-skills.md).

Use the Now Assist Admin console to install and configure Now Assist plugins, as well as perform the following tasks:

-   Set up and configure skills to align with your business processes.
-   Monitor and analyze usage, including adoption rates and performance metrics across the platform.
-   Manage provider policies, data handling rules, and access controls.
-   Turn on and configure the Now Assist panel.
-   Manage large language models \(LLMs\).
-   Configure translation for Now Assist.

If you need to customize or adapt existing skills, you can use the Now Assist Skill Kit to build, customize, and test generative AI skills that are tailored to your organization’s workflows. With features like a prompt editor, visual builder, and evaluation tools, it helps you fine-tune performance and ensure quality. It also integrates with the Now Assist Data Kit and Now Assist Guardian for testing and governance, making it a flexible and secure way to extend AI across the ServiceNow platform.

Roles and responsibilities:

-   **[Now Assist Admin \[sn\_nowassist\_admin.nsa\_admin\]](../../now-assist-admin/reference/roles-installed-with-now-assist-admin.md#)**

    This role is required to install Now Assist plugins, activate skills, and configure Now Assist preferences and settings.

-   **[Skill Kit admin \[sn\_skill\_builder.admin\]](../../now-assist-skill-kit/reference/na-skill-kit-roles.md#)**

    This role is required to create, update, and publish skills in Now Assist Skill Kit.


For more information about these tools and features, see:

-   [Overview tab in Now Assist Admin](../../now-assist-platform/concept/configuring-now-assist.md)
    -   [Now Assist panel](../../now-assist-platform/concept/now-assist-panel-overview.md)
    -   [Manage AI models](../../now-assist-admin/task/manage-large-language-models.md)
    -   [Analyzing Now Assist performance](../../now-assist-analytics/concept/now-assist-analytics.md)
    -   [Multilingual service for Now Assist](../../now-assist-platform/concept/translation-for-now-assist.md)
    -   [Now Assist for Mobile](https://www.servicenow.com/docs/access?context=now-assist-mobile-landing&version=zurich&pubname=zurich-mobile&ft:locale=en-US)
-   [Now Assist Skill Kit](../../now-assist-skill-kit/concept/now-assist-skill-kit-landing.md)

## Agentic AI

In an agentic AI system, autonomous agents perform complex tasks by reasoning, planning, and executing actions across multiple steps. These agents are not just reactive; they can break down goals, make decisions, and coordinate with other agents or systems to complete workflows. In AI Agent Studio, AI agents and agentic workflows are built to handle tasks such as resolving incidents, managing requests, or navigating service catalogs using generative AI and orchestration logic. For a list of available agentic workflows by product, see [Now Assist agentic workflows](../../now-assist-ai-agents/concept/sn-aia-use-cases-list.md).

Use AI Agent Studio to perform the following tasks:

-   Build or modify AI agents and agentic workflows using intuitive list views and guided setup tools.
-   Simulate tasks and view execution logic to refine agent behavior.
-   Access execution logs and version control to track performance and changes.
-   Use the Settings page to enable Now Assist Guardian for runtime safety, including detection of offensive content and prompt injection.
-   Use the AI Agent Analytics dashboard to view usage stats, efficiency gains, and execution volume to help measure value.

The Model Context Protocol \(MCP\) client enables you to access the Model Context Protocol tools that are hosted externally and published using an MCP Server. MCP facilitates communication between an AI host application \(like AI Agent Studio\) and one or more MCP servers that expose specific capabilities such as tools.

The MCP Server Console is a tool for administrators to set up and manage Model Context Protocol \(MCP\) servers. These servers provide AI applications with access to ServiceNow features like incident lookups, case summaries, and workflow actions. The console lets you choose which capabilities to make available, ensuring everything stays secure and compliant. Then, from an MCP client, users can request information from the server and automate functionality using the available tools and data that the server returns.

Roles and responsibilities:

-   **[AI Agent Admin \[sn\_aia\_admin\]](../../now-assist-ai-agents/reference/na-aia-reference.md)**

    This role is required to create, manage, update, test, and delete AI agents and agentic workflows.

-   **[MCP Client Admin \[sn\_mcp\_client.admin\]](../../model-context-protocol-client/reference/mcp-reference.md)**

    This role is required to administer the MCP client in AI Agent Studio. It is inherited from the AI Agent Admin \[sn\_aia.admin\] role.

-   **[MCP Server administrator \[sn\_mcp\_server.admin\]](../../mcp-server-console/reference/installed-mcp-server-console.md)**

    This role is required to administer the MCP Server Console.


For more information about these tools, see:

-   [Now Assist AI agents](../../now-assist-ai-agents/reference/na-ai-agents.md)
    -   [AI Agent Studio](../../now-assist-ai-agents/concept/ai-agent-studio.md)
    -   [Implement access control in Now Assist AI agents](../../now-assist-ai-agents/concept/aia-security-implementation.md)
    -   [AI Agent Analytics dashboard](../../now-assist-ai-agents/concept/ai-agent-dashboard.md)
    -   [Examples of using AI agents](../../now-assist-ai-agents/concept/ai-agent-examples.md)
-   [Model Context Protocol Client](../../model-context-protocol-client/reference/mcp-client.md)
-   [MCP Server Console](../../mcp-server-console/concept/mcp-server-console-landing.md)

## Conversational AI engagement

Now Assist in Virtual Agent acts as the conversational front door to your organization’s AI capabilities. It enables users to interact naturally with AI-powered assistants that understand intent, recommend actions, and deliver synthesized responses—all within familiar channels like the service portal, mobile app, and Microsoft Teams. This conversational layer connects users to a wide range of AI-powered resources, including AI agents, generative AI skills, catalog items, Virtual Agent topics, Q&amp;A Genius results from AI Search, and even custom subflows and actions.

By integrating with the AI agent framework, Virtual Agent can discover and trigger agentic workflows that dynamically solve problems based on context. For example, a user might ask about ordering a device, and the system can invoke a multi-turn catalog ordering skill, refine the request, and complete the task, all in one conversation. Similarly, Q&amp;A Genius capabilities allow users to ask open-ended questions and receive actionable answers, links, or follow-up options, improving deflection rates and reducing the need for live agent intervention.

Now Assist in Virtual Agent also makes it easier to discover content without needing to know exact keywords. Users can search for and interact with catalog items, AI agents, and Virtual Agent topics using natural language. LLM topic discovery and Knowledge Graph slot-filling can return personalized responses and reduce repetitive questions.

To configure Now Assist in Virtual Agent, you set up an assistant. An assistant is a container for a specific conversational experience that can be delivered in portals on your instance, mobile apps, Microsoft Teams, and Slack. Use the Assistant Designer to create, configure, and manage these assistants, as well as link them to conversational assets in Virtual Agent.

To implement Now Assist in Virtual Agent, admins use guided setup that requires no deep technical expertise. Assistant configuration includes the following options:

-   AI agent enablement and orchestration
-   Search sources
-   Knowledge Graph schema usage
-   Conversational assets, such as Virtual Agent topics, subflows, actions, generative AI skills, and AI agents
-   The portals, channels, or apps the assistant will be used in
-   Branding: the look and feel of the assistant
-   Chat experience, such as greeting, closing, and fallback messages

You can also customize an assistant for the Now Assist panel. The Now Assist panel is available in workspace experiences and is typically used for contextual assistance within a specific workflow or record. Now Assist panel assistants have different configuration options and skill availability.

Roles and responsibilities:

-   **Virtual Agent \[virtual\_agent\_admin\]**

    This role, or the admin role, is required to install Now Assist in Virtual Agent and set up and manage assistants in Assistant Designer. It is also required for users who create and manage Virtual Agent topics and assets.

-   **[Now Assist Admin \[sn\_nowassist\_admin.nsa\_admin\]](../../now-assist-admin/reference/roles-installed-with-now-assist-admin.md#)**

    This role is required to turn on and configure the Now Assist panel in the Now Assist Admin console.


For more information about these tools, see:

-   [Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)
    -   [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)
    -   [Enhanced chat](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)
    -   [Integrating Now Assist in Virtual Agent with Microsoft Teams](https://www.servicenow.com/docs/access?context=integrating-now-assist-va-msteams&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)
    -   [Using Now Assist in Virtual Agent conversations with Slack](https://www.servicenow.com/docs/access?context=na-va-llm-slack&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)
    -   
-   [Now Assist for Mobile](https://www.servicenow.com/docs/access?context=now-assist-mobile-landing&version=zurich&pubname=zurich-mobile&ft:locale=en-US)
-   [Now Assist panel](../../now-assist-platform/concept/now-assist-panel-overview.md)

