---
title: Supporting information for Now Assist for Integrated Risk Management \(IRM\)
description: Get a quick overview of the important information that is related to the Now Assist for Integrated Risk Management \(IRM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/now-assist-irm-supporting-info.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Explore, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Supporting information for Now Assist for Integrated Risk Management \(IRM\)

Get a quick overview of the important information that is related to the Now Assist for Integrated Risk Management \(IRM\) application.

## Supported versions

Now Assist for IRM is supported starting from the Yokohama Patch 3 release.

-   GRC: Regulatory Change Management application: version 20.1.2
-   Now Assist for IRM application: version 20.1.1

## Supported language models

You can use Azure OpenAI, Google Gemini, or Anthropic Claude on AWS as the AI model providers for supported Now Assist capabilities. Model availability depends on the feature and your Now Assist subscription. For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md).

As of version 22.4.0, Now Assist for IRM supports Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini models in addition to the previously supported models. The default model for the issue summarization skill is Azure OpenAI gpt-5.4-mini.

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

-   Issue Summarization
-   Risk Assessment Summarization
-   Recommendation for similar control objectives
-   Rationalization

</td><td rowspan="3">

-   Optimize GRC issue resolution agentic workflow
-   Get Regulatory Insights agentic workflow
-   Generate Regulatory Action Plans agentic workflow

</td></tr><tr><td>

Core UI

</td><td>

Issue Summarization

</td></tr><tr><td>

Compliance Workspace

</td><td>

-   Issue Summarization
-   Regulatory alert summarization
-   Regulatory alert impacted citations
-   Regulatory alert impacted control objectives
-   Regulatory alert impacted controls

</td></tr></tbody>
</table>## Security enhancements

For information about security enhancements for AI agents, see [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md).

## Application information

Activate the Now Assist for IRM store app \(sn\_irm\_gen\_ai\) to use the skills and agentic workflows.

This store app has the following dependencies:

-   Now Assist Platform.
-   GRC Common generative AI.
-   GRC Shared generative AI.
-   GRC Compliance generative AI.
-   Recommendation Template.

For more information, see [Configure Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/configure-now-assist-for-irm.md).

