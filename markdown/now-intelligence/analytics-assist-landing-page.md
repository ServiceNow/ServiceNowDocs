---
title: Generate or export dashboards and data visualizations in the Now Assist panel
description: Generate and export Platform Analytics artifacts from conversational interactions. For example, ask for information about the number of open incidents and get a single-score data visualization. Then export that visualization as a PDF file, all in the Now Assist panel.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [generative AI, chat skills]
breadcrumb: [Now Assist in Platform Analytics, Platform Analytics]
---

# Generate or export dashboards and data visualizations in the Now Assist panel

Generate and export Platform Analytics artifacts from conversational interactions. For example, ask for information about the number of open incidents and get a single-score data visualization. Then export that visualization as a PDF file, all in the Now Assist panel.

## Get started

<table id="table_yj4_1lk_12c" class="nav-card"><tbody><tr><td>

[Explore![](../../../reuse/icons/brand-icons/bus-explore.svg)Learn more about how you can work with Platform Analytics in the Now Assist panel](../concept/exploring-analytics-assist.md)

</td><td>

[Configure![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Enable visualization generation and export skills for an instance](../concept/configuring-now-ass-skills-pa.md)

</td><td>

[Generate data visualizations![](../../../reuse/icons/brand-icons/bus-app-creator.svg)How to create data visualizations conversationally in the Now Assist panel](../task/use-dv-generation.md)

</td></tr><tr><td>

[Export dashboards and data visualizations![](../../../reuse/icons/brand-icons/bus-supervised-machine-learning.svg)Use AI to export dashboards and data visualizations conversationally in the Now Assist panel](../task/export-db-dv-now-assist-panel.md)

</td><td>

[Reference![](../../../reuse/icons/brand-icons/bus-learn.svg)Roles and tables that are included with the data visualization generation and export skills](analgen-reference.md)

</td><td>

 

</td></tr></tbody>
</table>**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some Now Assist products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect information from tables and indicators that will be used to generate analytics. For example, information from the Incident table or the Number of open incidents indicator could be collected for requests for incident data visualizations. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://www.servicenow.com/docs/access?context=opt-out-of-data-sharing-for-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

For more information, see the [Now Assist documentation](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

-   **[Explore generating or exporting dashboards and visualizations in the Now Assist panel](../concept/exploring-analytics-assist.md)**  
Generate and export Platform Analytics artifacts from conversational interactions. For example, ask for information about the number of open incidents and get a single-score data visualization. Then export that visualization as a PDF file, all in the Now Assist panel.
-   **[Configuring Now Assist panel skills for Platform Analytics](../concept/configuring-now-ass-skills-pa.md)**  
Activate the skills for generating and exporting Platform Analytics dashboards and data visualizations from conversations in the Now Assist panel.
-   **[Generate visualizations in the Now Assist panel](../task/use-dv-generation.md)**  
Request generative AI to create a visualization of data that you want to see. If you are on a dashboard that you can edit, you can add the visualization to that dashboard.
-   **[Export dashboards and data visualizations from the Now Assist panel](../task/export-db-dv-now-assist-panel.md)**  
Export or schedule the export of dashboards and data visualizations conversationally through AI instead of going through the Platform Analytics user interface.
-   **[Reference for dashboard and visualization skills](analgen-reference.md)**  
Information about the roles, tables, and scheduled jobs included with the data visualization generation and dashboard and visualization export skills.

**Parent Topic:**[Now Assist in Platform Analytics](../../performance-analytics/concept/now-assist-platform-analytics.md)

