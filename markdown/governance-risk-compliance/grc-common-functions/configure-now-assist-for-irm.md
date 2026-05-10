---
title: Configure Now Assist for Integrated Risk Management \(IRM\)
description: If you have the admin role, you can configure Now Assist for IRM so that your agents can use the generative AI skills in the IRM workspace.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [configure]
breadcrumb: [Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Configure Now Assist for Integrated Risk Management \(IRM\)

If you have the admin role, you can configure Now Assist for IRM so that your agents can use the generative AI skills in the IRM workspace.

## Now Assist for IRM Configuration overview

**Important:** After installing Now Assist for IRM, all Now Assist for IRM skills and agentic workflows are activated by default.

Use the Now Assist Admin console to configure Now Assist for IRM. This console contains everything that you need to install plugins and configure the generative AI skills. For additional information, see [Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

For earlier versions, go to [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/application-manager.md) to upgrade it to a later version.

For information about configuring generative AI skills and prompts, see [Configuring Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-na-landing.md).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Now Assist for IRM plugins

Activate the Now Assist for IRM store app \(sn\_irm\_gen\_ai\) to use the skills and agentic workflows.

This store app has the following dependencies:

-   Now Assist Platform

    Integrates generative AI into ServiceNow workflows, enabling intelligent assistance through summarization, content creation, conversational AI, and agentic workflows for IT, HR, and compliance processes. For more information, see [Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

-   GRC Common Generative AI

    Provides foundational AI capabilities for Governance, Risk, and Compliance \(GRC\), automating tasks like risk assessments and compliance documentation while helping ensure consistency across GRC workflows.

-   GRC Shared Generative AI

    Delivers centralized generative AI services for multiple GRC domains, supporting shared governance, secure automation, and integration with AI systems for compliance and risk management.

-   GRC Compliance Generative AI

    Enables continuous monitoring, predictive risk management, and automated regulatory mapping to transform compliance from periodic audits to real-time oversight.

-   Recommendation Template

    Provides actionable, AI-powered insights seamlessly within the user interface. The framework offers rich contextual details about recommendations to enable users to make informed decisions and take necessary follow-up actions effortlessly. Admin users can set up contexts for recommendations, and compliance users can review the recommendations for implementation. For more information, see [Recommendation contexts and templates](../../grc-rcm/concept/recommendation-contexts.md).


For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

**Note:** For more information on Retrieval Augmented Generation \(RAG\) and Retention policies, see [Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/indexed-sources-ais.md) and [User data usage policy for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/user-data-usage-policy-now-assist.md).

