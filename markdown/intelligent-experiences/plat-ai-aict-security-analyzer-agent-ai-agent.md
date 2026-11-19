---
title: AICT security analyzer AI agent
description: This AI agent generates context for a detected AI security event by aggregating asset, prompt, cross-threat, and correlation data. It then computes a confidence score from detection strength, event risk, and authorization signals.Post-runtime probabilistic metrics require that the AICT Security Analyzer agent is turned on. Both the AI agent and probabilistic metrics are turned off by default, and the sampling rate for the metrics is set to 1%. Turn them on to get additional monitoring and analysis of your AI systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-aict-security-analyzer-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-11-16"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# AICT security analyzer AI agent

This AI agent generates context for a detected AI security event by aggregating asset, prompt, cross-threat, and correlation data. It then computes a confidence score from detection strength, event risk, and authorization signals.

## Workflow

For all security events, the agent deterministically executes outcomes in a single finalization step: creating a security incident for critical severity events with no open duplicate, saving a triage record capturing the full verdict and rationale, and triggering an AI insight for platform-wide visibility after the triage record is committed.

1.  Retrieve the detected AI security event record and gather its full context, including the related asset, prompt, cross-threat indicators, and recent threat correlation.
2.  If the event context indicates an error, finalize the analysis immediately with the error details and stop. If the event is missing, or lacks its event type, asset, or target record, the agent saves a triage record with verdict error, score 0, and the error details.
3.  Calculate a confidence score \(0-100\) using detection strength, event type risk, prompt authorization signals, and any cross-threat or correlation overrides. Critical events have a score of 90-100.
4.  Finalize the analysis by determining severity and creating a security incident with no open duplicate. Save a triage record with the full rationale, and trigger an AI insight for platform-wide visibility.
5.  If finalization fails, failures appear in the system log and the triage record. If incident creation fails, the triage record is saved with Critical severity and verdict incident\_creation\_failed. No incident is linked. The analysis reports success.

    If triage save fails, the analysis reports failure and the agent shows an error. Any incident created or matched during the analysis remains and isn't linked to a triage record. If a triage record already existed for the event, it keeps its previous values.


<table id="table_onk_rvj_glc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

 **Warning:** Turning on external discovery exposes security event data to outside agents.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Assess Threat - Gathers the event, the asset context \(its system prompt and transaction summary\), cross-threat indicators, and recent threat correlation \(7-day window, up to 20 events\).

Finalize Analysis - Derives severity from the score, runs the duplicate check, creates the incident, and saves the triage record.


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_ai\_governance.ai\_steward and sn\_ai\_security.viewer

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_ai\_governance.ai\_steward and sn\_ai\_security.viewer

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platform-ai-agents-overview.md)

## AICT Security Analyzer agent and Post-runtime settings

Post-runtime probabilistic metrics require that the AICT Security Analyzer agent is turned on. Both the AI agent and probabilistic metrics are turned off by default, and the sampling rate for the metrics is set to 1%. Turn them on to get additional monitoring and analysis of your AI systems.

### Metrics turned off by default

The following metrics are turned off by default so that no AI usage is consumed until you choose to turn them on. For more information about configuring these metrics, see [Configure post-runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-event-metrics.md).

**Warning:** AI judge model classifications are probabilistic in nature and may be incomplete or incorrect. They don't constitute professional advice and shouldn't be relied on as the sole basis for assessing risk.

-   Agent goal deviation
-   Correctness detection
-   Data integrity incident detection
-   Excessive agency
-   System prompt leakage

