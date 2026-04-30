---
title: Supporting information for Now Assist for Integrated Risk Management \(IRM\)
description: Get a quick overview of the important information that is related to the Now Assist for Integrated Risk Management \(IRM\) application.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Explore, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Supporting information for Now Assist for Integrated Risk Management \(IRM\)

Get a quick overview of the important information that is related to the Now Assist for Integrated Risk Management \(IRM\) application.

## Supported versions

Now Assist for IRM is supported starting from the Yokohama patch 3 release.

-   GRC: Regulatory Change Management application: version 20.1.2
-   Now Assist for IRM application: version 20.1.1

## Supported language models

You can use Now LLM Service, Now LLM LTS, Azure OpenAI, Google Gemini, or Anthropic Claude on AWS, as the AI model provider for all Now Assist skills and AI agents. For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Supported user interfaces

The Now Assist for IRM application includes the skills and agentic workflows that are listed in the following table.

<table id="table_dhw_xcj_d2c"><thead><tr><th>

Interface

</th><th>

Skill

</th><th>

Workflow

</th></tr></thead><tbody><tr><td>

Risk Workspace

</td><td>

-   Issue summarization
-   Risk assessment summarization
-   Recommendation for similar control objectives
-   Rationalization

</td><td rowspan="3">

-   Optimize GRC issue resolution agentic workflow
-   Get regulatory analysis agentic workflow
-   Generate regulatory action plan agentic workflow

</td></tr><tr><td>

Core UI

</td><td>

Issue summarization

</td></tr><tr><td>

Compliance Workspace

</td><td>

-   Issue summarization
-   Regulatory alert summarization
-   Regulatory alert impacted citations
-   Regulatory alert impacted control objectives
-   Regulatory alert impacted controls
-   Regulatory alert impacted policies

</td></tr></tbody>
</table>## Security enhancements

For information about security enhancements for AI agents, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Application information

Activate the Now Assist for IRM store app \(sn\_irm\_gen\_ai\) to use the skills and agentic workflows.

This store app has the following dependencies:

-   Now Assist Platform

    Integrates generative AI into ServiceNow workflows, enabling intelligent assistance through summarization, content creation, conversational AI, and agentic workflows for IT, HR, and compliance processes. For more information, see [Now Assist Platform](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

-   GRC Common Generative AI

    Provides foundational AI capabilities for Governance, Risk, and Compliance \(GRC\), automating tasks like risk assessments and compliance documentation while helping ensure consistency across GRC workflows.

-   GRC Shared Generative AI

    Delivers centralized generative AI services for multiple GRC domains, supporting shared governance, secure automation, and integration with AI systems for compliance and risk management.

-   GRC Compliance Generative AI

    Enables continuous monitoring, predictive risk management, and automated regulatory mapping to transform compliance from periodic audits to real-time oversight.

-   Recommendation Template

    Provides actionable, AI-powered insights seamlessly within the user interface. The framework offers rich contextual details about recommendations to enable users to make informed decisions and take necessary follow-up actions effortlessly. Admin users can set up contexts for recommendations, and compliance users can review the recommendations for implementation. For more information, see [Recommendation contexts and templates](../../grc-rcm/concept/recommendation-contexts.md).


For more information, see [Configure Now Assist for Integrated Risk Management \(IRM\)](configure-now-assist-for-irm.md).

