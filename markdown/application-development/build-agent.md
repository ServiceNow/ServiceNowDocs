---
title: Build Agent
description: The ServiceNow Build Agent application is an autonomous AI agent that creates and updates ServiceNow applications from natural language prompts. You can also use Build Agent to get answers to general ServiceNow development questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/build-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-28"
reading_time_minutes: 5
keywords: [Build Agent, AI agent, autonomous AI, application development, ServiceNow applications, conversational interface, natural language, application lifecycle management, ServiceNow Otto, AI Agents, generative AI, agentic AI]
audience: programmer
breadcrumb: [Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Build Agent

The ServiceNow® Build Agent application is an autonomous AI agent that creates and updates ServiceNow applications from natural language prompts. You can also use Build Agent to get answers to general ServiceNow development questions.

Build Agent is available in ServiceNow Studio and the ServiceNow IDE. It appears as a chat panel with a multi-turn conversation interface. Use Build Agent to do the following:

-   Create and edit ServiceNow applications from natural language prompts.
-   Design flows, create catalog items, and create Automated Test Framework \(ATF\) tests.
-   Refactor tables, explain and document code, fix errors, and run queries.
-   Get answers to ServiceNow development questions.

**Note:** You can use Build Agent if you have the admin role.

## Get started

<table id="table_a3w_q5k_hgc" class="nav-card"><tbody><tr><td>

[Explore\[Omitted image "bus-explore.svg"\] Alt text:Learn how Build Agent works and what it can create.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/exploring-build-agent.md)

</td><td>

[Configure\[Omitted image "bus-sdlc.svg"\] Alt text:Install and configure Build Agent.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/install-build-agent.md)

</td></tr><tr><td>

[Use\[Omitted image "bus-start-developing.svg"\] Alt text:Create and update ServiceNow applications with Build Agent.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/use-build-agent.md)

</td><td>

[Reference\[Omitted image "bus-learn.svg"\] Alt text:Build Agent reference material, such as example prompts.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-agent-reference-landing.md)

</td></tr></tbody>
</table>**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some AI products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## Helpful resources

Use the following resources to learn about related products and to get help:

-   **Autonomous Engineer**

    For information about the agentic AI worker that builds applications from your requirements, see [Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/autonomous-engineer.md).

-   **Build Agent and Autonomous Engineer**

    For the differences between the two products and what they share, see [Autonomous Engineer and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-build-agent-relationship.md).

-   **Limitations**

    For limitations that apply when you use Build Agent, see [Build Agent limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-agent-limitations.md).

-   **Example prompts**

    For sample prompts to try with Build Agent, see [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-agent-example-prompts.md).

-   **Support**

    [Contact Customer Service and Support](https://support.servicenow.com/now)


## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect case information \(for chat summarization, resolution notes generation, knowledge generation, call summarization\), chat transcripts \(for chat recommendation\), and email information \(for email response\). Customers can opt out of future data collection at any time, as described in the [AI Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [ServiceNow AI documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-products.md).

-   **[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/exploring-build-agent.md)**  
Build Agent enables developers to create, edit, and deploy full-stack ServiceNow® applications to update sets that encompass both user interface and back-end components.
-   **[Build Agent configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configure-build-agent.md)**  
Build Agent connects your instance to AI-powered design workflows. Set up the required application and MCP server connections to start using it.
-   **[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/use-build-agent.md)**  
Build Agent is an autonomous AI agent native to ServiceNow that translates plain language instructions into ready-to-deploy applications and metadata, using the platform’s domain language and guardrails. It's purpose-built for full-stack creation and editing across tables, flows, UI, and scripts, and it operates as the core engine for agentic development on the ServiceNow AI Platform.
-   **[Build Agent reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-agent-reference-landing.md)**  
Reference topics provide additional information about using Build Agent to create and edit apps, as well as ServiceNow metadata.

**Parent Topic:**[Build](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-ai-workflow-factory-prime.md)

