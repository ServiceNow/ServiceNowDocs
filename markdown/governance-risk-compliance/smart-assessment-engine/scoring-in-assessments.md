---
title: Scoring assessments
description: Scoring in Smart Assessment Engine is a systematic way to evaluate responses to various questions within an assessment. By attributing scores to answers, you can translate qualitative responses into quantitative data, offering a measurable and comparable outcome for each assessment.
locale: en-US
release: xanadu
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
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


## Scoring results

The final scores are displayed based on the upstream application requirement. They determine how and where the scores are shown to the end user, providing flexibility for score visualization and presentation.

Each section or assessment level has a metric record connected to it through a metric\_mapping record. To identify the scores, metric\_mapping can be used to check the metric associated with each section, and from the associated metric record, the metric\_instance can be located.

Once the scoring is completed, the final scores are available as follows:

-   Question level scores are stored in the question instance \(sn\_smart\_asmt\_question\_instance\) table for individual questions.
-   Section, subsection, and assessment level scores are stored in the \(sn\_smart\_scoring\_metric\_instance\) table.

## Benefits of scoring

id="ul\_m4c\_r4q\_wdc"&gt;

Scoring in Smart Assessment Engine transforms subjective responses into objective data. This data enables you to understand and use assessment results effectively, such as for identifying areas of improvement, evaluating progress, or tracking outcomes. Benefits of scoring include the following:

-   Aids in analyzing complex data and making informed decisions by providing clear, objective metrics.
-   Aligns assessments with your specific goals and needs because scores can be assigned and calculated in various ways.
-   Simplifies the process of interpreting results. Instead of sifting through qualitative data, you can quickly glance at numerical scores to analyze performance.
-   Confirms that all responses are evaluated consistently, reducing the likelihood of bias.

