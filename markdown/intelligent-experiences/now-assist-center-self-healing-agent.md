---
title: Self-healing AI agent
description: Use the self-healing AI agent in the AI Admin Center conversational experience to diagnose and resolve common AI administration issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-center-self-healing-agent.html
release: zurich
topic_type: concept
last_updated: "2026-07-30"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Using the ServiceNow Otto panel conversational experience, Use, AI Admin Center, Enable AI experiences]
---

# Self-healing AI agent

Use the self-healing AI agent in the AI Admin Center conversational experience to diagnose and resolve common AI administration issues.

## Self-healing AI agent overview

The self-healing AI agent is a diagnostic assistant in the AI Admin Center conversational experience. It interprets your issue description and classifies it against a library of known AI admin failure patterns. The AI agent presents a root cause hypothesis with a confidence level, enabling you to make informed decisions about how to resolve the issue.

The self-healing AI agent is turned on by default.

The self-healing AI agent may work with other AI agents to accomplish tasks. For more information on AI agents, see [Explore AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/exploring-ai-agents.md).

## AI agent details

The self-healing AI agent capabilities are associated with the following agents.

<table id="table_vsk_1jj_yjc"><thead><tr><th>

Agent

</th><th>

Capability

</th></tr></thead><tbody><tr><td>

SHA Diagnostic Agent

</td><td>

Runs configuration diagnostics and presents actionable results to the admin.

</td></tr><tr><td>

SHA Triage Agent

</td><td>

Assesses whether the admin's AI problem description contains enough information to produce a meaningful diagnosis.

 Asks at most one targeted clarification question per turn, with a maximum of two turns.

 Outputs a visible triage summary confirming the final problem description and readiness status so that behavior can be verified in both standalone and workflow testing.

</td></tr></tbody>
</table>For more information on viewing your AI agents, see [View your AI assets in the asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-view-ai-assets.md).

## AI agent access

Role required: sn\_na\_center.nac\_admin

## AI agent uses

Use the self-healing AI agent to help with issues such as:

-   AI Admin Center configuration or setup problems
-   Plugin installation or activation failures
-   Missing or turned off Now Assist application features
-   Integration connectivity or credential problems
-   Role or permission misconfigurations affecting Now Assist access
-   Feature flags or activation toggles in an unexpected state
-   Compatibility conflicts between Now Assist and other plugins or versions

For more information, see the troubleshooting issues described in KB article [KB2330598](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2330598) on Now Support.

## AI agent actions

When used, the AI agent may attempt the following actions:

-   Interpret the information provided by the user.
-   Compare the information against documented issues.
-   Present a root cause hypothesis with a confidence level.
-   Recommend remediation actions after receiving user confirmation.
-   Maintain issue context throughout the conversation.

## How it works

1.  Describe your issue in the conversational interface in AI Admin Center.
2.  The AI agent interprets your description and matches it against known failure patterns.
3.  The AI agent displays the possible root cause of the issue along with its degree of confidence that it is correct.
4.  You review the hypothesis and confirm, adjust, or provide additional details about the issue.
5.  After you confirm the diagnosis, the AI agent guides you toward a resolution.

    Depending on your issue, the agent may do one of the following:

    -   Walk you through specific configuration steps.
    -   Link you to relevant documentation or troubleshooting articles.
    -   Suggest settings or statuses to verify.
    -   Recommend escalation to support if the issue requires specialized help.
6.  The AI agent retains your issue description, the diagnosis, and the confidence level throughout your session so you can ask follow-up questions without repeating context.

**Parent Topic:**[Using the conversational experience in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/using-now-assist-panel-now-assist-center.md)

