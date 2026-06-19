---
title: Exploring Now Assist for Integrated Risk Management \(IRM\)
description: With the Now Assist for Integrated Risk Management \(IRM\) application, you can use generative AI to support key IRM tasks such as summarizing issues, identifying risks, and reviewing controls. These capabilities are integrated into IRM records and help streamline how you work with issues, risks, controls, policy exceptions, and more.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/exploring-now-assist-for-irm.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Exploring Now Assist for Integrated Risk Management \(IRM\)

With the Now Assist for Integrated Risk Management \(IRM\) application, you can use generative AI to support key IRM tasks such as summarizing issues, identifying risks, and reviewing controls. These capabilities are integrated into IRM records and help streamline how you work with issues, risks, controls, policy exceptions, and more.

## Now Assist for IRM overview

The following generative AI capabilities are available in Now Assist for IRM:

-   Simplify and speed up routine IRM tasks with AI-powered assistance embedded in your records.
-   Gain quick insights into IRM data without manually parsing through detailed documentation.
-   Identify potential risks early by analyzing patterns in existing data.
-   Improve decision-making with AI-generated insights available directly in your workflows.

## Now Assist for IRM skills/workflows

Now Assist for IRM includes generative AI capabilities that help you interpret and act on IRM records more efficiently. These capabilities support tasks such as summarizing issue details, reviewing control effectiveness, identifying risks, and analyzing policy exceptions.

<table id="table_amn_nsd_bhc"><thead><tr><th>

Workflow

</th><th>

Feature

</th><th>

User role

</th></tr></thead><tbody><tr><td>

[Using agentic workflows in IRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/using-agentic-ai-workflows.md) agentic workflow

</td><td>

Leverage the power of AI agents to generate an action plan and suggest remediation tasks for a GRC issue.

</td><td>

-   sn\_grc\_genai.issue\_user
-   sn\_irm\_gen\_ai.user
-   sn\_grc\_genai.issue\_aiagent\_user

</td></tr></tbody>
</table><table id="table_p1h_lgx_12c"><thead><tr><th>

Skill

</th><th>

Feature

</th><th>

User role

</th></tr></thead><tbody><tr><td>

[Issue Summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-summarization-skill.md)

</td><td>

Analyze issue records using generative AI to generate concise summaries, improving organizational efficiency, team coordination, and productivity.

</td><td>

-   sn\_grc\_genai.issue\_user
-   sn\_irm\_gen\_ai.user

</td></tr><tr><td>

[Generate recommendation for similar control objective](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/generate-recommendation-for-a-new-control-objective.md)

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

[AI-driven regulatory alert summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/regulatory-alert-summarization.md)

</td><td>

Leverage Now LLM Service to convert regulatory content into concise, business-relevant summaries with key changes, deadlines, and compliance actions—delivered in real time.

</td><td>

-   sn\_irm\_gen\_ai.user
-   sn\_grc\_reg\_change.user
-   sn\_grc\_comp\_genai.reg\_change\_ai\_user

</td></tr><tr><td>

[AI-generated recommendations for a regulatory alert skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/recommendations-for-a-regulatory-alert.md)

</td><td>

Use this skill to identify relevant control objectives linked to incoming regulatory changes. It streamlines the compliance process and reduces manual effort.

</td><td>

-   sn\_irm\_gen\_ai.user
-   sn\_grc\_reg\_change.user
-   sn\_grc\_comp\_genai.reg\_change\_ai\_user

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using Now Assist for IRM, see:

-   [Supporting information for Now Assist for IRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/now-assist-irm-supporting-info.md)
-   [Configure Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/configure-now-assist-for-irm.md)
-   [Activate skills in Now Assist for IRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/activate-na-skills-in-irm.md)
-   [Activate agentic workflows in Now Assist for IRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/activate-agentic-workflows.md)
-   [Customize the issue summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/customize-issue-summarization-skill.md)
-   [Using Now Assist for IRM skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/using-now-assist-for-irm-to-summarize-issues.md)
-   [Summarize an issue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/summarize-an-issue.md)
-   [Using agentic workflows in IRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/using-agentic-ai-workflows.md)
-   [Optimize GRC issue resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/generate-grc-issue-resolution.md)

