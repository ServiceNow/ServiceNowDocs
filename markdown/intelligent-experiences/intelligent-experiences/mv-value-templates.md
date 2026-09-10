---
title: Value templates
description: Value templates define how the AI Control Tower calculates the productivity value of an AI system. Each template captures a persona, usage indicators, a time value type, and a quality score.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
---

# Value templates

Value templates define how the AI Control Tower calculates the productivity value of an AI system. Each template captures a persona, usage indicators, a time value type, and a quality score.

## Value template overview

A value template, also called a productivity template, is the record that the AI Control Tower \(AICT\) uses to measure the productivity value of an AI system. Each template defines a name, a department, a description, and a persona, and then sets the indicators that determine how usage and time saved are calculated.

Every AI system supports a persona, such as agent, fulfiller, requester, developer, or others. You select the persona that the AI system supports so that value is attributed to the correct group of users.

A value template is reusable. You define it once and map it across as many AI systems as you want, so you don't repeat the same calculation for every skill or agent. The AI Control Tower ships out-of-the-box templates, and you can also create your own.

The AI Control Tower ships the following out-of-the-box value templates:

-   Third-party Assets
-   ServiceNow Skills
-   ServiceNow Agents
-   ServiceNow Agentic Workflows

## Key benefits

Value templates provide the following benefits:

-   Calculate productivity value consistently across ServiceNow and third-party AI systems.
-   Measure the time saved by each AI system by using out-of-the-box indicators or a fixed baseline.
-   Factor the quality of AI output into the value calculation through a quality score.
-   Attribute value to a specific persona so that results reflect the users who benefit.
-   Reuse a single value definition across multiple AI systems.
-   Capture value automatically each day after you publish a template.
-   Measure value by persona and by department.
-   Map default templates automatically to newly discovered AI systems.

## How value templates are composed

A value template combines the following elements to produce a value calculation:

-   **Usage indicators:** A set of out-of-the-box indicators measures execution counts, including agent execution, use case execution, skill execution, worker execution, and execution from third-party systems. Each indicator reads the table where those executions are stored.
-   **Time value type:** Sets how time saved is calculated. Select an indicator to derive time saved from usage, or select a constant to apply a fixed baseline that you define.
-   **Quality score:** Represents the quality of each execution. You can apply a constant value, such as 50 percent or 70 percent, or derive the score from observability performance evaluation. When an AI system has no quality score, the value defaults to 50 percent, which you can overwrite.

Two out-of-the-box indicators calculate time saved: one captures the read and write token counts and computes the total time saved, and one counts each consumed assist as one minute saved. When neither indicator fits, you can define a constant baseline, such as five minutes saved per incident summarization, based on your own assessment.

When the time value type uses the quality score, the AI Control Tower reads the score from observability. Observability runs a performance evaluation for each AI agent and AI system against production data.

The template elements combine into the productivity value using the following formula: **Productivity = Usage × Time Saved per invocation × Acceptance Rate**. The acceptance rate is the percentage of AI-generated outputs that end users accept, and it corresponds to the quality-score factor. It can be a constant, such as 50 percent, or a Performance Analytics \(PA\) indicator. For the full formula, the metric definitions, and a worked example, see [Value calculation formula and metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mv-value-calculation-formula-metrics.md).

## The three metrics at a glance

However the fields are labeled in the interface, every value template comes down to the same three numbers.

|Metric|What it answers|How you provide it|
|------|---------------|------------------|
|Usage|How often is this AI system used?|A daily Performance Analytics \(PA\) indicator that counts executions.|
|Time saved|How much manual effort does one use avoid?|A constant, such as 15 minutes, or a PA indicator. The constant is the manual execution time minus the AI execution time.|
|Acceptance rate \(quality\)|How much of the AI output do people actually accept?|A constant, such as 50 percent, or a PA indicator. Defaults to 50 percent when no score is available.|

**Note:**

The third metric appears as **Quality type** and **Quality constant \(in %\)** in the calculation builder, and as the acceptance rate in the productivity formula. They refer to the same factor: the share of AI outputs that are accepted.

After you publish a template, the default AI value engine job runs each day, captures value for the mapped AI systems, and populates the Value dashboard.

## Considerations

Consider the following when you work with value templates:

-   Each deployed AI system must have one published value template so that value calculation continues without interruption.
-   You can create a published template for each persona, such as agent or requester. At least one published template must remain mapped to the AI system.
-   A value job runs each night and calculates usage for the previous day, so the Value dashboard shows the value from the previous day.

