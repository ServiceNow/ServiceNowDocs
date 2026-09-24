---
title: AI agent containment using kill switch protocol manually
description: Explore how deactivating AI agents works to enforce guardrails and help improve your security posture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-exploring-ai-agent-containment.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Managing AI asset security, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# AI agent containment using kill switch protocol manually

Explore how deactivating AI agents works to enforce guardrails and help improve your security posture.

AI agents operate as autonomous actors across the enterprise, frequently with elevated or administrative privileges. AI agent containment using kill switch protocol gives you the ability to immediately contain an AI agent and revoke all of its active credentials across the connected enforcement points that you configured.

Control enforcement points \(PEPs\) are part of AI agent containment. CEPs can be identity providers, AI agent runtimes, or infrastructure platforms. Supported AI agent platforms are AWS Bedrock, AWS Bedrock AgentCore, Azure AI Foundry, Gemini Enterprise Agent Platform \(agents with a unique identity only\), and ServiceNow AI agents. The supported identity provider is Okta.

When you contain an AI agent, AI Control Tower issues revocation requests and confirms enforcement completion from each configured CEP before declaring the agent contained.

## Example: Malicious activity by an AI agent

An AI steward receives a tip from a vendor that an AI agent integrated with their platform is generating suspicious API calls. The steward opens the Security page of AI Control Tower and notices a critical security event involving the AI agent. Upon viewing the AI asset, AI Control Tower alerts the steward that malicious activity was detected. Traceloop data and control enforcement points \(CEPs\) provide a summary of the agent behavior.

\[Omitted image "gov-sec-malicious-activity.png"\] Alt text: Malicious activity evidence shown for an agent.

The system suggests that the next best action is to deactivate the AI agent. The analyst deactivates the AI agent and receives confirmation that the AI agent was deactivated in Okta as well as AWS Bedrock.

## Audit and compliance

Every containment action including the CEP-by-CEP confirmation, produces a complete, immutable audit trail shown in the agent containment list. This audit record can help satisfy compliance documentation requirements.

## Next steps

To configure and use AI agent containment with kill switch protocol, see [Configure AI agent containment using kill switch protocol manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-ai-agent-containment.md) and [Contain AI agents manually using kill switch protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md).

**Parent Topic:**[Exploring security in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-exploring.md)

