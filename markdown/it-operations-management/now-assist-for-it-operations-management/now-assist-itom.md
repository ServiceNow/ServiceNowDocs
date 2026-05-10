---
title: Now Assist for ITOM
description: Use the ServiceNow Now Assist for ITOM application to analyze alerts in Event Management. Alert analyses include a human-readable brief of the alert and technical information to help you investigate the alert more effectively.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [generative AI for IT Operations Management, generative AI for ITOM, alert analysis]
breadcrumb: [IT Operations Management]
---

# Now Assist for ITOM

Use the ServiceNow® Now Assist for ITOM application to analyze alerts in Event Management. Alert analyses include a human-readable brief of the alert and technical information to help you investigate the alert more effectively.

## Get started

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

-   Foundation: AI basics to deliver insights
-   Advanced: AI to boost productivity across relevant use cases
-   Prime: Act autonomously with all AI assets, and create your own

For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

For information about AI assets that are available on the ServiceNow AI Platform, see the following topics:

-   [Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills.md)
-   [Now Assist agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sn-aia-use-cases-list.md)

<table id="table_arj_d2f_l1c" class="nav-card"><tbody><tr><td>

[Explore![](../../../reuse/icons/brand-icons/bus-explore.svg)Learn more about Now Assist for ITOM](alert-summary-now-assist.md)

</td><td>

[Configure![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Configure the Now Assist for ITOM application to get started](now-assist-itom-configure.md)

</td><td>

[Use generative AI![](../../../reuse/icons/brand-icons/bus-integration-and-apis.svg)Use generative AI capabilities offered by Now Assist for ITOM](now-assist-itom-use.md)

</td></tr><tr><td>

 

</td><td>

[Use agentic AI![](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg)Use agentic workflows in Now Assist for ITOM](now-assist-itom-ai-agent-workflows.md)

</td><td>

 

</td></tr></tbody>
</table>**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some Now Assist products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

**Note:** Currently, Otto for ITOM only analyzes tag-based, rule-based, and Log Analytics alert groups. For all other alert group types, it only analyzes the parent alert.

## Dependencies

For a list of Otto for ITOM plugin dependencies, see [Applications installed with Now Assist for ITOM](../reference/app-now-assist-itom.md).

## Troubleshoot and get help

-   [ServiceNow Community on AI and Intelligence](https://www.servicenow.com/community/ai-intelligence-articles/tkb-p/ai-platform-kb)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

**Important:** Don't use Now Assist for ITOM for critical security alerts.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [Now Assist documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

**Related topics**  


[Explore Now Assist for ITOM](alert-summary-now-assist.md)

