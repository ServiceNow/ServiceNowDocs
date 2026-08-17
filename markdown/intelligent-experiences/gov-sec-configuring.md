---
title: Configuring security metrics in AI Control Tower
description: Plan and configure your implementation of security metrics. You can configure metrics to measure the integrity of your data model and monitor potential threats in large language model \(LLM\) input and output. You can also customize the AI asset security score.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-sec-configuring.html
release: zurich
topic_type: concept
last_updated: "2026-05-04"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI, configure]
breadcrumb: [Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Configuring security metrics in AI Control Tower

Plan and configure your implementation of security metrics. You can configure metrics to measure the integrity of your data model and monitor potential threats in large language model \(LLM\) input and output. You can also customize the AI asset security score.

-   **[Configure overview security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-overview.md)**  
If you have external AI agent data you want reflected in the Privileged AI agents metric, set up a Traceloop connection to the external AI server and perform other setup to make sure agent data appears in the metric. Or, set up a static connection for Amazon Web Services \(AWS\) or Azure.
-   **[Configure Veza access intelligence in the agent map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-veza-access-intelligence.md)**  
Integrate Veza with ServiceNow to display agent risk scores and severity levels in the agent map. Complete this configuration for each hyperscaler that has AI assets you want to monitor.
-   **[Activate design-time security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-design-time.md)**  
Set up AI Service Graph Connectors for the AI security tools you currently use to import AI model vulnerability and AI validation \(automated red teaming\) data and show it in design-time metrics. To see additional metrics, including details for each metric, install the AI Security Exposure Management plugin \(com.sn\_sec\_ai\).
-   **[Configure runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-pi-sensitive-metrics.md)**  
Set up a Traceloop connection and API key for prompt injection, offensive content, sensitive data input, and sensitive data anonymized trace data from external AI servers. Review data privacy for sensitive data patterns to detect in LLM input and output.
-   **[Configure post-runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-event-metrics.md)**  
Customize security and content moderation policies, sampling rate, skill call usage limit, LLMs to use, and other settings for the Top AI asset security events metric and others.
-   **[Configure the AI asset security score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-score.md)**  
Customize the AI asset security score to align with your enterprise's security practices. You can omit large language model \(LLM\) guardrail categories from the score or change the weights of categories.
-   **[Configure AI agent containment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-ai-agent-containment.md)**  
Connect identity providers and hyperscalers to ServiceNow to let you contain and enforce guardrails for AI assets at runtime using kill switch protocol.
-   **[Update system property to limit records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-system-property.md)**  
Update the sn\_ai\_security.analyzer\_max\_record\_age\_hours system property to limit the age \(in hours\) of AI asset invocation records evaluated for AI asset security metrics.

**Parent Topic:**[Managing AI asset security with AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-landing.md)

