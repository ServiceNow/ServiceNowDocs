---
title: Exploring Now Assist for Software Asset Management \(SAM\)
description: With the Now Assist for Software Asset Management \(SAM\) application, Software Asset Management managers can use generative AI capabilities for tasks such as generating compliance summaries, optimization recommendations, and automating SaaS user resolution.
locale: en-US
release: australia
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Exploring Now Assist for Software Asset Management \(SAM\)

With the Now Assist for Software Asset Management \(SAM\) application, Software Asset Management managers can use generative AI capabilities for tasks such as generating compliance summaries, optimization recommendations, and automating SaaS user resolution.

## Now Assist for SAM overview

The following generative AI capabilities are available:

-   Generate detailed publisher and product summaries to enhance software estate visibility and streamline compliance evaluation.
-   Generate recommended actions to manage software license compliance and optimize licensing spend.
-   Generate user resolution rules to ensure accurate mapping of incoming subscription data to SAM users.
-   Create entitlements by extracting information from software contracts thereby reducing manual effort.

The generative AI skills can be used only by the sam\_user role and the sam\_admin role.

Custom role configurations for accessing generative AI skills are preserved. For example, if you added an alternative role such as the sam\_admin role instead of the default sam\_user role, the sam\_admin role will retain access, while the sam\_user role will lose access, as per the custom configuration.

The sam-user role also contains the Now Assist Admin User \(sn\_nowassist\_admin.user\) role. This provides the sam\_user role read-only access to the Now Assist Admin to view the generative AI skills.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see Large language models on the ServiceNow AI Platform®.

Domain separation is supported in Now Assist for Software Asset Management \(SAM\). For details, see Domain separation in the Now Assist Admin console.

## Now Assist for SAM skills

The Now Assist for SAM application includes generative AI that provides your Software Asset Management managers with an AI-based summary of products and publishers within your organization's software estate.

Additionally, you also get AI-powered recommended actions that help you to mitigate license compliance risk.

-   **Publisher compliance summarization**

    Provides insights into publisher summaries, focusing on software deployment, license compliance, optimizations, and configuration health. The streamlined process highlights critical information about your software assets, making it easier for you to manage licenses and ensure compliance with publisher contracts.

    ![Microsoft compliance summary.](../image/now-assist-summarization.png)

-   **Product compliance summarization**

    Provides insights into specific product summaries for publishers, focusing on software deployment, license compliance, optimization, and issues.

    ![SQL Server product summarization](../image/now-assist-sam-product-summary.png)

-   **Recommended actions**

    Provides a list of recommended actions that you can perform to fix any configuration, maintenance, and optimization related issues to manage software license compliance and optimize licensing spend.

    ![List of recommended actions for a product](../image/now-assist-sam-recommended-actions.png)

-   **SaaS user resolution**

    Use generative AI to automatically analyze incoming SaaS subscription data and generate user resolution rules to map User Principal Names to corresponding user records within the Software Asset Management application.

    **Note:** To effectively use the SaaS user resolution generative skill, ensure that you have the latest compatible versions of both the Software Asset Management plugin and the Software Asset Management - SaaS License Management plugin.

    Upon activation of the SaaS user resolution skill, a series of automated processes are triggered. First, the **Downgrade subscriptions** scheduled job is executed on a cadence, daily or weekly, that depends on your SaaS subscription. After the **Downgrade subscriptions** job is successfully executed, the **SAM - Generate user resolution rule** scheduled job is initiated, creating a new user resolution rule for the relevant SaaS integration profile and resolving all associated users.

-   **Contract entitlement data extraction**

    Use generative AI to provide a streamlined and automated process for extracting licensing data from contracts and generating software entitlements, enhancing productivity and accuracy.

    DocIntel, a ServiceNow tool, is used to extract information from contracts. After data has been extracted from Docintel, a synchronous call is made to the prediction server to predict the product, publisher, and edition based on the product description for each entitlement. The Software Asset Management application performs post processing on the fields extracted from DocIntel to map to the supported values for different entitlement fields.

    **Note:** For more information on DocIntel, see [Document Intelligence documentation](https://servicenow.com/docs/bundle/vancouver-intelligent-experiences/page/administer/document-intelligence/concept/document-intelligence-landing.html).

    DocIntel is an intuitive and flexible application for dynamic businesses with highly variable document processing needs that change over time. DocIntel processes PDFs and images. Following are the image size and page count limits:

    -   10 MB per attachment
    -   10 pages for images \(JPG, JPEG, or PNG\) and 25 pages for PDFs
    **Note:** DocIntel won’t process images or PDFs that exceed the recommended limits. For example, if you upload a PDF consisting of 26 pages, only 25 pages are processed. Similarly, if you upload 11 pages for images, only 10 pages are processed.

    Each document is processed as a separate document task tied to a record in the ITAM Contract Import \[itam\_contract\_import\] table. The document task can be created from a new file uploaded directly or from an existing attachment on the contract record.

    Once the document is uploaded to DocIntel, a flow designer flow is executed to retrieve the values from the document and populate the ITAM Contract Import \[itam\_contract\_import\] table.

    For extracting entitlements from contracts, you can opt in to participate in the Software Asset Management Content Service. The Software Asset Management Content Service is an IT Asset Management shared service that provides users with continual software recognition improvements. For additional details, see [Software Asset Management Content Service](../../software-asset-management2/concept/c_SAMContentService.md).


-   **[Supporting information for Now Assist for Software Asset Management \(SAM\)](supporting-information-now-assist-sam.md)**  
Get a quick overview of the important information that is related to the Now Assist for Software Asset Management \(SAM\) application.

**Parent Topic:**[Now Assist for Software Asset Management \(SAM\)](now-assist-sam.md)

