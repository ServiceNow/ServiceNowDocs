---
title: Exploring Now Assist in AI Risk and Compliance
description: With Now Assist in AI Risk and Compliance, part of the Now Assist for Integrated Risk Management \(IRM\) application, you can use agentic workflows and generative AI skills that streamline issue summarization, control objective creation, and respond to smart assessment questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc-exploring-now-assist.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-06-17"
reading_time_minutes: 7
keywords: [Now Assist, generative AI]
breadcrumb: [Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Exploring Now Assist in AI Risk and Compliance

With Now Assist in AI Risk and Compliance, part of the Now Assist for Integrated Risk Management \(IRM\) application, you can use agentic workflows and generative AI skills that streamline issue summarization, control objective creation, and respond to smart assessment questions.

## Now Assist in AI Risk and Compliance overview

Organizations deploying AI systems must continuously evaluate AI-related risks, monitor regulatory requirements, and ensure compliance with evolving AI governance standards. These activities are often performed manually, which can result in delays, inconsistent risk assessments, and difficulty tracking mitigation efforts across the enterprise.

Now Assist in AI Risk and Compliance provides a set of generative AI skills and agentic workflows designed to address these challenges.

The summarization skill enables you to generate concise summaries of issues, highlighting key details, impact scope, and required actions to accelerate triage and response. The assessment summarization skill creates comprehensive risk evaluation summaries that distill complex risk factors, assessment findings, and remediation priorities into actionable insights. The response assist skill generates contextually relevant response recommendations for assessments based on past responses and uploaded documents to improve consistency and reduce repetitive work.

## Now Assist in AI Risk and Compliance benefits

The generative AI skills for Now Assist in AI Risk and Compliance offer the following benefits:

-   Automated assessment of AI systems, reducing manual effort in reporting issues, summarizing issues for context, responding to assessments, and rationalizing control objectives.
-   Minimized human intervention in repetitive tasks, enabling risk and compliance analysts to focus on strategic planning, risk mitigation, and stakeholder engagement.
-   Scalable and configurable framework, supporting integration of new AI Risk and Compliance skills and workflows to adapt to evolving regulatory landscapes and organizational needs.

The agentic workflows for Now AssistAI Risk and Compliance offer the following benefits:

-   Context-enriched risk analysis, enabling you to enhance AI risk records through an automated agent that surfaces relevant regulatory guidance, industry standards, and internal governance references, helping to reduce time spent manually researching compliance context.
-   Automated control mapping, enabling workflows to recommend affected and duplicate governance controls, compliance policies, and regulatory requirements based on historical data and organizational risk frameworks, helping to accelerate impact analysis and reduce the risk of control gaps.

## Now Assist in AI Risk and Compliance skills

The following generative AI skills are available in Now Assist in AI Risk and Compliance:

<table id="table_p1h_lgx_12c"><thead><tr><th>

Skill

</th><th>

Description

</th><th>

User

</th></tr></thead><tbody><tr><td>

Report a GRC issue

</td><td>

Flag GRC issues to the Virtual Agent through utterances. Catalog the issue with fully filled form fields and simplify reporting across development, data science, and operations teams. For example, an AI Steward discovers anomalous results in a customer segmentation model affecting a specific demographic. With Report a GRC Issue, the concern is immediately escalated with structured context rather than waiting for scheduled audits. This enables the compliance team to address the issue within hours of discovery.

For more information, see [Report a GRC issue AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-submission-ai-agent.md).

</td><td>

To report a GRC issue, you need the sn\_airc\_gen\_ai.airc\_ai\_agent\_user role.

</td></tr><tr><td>

Issue Summarization

</td><td>

Automatically generate concise summaries of issues, highlighting key details, impact scope, and required actions to accelerate triage and response. For example, an AI Risk and Compliance Manager receives numerous issue reports about an AI-powered fraud detection system within a week. With Issue Summarization, these reports are distilled into a ranked list of concerns by category: data privacy gaps, performance degradation, and model drift. This enables the manager to focus resolution efforts on high-impact categories, reducing triage time from four hours to thirty minutes.

For more information, see [Issue Summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-summarization-skill.md).

</td><td>

To use the issue summarization skill, you need the sn\_airc\_gen\_ai.airc\_ai\_agent\_user and sn\_airc\_gen\_ai.airc\_ai\_user roles.

</td></tr><tr><td>

Risk Assessment Summarization

</td><td>

Analyze risk assessment data and generate natural language summaries of identified risks, trends, and patterns for specific AI systems. Provide executive-level insights and highlights critical risks requiring attention.For example, an AI Risk and Compliance Manager oversees several AI systems and is working on presenting findings to the Board Audit Committee. With Risk Assessment Summarization, assessment data is consolidated into executive insights highlighting regulatory, fairness, and operational risks across the portfolio. This enables the manager to present a brief strategic summary instead of a long form report, enabling swifter board decisions.

For more information, see [Generate a risk assessment summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/generate-risk-assessment-summary-genai.md).

</td><td>

To use the risk assessment summarization skill, you need the sn\_airc\_gen\_ai.airc\_ai\_agent\_user or sn\_airc\_gen\_ai.airc\_ai\_user roles.

</td></tr><tr><td>

Smart Assessment Response Assist

</td><td>

Generate contextually relevant response recommendations for assessments based on organizational policies, historical patterns, and industry best practices to improve consistency and efficiency.

 For example, an AI Risk and Compliance Manager assesses an AI model for diagnostic recommendations and identifies data bias risk in the training data. With Smart Assessment Response Assist, the system recommends compliant remediation paths based on organizational policies and similar successful implementations. This enables consensus on the optimal approach in one meeting rather than extended debate.

 For more information, see [Smart Assessment response assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/ai-generated-responses-for-smart-assessment.md).

</td><td>

To use the smart assessment response assist skill, you need the sn\_airc\_gen\_ai.airc\_ai\_agent\_user or sn\_airc\_gen\_ai.airc\_ai\_user roles.

</td></tr><tr><td>

Recommendation for similar control objectives

</td><td>

Use this skill to automatically identify common control objectives across risk domains and reduce redundancy within the compliance library.For example, an AI Product Owner launches a new algorithmic trading AI system and needs applicable controls from an enterprise library. With Recommendation for Similar Control Objectives, the most relevant controls are recommended based on the system's risk profile. This enables the product owner to validate suggestions quickly, reducing control design time.

For more information, see [Generate recommendation for similar control objective](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/generate-recommendation-for-a-new-control-objective.md).

</td><td>

To use the skill for recommendation for similar control objectives, you need the sn\_airc\_gen\_ai.airc\_ai\_agent\_user or sn\_airc\_gen\_ai.airc\_ai\_user roles.

</td></tr><tr><td>

Common control objective creation

</td><td>

After recommendations are reviewed and accepted, use this skill to create a new common control objective by merging details from the accepted control objectives.

 For example, an AI Risk and Compliance Manager oversees AI models across different business functions. With Common Control Objective Creation, a few reusable control objectives are identified from the portfolio. This enables new AI projects to inherit existing controls from a central library, reducing governance design time.

 For more information, see [Act on the recommendations for similar control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/take-actions-on-the-recommendations-for-similar-control-objectives.md).

</td><td>

To use the common control objective creation, you need the sn\_airc\_gen\_ai.airc\_ai\_agent\_user or sn\_airc\_gen\_ai.airc\_ai\_user roles.

</td></tr></tbody>
</table>**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some AI products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

