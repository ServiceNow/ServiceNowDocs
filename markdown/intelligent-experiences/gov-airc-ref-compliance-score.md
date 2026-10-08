---
title: AI system compliance score calculation reference
description: Formula, calculation rules, scheduled jobs, and properties that determine the compliance score of an AI system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-airc-ref-compliance-score.html
release: brazil
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
keywords: [compliance score, AI system compliance, scheduled jobs, AI Risk and Compliance]
breadcrumb: [Reference, Managing risk and compliance, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# AI system compliance score calculation reference

Formula, calculation rules, scheduled jobs, and properties that determine the compliance score of an AI system.

## Formula

```
AI system compliance score = average of the compliance scores of its active related entities
```

The result is a whole number from 0 to 100. The decimal part of the average is truncated, not rounded \(for example, an average of 66.7 produces a score of 66, not 67\).

## Calculation rules

The following table lists the rules that apply to the compliance score of an AI system.

|Rule|Behavior|
|----|--------|
|Entity link|Only entities linked to the AI system in the AI system entity map \[sn\_grc\_ai\_gov\_ai\_system\_entity\_map\] table contribute|
|Active entities|Inactive entities don't contribute|
|Third-line audit entries|Entities that belong to third-line audit entries don't contribute|
|Excluded AI systems|AI systems in the Retired or Canceled state have no score calculated|
|No related entities|The score is 0|
|Whole number|The average is truncated to a whole number before it is stored; the decimal part is dropped, not rounded|

## Scheduled jobs

The following table lists the scheduled jobs that keep the compliance scores current.

|Scheduled job|Purpose|
|-------------|-------|
|Compliance Score V2|Calculates the compliance score of each entity every two minutes from the entities queued in the compliance score table \[sn\_compliance\_compliance\_score\].|
|AI system Compliance score calculation|Calculates the compliance score of each AI system from the scores of its linked entities|
|AIRC daily compliance score scheduled job|Refreshes the data for the compliance score widget on the home page each day|

An entity is queued for the **Compliance Score V2** job when a control changes compliance status, a control is added to or removed from the entity, the entity is activated or inactivated, or its hierarchy changes. The **Entity hierarchy based scoring** property determines how the score is calculated.

## Compliance score gauge

The Compliance score card shows the score on a colored gauge. The gauge's color bands are a fixed default of the visualization component and aren't an admin-configurable setting.

## Properties

The following table lists the properties that select the two priority frameworks of each type that appear on the Compliance score card. For steps to configure these properties, see [Set up AI Risk and Compliance properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configure-airc-properties.md).

|Property|Purpose|
|--------|-------|
|sn\_grc\_ai\_gov.highlighted\_authority\_document|Up to two authority documents to show as priority frameworks|
|sn\_grc\_ai\_gov.highlighted\_policy|Up to two policies to show as priority frameworks|

