---
title: Value calculation formula and metrics
description: The AI Control Tower calculates the productivity value of an AI system by multiplying usage, time saved per invocation, and the acceptance rate.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Value calculation formula and metrics

The AI Control Tower calculates the productivity value of an AI system by multiplying usage, time saved per invocation, and the acceptance rate.

## Productivity formula

The AI Control Tower calculates the productivity value of an AI system with the following formula:

```
Productivity = Usage × Time Saved per invocation × Acceptance Rate
```

## Metric definitions

-   **Persona**

    The user role for whom the value is calculated, specific to the selected AI system, such as agent, requester, developer, and others.

-   **Usage**

    The number of times a specific AI skill, agent, or feature is triggered within the platform. Usage is measured by counting events in logs, or by aggregating unique user interactions, over a defined period \(currently daily\). For example, if the Incident Summarization skill is triggered 94 times on August 18, its usage for that day is 94. Usage is calculated through a Performance Analytics \(PA\) indicator. Only daily indicators are supported. An out-of-the-box daily PA indicator job calculates usage scores for the previous day. Custom indicators must be daily and must complete their run before 1:00 p.m. each day.

-   **Time Saved**

    The reduction in manual effort per invocation. It is estimated as the difference between the time a user spends performing the task manually and the time spent with AI assistance. Time saved can be a constant, such as 15 minutes, or an indicator. If it is an indicator, it follows the same rules as the usage indicator. For example, if each Knowledge Base \(KB\) generation call uses 5 assists and each assist saves 1 minute, the calculation records 5 minutes saved.

-   **Acceptance Rate**

    The percentage of AI-generated outputs that end users accept, which indicates the effectiveness of, and trust in, the AI solution. Acceptance Rate = \(Accepted AI outputs ÷ Total AI outputs\) × 100. The acceptance rate can be a constant value, such as 50 percent, or a PA indicator that follows the same rules as usage.


## Sample calculation: HR case summarization

The following example shows how the productivity metrics are derived for the HR case summarization skill.

|Metric|Value|
|------|-----|
|Count of HR cases created|5,000|
|HR cases not processed by agentic AI|2,750|
|Cases with summarization \(45%\) — Usage|2,250|
|Cases with accepted summarization \(30%\) — Acceptance rate|675|
|Time saved per execution|5 mins|

