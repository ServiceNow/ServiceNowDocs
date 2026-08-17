---
title: Generate regulatory action plan agentic workflow
description: The generate regulatory action plan workflow uses generative AI to create actionable compliance steps for regulatory alerts. It supports organizations in organizing risk mitigation activities and maintaining alignment with regulatory requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/regulatory-change-management-service-portal/rcm-agent-actions-workflow.html
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-11-10"
reading_time_minutes: 5
keywords: [Now Assist, regulatory action plan, agentic workflow, Integrated Risk Management]
breadcrumb: [AI in Regulatory Change Management, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Generate regulatory action plan agentic workflow

The generate regulatory action plan workflow uses generative AI to create actionable compliance steps for regulatory alerts. It supports organizations in organizing risk mitigation activities and maintaining alignment with regulatory requirements.

## Generate regulatory action plan agentic workflow overview

If you have the RCM user \[sn\_grc\_reg\_change.user\] role and the sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user role, you can generate regulatory action plans using the generate regulatory action plan agentic workflow in the ServiceNow Otto panel.

This workflow analyzes impacted areas and similar historical alerts to create change tasks and action tasks that help implement regulatory change.

After the workflow is started, the regulatory change task planning agent identifies the optimal steps for working on a regulatory alert by referencing the past similar regulatory alert details and impacted areas of the current regulatory alert, so that the output includes a clear, categorized set of tasks grouped by type, complete with key dates and source references for traceability.

Key Inputs:

-   Impacted areas identified by recommendation skills
-   Regulatory alert details \(Title, Description, Effective date, Compliance date\)
-   Historical alerts for pattern matching

Processing Jobs:

Regulatory change task planning agent: Validates impacted areas, analyzes historical alerts for similar compliance actions, and generates structured action plans grouped by task type \(control updates, policy revisions, citation amendments\).

Key Outputs:

-   Action plan displayed in the **Regulatory tasks** tab
-   Tasks categorized by impacted area type with ownership and timelines
-   Option to accept or dismiss the proposed plan

You can get started by selecting **Generate action plan** from the **Ask ServiceNow Otto** action menu on a regulatory alert page or by selecting **Generate Regulatory Action Plan** from the ServiceNow Otto panel.

Integrated within the ServiceNow Otto panel, this workflow provides a seamless experience for users, helping to reduce manual effort and improve accuracy while supporting multiple regulatory domains and task types.

For more information, see [Use agentic AI in ServiceNow Otto for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/use-agentic-ai-in-risk-sustainability.md), [Activate the Generate regulatory action plan agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/activate-rcm-agent-actions-workflow.md), and [Generate regulatory action plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/generate_regulatory_action_plans.md).

## Benefits of the workflow

-   Automated action plan creation: Eliminates manual drafting by generating structured regulatory action plans for each alert.
-   Leverages historical data: Analyzes similar past alerts and action plans to recommend accurate, proven tasks.
-   Consolidated and organized tasks: Creates change tasks and action tasks grouped by impacted areas for easier assignment and tracking.
-   Improved consistency and accuracy: Reduces variability in compliance responses through AI-driven recommendations.
-   Faster implementation: Converts compliance strategies into actionable tasks with clear ownership and timelines.
-   Integration with ServiceNow Otto panel: Provides a seamless experience for accessing generative AI capabilities within Regulatory Change Management \( RCM\).
-   Supports multiple task types: Enables adding multiple regulatory tasks and source document import tasks to a single alert.

**Note:** Only users with sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user roles can access this workflow.

## ServiceNow Otto in RCM agentic workflows

RCM uses the following ServiceNow Otto agentic workflows:

<table id="table_okm_2lg_dhc"><thead><tr><th>

Workflow

</th><th>

Description

</th><th>

User

</th></tr></thead><tbody><tr><td>

Get regulatory analysis agentic workflow

</td><td>

Analyze and enrich regulatory alerts by using the get regulatory analysis agentic workflow in the ServiceNow Otto panel. This agentic workflow uses web search to enhance alert context and recommends potential impacts on citations, policies, and control objectives to support faster and more accurate compliance decisions. For more information, see [Activate the get regulatory analysis agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/activate-rcm-agent-workflow.md)and [Analyze and enrich regulatory alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/get-rcm-reg-insight.md).

</td><td>

sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user

</td></tr><tr><td>

Generate regulatory action plan agentic workflow

</td><td>

Generate regulatory action plans by using the generate regulatory action plan agentic workflow in the ServiceNow Otto panel. This agentic workflow analyzes impacted areas and similar historical alerts to create change tasks and action tasks that help implement regulatory change.For more information, see [Activate the Generate regulatory action plan agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/activate-rcm-agent-actions-workflow.md) and [Generate regulatory action plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/generate_regulatory_action_plans.md).

</td><td>

sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user

</td></tr></tbody>
</table>**Related topics**  


[Explore ServiceNow Otto skills and agentic workflows in Regulatory Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/rcm-exploring-now-assist-for-irm.md)

[Supporting information for ServiceNow Otto for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/now-assist-irm-supporting-info.md)

[Analyze and enrich regulatory alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/get-rcm-reg-insight.md)

[Generate regulatory action plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/generate_regulatory_action_plans.md)

