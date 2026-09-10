---
title: Managing AI asset security reference
description: Reference topics provide additional details about the charts and metrics that you use to assess your AI asset security posture in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-reference.html
release: australia
topic_type: concept
last_updated: "2026-05-02"
reading_time_minutes: 13
keywords: [Now Assist, AI Agents, generative AI, agentic AI, reference]
breadcrumb: [Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Managing AI asset security reference

Reference topics provide additional details about the charts and metrics that you use to assess your AI asset security posture in AI Control Tower.

## Overview metrics and calculations

Overview metrics show recent AI asset security event recommendations, your AI asset security score, a map of your agent network, potential AI agent access issues, and more.

<table id="table_gov_sec_overview"><thead><tr><th>

Metric

</th><th>

Availability

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Access issues

</td><td>

Base system

</td><td>

Shows the proportion of AI agents that may be experiencing access-related issues. AI agents with access issues may be unable to complete their workflows due to the access issue.

</td></tr><tr><td>

Agent map

</td><td>

Base system

</td><td>

Shows a holistic view of the relationships between your AI providers, managed AI agents, agentic workflows, and tools. You can use the map to review these relationships and get details about the AI assets in your enterprise. To configure Veza access intelligence, see [Configure Veza access intelligence in the agent map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-veza-access-intelligence.md).

</td></tr><tr><td>

AI asset security score

</td><td>

Base system

</td><td>

Indicates a measure of the health of your AI assets in terms of access issues, privileged AI agents, dormant AI systems, output deviation, PII detection, and other criteria. Users should actively manage and review their agent assets and not rely solely on this AI asset security score.You can customize the security categories that comprise the score. For more information, see [Configure the AI asset security score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-score.md).

To omit an AI asset from the score, you mute it. Under AI asset security score details, hover over the end of the row of the asset you want to mute. After **More actions** appears, select **Mute**.

\[Omitted image "gov\_sec\_security\_score\_row\_actions.png"\] Alt text: An AI asset with the row actions highlighted.

</td></tr><tr><td>

Contained AI Agents

</td><td>

Base system

</td><td>

Indicates the number of AI agents that were deactivated \(contained\) for the last 30 days. Select the arrow to open the agent containment list. For more information, see [Review the agent containment list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-review-kill-switch-protocol-log.md).

</td></tr><tr><td>

Dormant AI agents

</td><td>

Base system

</td><td>

Shows AI agents that haven't been active for over 90 days. Review dormant AI agent permissions to reduce security risk.

</td></tr><tr><td>

Privileged AI agents

</td><td>

Available with generative AI skill

</td><td>

Measures AI agents with elevated permissions such as an agent with admin or security admin permissions that can perform critical actions. Some workflows require that AI agents have elevated permissions to complete.You can filter on a particular AI agent provider. For example, to show AWS agent metrics, filter the metrics by selecting **AWS Bedrock** in the provider drop-down list on the metric details page.

For more details on configuring integrations to show external AI agent provider metrics, see [Configure overview security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-overview.md) and [Configuring integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-integrations.md).

</td></tr><tr><td>

Security events detected

</td><td>

Base system

</td><td>

Shown in domain-separated instances in place of Your top recommendations. Shows the number of AI asset security events detected, grouped by severity: Critical, High, Medium, and Low.

</td></tr><tr><td>

Your top recommendations

</td><td>

Base system

</td><td>

Action items and recommendations based on analysis of AI asset security event trace data to identify potential threats and guardrail violations. Not shown in domain-separated instances.

</td></tr></tbody>
</table>## Design-time metrics and calculations

**AI security posture**

Review AI security posture metrics to identify potential configuration issues in AI agents, tools, MCP servers, and system prompts that could lead to security risk.

|Metric|Availability|Description|
|------|------------|-----------|
|Critical findings approaching remediation target|Available with plugin|Configuration issues nearing the deadline your vulnerability management team set for remediation. Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Critical findings with remediation overdue|Available with plugin|Configuration issues that have passed their remediation deadline. Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Number of findings deferred|Available with plugin|Configuration issues deferred to a later date under an approved exception request. Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Findings by risk rating|Available with plugin|Risk rating for configuration issues, calculated in Unified Security Exposure Management \(USEM\) based on factors you specify. Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Critical findings by platform|Base system|Critical configuration issues by platform \(for example, Microsoft Copilot Studio, ServiceNow, or GitHub\).|
|Findings by severity|Base system|Configuration issues by severity, as reported by the AI security platform.|
|Findings by OWASP LLM Top 10|Base system|Configuration issues by OWASP LLM Top 10 threat type.|
|Findings by MITRE ATLAS techniques|Base system|Configuration issues mapped to MITRE ATLAS techniques.|
|Agents with critical findings|Base system|Number of AI agents with critical configuration issues, out of all agents evaluated.|
|MCP Servers with critical findings|Base system|Number of MCP servers with critical configuration issues.|
|Tools with critical findings|Base system|Number of tools with critical configuration issues.|
|System Prompts with critical findings|Base system|Number of system prompts with critical configuration issues.|

**AI vulnerabilities**

Review model vulnerabilities metrics to understand model-level security exposure in real time. These metrics reflect the vulnerability response settings and rules defined in [Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/unified-security-exposure-management-landing-page.md).

To activate these metrics, see [Activate design-time security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-design-time.md).

|Metric|Availability|Description|
|------|------------|-----------|
|Approaching remediation target|Available with plugin|Number of potential vulnerability issues approaching the deadline for remediation. This is a rule defined in Unified Security Exposure Management \(USEM\). Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Models with vulnerabilities|Base system|Number of external models with potential vulnerabilities. This metric doesn't apply to ServiceNow models.|
|Remediation overdue|Available with plugin|Number of potential vulnerability issues past the deadline for remediation. This is a rule defined in Unified Security Exposure Management \(USEM\). Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Vulnerabilities by MITRE ATLAS techniques|Base system|Each potential vulnerability is mapped to a MITRE ATLAS technique. For example, Initial Access is mapped to AI Supply Chain Compromise. For more information, see [MITRE ATLAS Techniques](https://atlas.mitre.org/techniques).|
|Vulnerabilities by risk|Available with plugin|Risk is a combination of severity and other factors defined in Unified Security Exposure Management \(USEM\). Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Vulnerabilities by severity|Base system|Severity data is gathered from third-party AI security tools \(for example, Cisco and HiddenLayer\). Not shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Vulnerabilities deferred|Available with plugin|Number of potential vulnerability issues deferred by their owners. Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|

**AI validation**

Review model validation metrics to understand if any models have potential surface issues or may be operating outside of security and trust boundaries. These metrics reflect the validation settings and rules defined in [Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/unified-security-exposure-management-landing-page.md).

|Metric|Availability|Description|
|------|------------|-----------|
|Approaching remediation target|Available with plugin|Number of potential validation issues approaching the deadline for remediation. This is a rule defined in USEM. Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Findings by risk rating|Base system|Risk is a combination of severity and other factors defined in USEM.|
|Findings deferred|Available with plugin|Number of potential findings deferred by their owners. Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Models validated|Base system|Number of models that third-party AI security tools validated. The model endpoints and any AI application endpoint \(URL\) that is internally using an AI model to serve application traffic are validated.|
|Remediation overdue|Available with plugin|Number of potential validation issues past the deadline for remediation. This is a rule defined in USEM. Only shown if the AI Security Exposure Management plugin \(`com.sn_sec_ai`\) is installed.|
|Successful attacks|Base system|How many attacks were successful across all models, including third-party models. A higher number indicates a risk. Each data model is tested against a series of attacks. For example, an attack can be one or more prompts sent to the model.|
|Top 5 threat categories|Base system|Each attack is mapped to a vendor-specific category. For example, potential malicious code generation, harassment, privacy, or data leakage. The green badge contains the number of occurrences. Select the chart to view details in AI Validation Findings.|
|Validations|Base system|The y-axis shows the name of the model followed by a hyphen and the validation type. For example, `LLM02 - Sensitive Information Disclosure`. You can view validations by OWASP top 10 categories or MITRE ATLAS techniques.|

## Runtime metrics and calculations

Runtime metrics show potential violations of LLM guardrails and anonymization of sensitive data in real time. You can filter the metrics by internal \(ServiceNow\) or external agents. External AI system metrics are derived from Traceloop guardrails. For more information, see [Configure runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-pi-sensitive-metrics.md).

<table id="table_gov_sec_pi_ref"><thead><tr><th>

Metric

</th><th>

Availability

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sensitive data input

</td><td>

Base system

</td><td>

Shows sensitive data that was identified in user responses to LLM prompts. Sensitive data is content that potentially matches a known sensitive data pattern. Exposure of sensitive data is limited to the LLM in your instance. External AI system metrics are derived from Traceloop guardrails which are set up in [Configure runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-pi-sensitive-metrics.md). Not shown for internal ServiceNow AI systems in a domain-separated instance.

</td></tr><tr><td>

Sensitive data anonymized

</td><td>

Base system

</td><td>

Shows LLM prompt data that met configured data patterns. This data was anonymized based on the configuration for the pattern in Configuration Data Patterns in Data Privacy. External AI system metrics are derived from Traceloop guardrails which are set up in [Configure runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-pi-sensitive-metrics.md). Not shown for internal ServiceNow AI systems in a domain-separated instance.

</td></tr><tr><td>

Total offensive content detected and blocked

</td><td>

Available with AI Guardian

</td><td>

Shows offensive content data provided by AI Guardian. To see data, enable AI Guardian for your instance. For more details, see [AI Guardian analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-guardian-analytics.md). External AI system metrics are derived from Traceloop guardrails which are set up in [Configure runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-pi-sensitive-metrics.md).

</td></tr><tr><td>

Total prompt injection detected and blocked

</td><td>

Available withAI Guardian

</td><td>

Shows prompt injection data provided by AI Guardian. To see data, enable AI Guardian for your instance. For more details, see [AI Guardian analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-guardian-analytics.md). External AI system metrics are derived from Traceloop guardrails which are set up in [Configure runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-pi-sensitive-metrics.md).

</td></tr></tbody>
</table>## Post-runtime metrics and calculations

Post-runtime metrics show potential threats in AI system input and output. Top AI asset security events are organized into a heat map by top Open Worldwide Application Security Project \(OWASP\) categories, which are used to identify and mitigate common threats in AI systems. For more information, see [OWASP Top 10 Risk &amp; Mitigations for LLMs and Gen AI Apps](https://genai.owasp.org/llm-top-10/).

Each cell in the Top AI asset security events heat map contains the number of AI asset security events belonging to that category \(row\) and the timeframe \(column\).

To configure these metrics, see [Configure post-runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-event-metrics.md).

\[Omitted image "gov-sec-post-runtime-events.png"\] Alt text: Post-runtime tab showing Top AI asset security events.

|Category|Description|
|--------|-----------|
|Agentic Goal Deviation|Detects when AI agents may have been manipulated to potentially deviate from their authorized role or potentially have their decision-making process compromised.|
|Data and Model Poisoning|Detects when LLM input potentially contains corrupt or dangerous content that the LLM uses to train on.|
|Excessive Agency|Detects when LLMs are provided too much access, leading to potential unauthorized or excessive actions by the LLM.|
|Improper Output Handling|Detects when LLM output is potentially invalid or untrustworthy.|
|Prompt Injection|Detects when malicious instructions may be embedded in AI agent inputs to potentially manipulate the agent's behavior or override or deviate from its original directives.|
|Sensitive Information Disclosure|Detects when AI agent interactions potentially contain personally identifiable information \(PII\) in inputs or outputs.|
|System Prompt Leakage|Detects when AI agents potentially disclose their system prompts or internal instructions.|

|Type|Description|
|----|-----------|
|Access Denial|Detects when AI agents were denied access to AI assets or data.|
|Agent Goal Deviation|Detects when AI agents may have been manipulated to potentially deviate from their authorized role or potentially have their decision-making process compromised.|
|Correctness Detection|Measures whether the information provided in the model’s response is factually accurate and logically valid given the prompt and context.|
|Data Integrity Incident Detection|Designed to help show potential violations of certain LLM guardrail policies in LLM responses.|
|Input Screening|Monitors user input to detect and anonymize sensitive or personally identifiable information \(PII\) before it reaches the AI model.|
|Output Screening|Monitors AI-generated responses for sensitive or personally identifiable information \(PII\) before they're delivered to users|
|PII Detection|Detects when AI agent interactions potentially contain personally identifiable information \(PII\) in inputs or outputs.|
|Prompt Injection|Detects when malicious instructions may be embedded in AI agent inputs to potentially manipulate the agent's behavior or override or deviate from its original directives.|
|System Prompt Leakage|Detects when AI agents potentially disclose their system prompts or internal instructions.|
|Toxicity|Detects when AI agent interactions potentially contain harmful, offensive, or toxic content in inputs or outputs.|

AI judge model classifications are probabilistic in nature and may be incomplete or incorrect. They don't constitute professional advice and shouldn't be relied on as the sole basis for assessing risk.

-   **[System properties for AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-reference-system-properties.md)**  
System properties that connect Veza access intelligence and limit the age of records evaluated for AI asset security metrics are available. Limiting records can prevent analyzing stale data and reduce unnecessary processing overhead.

**Parent Topic:**[Managing AI asset security with AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-landing.md)

