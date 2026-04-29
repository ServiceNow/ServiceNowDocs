---
title: Verifying scoring calculations using the classic assessment engine
description: You can review scores and risk ratings in your questionnaires to help ensure the accuracy and consistency of risk scoring by verifying the correct application of weights, normalized values, scoring methods, and risk rating scales. Based on the different weights you assign, Third-party Risk Management aggregates these values and produces a composite score.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Scoring calculations using the classic assessment engine, Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Verifying scoring calculations using the classic assessment engine

You can review scores and risk ratings in your questionnaires to help ensure the accuracy and consistency of risk scoring by verifying the correct application of weights, normalized values, scoring methods, and risk rating scales. Based on the different weights you assign, Third-party Risk Management aggregates these values and produces a composite score.

## Verification checklist

The \[sn\_vdr\_risk\_asmt.vendor\_assessor\] or \[sn\_vdr\_risk\_asmt.vendor\_manager\] role is required to perform all related actions by using the Vendor Management Workspace or VRM Classic user interface. For full descriptions of assessment configuration and set up, see [Classic assessment configuration](../../grc-vendor-risk-implementation/concept/tprm-ongoing-config.md).

Here are some of the configurations that you can check while reviewing scores and risk ratings:

<table id="table_vkx_hjq_hcc"><thead><tr><th>

Configurations

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scoring method

</td><td>

Verify that the correct scoring method has been selected. You can select or update scoring methods for risk area domains, risk area criteria, and component criteria. For example, confirm that Min Risk is used instead of Average Risk if that aligns better with your assessment goals.

 For more information, see [Define a third-party risk domain](../task/tprm-risk-domain-define.md), [Define third-party risk area criteria](../task/tprm-risk-domain-criteria-df.md), and [Define component criteria](../task/tprm-component-criteria-define.md).

</td></tr><tr><td>

Weights

</td><td>

Verify the accuracy of weights applied to risk areas, risk criteria, risk components, and questions.You can apply custom weights to reflect the importance and priority of different types of risk.

Weight values for questions must be whole integers. Using decimals results in incorrect scores. For example, use 56 and not 0.56.

For more information on how to assign or update weights, see [Define a third-party risk domain](../task/tprm-risk-domain-define.md), [Define third-party risk area criteria](../task/tprm-risk-domain-criteria-df.md), [Define component criteria](../task/tprm-component-criteria-define.md), and [Define a question](../../grc-vendor-risk-implementation/task/tprm-questions-create.md).

</td></tr><tr><td>

Scoring calculations

</td><td>

Verify that calculations, normalized values, and unanswered questions are behaving as expected. For example, confirm that you’re accounting for unanswered questions not being included as part of the scoring calculation. For information on the different formulas used to calculate scores and ratings, see [Scoring calculations using the classic assessment engine](vendor-ratings-scoring.md).

For information on how to use normalized values to calculate assessment scores for Choice or Multiple Selection questions with the scored check box not selected [Normalize the scores for metrics](../../grc-vendor-risk-implementation/concept/set-max-norm-input.md).

</td></tr></tbody>
</table>## How to view risk ratings

You can view risk ratings for individual third parties, engagements, assessments, and questionnaires.

The following risk ratings are available to view.

-   Computed risk rating: The overall risk rating for the third party, calculated after the assessment.
-   Third party rating: An aggregate of all engagement ratings.
-   Engagement risk rating: Determined by the component criteria
-   Subsidiary risk rating: If company1 has company2 and company3 as subsidiaries, the aggregate of final ratings on company2 and company3 are the subsidiary ratings on company1.
-   Risk intelligence rating: Aggregate of all provider ratings.
-   Assessment rating: Determined by weights defined by category, calculations, and more.

**Note:** Risk ratings and scores are only available to view after assessments have been completed and scores have been integrated from a provider.

You can view all associated ratings for a third party by navigating to its Risk ratings related list. Navigate to **All** &gt; **Third-party Risk Management** &gt; **Third Parties** &gt; **All Third Parties** and select the third party you want. The following example shows you can view all available risk ratings as well as the Third-party risk components, Third-party risk areas, Assessments, Tiering assessments, Repeating assessments related lists, and more.

![Risk ratings and associated background information available for a Third party record.](../image/tprm-calc-tp-level.png "Example of a third-party record")

You can view all associated ratings for an engagement by navigating to its Risk ratings related list. Navigate to **All** &gt; **Third-party Risk Management** &gt; **Engagements** &gt; **All Engagements** and select the engagement you want. The following example shows you can view all available risk ratings as well as the Engagement risk components, Third-party risk areas, Assessments, Tiering assessments, Repeating assessments related lists, and more.

![Risk ratings and associated background information for an engagement record.](../image/tprm-calc-engage-level.png "Example of an engagement record")

You can view all associated ratings for an assessment by navigating to its Risk ratings related list. Navigate to **All** &gt; **Third-party Risk Management** &gt; **External Risk Assessments** &gt; **All Assessments** and then select the assessment you want. The following example shows you can view all available risk ratings as well as the Third-party risk areas, Questionnaires, Document requests, Downstream supplier related lists, and more.

![Risk ratings and associated background information available for an assessment record.](../image/tprm-calc-assess-level.png "Example of assessment record")

You can view all associated ratings for a questionnaire by navigating to its Risk ratings list. After navigating to an assessment, select the questionnaire you want to view. The following example shows you can view all available risk ratings, risk scores, and more.

![Risk ratings and scores available in questionnaire record.](../image/tprm-calc-q-level.png "Example of a questionnaire record")

**Parent Topic:**[Scoring calculations using the classic assessment engine](vendor-ratings-scoring.md)

