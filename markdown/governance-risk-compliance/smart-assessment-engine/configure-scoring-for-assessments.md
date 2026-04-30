---
title: Configure scoring for an assessment
description: Set up scoring for your assessment responses to calculate meaningful scores at the assessment, section, or subsection level.
locale: en-US
release: xanadu
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Scoring assessments, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configure scoring for an assessment

Set up scoring for your assessment responses to calculate meaningful scores at the assessment, section, or subsection level.

## Before you begin

-   Confirm that the smart assessment scoring plugin \[com.sn\_smart\_scoring\] is installed.
-   Role required: sn\_smart\_asmt.template\_manager or sn\_smart\_asmt.assessment\_admin

## About this task

-   Scoring can only be configured on a draft template. Once the template is published, you can no longer configure scoring for it.
-   If questions are skipped and not answered, they’re excluded from the score calculation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** to access the assessment workspace landing page.

2.  Create an assessment or open an existing assessment template, which is in a draft state to configure scoring.

3.  Select the **Scoring** tab.

4.  Under **Scoring settings**, select the **Enable scoring for this template** option.

    -   The **Enable scoring for this template** option enables you to apply scoring at the assessment, section, subsection, and question levels.
    -   Once scoring is enabled, you can enable normalization and configure its default settings. For more information, refer to [Configure normalization in assessment](configure-normalization-in-assessment.md)
5.  To activate scoring at assessment level, select the **Assessment score** option.

    Enabling the **Assessment Score** option initiates the calculation of the assessment-level score, which can be grouped by sections or questions.

6.  On the form, fill in the fields.

<table id="table_dgs_2gh_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group By

</td><td>

Option to select how the assessment score is calculated.-   **All sections together**

Score is calculated by combining the scores from all sections.

-   **All questions together**

Score is calculated by combining the scores of all individual questions.

</td></tr><tr><td>

Apply function

</td><td>

Function used to calculate the assessment score. For example if you select sum, scores for questions are added and that is the final score.The following function can be used:

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

</td></tr></tbody>
</table>7.  Select **Save**.

8.  Select the **Questions** tab.

9.  Turn on the toggle switch on the question for which you want to configure scoring.

10. On the form, fill in the fields.

<table id="table_zgp_jbn_xdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scores

</td><td>

Relevant score for the option. For number question types, the assessor's numeric response is used as the score.

</td></tr><tr><td>

Question Weight

</td><td>

Question weight shows how important a question is within the section or subsection, affecting its impact on the section or subsection's score. By default, the weight is added as 1. You can update it as necessary.

</td></tr><tr><td>

Scoring when unanswered

</td><td>

If questions are unanswered, this setting determines how they’re scored.**Note:** By default, the option **Skip scoring if question is unanswered** is checked. If you cleared this option, the **Default score** field is displayed.

</td></tr><tr><td>

Default score

</td><td>

Default score for the question, which is used in case the question goes unanswered.

</td></tr></tbody>
</table>    **Note:** Scoring logic varies by question type.

    -   For multi-select, you can assign scores to options, apply functions, and set question weights.
    -   For radio options, you can assign scores to choices and set question weights.
    -   For number-type questions, the assessor's numeric response is directly used as the score.
11. Select **Save**.

12. Turn on the toggle switch on the subsection for which you want to configure scoring.

13. On the form, fill in the fields.

<table id="table_rj4_kcn_xdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Apply function

</td><td>

Function used to calculate the subsection score. For example if you select sum, scores for questions are added and that is the final score.The following function can be used:

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

</td></tr><tr><td>

Subsection weight

</td><td>

Subsection weight shows how important a subsection is within a section, affecting its contribution to the section's score. By default, the weight is added as 1. You can update it as necessary.

</td></tr><tr><td>

Scoring when subsection is unanswered

</td><td>

If all questions within a subsection remain unanswered, this setting determines how they’re scored. **Note:** By default, the option **Skip scoring if all scored questions are unanswered and default values have not been set** is checked. If you cleared this option, the **Set default score for subsection** field is displayed.

</td></tr><tr><td>

Set default score for subsection

</td><td>

Default score for the subsection, which is used in case the all questions within the subsection are unanswered.

</td></tr></tbody>
</table>    **Note:** The subsection scores are calculated by grouping question scores based on the defined criteria.

14. Select **Save**.

15. Turn on the toggle switch on the section for which you want to configure scoring.

    ![Scoring section.](../image/scoring-section.jpg)

16. On the form, fill in the fields.

<table id="table_fcf_x2n_xdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group By

</td><td>

Option to select how the section score is calculated.-   **All subsections together**

Score is calculated by combining the scores from all subsections.

-   **All questions together**

Score is calculated by combining the scores of all individual questions.

</td></tr><tr><td>

Apply function

</td><td>

Function used to calculate the Section score. For example if you select sum, scores for questions are added and that is the final score.The following function can be used:

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

</td></tr><tr><td>

Section weight

</td><td>

Section weight shows how important a section is within an assessment, affecting its contribution to the assessment's score. By default, the weight is added as 1. You can update it as necessary.

</td></tr><tr><td>

Scoring when section is unanswered

</td><td>

If all questions within a section remain unanswered, this setting determines how they’re scored.**Note:** By default, the option **Skip scoring if all scored questions are unanswered and default values have not been set** is checked. If you cleared this option, the **Set default score for section** field is displayed.

</td></tr><tr><td>

Set default score for section

</td><td>

Default score for the section, which is used in case all questions within the section are unanswered.

</td></tr></tbody>
</table>17. Select **Save**.


## Result

The scoring is now configured at all required levels.

