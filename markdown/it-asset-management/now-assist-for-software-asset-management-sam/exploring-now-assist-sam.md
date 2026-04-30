---
title: Exploring Now Assist for Software Asset Management \(SAM\)
description: With the Now Assist for Software Asset Management \(SAM\) application, Software Asset Management managers can use generative AI capabilities for tasks such as generating compliance summaries, optimization recommendations, and automating SaaS user resolution.
locale: en-US
release: yokohama
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Exploring Now Assist for Software Asset Management \(SAM\)

With the Now Assist for Software Asset Management \(SAM\) application, Software Asset Management managers can use generative AI capabilities for tasks such as generating compliance summaries, optimization recommendations, and automating SaaS user resolution.

## Now Assist for SAM overview

The following generative AI capabilities are available:

-   Generate detailed publisher and product summaries to enhance software estate visibility and streamline compliance evaluation.
-   Generate recommended actions to manage software license compliance and optimize licensing spend.
-   Generate user resolution rules to ensure accurate mapping of incoming subscription data to SAM users.

The generative AI skills can be used only by the sam\_user role and the sam\_admin role.

Customizations to In-product display roles for accessing generative AI skills are preserved. For example, if you added an alternative role such as the sam\_admin role instead of the default sam\_user role, the sam\_admin role will retain access, while the sam\_user role will lose access, as per the custom configuration.

The sam-user role also contains the Now Assist Admin User \(sn\_nowassist\_admin.user\) role. This provides the sam\_user role read-only access to the Now Assist Admin to view the generative AI skills.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Now Assist for SAM skills

The Now Assist for SAM application includes generative AI that provides your Software Asset Management managers with an AI-based summary ofproducts and publishers within your organization's software estate.Additionally, you also get AI-powered recommended actions that help you to mitigate license compliance risk.

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


-   **[Supporting information for Now Assist for Software Asset Management \(SAM\)](supporting-information-now-assist-sam.md)**  
Get a quick overview of the important information that is related to the Now Assist for Software Asset Management \(SAM\) application.

**Parent Topic:**[Now Assist for Software Asset Management \(SAM\)](now-assist-sam.md)

