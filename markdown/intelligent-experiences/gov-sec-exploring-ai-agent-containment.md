---
title: AI agent containment using kill switch protocol
description: Explore how detecting malicious activity and deactivating AI agents works to enforce guardrails and help improve your security posture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-exploring-ai-agent-containment.html
release: australia
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# AI agent containment using kill switch protocol

Explore how detecting malicious activity and deactivating AI agents works to enforce guardrails and help improve your security posture.

AI agents operate as autonomous actors across the enterprise, frequently with elevated or administrative privileges. AI agent containment using kill switch protocol gives you the ability to immediately contain an AI agent and revoke all of its active credentials across connected systems.

Policy enforcement points \(PEPs\) are part of AI agent containment. PEPs can be identity providers, AI agent runtimes, or infrastructure platforms. When you contain an AI agent, AI Control Tower doesn't just issue revocation requests; it confirms enforcement completion from each individual PEP before declaring the agent contained.

## Example: Malicious activity by an AI agent

An AI steward receives a tip from a vendor that an AI agent integrated with their platform is generating suspicious API calls. The steward opens the Security page of AI Control Tower and notices a critical security event involving the AI agent. Upon viewing the AI asset, AI Control Tower alerts the steward that malicious activity was detected. Traceloop data and policy enforcement points \(PEPs\) provide a summary of the agent behavior.

\[Omitted image "gov-sec-malicious-activity.png"\] Alt text: Malicious activity evidence shown for an agent.

The system suggests that the next best action is to deactivate the AI agent. The analyst deactivates the AI agent and receives confirmation that the AI agent was deactivated in Okta as well as AWS Bedrock.

## Audit and compliance

Every containment action including the PEP-by-PEP confirmation, produces a complete, immutable audit trail shown in the kill switch protocol log. This audit record can help satisfy compliance documentation requirements.

## Next steps

To configure and use AI agent containment with kill switch protocol, see [Configure AI agent containment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-ai-agent-containment.md) and [Manage AI agents using kill switch protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md).

**Parent Topic:**[Exploring security in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-exploring.md)

