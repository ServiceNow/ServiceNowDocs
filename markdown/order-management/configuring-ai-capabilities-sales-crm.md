---
title: Configuring AI capabilities in Sales CRM
description: Use the AI Admin Hub console to activate the various AI applications and skills that you're entitled to use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configuring-ai-capabilities-sales-crm.html
release: australia
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 5
breadcrumb: [Configure, Sales Customer Relationship Management]
---

# Configuring AI capabilities in Sales CRM

Use the AI Admin Hub console to activate the various AI applications and skills that you're entitled to use.

## Installation overview

ServiceNow structures its products and packages in three tiers: Foundation, Advanced, and Prime. Each tier incorporates AI and builds progressively on the previous one with additional AI capabilities, agents, and governance tools. For more information about product tiers, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

Before installing the ServiceNow Otto plugins, review the [ServiceNow® AI implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sn-ai-implementation-landing.md) for best practices and additional resources.

You must install at least one ServiceNow Otto application before you can configure any skills. Install the following plugins using the Application Manager to enable AI skills and capabilities for Sales CRM:

-   ServiceNow Otto for Sales Automation \(sn\_som\_gen\_ai\)
-   ServiceNow Otto for CPQ \(sn\_som\_gen\_ai\_cpq\)
-   ServiceNow Otto for Order Management \(sn\_som\_gen\_ai\_om\)

For more information on installing AI plugins, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

**Note:** In Sales CRM, AI skills aren't automatically enabled after plugin activation. You must enable them from the AI Admin Hub console.

## Configuration tasks

Perform the tasks listed in the following tables to enable the respective AI skill or feature.

|AI feature|Configuration task|
|----------|------------------|
|[Nurturing leads using agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/help-nurture-new-leads-agentic-workflow.md)|[Nurturing leads using agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/help-nurture-new-leads-agentic-workflow.md)|
|[CRM conversational query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/manage-opportunity-records.md)|[CRM conversational query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/crm-conversational-query.md)|
|[Summarize opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-som-summarize-opportunity.md)|[Customize the opportunity summarization skill in ServiceNow Otto for Sales Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/customize-opportunity-summarization-skill-now-assist-som.md)|
|[View opportunity scores and insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-opty-scores-insights.md)|[Set up ML-based opportunity scoring and insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-opty-score-insights.md)|
|[AI sales activity association](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-ai-sales-activity-association.md)|[Install AI sales activity association](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-ai-sales-activity-association.md)|

|AI feature|Configuration task|
|----------|------------------|
|[Summarize a quote using quote summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/summarize-quote.md)|[Customize a quote summarization skill in ServiceNow Otto for Configure, Price, Quote \(CPQ\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/customize-quote-summarization-skill.md)|
|[Using Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/use-advanced-approval-mgmt-ai.md)|[Configuring Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-advanced-approval-mgmt-ai.md)|

|AI feature|Configuration task|
|----------|------------------|
|[Summarize an order using Summarization for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-mgmt-summarize-order.md)|[Customize an order summarization skill in ServiceNow Otto for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/customize-order-summarization-skill-now-assist-order-management.md)|
|[Manage order operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-business-portal.md)|[Configuring the Manage Order Operations application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-manage-order-operations.md)|
|[Manage invoice operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-business-portal.md)|[Configuring the Manage Invoice Operations application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-manage-invoice-operations.md)|

## Skills in global domain reuse

By default, all skills exist in the global domain. When you use AI in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, AI only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

**Parent Topic:**[Configuring Sales Customer Relationship Management applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-configuring.md)

**Related topics**  


[AI capabilities in Sales CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/ai-capabilities-sales-crm.md)

[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)

