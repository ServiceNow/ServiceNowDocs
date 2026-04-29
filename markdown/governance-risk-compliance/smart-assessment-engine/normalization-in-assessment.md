---
title: Normalization in assessment
description: Normalization in Smart Assessment Engine refers to adjusting assessment question scores to a common scale to promote fair comparison and prioritization.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Scoring assessments, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Normalization in assessment

Normalization in Smart Assessment Engine refers to adjusting assessment question scores to a common scale to promote fair comparison and prioritization.

## Exploring normalization

Scoring in Smart Assessment Engine enables you to translate qualitative responses into quantitative data, which provides a measurable and comparable outcome for each assessment. For more information on scoring, refer to [Scoring assessments](scoring-in-assessments.md). Normalization in scoring addresses the issue of inconsistent scoring scales across different assessments, promoting fairness and comparability. It enables for accurate aggregation and analysis of scores, regardless of varying question difficulty or formats. Without normalization, scores from different assessments or sections can be misleading, leading to unfair evaluations and inaccurate insights. Normalization is supported for number, drop-down, radio button, and check box type questions.

Normalization is the process by which raw scores \(the actual score earned\) are transformed into a standardized range or distribution. This transformation facilitates comparison across different questions, sections, subsections, or entire assessments. The normalization feature confirms that scores from various components, which may differ in structure, difficulty, or scoring methods, are adjusted to a common scale. This is essential for providing fair comparisons, accurate analytics, and consistent insights. Normalization helps standardize these measurements, enabling different metrics or scores to be evaluated on the same scale.

The assessment admin defines the default normalization strategy for template categories, confirming consistent scoring logic across assessments. They can also configure the normalization formula or create custom formulas.

The template manager can do the following:

-   Enables or disables normalization after scoring and aggregation details are set up.
-   Defines normalization parameters at various aggregation levels \(assessment, section, subsection or questions\)
-   Overrides default normalization parameters to determine the best strategy for their assessment.

Learn how normalization adjusts individual assessment scores to a common scale, enabling comparison across different assessments. For more information, refer to [Score normalization](score-normalization.md).

## Default Normalization

A template's purpose determines its default normalization settings, including whether normalization is enabled and which normalization strategy is used. Changing the purpose resets normalization settings, but reassigning the purpose is required to update template values. You can define a default normalization configuration and apply it automatically at various levels within an assessment, including the assessment itself, sections, subsections, and individual questions. The Linear normalization strategy is available by default. You can also create a custom normalization strategy. For more information, refer to [Create a normalization strategy](../task/create-a-normalization-strategy.md).

## Normalization configuration behavior

Normalization behaves differently depending on whether it’s overridden at a specific level. An override happens when you manually change the normalization settings at a level, for example, turning it on when it’s off by default, turning it off when it’s on by default, or modifying the strategy or input values while it’s enabled.

If you don’t override the configuration, enabling scoring at a level will automatically apply normalization using default values, and any changes to those defaults will be reflected across levels. Disabling scoring will also disable normalization.

However, if you override the configuration, any changes made to the default settings won’t affect that level, it will retain the customized behavior you’ve set.

## States of normalization

The normalization state can vary at all levels based on the normalization strategy used or any updates made to it.

-   **Default strategy from template settings**

    This state is displayed when default normalization is enabled and no configurations are overridden.

-   **Default strategy with some overrides**

    This state is displayed when default normalization is enabled and only input values are changed, with the same strategy as default.

-   **Custom strategy**

    This state is displayed when the normalization strategy differs from the default or when normalization is enabled explicitly at the level despite being turned off by default.

-   **Set up normalization**

    This state is displayed when normalization is turned off at the level, either due to default settings or explicit user action.


## Benefits of normalization

Normalization in Smart Assessment Engine offers numerous benefits, confirms that all scores are on the same scale, making it easier to aggregate and analyze data.

-   Normalization provides transparency in the assessment process, as scores are adjusted to a common scale, making it easier to understand the results.
-   Normalization simplifies aggregation by removing the complexity of aggregating scores across different scoring scales and methodologies.
-   Normalization creates a uniform scoring model, enabling consistent and fair comparisons, and facilitating apples-to-apples comparisons.
-   Normalization makes it easier to understand and interpret scores, as they’re all on the same scale.
-   Normalization enables decision-makers to make more informed decisions, as they’re based on a consistent and fair comparison of scores.

