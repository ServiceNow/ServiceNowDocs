---
title: AI capabilities in Sales CRM
description: Sales CRM includes generative and agentic AI capabilities that helps you automate sales workflows and enables sales teams to work more efficiently within your CRM environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/ai-capabilities-sales-crm.html
release: australia
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 7
breadcrumb: [Explore, Sales Customer Relationship Management]
---

# AI capabilities in Sales CRM

Sales CRM includes generative and agentic AI capabilities that helps you automate sales workflows and enables sales teams to work more efficiently within your CRM environment.

## AI plugins for Sales CRM

ServiceNow AI Platform and the following ServiceNow Otto plugins together provide AI capabilities for Sales CRM workflows:

-   ServiceNow Otto for Sales Automation \(sn\_som\_gen\_ai\)
-   ServiceNow Otto for Configure, Price, Quote \(CPQ\) \(sn\_som\_gen\_ai\_cpq\)
-   ServiceNow Otto for Order Management \(sn\_som\_gen\_ai\_om\)

These plugins are included in the existing Sales CRM products, bringing AI-powered automation through three licensing tiers each reflecting a different level of automation maturity:

-   Foundation: Default AI assistance for simple sales processes.
-   Advanced: Agentic workflows and multi-step automation.
-   Prime: Custom AI agent development.

Each ServiceNow Otto plugin packages the individual AI plugins and required dependencies.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## ServiceNow Otto for Sales Automation benefits

|Benefit|Feature|Store plugin|Used with|
|-------|-------|------------|---------|
|Manage the lead life cycle using an agentic workflow.|[Nurturing leads using agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/help-nurture-new-leads-agentic-workflow.md)|Sales Development AI Agents \(com.sn\_sd\_ai\_agents\)|Lead Management|
|Retrieve, update, create, and delete opportunity records and related CRM data from an MCP client using natural language.|[CRM conversational query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/manage-opportunity-records.md)|Opportunity Management AI Features \(com.sn\_opty\_mgmt\_ai\)|Opportunity Management|
|Get an immediate view of key details, customer needs, recent activity, and risks about an opportunity without reviewing multiple records.|[Summarize opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-som-summarize-opportunity.md)|Opportunity Management AI Features \(com.sn\_opty\_mgmt\_ai\)|Opportunity Management|
|Score opportunities, surface risk signals, and deliver qualitative insights that help sellers and leaders make faster, more confident decisions using machine learning.|[View opportunity scores and insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-opty-scores-insights.md)|Opportunity Management ML \(sn\_opty\_mgmt\_ml\)|Opportunity Management|
|Associate sales emails with CRM records using AI-powered workflow.|[AI sales activity association](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-ai-sales-activity-association.md)|AI sales activity association \(com.sn\_act\_assoc\_agent\)|Activity Management|

## ServiceNow Otto for CPQ

|Benefit|Feature|Store plugin|Used with|
|-------|-------|------------|---------|
|Generate a consolidated report of a quote record to quickly understand the quote without manually reviewing multiple fields, line items, or related records.|[Summarize a quote using quote summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/summarize-quote.md)|Summarization for Quote Management \(com.sn\_qut\_sum\_skill\)|Quote Experience|
|Automate and streamline the sales quote creation and modification process by using AI to detect quote needs from triggers like opportunity stage changes and keywords.|[Manage quotes using the Quote AI Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/manage-quote-using-quote-ai-agent.md)|Summarization for Quote Management \(com.sn\_qut\_sum\_skill\)|Quote Experience|
|Enable agents to submit quotes for approval and approvers to take action on approval requests directly from their MCP client, such as the Claude Desktop application.|[Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-advanced-approval-mgmt-ai.md)|Advanced Approval Management AI \(sn\_adv\_apr\_mgt\_ai\)|Advanced Approval Management|

## ServiceNow Otto for Order Management benefits

|Benefit|Feature|Store app|Used with|
|-------|-------|---------|---------|
|Make more accurate and faster decisions and improve customer responsiveness by generating order summaries for complex orders.|[Summarize orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-mgmt-summarize-order.md)|Summarization for Order Management \(com.sn\_ord\_sum\_skill\)|Order Management|
|Improve productivity of order agents by enabling them to update order and order line details in bulk.|[Manage order updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/bulk-update-order-lines-with-now-assist.md)|Assist Order Management AI Agent \(com.sn\_order\_cap\_aias\)|Order Management|
|Enable B2B customers to request changes to orders via chat and voice options.|[Manage order operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-business-portal.md)|Manage Order Operations \(com.sn\_ord\_ops\_aias\)|Business Portal|
|Enable B2B customers to dispute invoices using chat and voice options.|[Manage invoice operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-business-portal.md)|Manage Invoice Operations \(com.sn\_inv\_ops\_aias\)|Business Portal|

**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some AI products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## What to do next

Install and configure the AI plugins to enable generative and agentic AI features that support Sales CRM workflows. For more information, see [Configuring AI capabilities in Sales CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-ai-capabilities-sales-crm.md).

## Troubleshoot and get help

-   [ServiceNow Community on AI and Intelligence](https://www.servicenow.com/community/ai-intelligence-articles/tkb-p/ai-platform-kb)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support.](https://support.servicenow.com/now?draw=case)

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

