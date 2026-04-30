---
title: Now Assist in AI Search
description: The Now Assist in AI Search ServiceNow Store application combines the power of search with a Large Language Model \(LLM\) to provide actionable AI-generated or AI-selected answers in user searches. By constraining the context passed to the LLM, Now Assist in AI Search can increase the likelihood that LLM responses are grounded in indexed content.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Now Assist in AI Search

The Now Assist in AI Search ServiceNow® Store application combines the power of search with a Large Language Model \(LLM\) to provide actionable AI-generated or AI-selected answers in user searches. By constraining the context passed to the LLM, Now Assist in AI Search can increase the likelihood that LLM responses are grounded in indexed content.

## Now Assist in AI Search overview

In Service Portal, Virtual Agent, Employee Center, and global searches, Now Assist in AI Search includes the following Genius Result configurations:

-   **[Now Assist Multi-Content Response Genius Results](../concept/now-assist-multi-content-qna-genius-results.md)**

    Now Assist Multi-Content Response Genius Results use your chosen LLM to generate Q&amp;A Genius Result answers synthesized from a variety of content sources. Answers can include content from knowledge articles, Service Catalog items, Knowledge Graph schema nodes, enhanced chat searches and conversations, and external content documents and attachments.

-   **[Now Assist Q&amp;A Genius Results](../concept/now-assist-qna-genius-results.md)**

    Now Assist Q&amp;A Genius Results use the Now LLM Service to generate actionable Q&amp;A Genius Result answers from the most relevant knowledge article results.

-   **[External Content Q&amp;A Genius Results](../concept/external-content-qna.md)**

    External Content Q&amp;A Genius Results generate actionable Q&amp;A Genius Result answers from documents in your Microsoft SharePoint Online instance.

-   **[Now Assist Actions Genius Results](../concept/now-assist-catalog-ordering-gr.md)**

    Now Assist Actions Genius Results use the Now LLM Service to select, filter, and display the most relevant Catalog Item and Virtual Agent topic results as answers.


All Now Assist Genius Result answers augment the user's search results, displaying as actionable answer cards. For reference, each answer card includes links to its source records or external documents.

## Get started

<table id="table_wzb_rmc_wyb" class="nav-card"><tbody><tr><td>

[Install![](../../../reuse/icons/brand-icons/bus-power.svg)Activate the Now Assist in AI Search plugin on your instance](../task/install-now-assist-ais.md)

</td><td>

[Configure![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Configure Now Assist in AI Search Genius Results for use in Service Portal, Virtual Agent, Employee Center, and global search](../concept/configuring-now-assist-ais.md)

</td><td>

[Reference![](../../../reuse/icons/brand-icons/bus-learn.svg)View components installed with Now Assist in AI Search](../concept/reference-now-assist-ais.md)

</td></tr></tbody>
</table>**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some Now Assist products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## Language support

Now Assist in AI Search natively supports searches, content, and answers in English. Additional languages are supported through Dynamic Translation. For details on translation functionality and supported languages, see [Dynamic Translation for Now Assist Q&amp;A Genius Results](../concept/dynamic-translation-na-gr.md).

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Further, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://www.servicenow.com/docs/access?context=opt-out-of-data-sharing-for-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

For more information, see the [Now Assist documentation](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

