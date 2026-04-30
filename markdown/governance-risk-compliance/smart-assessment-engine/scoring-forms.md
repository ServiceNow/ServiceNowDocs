---
title: Scoring forms
description: Learn about the fields of the scoring forms. Use this form while configuring scoring for an assessment.
locale: en-US
release: yokohama
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2026-02-25"
reading_time_minutes: 3
breadcrumb: [Configure scoring for an assessment, Scoring assessments, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Scoring forms

Learn about the fields of the scoring forms. Use this form while configuring scoring for an assessment.

## Assessment scoring form

<table id="table_igk_dbk_k3c"><thead><tr><th>

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

Function used to calculate the assessment score. For example if you select sum, scores for questions are added and that is the final score.The following functions can be used:

-   **Average**

Divides the sum of all scores by the number of sections or questions.

-   **Maximum**

Selects the maximum score among all sections or questions.

-   **Minimum**

Selects the minimum score among all sections or questions.

-   **Sum**

Adds the scores for all sections or questions.

-   **Weighted average**

Assigns greater importance to values based on their weight. To calculate it, multiply each question, section or subsections score by its weight, sum up the results, and divide that by the total weight.


</td></tr></tbody>
</table>## Question scoring form

<table id="table_z3x_jbk_k3c"><thead><tr><th>

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
</table>## Subsection scoring form

<table id="table_ik5_lbk_k3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Apply function

</td><td>

Function used to calculate the subsection score. For example if you select sum, scores for questions are added and that is the final score.The following functions can be used:

-   **Average**

Divides the sum of all scores by the number of sections or questions.

-   **Maximum**

Selects the maximum score among all sections or questions.

-   **Minimum**

Selects the minimum score among all sections or questions.

-   **Sum**

Adds the scores for all sections or questions.

-   **Weighted average**

Assigns greater importance to values based on their weight. To calculate it, multiply each question, section or subsections score by its weight, sum up the results, and divide that by the total weight.


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
</table>## Section scoring form

<table id="table_hhp_pbk_k3c"><thead><tr><th>

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

Function used to calculate the Section score. For example if you select sum, scores for questions are added and that is the final score.The following functions can be used:

-   **Average**

Divides the sum of all scores by the number of sections or questions.

-   **Maximum**

Selects the maximum score among all sections or questions.

-   **Minimum**

Selects the minimum score among all sections or questions.

-   **Sum**

Adds the scores for all sections or questions.

-   **Weighted average**

Assigns greater importance to values based on their weight. To calculate it, multiply each question, section or subsections score by its weight, sum up the results, and divide that by the total weight.


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
</table>