---
title: Exploring Value features in AI Control Tower
description: Learn about the Value dashboard components, tabs, widgets, templates, and cost framework that help you measure and track AI system business impact.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/measure-ai-exploring-aict-value.html
release: zurich
topic_type: concept
last_updated: "2026-05-25"
reading_time_minutes: 3
breadcrumb: [Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# Exploring Value features in AI Control Tower

Learn about the Value dashboard components, tabs, widgets, templates, and cost framework that help you measure and track AI system business impact.

## Value overview

The Value feature in AI Control Tower Insights section helps organizations track and communicate the business impact of their AI agent investments. As AI agents automate business processes at scale, the Value feature enables you to measure tangible benefits—from process automation rates and cycle time reduction to cost savings and labor hour reclamation—and demonstrate ROI to stakeholders.

The Value feature provides multi-dimensional analysis of business metrics by agent, use case, business unit, or portfolio; benchmarking and trending to track momentum over time; cost-benefit comparison of deployment and maintenance costs against measurable returns; and executive-ready dashboards that translate AI performance into business language for stakeholder communication. You can also export value metrics for integration with business cases, financial planning, and enterprise reporting systems.

## Value dashboards

The Value feature provides three main dashboard types, each tailored to different use cases and audiences:

-   **Enterprise Value Dashboard**

    Shows aggregated value metrics across all AI systems from all vendors in your environment, including ServiceNow AI, Microsoft AI, Amazon AI, Google Cloud AI, and others. Use this dashboard for organization-wide value analysis and executive reporting. For more information, see [Value dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/measure-aict-value-insights.md).

-   **Engagement Dashboard**

    Tracks how your organization is adopting and using AI systems across departments and geographies. Measures AI action volume, identifies unused systems, and shows adoption patterns. For more information, see [Engagement dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/measure-aict-engagement-insights.md).

-   **ServiceNow AI Dashboard**

    Dedicated view of creator skills metrics \(generative AI skills only\) from ServiceNow. Useful for understanding the specific value of ServiceNow's native AI capabilities independent of multi-vendor landscape. For more, see [ServiceNow AI dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/measure-snow-ai-insights.md).


## Value templates

Value templates are the foundation of value calculation. A value template defines:

-   What business outcomes or metrics matter to your organization
-   How those outcomes are calculated from AI system activity
-   Which AI systems contribute to specific value metrics
-   How to translate technical metrics into business value

Templates enable customization so that value metrics reflect your organization's specific priorities rather than generic defaults. See [Value templates in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/measure-ai-explore-value-templates.md) for template architecture and types.

## Cost framework

The cost framework tracks expenses associated with AI systems and calculates return on investment. It captures:

-   **Token costs:** LLM usage costs based on prompt and completion tokens
-   **Assistant costs:** Maintenance and operational costs for AI agents and assistants
-   **Total AI cost:** Aggregate cost across all AI systems
-   **Net returns:** Benefits \(productivity gains\) minus costs, for ROI calculation

To learn more, see [Cost Framework in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/measure-ai-explore-value-cost-framework.md).

## Asset-level value tracking

In addition to the aggregated dashboards, you can view value metrics at the individual AI system \(asset\) level. Asset record pages show:

-   Value details tab with productivity gains and cost metrics for that system
-   Engagement metrics specific to that asset
-   Associated value templates
-   Historical value trends

This enables asset owners and stakeholders to understand the specific value contribution of individual AI systems.

