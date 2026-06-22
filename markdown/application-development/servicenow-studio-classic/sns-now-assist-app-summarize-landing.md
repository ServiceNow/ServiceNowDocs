---
title: Now Assist for app summary generation in ServiceNow Studio
description: Use the ServiceNow Now Assist for Creator application to use generative AI for summarizing an app. With a single button, Now Assist for Creator generates the app summary that you can then copy to the app description, or use to find duplicate apps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/sns-now-assist-app-summarize-landing.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist tools and AI files, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Now Assist for app summary generation in ServiceNow Studio

Use the ServiceNow® Now Assist for Creator application to use generative AI for summarizing an app. With a single button, Now Assist for Creator generates the app summary that you can then copy to the app description, or use to find duplicate apps.

\[Omitted image "now-assist-app-summary.png"\] Alt text: Summarize what an app does

## Get started

<table id="table_wgj_xvj_12c" class="nav-card presentation"><tbody><tr><td>

[Explore\[Omitted image "bus-explore.svg"\] Alt text:Learn about summarizing apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-exploring-now-assist-app-summarize.md)

</td><td>

[Configure\[Omitted image "bus-sdlc.svg"\] Alt text:Set up app summary generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-config-now-assis-app-summarize.md)

</td></tr><tr><td>

[Use\[Omitted image "bus-integration-and-apis.svg"\] Alt text:Generate a summary of your app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/summarize-an-app-in-servicenow-studio.md)

</td><td>

[Reference\[Omitted image "bus-learn.svg"\] Alt text:Get details about properties, roles, and more](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-now-assist-app-summarize-reference.md)

</td></tr></tbody>
</table>**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some Now Assist products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## Helpful resources

Some ServiceNow resources that can provide you with helpful information are:

-   **\[Omitted image "dcx-icon-community.svg"\]ServiceNow Community**

    [ServiceNow Community](https://www.servicenow.com/community/now-assist/ct-p/now-assist)

-   **\[Omitted image "dcx-icon-support.svg"\] Support**




## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect information about applications \(and associated application files\) in which App generation was utilized. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/opt-out-of-data-sharing-for-now-assist.md).

-   **[Exploring Now Assist for app summary generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-exploring-now-assist-app-summarize.md)**  
With the Now Assist for Creator application, you can generate a summary of an app. You can then copy the summary to the description for the app, and use it to check for duplicate apps.
-   **[Configuring Now Assist for app summary generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-config-now-assis-app-summarize.md)**  
Enable the app summary generation skill in the Now Assist for Creator application so that you can get started with summarizing applications.
-   **[Summarize the contents of an app in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/summarize-an-app-in-servicenow-studio.md)**  
Generate a summary of your app using Now Assist for Creator in ServiceNow Studio. After reviewing the summary, you can use it as a description for your app.
-   **[Now Assist for app summary generation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-now-assist-app-summarize-reference.md)**  
The following roles are required for use with the Now Assist for Creator app summary generation skill.

**Parent Topic:**[Now Assist tools and AI files in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/working-with-now-assist-tools-sn-studio.md)

