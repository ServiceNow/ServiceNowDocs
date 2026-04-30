---
title: Scoring calculations using the classic assessment engine
description: Perform a comprehensive external risk assessment when calculating multiple ratings and scores by using the Third-party Risk Management application. You can gain a deeper understanding of the overall calculation process and learn how user-defined parameters and configurations influence the results of the questionnaires.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Scoring calculations using the classic assessment engine

Perform a comprehensive external risk assessment when calculating multiple ratings and scores by using the Third-party Risk Management application. You can gain a deeper understanding of the overall calculation process and learn how user-defined parameters and configurations influence the results of the questionnaires.

## Risk rating scale

Every time that you create a questionnaire, the system applies a default risk rating. You can configure the risk rating scale, which includes the categories, minimum, and maximum values, to meet your specific questionnaire needs that can vary for each assessment. For example, you can define risk rating values as colors rather than **1-Very High** through **5-Very Low**.

The following example shows the default risk ratings that are provided as part of the base system.

![List of default risk ratings. For the text description, refer to the text that preceded this example.](../image/vendor-risk-rating-scale.png "Default risk rating scale")

## Score calculation mechanism

The score calculation mechanism for each external assessment uses the ServiceNow AI Platform® assessment score calculation engine. This engine performs these calculations by using a series of related equations that are dynamically recalculated. You define the following parameters that affect the calculated assessment rating:

-   Questions \(metrics\)

    For more information on how to define a question, see [Define a question](../../grc-vendor-risk-implementation/task/tprm-questions-create.md).

-   Metric scale definition

    For more information on how to define the metric scale definition, see [Define a question](../../grc-vendor-risk-implementation/task/tprm-questions-create.md).

-   Categories

    For more information on how to define a category, see [Set up and maintain a question bank](../../grc-vendor-risk-implementation/task/tprm-question-bank-create.md).

-   Weights

    For more information on how to define a weight, see [Define component criteria](../task/tprm-component-criteria-define.md).

-   Risk rating scale

    For more information on how to define a risk rating scale, see [Set up risk rating scales for scoring](../../grc-vendor-risk-implementation/task/tprm-risk-rating-scales-config.md).

-   Business service rating scale

    At the end of the scoring calculation, if a third party or engagement is associated with a business service that you defined in the Service \[cmdb\_ci\_service\] table, that criticality weight is factored into the calculation. Different business services may have varying levels of associated risks. By adjusting the criticality weight, you can use the resulting values to adjust your risk mitigation strategies.

    **Note:** Only answered questions contribute to overall calculations.

    You can define the criticality weights by navigating to **All** &gt; **Self-Service** &gt; **Third-party Risk Management** &gt; **Assessment Setup** &gt; **Business Service Rating Scale**.

    As part of the base system, four ratings are defined:

    -   1 - most critical
    -   2 - somewhat critical
    -   3 - less critical
    -   4 - not critical
    You can associate each third party or engagement with multiple business services.


**Note:** A business service is a defined sequence of tasks or activities that contribute to the delivery of a service such as email, IT services, E-commerce.

The following infographic shows the assessment rating calculation process.

![Infographic that shows the calculation of the assessment rating. For the text description, refer to the list that follows.](../image/score-calculation-mechanism.png "Assessment rating calculation process")

1.  Each question on the questionnaire has these values calculated:
    1.  questionRatings: The rating for each question is calculated by the responses. For non-scored questions, the rating is determined by the metric scale definition and the values associated with the answers. For scored questions, `questionRating` is set to `0` or `1` depending on whether the correct answer is selected. The `questionRating` is not a value that is stored in a table.

    2.  questionPercentContribution: The percent contribution of each question within its category is determined by this calculation. This value is based on the weight that is assigned by the third-party risk manager to the question and the overall weight of the category. The questionPercentContribution is not a value that is stored in a table.
    3.  questionNormalizedValue: The normalized value for each question is calculated by multiplying the question rating, question percent contribution, and a constant value \(100\). This value enables you to compare questions with different weights and ratings.
2.  The categories of each questionnaire have these ratings calculated:
    1.  categoryRating: The rating for each category is calculated by summing up the normalized values of all the questions within the category. The category rating is derived from the associated risk rating scale.
    2.  categoryNormalizedValue: The category rating is normalized by multiplying it with the category weight to enable you to compare values across all categories.
3.  Questionnaire, questionnaireQuantitativeScore: The overall quantitative score for the assessment is calculated by summing up the normalized category scores. This score represents the risk score for the questionnaire.
4.  Documents, Qualitative Score: The calculation for the qualitative risk rating for the document requests is based on the answer to the default question “Do you have document ‘document name’? on the document request. This rating can be overridden by the third-party risk assessor if necessary.
5.  Assessment, assessmentRating: The final rating for the assessment is calculated by taking the weighted average of the questionnaires and document requests within each third-party risk area. The weights are determined by the risk area scoring method.

**Note:** Only answered questions contribute to overall calculations.

## Scored option for questions

Selecting the scored option \(**Scored** check box\) is optional. When the **Scored** check box is selected, the system treats the question as a correct/incorrect question. In this case, the system does not calculate `questionRating` using the metric scale definition \(High/Low\) formula. Instead, `questionRating` is set to `1` when the correct answer is selected and `0` when an incorrect answer is selected.

The system still calculates `questionPercentContribution` for scored questions based on the question weight within its category. The normalized value is then calculated using the standard normalization equation \(`questionNormalizedValue = 100 * questionRating * questionPercentContribution`\). As a result, a scored question contributes `0` when answered incorrectly, and contributes its weighted share of the maximum score \(100\) based on `questionPercentContribution` when answered correctly.

The **Maximum normalization** input field applies only when the **Scored** check box is not selected, because it is used with the High/Low rating calculation. When the **Scored** check box is selected, the maximum normalization input does not affect scoring. For more information on questions and normalized scores, see [Set up and maintain a question bank](../../grc-vendor-risk-implementation/task/tprm-question-bank-create.md), [Define a question](../../grc-vendor-risk-implementation/task/tprm-questions-create.md) and [Normalize the scores for metrics](../../grc-vendor-risk-implementation/concept/set-max-norm-input.md).

## questionRating calculation

You use the `questionRating` calculation to define the relative degree of significance of each individual assessment metric as compared to other metrics. This key variable helps to calculate the normalized value later in the process.

You can define the **Scale definition** for an individual assessment metric by setting it to be **High** or **Low**.

The following example shows how the metric scale definition field was defined in the Assessment Metric form.

![Metric scale definition example. For the text description, refer to the text that follows.](../image/questionRating-assessment-rating.png "Metric scale definition example")

-   **High** means that large numerical values indicate a positive result. If the metric scale definition is high, the following equation is used:

    `questionRating = (value - minValue) / (maxValue - minValue)`

-   **Low** means that small numerical values indicate a positive result. If the metric scale definition is low, the following equation is used:

    `questionRating = 1 - ((value - minValue) / (maxValue - minValue))`


The following example shows the question value field that is defined in the assessment instance question form.

![Assessment question value field example. For the text description, refer to the text that follows.](../image/questionRating-assessment-instance-question.png "Assessment question value example")

The **value** used in the equation is taken from the response to the question. The configuration of the metric defines the correct answer, which is the value, and the other values that are associated with the other incorrect or less desirable answers. The questionRating is not a value that is stored in a table.

## questionPercentContribution calculation

The `questionPercentContribution` defines the degree of significance of the assessment metric within the category where it’s included. This key variable is used in calculating the normalized value later in the process.

The following equation is used to calculate the `questionPercentContribution`.

`questionPercentContribution = (questionWeight / sumOfAllQuestionWeightsWithinCategory)`

**Note:** sumOfAllQuestionWeightsWithinCategory is the sum of weights in the category for questions that are answered.

The **Category** represents a theme for evaluating the assessable records in a metric type. You can define this category's example with the return on investment \(ROI\), risk, performance, security, personal data, and so on.

The **Weight** is a numerical value that represents the metric importance that relates to other metrics. A higher weight in proportion to the overall weight of the category has a stronger influence on the final score. You can define the weight, set it to any integer, and apply it to questions and categories.

**Note:** The questionPercentContribution is not a value that is stored in a table.

The following example shows the question category and weight field that you can define in the assessment metric form.

![Category and Weight field examples. For the text description, refer to the text that preceded this example.](../image/questionPercentContribution-assessment.png "Assessment question category and weight example")

## questionNormalizedValue calculation

The `questionNormalizedValue` enables questions with different weights and ratings to be compared equally on the same scale.

The following equation is used to calculate the `questionNormalizedValue`.

`questionNormalizedValue = 100 * questionRating * questionPercentContribution`

Each answer to every question \(assessment metric\) on the questionnaire has a **normalized value**. This normalized value enables you to make a meaningful comparison that is later rolled up to the category and the overall assessment results.

The following example shows a list of normalized values for an assessment group.

![Assessment group normalized value list. For the text description, refer to the text that preceded this example.](../image/questionNormalizedValue-assessmentgroup.png "Normalized value list for an assessment group example")

## categoryRating calculation

Now that there are normalized values for each metric within the category, the `categoryRating` calculates a value for the entire category that can then be normalized by using the `categoryNormalizedValue` equation to facilitate inter-category comparisons.

The following equation is used to calculate the `categoryRating`.

`categoryRating = sumOfAllQuestionNormalizedValuesWithinCategory`

The category **Rating** is the sum of all normalized values for the metrics within the category.

The stated **Risk Rating** for each category is derived from the associated Risk Rating Scale.

The following example shows the list of category ratings and risk ratings for an assessment category.

![Categories Rating and Risk rating list. For the text description, refer to the text that preceded this example.](../image/categoryRating-categories.png "Categories rating and risk rating list example")

## categoryNormalizedValue calculation

With the Category Ratings established, the `categoryNormalizedValue` equation uses this rating and the category weight to normalize the result across all categories.

The following equation is used to calculate the `categoryNormalizedValue`.

`categoryNormalizedValue = categoryRating * (categoryWeight / sumOfAllCategoryWeights)`

This calculated normalized value performs a more meaningful comparison that is later rolled up to the overall assessment results. Higher **categoryWeight** values increase the normalized value of the category.

The following example shows the list of normalized values for an assessment category.

![Categories Normalized value list example. For the text description, refer to the text that preceded this example.](../image/categoryNormalizedValue-categories.png "Categories normalized value list example")

## questionnaireQuantitativeScore calculation

With all categories normalized, the overall quantitative score for the assessment is calculated.

The following equation is used to calculate the `questionnaireQuantitativeScore`.

`questionnaireQuantitativeScore = sumOfAllCategoryNormalizedValues`

The output from the `questionnaireQuantitativeScore` equation is the sum of the normalized category scores. It’s presented as the **Risk Score** on the record for the questionnaire.

The following example shows a risk score for a questionnaire.

![Questionnaire Risk Score example. For the text description, refer to the text that preceded this example.](../image/questionnaireQuantitativeScore-risk-score.png "Questionnaire record with risk score example")

## Qualitative score for documents

Document Requests have a risk rating that is a qualitative score. The preliminary risk rating is based on the answer to the default question “Do you have document ‘document name’?”.

The document risk rating uses the scale that is shown in the following table.

|Response|Risk Rating|
|--------|-----------|
|Yes|Low|
|No or unanswered|High|
|N/A|Moderate|

The following example shows a risk rating for a document request.

![Document Requests Risk rating example. For the text description, refer to the text that preceded this example.](../image/document-requests.png "Document request risk rating example")

After the document is reviewed, it might be found to be deficient, so the Third-party risk assessor can override the default rating. The assessment retains the current **Risk Rating** and the **Original Risk Rating**. The stated **Risk Rating** for each category is derived from the associated Risk Rating Scale.

The following example shows a categories related list that includes the original and current risk rating.

![Categories related list showing the original and current risk rating example. For the text description, refer to the text that preceded this example.](../image/categories.png "Categories related list example")

## assessmentRating calculation

For any external assessment, the final rating for the assessment is calculated as the weighted average of the questionnaires and document requests within each third-party risk area.

The following equation is used to calculate the `assessmentRating`.

`assessmentRating = (AVG (Questionnaire + Document Request for a risk area) * weight assigned to that risk area + (Questionnaire + Document Request for another risk area) * weight assigned to that risk area) / the sum of the weights`

-   Questionnaire 1 = defined in the Security Risk Area
-   Questionnaire 2 = defined in the Financial Risk Area
-   Questionnaire 3 = defined in the Financial Risk Area
-   Document Request 1 = defined in the Security Risk Area

The risk area criteria are set like the example shown in the following table:

|Risk Area|Scoring Method|Weight|
|---------|--------------|------|
|Security Risk|Average Risk|10|
|Financial Risk|Max Risk|20|

The final rating for the assessment is calculated by using this equation:

`assessmentRating = (AVG (Questionnaire 1 + Document Request 1) * 10 + MAX (Questionnaire 2 + Questionnaire 3) * 20) / (10 + 20).`

The final rating is the overall assessment rating that considers the scores and ratings from all assessments conducted for a third-party or engagement. It’s calculated by taking the weighted average of the questionnaires and document requests within each risk area. This calculation process ensures that all relevant metrics, categories, and weights are taken into account based on how you defined these parameters and configurations. The calculation process and the factors involved can help you make informed decisions and take appropriate actions based on the final rating.

**Note:** For information on verifying risk ratings and scoring calculations, see [Verifying scoring calculations using the classic assessment engine](tprm-verif-q.md).

-   **[Verifying scoring calculations using the classic assessment engine](tprm-verif-q.md)**  
You can review scores and risk ratings in your questionnaires to help ensure the accuracy and consistency of risk scoring by verifying the correct application of weights, normalized values, scoring methods, and risk rating scales. Based on the different weights you assign, Third-party Risk Management aggregates these values and produces a composite score.

**Parent Topic:**[Third-party Risk Management reference](tprm-reference.md)

**Related topics**  


[Verifying scoring calculations using the classic assessment engine](tprm-verif-q.md)

