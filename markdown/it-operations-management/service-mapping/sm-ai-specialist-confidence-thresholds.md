---
title: Business App Mapping AI Agent confidence thresholds
description: Use this reference to understand how the Business App Mapping AI Agent handles matches based on their AI confidence score, and what action is taken for each score range.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-04-16"
reading_time_minutes: 1
keywords: [Business App Mapping AI Agent, confidence thresholds, CSDM, ITOM]
breadcrumb: [AI Agents for Service Mapping, AI capabilities in Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Business App Mapping AI Agent confidence thresholds

Use this reference to understand how the Business App Mapping AI Agent handles matches based on their AI confidence score, and what action is taken for each score range.

|Score range|Confidence level|Action|
|-----------|----------------|------|
|0.3 – 1.0|High|The agent automatically creates a "Uses::Used by" relationship in \[cmdb\_rel\_ci\]. A business application can be linked to multiple services.|
|0.1 – 0.29|Medium|The agent saves the candidate to the staging table \[sn\_sm\_gen\_ai\_ba\_candidate\_rel\] for administrator review. No relationship is created automatically. Administrators can accept a candidate to create the \[cmdb\_rel\_ci\] relationship, or dismiss it.|
|Below 0.1|Low|The candidate is filtered out. The agent does not create a record or a relationship.|

**Parent Topic:**[AI Agents for Service Mapping](../concept/service-mapping-ai-specialists.md)

