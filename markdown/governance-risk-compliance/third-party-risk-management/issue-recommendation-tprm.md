---
title: TPRM issue recommendation skill
description: The issue recommendation skill in Now Assist for Third-party Risk Management \(TPRM\) uses generative AI to suggest potential issues based on historical assessment data, helping assessors and reviewers identify relevant risks more efficiently while retaining control over which issues are created.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Exploring, Now Assist, Third-party Risk Management, Governance, Risk, and Compliance]
---

# TPRM issue recommendation skill

The issue recommendation skill in Now Assist for Third-party Risk Management \(TPRM\) uses generative AI to suggest potential issues based on historical assessment data, helping assessors and reviewers identify relevant risks more efficiently while retaining control over which issues are created.

## Overview of issue recommendations

Third-party assessment reviewers \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] can use TPRM issue recommendations review completed third-party assessments after questionnaire responses are submitted. The TPRM issue recommendation skill analyzes historical issues created from all assessments, along with historical Smart Assessment and Classic assessment questions and responses, to generate suggested issues when semantically similar questions exist and the intended meaning of the answers is consistent.

For more information, see [Generate issue recommendations for TPRM](../task/create-recommendation-tprm-issue.md) and [Create or dismiss issues using recommendations](../task/manage-recommendation-issue.md).

## Benefits of issue recommendations

-   Generates potential issues based on intention from historic questions and answers.
-   Helps reviewers focus on relevant risks without reanalyzing every assessment response from scratch.
-   Supports consistent issue identification across all assessments while preserving human judgment.

## Components of an issue recommendation

When issue recommendations are generated, each recommendation includes contextual information to help reviewers evaluate its relevance:

-   Issue name and description
-   Related smart assessment question
-   Assessment type used as reference data
-   Priority derived from historical issue data
-   Historical issues used to generate the recommendation

The following table describes the key elements associated with an issue recommendation:

|Element|Description|
|-------|-----------|
|Issue description|Summary of the recommended issue generated from historical assessment findings.|
|Smart assessment question instance|Assessment question associated with the recommended issue.|
|Types|Source of the historic data. By default, it is from the previous assessments.|
|Historical issues|Previously created issues that were used as reference data to generate the recommendation.|
|Priority|Priority of the historical issue.|

**Note:** Issue recommendations can be generated only from Smart Assessment Engine questionnaires. They are generated based on historical assessment data from classic and smart assessments and configured recommendation logic. Reviewers must evaluate and confirm each recommendation before creating an issue.

The accuracy of issue recommendations depends on the quality and configuration of Smart Assessment Engine templates, including supported question types and historical issue data.

**Related topics**  


[TPRM issue recommendation skill](issue-recommendation-tprm.md)

[Create or dismiss issues using recommendations](../task/manage-recommendation-issue.md)

[Activate TPRM issue recommendation skill](../task/tprm-recommend-an-issue.md)

