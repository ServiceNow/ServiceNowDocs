---
title: Conversational evaluator
description: Conversational evaluator measures the quality of Virtual Agent conversations in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mv-conversational-evaluator.html
release: brazil
topic_type: concept
last_updated: "2026-09-23"
reading_time_minutes: 2
keywords: [Conversational Evaluator, AI Control Tower, Virtual Agent, auto-evaluation]
breadcrumb: [Explore, Measure AI system, Measure AI systems, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Conversational evaluator

Conversational evaluator measures the quality of Virtual Agent conversations in AI Control Tower.

## Conversational evaluator overview

Conversational Evaluator gives you a measurable view of conversation quality so you can track Virtual Agent performance over time.

A conversation that saves time for a live agent is treated as a successful conversation. Conversational Evaluator combines quality scores with value metrics, such as estimated time savings, so you can connect conversation quality to business impact.

You access Conversational Evaluator from the **Evaluation** tab in AI Control Tower.

**Note:** Generative AI may produce inaccurate or incomplete information. Always validate AI-generated content.

## Benefits

Conversational evaluator provides the following benefits:

-   Track Virtual Agent performance across a defined set of quality metrics.
-   Define your own quality benchmark by rating conversations.
-   Estimate the hours and cost that Virtual Agent conversations save.

## How it works

Conversational evaluator uses an auto-evaluation framework to score Virtual Agent conversations. It works as follows:

1.  The system identifies qualified conversations by excluding conversation types that aren't suitable for evaluation.
2.  The system selects a random sample of qualified conversations for auto-evaluation.
3.  The auto-evaluation framework scores each sampled conversation against a set of quality metrics and rolls the metric scores up into a user satisfaction score.
4.  The system calculates value metrics, such as estimated time savings and estimated Virtual Agent efficiency, based on the evaluated conversations.

## Conversations excluded from evaluation

The following conversation types are excluded from auto-evaluation by default:

-   Conversations that use an inaccessible or empty knowledge base
-   Conversations that transfer immediately to a live agent
-   Short conversations
-   Conversations started by custom triggers

A script include controls these exclusion rules. You can extend the script include to exclude other types of conversations, such as conversations from a specific geographic location.

## Evaluation metrics

The auto-evaluation framework scores conversations on the following metrics, which roll up into the **User Satisfaction** score:

-   Request completion
-   Intent accuracy
-   Slot filling
-   Truthfulness
-   Context retention
-   Conciseness
-   Smoothness — deadlock avoidance
-   Coherence

## Value metrics

The **Value** view shows metrics that estimate the business impact of Virtual Agent conversations, including **Total evaluations**, **Average auto-evaluation score**, and **Evaluation score trend**.

Conversations are grouped into small, medium, and large sizes based on the number of words in each conversation. For example, a conversation of about 200 words or fewer is a small conversation.

You can view conversation efficiency and time savings by conversation size or by content type, such as knowledge and catalog.

The value metrics also include a user acceptance score and an estimated cost saving calculation that converts hours saved into a currency value.

**Related topics**  


[Review conversation evaluation scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mv-review-conversation-evaluation-scores.md)

[mv-label-a-conversation-evaluation]

[Calculate Virtual Agent cost savings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mv-calculate-virtual-agent-cost-savings.md)

