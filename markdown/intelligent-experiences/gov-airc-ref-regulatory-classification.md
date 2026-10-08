---
title: Regulatory risk classification reference
description: Risk assessment methodologies, formulas, risk ratings, and records that determine the regulatory risk classification of an AI asset.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-airc-ref-regulatory-classification.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 4
keywords: [regulatory risk classification, automated risk classification, risk ratings, AI Risk and Compliance]
breadcrumb: [Reference, Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Regulatory risk classification reference

Risk assessment methodologies, formulas, risk ratings, and records that determine the regulatory risk classification of an AI asset.

## Risk assessment methodologies

The following table lists the predefined risk assessment methodology \(RAM\) that produces an automated classification. The RAM ships in the Draft state. Publish the RAM before you use it. For the RAMs that produce an assessed classification, see [AI risk score calculation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-ref-risk-score-calculation.md).

|RAM|Applies to|Score formula|RAM selection|
|---|----------|-------------|-------------|
|Automated risk classification for AI system|AI systems|Highest of six factor scores|Specified by the **sn\_grc\_ai\_gov.ai\_system\_automated\_risk\_classification\_asmt\_ram** property|

## Risk ratings

The following table lists how the automated RAM converts a score on a scale of 0 to 10 to a rating.

|Score|Rating|
|-----|------|
|0|To be determined|
|0.1 to 5.00|Low|
|5.01 to 7.00|Medium|
|7.01 to 9.00|High|
|9.01 to 10|Unacceptable|

An asset without an inherent rating is treated as To be determined. In the automated RAM, a score above 0 but below 0.1 also falls in the To be determined risk rating.

## Automated classification formulas

The automated RAM uses the following formulas.

```
Factor score = (points total ÷ maximum possible points) × 8
Inherent score = Maximum(factor 1, factor 2, factor 3, factor 4, factor 5, factor 6)
```

A factor whose points total is 9000 or more scores 10. For a field that accepts several selections, the points total uses the highest value among the selected options. The factor score has two decimal places.

## Automated classification factors

The following table lists the six factors and the Use and purpose fields that each factor uses.

|Factor|Fields and maximum points|Maximum total|
|------|-------------------------|-------------|
|Context of Use|Interaction type with end users \(60\), Area where the AI system is used \(80\), Intended outcome of the AI system \(60\)|200|
|Autonomy &amp; Role of Human Oversight|System autonomy level \(50\), Type of output produced \(50\), Level of human involvement \(50\)|150|
|Data &amp; Model Risks|Type of output produced \(50\), Data used by the system \(40\)|90|
|Impact on Individuals &amp; Society|People affected by the AI system \(50\), Type of output produced \(50\), Intended outcome of the AI system \(60\)|160|
|Cybersecurity &amp; Systemic Risks|Area where the AI system is used \(80\), Data used by the system \(40\), System autonomy level \(50\)|170|
|Governance &amp; Compliance Maturity|Area where the AI system is used \(80\), People affected by the AI system \(50\), Level of human involvement \(50\)|180|

## Use and purpose answer point values

The following tables list the point value of each answer option for every Use and purpose field.

|Answer option|Points|
|-------------|------|
|Not Applicable|0|
|Efficiency Boost|10|
|Quality Enhancement|20|
|Decision Guidance|30|
|Automation of Tasks|40|
|Customer Experience Upgrade|50|
|Insight Generation|60|

|Answer option|Points|
|-------------|------|
|Internal Operations|10|
|Customer Services|20|
|Sales &amp; Marketing|30|
|Finance &amp; Accounting|40|
|IT &amp; Security|50|
|Supply Chain|60|
|HR &amp; Workforce|70|
|External Partner Ecosystem|80|

|Answer option|Points|
|-------------|------|
|Simple Alerts|10|
|Insight &amp; Summaries|20|
|Ranking &amp; Scores|30|
|Recommendations|40|
|Generated Content|50|
|Automated Decisions|9000|
|System Actions|9010|

|Answer option|Points|
|-------------|------|
|Internal Team|10|
|Specific Customer Groups|20|
|General Customer Base|30|
|External Partners|40|
|Public or Large Audiences|50|

|Answer option|Points|
|-------------|------|
|Not Applicable|0|
|Full User Control|10|
|User-Guided with AI Support|20|
|Shared Control|30|
|AI-Initiated with User Approval|40|
|Fully Automated Workflow|50|

|Answer option|Points|
|-------------|------|
|Public or General Info|10|
|Business Operational Data|20|
|Customer Interaction Data|30|
|Behavioral or Usage Data|40|
|Profile or Account Data|9000|
|Sensitive Business Data|9010|

|Answer option|Points|
|-------------|------|
|Not Applicable|0|
|No Direct Interaction|10|
|Background Support|20|
|Notifications &amp; Prompts|30|
|User-Facing Recommendations|40|
|Chat-Based Interaction|50|
|Interactive Experience|60|

|Answer option|Points|
|-------------|------|
|Not Applicable|0|
|Assistive \(AI suggests\)|10|
|Semi-Automated \(acts with confirmation\)|20|
|Condition-Based Automation|30|
|Event-Triggered Automation|40|
|Fully Automated Execution|50|

Selecting **Profile or Account Data**, **Sensitive Business Data**, **Automated Decisions**, or **System Actions** triggers the 9000-point override described in the Automated classification formulas section, regardless of the other answers on the same asset: The factor score becomes 10 and the inherent score is Unacceptable.

## Records and fields

The following table lists the records and fields that store the classification.

|Record|Field|Purpose|
|------|-----|-------|
|Asset governance details \[sn\_ai\_governance\_asset\_governance\_details\]|Inherent risk rating|Inherent rating that the classification assessment produces|
|AI system entity map \[sn\_grc\_ai\_gov\_ai\_system\_entity\_map\]|Risk classification|Classification of the related entity, copied from the governance details record|

## Properties

The following table lists the property that controls automated classification.

|Property|Purpose|
|--------|-------|
|sn\_grc\_ai\_gov.ai\_system\_automated\_risk\_classification\_asmt\_ram|Published RAM that classifies AI systems automatically|

