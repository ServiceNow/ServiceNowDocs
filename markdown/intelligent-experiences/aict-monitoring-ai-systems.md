---
title: Monitoring AI assets
description: Evaluate the quality and safety of AI interactions across your portfolio using automated scoring, configurable metrics, and trend analysis for both ServiceNow and external AI systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-monitoring-ai-systems.html
release: zurich
topic_type: concept
last_updated: "2026-04-17"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI, use]
breadcrumb: [AI Control Tower, Enable AI experiences]
---

# Monitoring AI assets

Evaluate the quality and safety of AI interactions across your portfolio using automated scoring, configurable metrics, and trend analysis for both ServiceNow and external AI systems.

AI systems can perform well at deployment and degrade weeks later as data sources shift and edge cases emerge. Monitoring in AI Control Tower addresses this by continuously scoring a sample of live AI interactions against configurable quality and safety metrics. AI stewards use the resulting scores to detect regressions, investigate the underlying causes, and coordinate with AI system owners on the changes that restore performance, across both ServiceNow and external AI systems.

Monitoring also feeds the AI value calculation. When you configure a value template to use quality score as a dimension, AI Control Tower pulls the live quality score from the monitoring pipeline into the productivity formula, so the value an AI system reports reflects how well it is actually performing. For more information about value templates and the dimensions they use, see [Measuring AI impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-measuring-ai-impact.md).

-   **[Monitoring and evaluating AI systems in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-landing.md)**  
Continuously monitor your ServiceNow and external AI systems to determine whether they meet quality and safety standards, and investigate root causes when they don't.

**Parent Topic:**[AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-landing.md)

