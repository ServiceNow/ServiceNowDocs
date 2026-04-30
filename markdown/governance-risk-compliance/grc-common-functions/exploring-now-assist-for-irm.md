---
title: Exploring Now Assist for Integrated Risk Management \(IRM\)
description: With the Now Assist for Integrated Risk Management \(IRM\) application, you can use generative AI to support key Integrated Risk Management \(IRM\) tasks such as summarizing issues, identifying risks, and reviewing controls. These capabilities are integrated into IRM records and help streamline how you work with issues, risks, controls, policy exceptions, and more.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Exploring Now Assist for Integrated Risk Management \(IRM\)

With the Now Assist for Integrated Risk Management \(IRM\) application, you can use generative AI to support key Integrated Risk Management \(IRM\) tasks such as summarizing issues, identifying risks, and reviewing controls. These capabilities are integrated into IRM records and help streamline how you work with issues, risks, controls, policy exceptions, and more.

## Now Assist for IRM overview

Now Assist for IRM enables you to use AI-driven skills and agentic workflows focused on Integrated Risk Management. Now Assist for IRM is available based on entitlements.

## Now Assist for IRM benefits

Now Assist for IRM offers the following benefits

-   Simplify and speed up routine IRM tasks with AI-powered assistance embedded in your records.
-   Gain quick insights into IRM data without manually parsing through detailed documentation.
-   Identify potential risks early by analyzing patterns in existing data.
-   Improve decision-making with AI-generated insights available directly in your workflows.

## Now Assist for IRM workflows/skills

<table id="table_amn_nsd_bhc"><thead><tr><th>

Workflow

</th><th>

Feature

</th><th>

User role

</th></tr></thead><tbody><tr><td>

[Using agentic workflows in Now Assist for Integrated Risk Management \(IRM\)](using-agentic-ai-workflows.md) agentic workflow

</td><td>

Leverage the power of AI agents to generate an action plan and suggest remediation tasks for a GRC issue.

</td><td>

-   sn\_grc\_genai.issue\_user
-   sn\_irm\_gen\_ai.user
-   sn\_grc\_genai.issue\_aiagent\_user
-   sn\_grc\_comp\_genai.reg\_change\_ai\_user

</td></tr><tr><td>

[Control Objective Change Agent](../../grc-policy-and-compliance/concept/control-objective-change-agent.md)

</td><td>

Automates updates to impacted control objectives when citation changes occur, ensuring descriptions and supplemental guidance remain accurate and aligned with evolving regulatory requirements.

</td><td>

sn\_irm\_gen\_ai.user

</td></tr></tbody>
</table><table id="table_p1h_lgx_12c"><thead><tr><th>

Skill

</th><th>

Feature

</th><th>

User role

</th></tr></thead><tbody><tr><td>

[Issue Summarization skill](issue-summarization-skill.md)

</td><td>

Analyze issue records using generative AI to generate concise summaries, improving organizational efficiency, team coordination, and productivity.

</td><td>

-   sn\_grc\_genai.issue\_user
-   sn\_irm\_gen\_ai.user

</td></tr><tr><td>

[AI-generated recommendations for similar control objective](../../grc-policy-and-compliance/concept/ai-generated-recommendations-for-similar-control-objective.md)

</td><td>

Control objective rationalization streamlines risk and compliance management by eliminating redundant or overlapping control objectives, improving efficiency while ensuring compliance.

</td><td>

-   sn\_irm\_gen\_ai.user
-   sn\_comp\_case.compliance\_​case\_analyst
-   sn\_comp\_case.compliance\_​case\_manager

</td></tr><tr><td>

Risk Assessment Summarization

</td><td>

Use Now LLM Service to generate risk assessment summaries from inherent, residual, target risks, and control effectiveness data. These summaries highlight key factors and relevant comments, helping assessors and approvers gain actionable insights.

</td><td>

-   sn\_grc\_sharegenai.risk\_asmt\_user
-   sn\_risk\_advanced.ara\_assessor
-   sn\_risk\_advanced.ara\_approver
-   sn\_irm\_gen\_ai.user

</td></tr><tr><td>

[Regulatory Alert Summarization skill](../../now-assist-irm/concept/regulatory-alert-summarization.md)

</td><td>

Leverage Now LLM Service to distill regulatory information into concise, business-relevant summaries that highlight most important changes, deadlines, and actions required for compliance in real-time.

</td><td>

-   sn\_grc\_reg\_change.user
-   sn\_grc\_comp\_genai.reg\_change\_ai\_user

</td></tr><tr><td>

[Regulatory alert recommendation skills](../../grc-rcm/concept/recommendations-for-a-regulatory-alert.md)

</td><td>

Use these skills to identify relevant citations, control objectives, controls, and policies linked to incoming regulatory changes. They streamline the compliance process and reduce manual effort by automatically analyzing regulatory alerts and recommending the most applicable impacted areas for your organization.

</td><td>

-   sn\_grc\_reg\_change.user
-   sn\_grc\_comp\_genai.reg\_change\_ai\_user

</td></tr><tr><td>

[Control objective impact analyzer skill](../../grc-policy-and-compliance/concept/control-objective-impact-analyzer-skill.md)

</td><td>

Evaluates citation updates and identifies which associated control objectives require attention. Displays impacted objectives and works with the Control Objective Change Agent for further updates.

</td><td>

sn\_irm\_gen\_ai.user

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using Now Assist for IRM, see:

-   [Supporting information for Now Assist for IRM](now-assist-irm-supporting-info.md)
-   [Configure Now Assist for Integrated Risk Management \(IRM\)](configure-now-assist-for-irm.md)
-   [Activate skills in Now Assist for IRM](../task/activate-na-skills-in-irm.md)
-   [Activate agentic workflows in Now Assist for IRM](../task/activate-agentic-workflows.md)
-   [Customize the issue summarization skill](../task/customize-issue-summarization-skill.md)
-   [Using Now Assist for IRM skills](using-now-assist-for-irm-to-summarize-issues.md)
-   [Summarize an issue](summarize-an-issue.md)
-   [Using agentic workflows in Now Assist for Integrated Risk Management \(IRM\)](using-agentic-ai-workflows.md)
-   [Optimize a issue resolution](../task/generate-grc-issue-resolution.md)
-   [Control Objective Change Agent](../../grc-policy-and-compliance/concept/control-objective-change-agent.md)
-   [Control objective impact analyzer skill](../../grc-policy-and-compliance/concept/control-objective-impact-analyzer-skill.md)

