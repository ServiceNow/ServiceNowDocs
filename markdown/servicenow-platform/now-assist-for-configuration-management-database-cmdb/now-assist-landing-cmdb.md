---
title: Now Assist for Configuration Management Database \(CMDB\)
description: Use ServiceNow Now Assist for Configuration Management Database \(CMDB\) to improve the quality of CMDB data, search the CMDB quickly, find and remedy issues with Service Graph Connector import sets, view comprehensive summaries for CIs, manually create CIs, and accelerate the process of remediating duplicate CIs.
locale: en-US
release: yokohama
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-01-28"
reading_time_minutes: 6
breadcrumb: [CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Now Assist for Configuration Management Database \(CMDB\)

Use ServiceNow® Now Assist for Configuration Management Database \(CMDB\) to improve the quality of CMDB data, search the CMDB quickly, find and remedy issues with Service Graph Connector import sets, view comprehensive summaries for CIs, manually create CIs, and accelerate the process of remediating duplicate CIs.

## Get started

<table id="table_mzj_vxd_rcc" class="nav-card presentation"><tbody><tr><td>

[Explore![](../../../reuse/icons/brand-icons/bus-explore.svg)Learn about Now Assist for CMDB](now-assist-cmdb-exploring.md)

</td><td>

[Configure![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Activate Now Assist for CMDB](now-assist-cmdb-configuring.md)

</td></tr><tr><td>

[Using skills in Now Assist for CMDB![](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg)](now-assist-cmdb-using-skills.md)[Use Now Assist for CMDB skills to view a concise summary of key CI data, to help you to resolve de-duplication tasks, or to reduce debugging and resolution time for failed Service Graph Connector import sets.](../../csdm-implementation/concept/csdm-content-frame-reference.md)

</td><td>

[Using agentic workflows in Now Assist for CMDB![](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg)Apply AI agentic workflows to accelerate results.](now-assist-cmdb-using.md)

</td></tr><tr><td>

[Reference![](../../../reuse/icons/brand-icons/bus-learn.svg)/&gt; Reference topics provide additional information about the property settings that you use to configure and administer Now Assist for CMDB.](../../csdm-implementation/concept/csdm-content-frame-reference.md)

</td><td>

 

</td></tr></tbody>
</table>**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some Now Assist products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## Troubleshoot and get help

-   [Ask questions and explore other resources for  in the ServiceNow Community](https://www.servicenow.com/community/)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now)

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect incident data \(for Incident Assist and Knowledge Assist\) and chat transcripts \(for Chat Assist\). Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://www.servicenow.com/docs/access?context=opt-out-of-data-sharing-for-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

For more information, see the [Now Assist documentation](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Available LLMs

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://www.servicenow.com/docs/access?context=opt-out-of-data-sharing-for-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

For more information, see the [Now Assist documentation](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

