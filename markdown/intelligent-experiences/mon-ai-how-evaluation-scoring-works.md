---
title: How evaluation scoring works
description: Understand how AI Control Tower calculates quality and safety scores so you can interpret results accurately and configure scoring to reflect your priorities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mon-ai-how-evaluation-scoring-works.html
release: zurich
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# How evaluation scoring works

Understand how AI Control Tower calculates quality and safety scores so you can interpret results accurately and configure scoring to reflect your priorities.

Evaluation scoring happens in two stages. The first stage calculates a score for each individual metric. The second stage combines those metric scores into a composite quality or safety score using the weights you configure.

## Stage 1: How each metric is scored

The scoring engine evaluates each metric independently across the traces or spans in a session. It averages all individual evaluations to produce a metric score for that session.

How that score is determined depends on the level at which the metric is evaluated.

-   **Session-level metrics**

    Produce one score for the entire session. No averaging is needed. Task completion is an example of a session-level metric.

-   **Trace-level metrics**

    Receive a separate score on each trace in the session. The metric score is the average across all traces. Overall task completeness is an example of a trace-level metric for ServiceNow AI systems.

-   **Span-level metrics**

    Receive a separate score on each span in the session. The metric score is the average across all spans. Tool error is an example of a span-level metric.


For example, Tool calling correctness is a binary metric evaluated on four spans in a session. Each span scores either 0% \(fail\) or 100% \(pass\): 100%, 100%, 0%, and 100%. The metric score is the average across the spans:

```
(100 + 100 + 0 + 100) ÷ 4 = 75%
```

After stage 1, every metric in your template has a single score for the session, regardless of how many traces, spans, or evaluations produced it.

## Stage 2: How metric scores combine into a single score

The metric scores from stage 1 are combined into a single measure score using the weights you configure in your metric template. Each metric's score is multiplied by its assigned weight, and the results are added together. All weights must sum to 100%.

A single measure can include metrics from any combination of levels. Stage 1 handles the level differences, so by the time a metric reaches stage 2, it is a single score with an assigned weight.

For example, a quality template for an external AI agent includes metrics from the session and span levels:

|Metric|Level|Weight|Score \(from Stage 1\)|
|------|-----|------|----------------------|
|Task completion|Session|25%|72%|
|Answer completeness|Span|40%|91%|
|Context relevance|Span|25%|79%|
|Tool error|Span|10%|85%|

The quality score is:

```
(72 x 0.25) + (91 x 0.40) + (79 x 0.25) + (85 x 0.10) = 18.0 + 36.4 + 19.75 + 8.5 = 83%
```

For a ServiceNow agent, the same principle applies with different metrics. A quality template includes Overall task completeness at 60% weight and Tool calling correctness at 40% weight. If Overall task completeness scores 85% and Tool calling correctness scores 75%, the quality score is:

```
(85 x 0.60) + (75 x 0.40) = 51.0 + 30.0 = 81%
```

## Metrics included and excluded from the formula

You don't have to include every evaluated metric in your metric template. Metrics that are evaluated but not included in a template still produce scores. You can view those scores when drilling into traces and spans, but they don't affect the quality or safety score. This is useful when you want to monitor a metric for a period before giving it weight in the formula.

## Security metrics and scoring

AI Control Tower also evaluates a set of security metrics that assess risks specific to AI system inputs and outputs, such as prompt injection attempts and exposed personal data. Security metrics serve a different purpose than quality and safety metrics: they identify risks rather than measure performance.

Security metrics aren't available in monitoring metric templates and don't contribute to composite quality or safety scores. For details on security metrics, see [Configuring security metrics in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configuring.md).

## When a metric in your template isn't evaluated

When a metric in your quality or safety template isn't evaluated on a given session, trace, or span, the composite score is calculated from the remaining evaluated metrics rather than resolving to zero. Partial evaluation coverage still produces a meaningful composite, so a single skipped or unavailable metric doesn't invalidate the score for that session.

For example, if your quality template includes Task completion, Answer completeness, and Context relevance, and Context relevance isn't evaluated on a particular session, the quality score for that session is calculated from Task completion and Answer completeness only.

## How session scores are aggregated

Session scores are the foundation for broader scores across AI Control Tower. At the system and portfolio level, scores are simple averages with no additional weighting.

-   **AI system score**

    Averages quality scores across all evaluated sessions for that system. Each session counts equally regardless of duration or token usage.

    When evaluation is enabled for an individual AI system, you can view the aggregated score by selecting the **Monitor** tab on the asset record.

-   **Portfolio score**

    Averages quality scores across all AI systems. Each system counts equally regardless of how many sessions it has.

    To review quality and safety scores for AI systems across your portfolio, navigate to **Monitor** &gt; **Overview**.


## Scoring formats

All metrics use a scale where higher is better.

-   **Binary**

    Produces a score of 0% \(fail\) or 100% \(pass\). Sexism detection, Profanity detection, and Tool calling correctness are binary. Because there are no partial scores, a single failure in a set of evaluations has an outsized effect on the average.

-   **Percentage**

    Produces a score on a continuous scale from 0% to 100%. Answer completeness and Context relevance are percentage metrics.

-   **Tiered**

    Produces specific score values rather than a full continuous scale. Overall task completeness scores as successful \(100%\), partial \(50%\), or unsuccessful \(0%\).


## Score color coding

|Color|Range|Meaning|
|-----|-----|-------|
|Red|0–50%|Low. Investigate immediately.|
|Orange|51–75%|Fair. Review recent sessions for trends.|
|Green|76–100%|Good. Meeting quality or safety targets.|

**Parent Topic:**[Exploring AI system monitoring in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-exploring-aict-evaluations.md)

