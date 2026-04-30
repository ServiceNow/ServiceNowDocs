---
title: Get regulatory analysis agentic workflow
description: The get regulatory analysis workflow provides AI-driven insights into regulatory alerts, identifying impacted areas, compliance gaps, and recommended actions for risk mitigation.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-11-10"
reading_time_minutes: 6
keywords: [Now Assist, regulatory analysis, agentic workflow, Integrated Risk Management]
breadcrumb: [Explore, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Get regulatory analysis agentic workflow

The get regulatory analysis workflow provides AI-driven insights into regulatory alerts, identifying impacted areas, compliance gaps, and recommended actions for risk mitigation.

## Get regulatory analysis agentic workflow overview

If you have the RCM user \[sn\_grc\_reg\_change.user\] role and the sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user role, you can analyze and enrich regulatory alerts using the get regulatory analysis agentic workflow in the Now Assist panel.

This workflow uses web search to enhance alert context, summarizes the alert, and recommends potential impacts on citations, policies, and control objectives to support faster and more accurate compliance decisions.

After the workflow is started, it combines multiple AI agents to perform key activities: enriching the alert with external context, generating recommendations, and structuring outputs for clarity.

Key Inputs:

Regulatory alert fields: Title, Description.

Processing Jobs:

-   Regulatory alert enrichment agent: Performs web search to enrich alert context and updates the enriched insights.
-   Regulatory alert recommendation agent: Generates recommendations for impacted areas \(citations, controls, policies\) based on alert content and templates.

Key Outputs:

-   Enriched insights with key dates, fines, and source references
-   Categorized recommendations for impacted areas
-   Option to accept recommendations and convert them into actionable compliance tasks

You can activate it by selecting **Get analysis** from the Ask Now Assist action menu on a regulatory alert page or by selecting **Get Regulatory Analysis** from the Now Assist panel.

By reducing manual research and supporting decision-making, the workflow helps organizations address compliance requirements across multiple regulatory frameworks while providing a structured approach for accuracy, scalability, and operational efficiency.

For more information, see [Use agentic AI in Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/concept/use-agentic-ai-in-risk-sustainability.md), [Activate the get regulatory analysis agentic workflow](../task/activate-rcm-agent-workflow.md), and [Analyze and enrich regulatory alerts](../task/get-rcm-reg-insight.md).

## Benefits of the workflow

-   Comprehensive AI-driven Impact Analysis: Identifies impacted controls, policies, and citations from regulatory alerts, enriches them with external context, and leverages generative AI with predictive models to suggest mitigation steps. Continuously improves recommendations through machine learning feedback loops and enables immediate conversion of accepted suggestions into actionable tasks for compliance teams.
-   Scalable and configurable: Supports multiple regulatory domains and record types, allowing customization of analysis parameters and display options.
-   Compliance accuracy: Delivers AI-powered insights to support better decision-making.
-   Manual effort reduction: Automates regulatory impact analysis to help save time and resources.
-   Clear visibility: Highlights affected areas to support faster prioritization and response.
-   Enhanced scalability: Enables organizations to manage multiple regulatory frameworks efficiently.
-   Enriched alerts with external context: Adds relevant information for better prioritization of compliance actions.
-   Automatic classification and summarization: Helps accelerate and reduce manual review.
-   Immediate task creation: Enables users to convert accepted recommendations into actionable tasks seamlessly.
-   Now Assist panel integration: Offers a unified experience for accessing generative AI capabilities within Regulatory Change Management \( RCM\).

**Note:** Only users with sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user roles can access this workflow.

## Now Assist in RCM agentic workflows

The following agentic workflows are available in Now Assist in RCM:

<table id="table_okm_2lg_dhc"><thead><tr><th>

Workflow

</th><th>

Description

</th><th>

User

</th></tr></thead><tbody><tr><td>

Get regulatory analysis agentic workflow

</td><td>

Analyze and enrich regulatory alerts by using the get regulatory analysis agentic workflow in the Now Assist panel. This agentic workflow uses web search to enhance alert context and recommends potential impacts on citations, policies, and control objectives to support faster and more accurate compliance decisions. For more information, see [Activate the get regulatory analysis agentic workflow](../task/activate-rcm-agent-workflow.md)and [Analyze and enrich regulatory alerts](../task/get-rcm-reg-insight.md).

</td><td>

sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user

</td></tr><tr><td>

Generate regulatory action plan agentic workflow

</td><td>

Generate regulatory action plans by using the generate regulatory action plan agentic workflow in the Now Assist panel. This agentic workflow analyzes impacted areas and similar historical alerts to create change tasks and action tasks that help implement regulatory change.For more information, see [Activate the generate regulatory action plan agentic workflow](../task/activate-rcm-agent-actions-workflow.md) and [Generate regulatory action plans](../task/generate_regulatory_action_plans.md).

</td><td>

sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user

</td></tr></tbody>
</table>**Note:** The get regulatory analysis agentic workflow relies on recommendation templates and alert configurations to generate actionable insights and tasks. Ensure that templates are properly set up and alerts are categorized to support workflow execution. For more information, see [Recommendation contexts and templates](../../grc-rcm/concept/recommendation-contexts.md), [Create a recommendation context](../../grc-rcm/task/configure-recommendation-context.md), and [Create a recommendation template](../../grc-rcm/task/create-a-recommendation-template.md).

**Related topics**  


[Exploring Now Assist in Regulatory Change Management \(RCM\)](../../grc-rcm/concept/rcm-exploring-now-assist-for-irm.md)

[Supporting information for Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/concept/now-assist-irm-supporting-info.md)

[Analyze and enrich regulatory alerts](../task/get-rcm-reg-insight.md)

[Generate regulatory action plans](../task/generate_regulatory_action_plans.md)

