---
title: Turn on the AICT Security Analyzer agent
description: Turn on the AICT Security Analyzer agent to get additional analysis of AI asset security events. The agent classifies events by severity, adds them to Your top recommendations, and creates relevant security tasks.Post-runtime probabilistic metrics require that the AICT Security Analyzer agent is turned on. Both the AI agent and probabilistic metrics are turned off by default, and the sampling rate for the metrics is set to 1%. Turn them on to get additional monitoring and analysis of your AI systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-sec-configure-security-analyzer-agent.html
release: australia
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Turn on the AICT Security Analyzer agent

Turn on the AICT Security Analyzer agent to get additional analysis of AI asset security events. The agent classifies events by severity, adds them to **Your top recommendations**, and creates relevant security tasks.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

## About this task

The AICT Security Analyzer agent is turned off by default, so that no AI usage is consumed until you choose to turn it on. When the agent is turned on, it analyzes security events using historical trends and intents. For more information about the agent, see [AICT security analyzer AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/plat-ai-aict-security-analyzer-agent-ai-agent.md).

**Note:** When you turn on the agent, any Post-runtime settings that are enabled increase monitoring for threats and may increase token consumption.

## Procedure

1.  In AI Control Tower, navigate to **Settings** &gt; **Rules and templates** &gt; **Security**.

2.  Select the **Security insights** tab.

    The **AICT Security Analyzer** section shows the current status of the agent.

3.  Select the arrow for **Open in AI Agent Studio**.

4.  In AI Agent Studio, turn on the AICT Security Analyzer agent.

    For more information, see [AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aias-landing.md).


## Result

The AICT Security Analyzer agent starts analyzing security events for the settings you have enabled. To confirm, return to the **Security insights** tab. The status of the agent shows **Enabled**.

**Parent Topic:**[Configuring security metrics in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-sec-configuring.md)

## AICT Security Analyzer agent and Post-runtime settings

Post-runtime probabilistic metrics require that the AICT Security Analyzer agent is turned on. Both the AI agent and probabilistic metrics are turned off by default, and the sampling rate for the metrics is set to 1%. Turn them on to get additional monitoring and analysis of your AI systems.

### Metrics turned off by default

The following metrics are turned off by default so that no AI usage is consumed until you choose to turn them on. For more information about configuring these metrics, see [Configure post-runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-sec-configure-event-metrics.md).

**Warning:** AI judge model classifications are probabilistic in nature and may be incomplete or incorrect. They don't constitute professional advice and shouldn't be relied on as the sole basis for assessing risk.

-   Agent goal deviation
-   Correctness detection
-   Data integrity incident detection
-   Excessive agency
-   Improper input and output handling
-   Prompt injection
-   Sensitive data disclosure
-   System prompt leakage

