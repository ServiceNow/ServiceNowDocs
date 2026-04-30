---
title: Configure Now Assist for Integrated Risk Management \(IRM\)
description: If you have the admin role, you can configure Now Assist for IRM so that your agents can use the generative AI skills in the IRM workspace.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-10-19"
reading_time_minutes: 2
keywords: [configure]
breadcrumb: [Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Configure Now Assist for Integrated Risk Management \(IRM\)

If you have the admin role, you can configure Now Assist for IRM so that your agents can use the generative AI skills in the IRM workspace.

## Now Assist for IRM Configuration overview

**Important:** After installing Now Assist for IRM, all Now Assist for IRM skills and agentic workflows are activated by default.

Use the Now Assist Admin console to configure Now Assist for IRM. This console contains everything that you need to install plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

For earlier versions, go to [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) to upgrade it to a later version.

For information about configuring generative AI skills and prompts, see [General guidelines for writing instructions for generative AI large language models \(LLMs\)](https://www.servicenow.com/docs/access?context=capabilities-bundle-landingpage&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Now Assist for IRM plugins

Activate the Now Assist for IRM store app \(sn\_irm\_gen\_ai\) to use the skills and agentic workflows.

This store app has the following dependencies:

-   Now Assist Platform

    Integrates generative AI into ServiceNow workflows, enabling intelligent assistance through summarization, content creation, conversational AI, and agentic workflows for IT, HR, and compliance processes. For more information, see [Now Assist Platform](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   GRC Common Generative AI

    Provides foundational AI capabilities for Governance, Risk, and Compliance \(GRC\), automating tasks like risk assessments and compliance documentation while helping ensure consistency across GRC workflows.

-   GRC Shared Generative AI

    Delivers centralized generative AI services for multiple GRC domains, supporting shared governance, secure automation, and integration with AI systems for compliance and risk management.

-   GRC Compliance Generative AI

    Enables continuous monitoring, predictive risk management, and automated regulatory mapping to transform compliance from periodic audits to real-time oversight.

-   Recommendation Template

    Provides actionable, AI-powered insights seamlessly within the user interface. The framework offers rich contextual details about recommendations to enable users to make informed decisions and take necessary follow-up actions effortlessly. Admin users can set up contexts for recommendations, and compliance users can review the recommendations for implementation. For more information, see [Recommendation contexts and templates](../../grc-rcm/concept/recommendation-contexts.md).


For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

**Note:** For more information on Retrieval Augmented Generation \(RAG\) and Retention policies, see [Indexed sources in AI Search](https://www.servicenow.com/docs/access?context=indexed-sources-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [User data usage policy for Now Assist](https://www.servicenow.com/docs/access?context=user-data-usage-policy-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

