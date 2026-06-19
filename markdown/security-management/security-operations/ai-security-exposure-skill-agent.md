---
title: Using the AI guardrails helper skill and agentic workflow
description: You have the option to use a generative AI skill and agentic workflow to help you understand what type of findings you have, understand the guardrails associated with findings, and see why the skill to mapped guardrails to particular findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-operations/ai-security-exposure-skill-agent.html
release: australia
product: Security Operations
classification: security-operations
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 2
breadcrumb: [AI Security Exposure Management, Use, Unified Security Exposure Management, Security Operations]
---

# Using the AI guardrails helper skill and agentic workflow

You have the option to use a generative AI skill and agentic workflow to help you understand what type of findings you have, understand the guardrails associated with findings, and see why the skill to mapped guardrails to particular findings.

## AI guardrails helper skill and agentic workflow overview

To use the AI guardrails helper skill and agentic, you must install the Now Assist for Vulnerability Response application \(sn\_vul\_ai\).

Roles required are sn\_vul.vulnerability\_admin or sn\_vul.vulnerability\_analyst admin

The AI Guardrails Helper is a combination of an AI skill and an AI agent. Together, they can help you identify existing mitigations in the form of guardrails for AI validation findings and automatically defer the findings with guardrails already mapped or create exception rules to auto-defer future findings.

The Now Assist panel must be activated. For more information, see .

See [Use the AI guardrails helper skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/ai-security-exposure-use-aiskill.md) and [Use the AI guardrails helper agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/ai-security-exposure-use-agent.md) for steps to use the skill and the agentic workflow.

-   **[Use the AI guardrails helper agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/ai-security-exposure-use-agent.md)**  
Use the AI agent to ask about the guardrails that were identified by the AI skill component in the AI Guardrails Helper, automatically defer findings with existing mitigations in the form of guardrails, or create exception rules to auto-defer future findings.
-   **[Use the AI guardrails helper skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/ai-security-exposure-use-aiskill.md)**  
This AI skill can help you identify finding types, understand the guardrails that might be already mapped to findings, and see why they were selected by the skill to map to specific findings. This information can help you determine which findings might be already mitigated or deferred for later review or remediation.

**Parent Topic:**[Exploring AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/exploring-ai-security-exposure.md)

