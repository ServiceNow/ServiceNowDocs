---
title: Managing evaluation cost
description: Reduce the assists that evaluation consumes by adjusting what you evaluate, how often you evaluate it, and which AI systems you evaluate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mon-ai-managing-evaluation-cost.html
release: zurich
topic_type: concept
last_updated: "2026-09-15"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Monitoring and evaluating AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Managing evaluation cost

Reduce the assists that evaluation consumes by adjusting what you evaluate, how often you evaluate it, and which AI systems you evaluate.

Evaluating both ServiceNow and external AI systems consumes assists. Three settings determine how many assists your evaluations consume.

-   Consider which metrics require evaluation. Each metric increases the visibility you gain into a session but also increases assist usage to evaluate it. Evaluate only the metrics that give you the insight you need.
-   Adjust the sample rate as needed. A higher sample rate evaluates more executions and gives you more confidence in your scores but also increases assist usage. Set the lowest rate that produces enough evaluated sessions to trust the score. ServiceNow AI systems use a single sample rate for all metrics. External AI systems have a sample rate per metric, so you can keep higher rates for the metrics that matter most and sample the rest.
-   Evaluate AI systems that require oversight. Evaluation runs for every AI system that has it turned on, so turn it off for the systems that you don't need to monitor, such as test or retired systems.

**Related topics**  


[Configure global metrics for ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-global-metrics-servicenow.md)

[Configure global metrics for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-global-metrics-external.md)

[Configure asset-specific metrics for ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-asset-metrics-servicenow.md)

[Configure asset-specific metrics for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-asset-metrics-external.md)

[Configure metrics evaluated for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-ai-system-metrics.md)

[Disable evaluation for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-disable-evaluation.md)

