---
title: Exploring Now Assist in Regulatory Change Management \(RCM\)
description: With Now Assist in Regulatory Change Management, part of the Now Assist for Integrated Risk Management \(IRM\) application, you can use agentic workflows and generative AI skills that streamline the analysis, summarization, and impact assessment of regulatory alerts. These capabilities empower compliance teams to act swiftly and accurately on regulatory changes.
locale: en-US
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-10-03"
reading_time_minutes: 14
keywords: [Now Assist, generative AI]
breadcrumb: [Explore, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Exploring Now Assist in Regulatory Change Management \(RCM\)

With Now Assist in Regulatory Change Management, part of the Now Assist for Integrated Risk Management \(IRM\) application, you can use agentic workflows and generative AI skills that streamline the analysis, summarization, and impact assessment of regulatory alerts. These capabilities empower compliance teams to act swiftly and accurately on regulatory changes.

## Now Assist in RCM overview

Organizations working in regulated environments must regularly interpret new and complex regulatory requirements, triage alerts, and determine which business areas are affected. These activities are often performed manually, which can result in delays, inconsistent analysis, and difficulty referencing previous regulatory responses.

Now Assist in Regulatory Change Management provides a set of generative AI skills and agentic workflows designed to address these challenges.

The summarization skill enables you to generate summaries of a regulatory alert and recommend impacted areas, including citations, control objectives, controls, and policies, for alerts in any state except Closed or Cancelled. The recommendation skills analyzes incoming alerts against existing citations, control objectives, controls and policies to generate suggestions, leveraging generative AI to support more consistent and efficient compliance analysis.

The Get Regulatory Analysis agentic workflow analyzes and enriches regulatory alerts in any state except Closed or Cancelled by leveraging web search and organizational data. It provides additional context for each alert and recommends potential impacts on citations, control objectives, controls, and policies. The Generate Regulatory Action Plan agentic workflow generates regulatory action plans for regulatory alert in the In Progress state by analyzing impacted areas and referencing similar historical alerts. It creates change tasks and action items that help teams implement regulatory changes.

## Now Assist in RCM benefits

The generative AI skills for **Now Assist in Regulatory Change Management** offer the following benefits:

-   Automated summarization of regulatory alerts, reducing manual effort in interpreting complex regulatory language and surfacing key details such as important dates, regulatory authority, key changes, and penalties/fines.
-   AI-powered recommendations of impacted areas, including citations, control objectives, and controls, helping compliance teams quickly assess business impact and prioritize responses.
-   Minimized human intervention in repetitive tasks, enabling regulatory analysts to focus on strategic planning, risk mitigation, and stakeholder engagement.
-   Accelerated regulatory change processing, enabling faster turnaround for compliance actions, audits, and reporting through embedded workflows and contextual recommendations.
-   Scalable and configurable framework, supporting integration of new RCM skills and workflows to adapt to evolving regulatory landscapes and organizational needs.

The agentic workflows for **Now Assist in Regulatory Change Management** offer the following benefits:

-   Context-enriched regulatory analysis, enabling you to enhance alerts through an automated agent that surfaces relevant external and internal references, helping to reduce time spent manually researching regulatory context.
-   Automated impact mapping, enabling workflows to recommend affected citations, control objectives, policies, and controls based on historical data and organizational frameworks helping to accelerate impact analysis and reduce the risk of oversight.
-   Actionable task generation, where workflows automatically create change tasks and action plans aligned with regulatory requirements, helping teams move from insight to execution without manual task creation.

## Now Assist in RCM skills

The following generative AI skills are available in Now Assist in RCM:

<table id="table_p1h_lgx_12c"><thead><tr><th>

Skill

</th><th>

Description

</th><th>

User

</th></tr></thead><tbody><tr><td>

Regulatory alert Summarization

</td><td>

Generate a concise summary of a regulatory alert using generative AI.

 The summary includes:-   Important dates \(for example, publication, compliance, effective\)
-   Regulatory authority \(for example, agency, jurisdiction\)
-   Summary of key changes
-   Penalties or fines

For more information, see [AI-driven regulatory alert summarization skill](../../now-assist-irm/concept/regulatory-alert-summarization.md).

</td><td>

To view your assigned regulatory alerts, you need the sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles.

</td></tr><tr><td>

Regulatory alert impacted citations

</td><td>

Recommend citations that may be affected by the regulatory alert. These recommendations help compliance teams identify relevant legal references and streamline the impact analysis process.For more information, see [AI-generated recommendations for a regulatory alert skill](recommendations-for-a-regulatory-alert.md).

</td><td>

To view your assigned regulatory alerts, you need the sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles.

</td></tr><tr><td>

Regulatory alert impacted control objectives

</td><td>

Recommend control objectives that may be affected by the regulatory alert. These recommendations help teams align regulatory changes with internal control frameworks and help ensure that compliance measures are updated accordingly.For more information, see [AI-generated recommendations for a regulatory alert skill](recommendations-for-a-regulatory-alert.md).

</td><td>

To view your assigned regulatory alerts, you need the sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles.

</td></tr><tr><td>

Regulatory alert impacted controls

</td><td>

Recommend controls that may be affected, such as operational, technical, or procedural safeguards. These recommendations support proactive compliance adjustments and risk mitigation.For more information, see [AI-generated recommendations for a regulatory alert skill](recommendations-for-a-regulatory-alert.md).

</td><td>

To view your assigned regulatory alerts, you need the sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles.

</td></tr><tr><td>

Regulatory alert impacted policies

</td><td>

Recommend policies that may be affected by the regulatory alert. These recommendations help compliance teams identify relevant internal policy documents and ensure alignment with updated regulatory requirements.For more information, see [AI-generated recommendations for a regulatory alert skill](recommendations-for-a-regulatory-alert.md).

</td><td>

To view your assigned regulatory alerts, you need the sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles.

</td></tr></tbody>
</table>**Note:**

By default, only alerts in the New state are eligible for summarization, though this can be configured to include other states; recommendations can be generated for alerts in any state except Closed or Cancelled. To access these skills, the sn\_grc\_comp\_genai.reg\_change\_ai\_user role must be manually assigned to users.

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

Analyze and enrich regulatory alerts by using the get regulatory analysis agentic workflow in the Now Assist panel. This agentic workflow uses web search to enhance alert context and recommends potential impacts on citations, policies, and control objectives to support faster and more accurate compliance decisions. For more information, see [Get regulatory analysis agentic workflow](../../now-assist-irm/concept/rcm-agent-insights-workflow.md) and [Analyze and enrich regulatory alerts](../../now-assist-irm/task/get-rcm-reg-insight.md).

</td><td>

sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user

</td></tr><tr><td>

Generate regulatory action plan agentic workflow

</td><td>

Generate regulatory action plans by using the generate regulatory action Plan agentic workflow in the Now Assist panel. This agentic workflow analyzes impacted areas and similar historical alerts to create change tasks and action tasks that help implement regulatory change.For more information, see [Generate regulatory action plan agentic workflow](../../now-assist-irm/concept/rcm-agent-actions-workflow.md) and [Generate regulatory action plans](../../now-assist-irm/task/generate_regulatory_action_plans.md).

</td><td>

sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user

</td></tr></tbody>
</table>**Note:** The generate regulatory action plan agentic workflow is available when regulatory alerts are in the In Progress state. The get regulatory analysis agentic workflow is available when regulatory alerts are in any state except for the Closed or Cancelled state. To access these workflows, you must be assigned the sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user role. The get regulatory analysis agentic workflow relies on recommendation templates and alert configurations to generate actionable insights and tasks. Ensure that templates are properly set up and alerts are categorized to support workflow execution. For more information, see [Recommendation contexts and templates](recommendation-contexts.md), [Create a recommendation context](../task/configure-recommendation-context.md), and [Create a recommendation template](../task/create-a-recommendation-template.md).

**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some Now Assist products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## What to explore next

To learn more about configuring and using Now Assist in Regulatory Change Management and Now Assist for IRM, see:

-   [Exploring Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/concept/exploring-now-assist-for-irm.md)
-   [Configure Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/concept/configure-now-assist-for-irm.md)
-   [Using Now Assist for Integrated Risk Management \(IRM\) skills](../../grc-common/concept/using-now-assist-for-irm-to-summarize-issues.md)
-   [Using agentic workflows in Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/concept/using-agentic-ai-workflows.md)
-   [AI-driven regulatory alert summarization skill](../../now-assist-irm/concept/regulatory-alert-summarization.md)
-   [AI-generated recommendations for a regulatory alert skill](recommendations-for-a-regulatory-alert.md)
-   [Activate the Regulatory alert summarization skill](../../now-assist-irm/task/summarize-a-regulatory-alert.md)
-   [Activate Regulatory alert recommendation skills](../../now-assist-irm/task/configure-recommendation-skill-for-a-regulatory-alert.md)
-   [Generate a regulatory alert summary](../../now-assist-irm/task/create-a-summary-of-a-reg-alert.md)
-   [Generate recommendations for regulatory alert impacted citations, control objectives, controls, and policies](../../now-assist-irm/task/create-recommendation-reg-alert.md)
-   [Get regulatory analysis agentic workflow](../../now-assist-irm/concept/rcm-agent-insights-workflow.md)
-   [Analyze and enrich regulatory alerts](../../now-assist-irm/task/get-rcm-reg-insight.md)
-   [Generate regulatory action plan agentic workflow](../../now-assist-irm/concept/rcm-agent-actions-workflow.md)
-   [Generate regulatory action plans](../../now-assist-irm/task/generate_regulatory_action_plans.md)

**Parent Topic:**[Exploring Regulatory Change Management](what-is-rcm.md)

**Related topics**  


[Regulatory Change Management application landing page](rcm-workspace-for-managers.md)

[Tasks page in the Compliance Workspace](tasks-page.md)

[Source document import tasks](source-document-import-tasks.md)

[Regulatory process flow and tasks](reg-change-workflow-swimlane.md)

[RSS feeds overview](rss-feeds.md)

[Impact assessments for the regulatory alerts](impact-assessment-task.md)

[Regulatory assessment for a regulatory alert](regulatory-assessment-in-rcm.md)

[Next Experience Discuss and Chat Collaboration](next-experience-discuss-chat-collaboration.md)

[Regulatory Change Management application in the Compliance Workspace](rcm-workspace-overview.md)

