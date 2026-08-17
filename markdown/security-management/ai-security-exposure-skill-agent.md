---
title: Using the AI guardrails helper skill and agentic workflow
description: You have the option to use a generative AI skill and agentic workflow to help you understand what type of findings you have, understand the guardrails associated with findings, and see why the skill mapped guardrails to particular findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/ai-security-exposure-skill-agent.html
release: zurich
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 2
breadcrumb: [AI Security Exposure Management, Use, Unified Security Exposure Management, Security Operations]
---

# Using the AI guardrails helper skill and agentic workflow

You have the option to use a generative AI skill and agentic workflow to help you understand what type of findings you have, understand the guardrails associated with findings, and see why the skill mapped guardrails to particular findings.

## AI guardrails helper skill and agentic workflow overview

To use the AI guardrails helper skill and agentic, you must install the ServiceNow Otto for Unified Security Exposure Management application \(sn\_vul\_ai\).

Roles required: sn\_vul.vulnerability\_admin or sn\_vul.vulnerability\_analyst admin

The AI Guardrails Helper is a combination of an AI skill and an AI agent. Together, they help you identify existing mitigations in the form of guardrails for AI validation findings. They automatically defer the findings with guardrails already mapped or create exception rules to auto-defer future findings.

The Now Assist panel must be activated. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).

See [Use the AI guardrails helper skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/ai-security-exposure-use-aiskill.md) and [Use the AI guardrails helper agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/ai-security-exposure-use-agent.md) for steps to use the skill and the agentic workflow.

-   **[Use the AI guardrails helper agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/ai-security-exposure-use-agent.md)**  
Use the AI agent to ask about guardrails identified by the AI skill component in the AI Guardrails Helper. Automatically defer findings with existing mitigations in the form of guardrails and create exception rules to automatically defer future findings.
-   **[Use the AI guardrails helper skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/ai-security-exposure-use-aiskill.md)**  
This AI skill identifies finding types and helps you understand guardrails that are already mapped to findings and why they were selected by the skill for mapping. This information helps you determine any findings that might be mitigated and deferred for later review and remediation.
-   **[Components installed with AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/installed-with-aisecmanagement.md)**  
Components installed with the AI Security Exposure Management application.

**Parent Topic:**[Exploring AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/exploring-ai-security-exposure.md)

