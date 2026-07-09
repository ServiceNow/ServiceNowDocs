---
title: AI in RPA Hub
description: Use Now Assist for RPA Hub to accelerate automation development with AI. Instead of writing code or configuring workflows manually, you can describe what you need in natural language and Now Assist generates automations, activities, and logic rules. You can preview generated code before deploying, ensuring it meets your requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/explore-now-assist-rpa-hub.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist for RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# AI in RPA Hub

Use Now Assist for RPA Hub to accelerate automation development with AI. Instead of writing code or configuring workflows manually, you can describe what you need in natural language and Now Assist generates automations, activities, and logic rules. You can preview generated code before deploying, ensuring it meets your requirements.

## Now Assist for RPA Hub overview

The Now Assist for RPA Hub application offers generative AI capabilities to accelerate your automation development process. The following generative AI capabilities are available in the RPA Desktop Design Studio application:

-   Build simple, brand-new automations quickly and efficiently.
-   Easily add new activities to existing automations, ensuring modularity and scalability.
-   Enhance the automation logic with text instructions, either in an empty activity or by selecting a component in an existing one.

Both new and experienced users can develop and build faster automation by using the Now Assist for RPA Hub application.

## Now Assist skill - RPA bot generation

The RPA bot generation skill helps users to build an automation that is based on text input. Access the RPA bot generation skill from the RPA Desktop Design Studio user interface.

For more information, see [Robotic Process Automation \(RPA\) bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-bot-generation.md).

## How to use the RPA bot generation skill

By using the RPA bot generation skill, your users can perform the following tasks:

-   **Create an automation with AI**

    Create an automation from text instructions and preview the options from the RPA Desktop Design Studio user interface. First, your user selects the **Create automation** option and then selects the **Build with Now Assist** option to get started. For more information, see [Create an automation with Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-automation-now-assist.md).

    The following example shows how an automation is created with the Now Assist in the RPA Desktop Design Studio user interface.

    \[Omitted image "build-now-assist-screen-rpa.png"\] Alt text: RPA Desktop Design Studio user interface that shows the \(1\) Create automation option and \(2\) Build with Now Assist option.

-   **Create an activity with AI**

    Create an activity from the text instructions and preview options. For more information, see [Create an activity with Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-activity-now-assist.md).

    The following example shows how an activity is created with Now Assist in the RPA Desktop Design Studio user interface.

    \[Omitted image "create-activity-now-assist-rpa.png"\] Alt text: RPA Desktop Design Studio user interface that shows the New activity by using Now Assist option.

-   **Extend automation logic with AI**

    Enhance an automation logic by using text instructions with the **Build automation** option, either from an empty activity or by selecting a component in an existing activity. For more information, see [Build an automation with Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/build-automation-now-assist.md).

    The following example shows an automation logic that is built with Now Assist from an empty activity on the design surface in the RPA Desktop Design Studio user interface.

    \[Omitted image "canvas-level-inline-prompt.png"\] Alt text: RPA Desktop Design Studio user interface that shows the Build automation option from an empty activity on the design surface.

    The following example shows an automation logic that is built with Now Assist by selecting a component in the RPA Desktop Design Studio user interface.

    \[Omitted image "comp-level-inline-prompt-example.png"\] Alt text: RPA Desktop Design Studio user interface that shows the Build automation option after a component is selected, for example, Start.


## Licensing requirements

The Now Assist for RPA Hub application requires a Workflow Data Fabric \(previously known as Automation Engine\) license and a Now Assist for Creator license.

## Application information

Activate the Now Assist for RPA Hub store app \(com.sn\_rpa\_na\) to use the RPA bot generation skill.

This store app has the following dependencies:

-   RPA Hub \(com.sn\_rpa\_fdn\)
-   Now Assist for Creator \(com.sn\_now\_creator\)

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

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

**Note:** We have controls in place to enable/disable the data collection and data processing.

