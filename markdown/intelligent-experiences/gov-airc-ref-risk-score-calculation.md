---
title: AI risk score calculation reference
description: Formulas, rating bands, lookup matrix, and rollup settings that determine the inherent, control effectiveness, and residual ratings of an AI system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-airc-ref-risk-score-calculation.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 4
keywords: [inherent risk, control effectiveness, residual risk, risk rollup, rating bands, AI Risk and Compliance]
breadcrumb: [Reference, Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# AI risk score calculation reference

Formulas, rating bands, lookup matrix, and rollup settings that determine the inherent, control effectiveness, and residual ratings of an AI system.

## Formulas

The risk assessment methodology \(RAM\) named Risk assessment for AI inventory uses the following formulas for each risk.

```
Inherent score = Average(Impact, Likelihood)
Control effectiveness % = (sum of weights of compliant controls ÷ sum of weights of compliant and non-compliant controls) × 100

```

The Impact and Likelihood factors use the same four score values, but different rating labels.

|Rating|Score|
|------|-----|
|Low|1|
|Medium|4|
|High|7|
|Critical|10|

|Rating|Score|
|------|-----|
|Unlikely|1|
|Likely|4|
|Highly likely|7|
|Almost certain|10|

The control effectiveness calculation uses only active controls with a status of Compliant or Non-compliant, weighted by the control weighting value. The result is rounded to a whole number. If the risk has no such controls, the result is 0.

The rollup combines the scores of the contributing risks into one score for the AI system.

```
AI system score = Average(score of each contributing risk)
AI system rating = rating band of the AI system score
```

**Note:**

The tables and formulas use "AI system" terminology throughout, matching the underlying table and field names. The same rollup, primary RAM, and formulas apply to AI models and datasets, because every AI digital asset is represented by the same AI system entity map record regardless of asset type.

## Inherent rating bands

|Rating|Lower limit of band|Rating value|
|------|-------------------|------------|
|Low|0|1|
|Medium|4|4|
|High|7|7|

## Control effectiveness rating bands

|Control effectiveness %|Level|Rating|Rating value|
|-----------------------|-----|------|------------|
|Less than 60|0|Ineffective|1|
|60 to 99|1|Needs improvement|4|
|100|2|Effective|7|

## Primary RAM requirements

The following table lists the requirements for a risk-based RAM to be the primary RAM of an AI system.

|Requirement|Value|
|-----------|-----|
|State|Published|
|Assessed on|Risks|
|Domain|AI risk and compliance|

The default primary RAM is selected in the following order.

1.  The RAM in the **sn\_grc\_ai\_gov.aisystem\_primary\_ram** property, when more than one eligible RAM exists and the RAM is eligible. If the property value isn't eligible, no default RAM is set.
2.  The first eligible RAM in alphabetical order by name, when the property is empty or only one eligible RAM exists.

## Rollup inputs

The following table lists what contributes to the AI system rollup.

|Input|Rule|
|-----|----|
|Related entities|Active entities in the AI system entity map whose primary RAM matches the primary RAM of the AI system, excluding third-line audit entries|
|Risks|All risks of the contributing entities, excluding third-line audit entries|
|Risk assessments|Active assessments on the contributing entities that use the primary RAM and are in the Monitor state|
|AI systems|All AI systems except those in the Retired or Canceled state|

## Rollup settings

|Setting|Value|
|-------|-----|
|Score rollup|Average|
|Annual loss expectancy rollup|Maximum|

## Rollup result stages

|Stage|Description|
|-----|-----------|
|Needs update|Result flagged for recalculation after the primary RAM of the AI system is set or changed, or after a score-affecting change on a related entity that uses the primary RAM|
|Processing|Result picked up by a scheduled job that recalculates the scores|
|Updated|Result stored with the new ratings. A result flagged again during processing returns to Needs update.|

## Properties

|Property|Purpose|
|--------|-------|
|sn\_grc\_ai\_gov.aisystem\_primary\_ram|Default primary RAM for AI systems when more than one eligible RAM exists|

## Assessed classification

The following table lists the predefined RAMs that produce an assessed classification. Each RAM ships in the Draft state. Publish a RAM before you use it.

|RAM|Applies to|RAM selection|
|---|----------|-------------|
|Risk classification for AI system|AI systems|Selected when the assessment starts|
|Risk classification for AI Model or Dataset|AI models and datasets|Selected when the assessment starts|

Both RAMs use the following formula.

```
Inherent score = Average(Impact score, Likelihood score)
```

The following table lists how each RAM converts the inherent score to a rating.

|Score|AI system|AI model or dataset|
|-----|---------|-------------------|
|0 to 5.00|Low|Low|
|5.01 to 7.00|Medium|Medium|
|7.01 to 9.00|High|High|
|9.01 to 10|Unacceptable|Critical|

The Impact factor is a weighted average of six subfactors. The following table lists each subfactor and its weight.

|Subfactor|Weight|
|---------|------|
|Regulatory scrutiny|15%|
|Financial impact|20%|
|Operational impact to the business|20%|
|Regulation complexity|20%|
|Number of businesses impacted|10%|
|Reputational impact|15%|

The following table lists how the weighted average converts to the Impact score.

|Weighted average|Impact score|
|----------------|------------|
|0 to 5.00|5|
|5.01 to 7.00|7|
|7.01 to 9.00|9|
|9.01 to 10|10|

The Likelihood factor uses a four-point scale. The following table lists each rating and its score.

|Rating|Score|
|------|-----|
|Rare|1|
|Possible|7|
|Likely|9|
|Immediate|10|

