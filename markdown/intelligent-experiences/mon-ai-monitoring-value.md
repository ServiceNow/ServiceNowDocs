---
title: How monitoring scores contribute to AI value
description: Quality scores from monitoring can feed the value calculation. The value an AI system reports then reflects how well it performs, not just how often it is used.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-monitoring-value.html
release: australia
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 1
keywords: [monitoring, value, quality score]
breadcrumb: [Explore, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# How monitoring scores contribute to AI value

Quality scores from monitoring can feed the value calculation. The value an AI system reports then reflects how well it performs, not just how often it is used.

Value calculations in AI Control Tower measure productivity by combining how often an AI system is used, how much time it saves per use, and a quality dimension.

```
Productivity = Usage × Time × Quality
```

The quality dimension can be a constant, an indicator, or the quality score that monitoring produces. When a value template uses the quality score, AI Control Tower pulls the live score from the monitoring pipeline into the calculation, so the productivity an AI system reports reflects how well it actually performs.

## Why quality scores improve value accuracy

Because quality is one of the three dimensions in the productivity formula, the quality score directly affects the value an AI system reports. A system that scores poorly on quality reports lower productivity, even when usage is high. Configuring evaluation metrics that reflect your organization's quality standards therefore produces more accurate value measurement. When the metrics behind a quality score don't match what your organization considers good performance, the resulting value is skewed.

## When a quality score is not available

A value template uses the quality score only when one exists for the asset. When evaluation is not enabled for an asset, or no sessions have been scored yet, the template uses the **Default quality constant** so that value calculation continues without interruption. To start generating quality scores, enable evaluation for the asset.

## Setting and tracking value with quality scores

An asset owner selects **Quality Score** as the **Quality type** when creating or editing a value template. The asset owner then tracks the resulting productivity in the Value area, where the value reflects both how often and how well the AI system performs.

For more information about value templates and the dimensions they use, see [Measuring AI impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-measuring-ai-impact.md).

**Parent Topic:**[Exploring AI system monitoring in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-exploring-aict-evaluations.md)

