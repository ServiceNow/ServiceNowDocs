---
title: Autonomous Engineer
description: The ServiceNow Autonomous Engineer application is an agentic AI worker that builds applications from your requirements. It generates a plan with structured work items, and background agents build the work items in parallel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/autonomous-engineer.html
release: australia
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 4
keywords: [Autonomous Engineer, Build Agent, implementation plan, agentic development, ServiceNow Studio, agent packs, work items, parallel execution]
audience: programmer
breadcrumb: [Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Autonomous Engineer

The ServiceNow® Autonomous Engineer application is an agentic AI worker that builds applications from your requirements. It generates a plan with structured work items, and background agents build the work items in parallel.

Autonomous Engineer takes your requirements as input, generates an implementation plan, and implements each work item in the plan. During planning and implementation, it applies implementation guidelines for the ServiceNow AI Platform. It also generates and runs Automated Test Framework \(ATF\) tests for each work item.

Autonomous Engineer is available in ServiceNow Studio and supports custom applications and agent pack implementations.

## Get started

<table id="table_ae_landing_nav" class="nav-card"><tbody><tr><td>

[Explore\[Omitted image "bus-explore.svg"\] Alt text:Learn how Autonomous Engineer works and when to use it.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/exploring-autonomous-engineer.md)

</td><td>

[Configure\[Omitted image "bus-sdlc.svg"\] Alt text:Set up Autonomous Engineer on your instance.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configure-autonomous-engineer.md)

</td></tr><tr><td>

[Use\[Omitted image "bus-start-developing.svg"\] Alt text:Run Autonomous Engineer to build applications from requirements.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-using-autonomous-engineer.md)

</td><td>

[Reference\[Omitted image "bus-learn.svg"\] Alt text:Reference information for Autonomous Engineer, including work item states and agent packs.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/autonomous-engineer-reference-landing.md)

</td></tr></tbody>
</table>## Helpful resources

Use the following resources to learn about related products and to get help:

-   **Build Agent**

    For information about the conversational agent that creates and updates applications, see [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-agent.md).

-   **Autonomous Engineer and Build Agent**

    For the differences between the two products and what they share, see [Autonomous Engineer and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-build-agent-relationship.md).

-   **Limitations**

    For limitations that apply when Autonomous Engineer runs, see [Autonomous Engineer limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-limitations.md).

-   **Agentic development overview**

    For an overview of agentic development, see [Agentic development on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/vibe-coding-landing.md).

-   **Support**

    [Contact Customer Service and Support](https://support.servicenow.com/now)


## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect case information \(for chat summarization, resolution notes generation, knowledge generation, call summarization\), chat transcripts \(for chat recommendation\), and email information \(for email response\). Customers can opt out of future data collection at any time, as described in the [AI Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [ServiceNow AI documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-products.md).

-   **[Exploring Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/exploring-autonomous-engineer.md)**  
Autonomous Engineer is an agentic worker that accepts requirements, generates a structured implementation plan, and builds all work items in parallel using background agents.
-   **[Configure Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configure-autonomous-engineer.md)**  
Configure Autonomous Engineer by installing it from the ServiceNow Store and enabling the features required for planning and parallel execution on your instance.
-   **[Using Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-using-autonomous-engineer.md)**  
Use Autonomous Engineer to provide requirements, review an implementation plan, and build all work items in parallel using background agents in Build Agent.
-   **[Autonomous Engineer reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/autonomous-engineer-reference-landing.md)**  
Reference information for Autonomous Engineer, including work item states, agent packs, and supported capabilities in Build Agent.

**Parent Topic:**[Build](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-ai-workflow-factory-prime.md)

