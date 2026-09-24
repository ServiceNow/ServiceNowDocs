---
title: Implementing AI on the ServiceNow AI Platform
description: Preparing for an AI implementation involves more than installing plugins — your data, applications, and AI policy each shape the result. Working through these foundations before activation reduces rework whether you're enabling conversational catalogs, automating content generation, or enriching user interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sn-ai-implementation-landing.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Getting started with AI, Enable AI Experiences]
---

# Implementing AI on the ServiceNow AI Platform

Preparing for an AI implementation involves more than installing plugins — your data, applications, and AI policy each shape the result. Working through these foundations before activation reduces rework whether you're enabling conversational catalogs, automating content generation, or enriching user interactions.

## Get started

<table id="table_vhh_f41_zgc" class="nav-card presentation"><tbody><tr><td>

[Organization and tools\[Omitted image "bus-optimize-manage.svg"\] Alt text:Learn about the applications and features that make up the ServiceNow AI experience.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/sn-ai-impl-overview-tools.md)

</td><td>

[Roles and responsibilities\[Omitted image "bus-3-person.svg"\] Alt text:Identify the administrative roles required to install, configure, and manage each ServiceNow AI capability.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-roles-responsibilities-ai-admin.md)

</td><td>

[Glossary\[Omitted image "bus-learn.svg"\] Alt text:Look up definitions for ServiceNow AI terminology.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-glossary.md)

</td></tr></tbody>
</table>**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

Additional implementation information is available on [Now Create](https://learning.servicenow.com/nowcreate).

For additional Now Assist resources, see [Additional resources for AI products and solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-additional-resources.md).

**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some AI products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. Customers can opt out of future data collection at any time, as described in the [AI Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

