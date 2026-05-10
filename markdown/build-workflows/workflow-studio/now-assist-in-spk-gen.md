---
title: Use Now Assist to create spokes and build actions
description: Use Now Assist in Spoke Generator to create spokes and actions by providing the required third-party API documentation snippet as an input.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Building spokes using Spoke Generator, Workflow Studio, Build workflows]
---

# Use Now Assist to create spokes and build actions

Use Now Assist in Spoke Generator to create spokes and actions by providing the required third-party API documentation snippet as an input.

## Capabilities

You can build custom spokes for the required third-party application by copying and pasting the required snippets from the API documentation. This feature is useful when the required third-party application doesn't have an OpenAPI Specification or Postman collection. This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

Spoke Generation skill is supported on these versions and later releases.

-   Zurich
-   Spoke Generator v4.1.0
-   Workflow Studio v28.0

## Skill version

Spoke Generation skill v1.0.4 is the latest version.

## App version

Now Assist for Spoke Generation v1.5.12 is the latest version.

## Activation of the spoke generation skill

The spoke generation skill offers generative AI capabilities to build spokes. This skill is installed with the Now Assist for Creator \(sn\_now\_creator\) application. You can install this application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

After installing the Now Assist for Creator \(sn\_now\_creator\) application, activate the Spoke Generation skill in the [Now Assist for Creator feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/now-assist-for-creator-landing.md) from the Now Assist Admin console.

![Spoke Generation skill in Now Assist Admin console.](../images/creator-skill-now-assist.png "Spoke Generation skill in Now Assist Admin console")

-   For information about the Now Assist Admin console, see [Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).
-   For steps to activate the required skill, see [Activate a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-a-now-assist-skill.md).

**Important:** Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Please check for availability updates in future releases.

**Important:** Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect information about scripts \(and associated script records\) in which Now Assist for code generation is called. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [Now Assist documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

