---
title: Scoring assessments
description: Scoring in Smart Assessment Engine is a systematic way to evaluate responses to various questions within an assessment. By attributing scores to answers, you can translate qualitative responses into quantitative data, offering a measurable and comparable outcome for each assessment.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Scoring assessments

Scoring in Smart Assessment Engine is a systematic way to evaluate responses to various questions within an assessment. By attributing scores to answers, you can translate qualitative responses into quantitative data, offering a measurable and comparable outcome for each assessment.

## Exploring scoring

In Smart Assessment Engine, scoring involves assigning numerical values to responses based on predefined criteria. You can apply scores to individual questions or to entire sections or subsections of questions. Scoring can be done for various question types, like radio buttons, check boxes, drop-down lists, and number fields. Each possible answer can be preassigned with a score, or scores can be calculated based on ranges or combinations of responses. Scoring provides a clear, objective measurement of the responses given in an assessment.

**Note:** Scoring logic varies by question type:

-   For multiselect question types, you can assign scores to options, apply functions, and set question weights.
-   For radio question types, you can assign scores to choices and set question weights.
-   For number question types, the assessor's numeric response is used as the score.

You can also normalize the scores in which raw scores \(the actual score earned on questions\) are transformed into a standardized range or distribution. For more information, refer to [Normalization in assessment](normalization-in-assessment.md).

## Scoring levels

Scores can be calculated using predefined functions at various levels within an assessment:

-   **Assessment level**

    Aggregates the scores from all sections and questions within that assessment.

-   **Section level**

    Aggregates the scores from all subsections and questions within that section.

-   **Subsection level**

    Aggregates the scores from all questions within that subsection.

-   **Question level**

    Calculates the scores for each individual question.


Functions, such as Sum, Min, Max, Average, and Weighted average, are available at the assessment, section, and subsection levels. At the question level, all functions except Weighted average are available. However, only one function can be defined at all levels.

The following function can be used:

-   **Average**

    The sum of all scores is divided by the number of sections or questions.

-   **Maximum**

    The maximum score among all sections or questions is selected.

-   **Minimum**

    The minimum score among all sections or questions is selected.

-   **Sum**

    Scores for all sections or questions are added.

-   **Weighted average**

    A weighted average assigns greater importance to values based on their weight. To calculate it, multiply each question, section or subsections score by its weight, sum up the results, and divide by the total weight.


After an assessment is completed, scores are calculated and stored at multiple levels, such as assessment, section, subsection, and question, based on the scoring configuration defined in the template. For more information about where scores are stored and how to access them, see [Scoring results](scoring-results.md).

## Benefits of scoring

Scoring in Smart Assessment Engine transforms subjective responses into objective data. This data enables you to understand and use assessment results effectively, such as for identifying areas of improvement, evaluating progress, or tracking outcomes. Benefits of scoring include the following:

-   Aids in analyzing complex data and making informed decisions by providing clear, objective metrics.
-   Aligns assessments with your specific goals and needs because scores can be assigned and calculated in various ways.
-   Simplifies the process of interpreting results. Instead of sifting through qualitative data, you can quickly glance at numerical scores to analyze performance.
-   Confirms that all responses are evaluated consistently, reducing the likelihood of bias.

