---
title: Calculating RTO and RPO
description: The BCM application provides an assessment questionnaire for calculating the recovery time objective \(RTO\) and recovery point objective \(RPO\) in the business impact analysis \(BIA\). As a pre-requisite to the BIA, BCM administrator defines the impact ratings and sets up the assessment questions. After receiving the responses to the assessment, the BCM application calculates the RTO and RPO.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Calculating RTO and RPO

The BCM application provides an assessment questionnaire for calculating the recovery time objective \(RTO\) and recovery point objective \(RPO\) in the business impact analysis \(BIA\). As a pre-requisite to the BIA, BCM administrator defines the impact ratings and sets up the assessment questions. After receiving the responses to the assessment, the BCM application calculates the RTO and RPO.

## BCM dependency tree

Before calculating the recovery time objective \(RTO\) and recovery point objective \(RPO\) in the business impact analysis \(BIA\), verify that all the required BCM applications are installed.

## BCM implementation

Setting up the impact ratings to evaluate an impact category is a crucial step in business continuity management. To grasp the importance of configuring these impact categories, refer to the steps needed for implementing the BCM process, as outlined in the checklist.

![Flowchart showing sequential BCM implementation steps from installing applications through configuring plan templates.](../../grc-bcm-implementation/image/BCMImplementationFlowchart.jpg "Graphical flowchart of BCM implementation checklist")

-   **BIA workflow**

    When a business impact analysis \(BIA\) owner submits the BIA for a review, the BIA is updated to the review state. The BIA owner responds to the questions in the assessment questionnaire. If you are an IT analyst or IT owner, you can estimate the recovery point objective for your data applications and systems by responding to the Recovery point objective assessment in the BIA. Based on the configuration set up by BCM administrator, the questions are displayed in the **Recovery point objective assessment** tab of the BIA.

    A sample BIA workflow is shown in the example.

    ![BIA workflow state diagram showing transitions from Draft through Approved with decision points.](../image/bia-lifecycle.png)


## Responding to the assessments

The business users and IT owners perform business impact analysis by responding to the assessments in the BIA component in the BCM UIB Workspace. A sample view of the **Assessments** tab is shown in the example.

![Assessments tab in the BIA.](../image/bia-assessments-tab.png)

If you are the IT owner, you can estimate the recovery point objective for your data applications and systems by responding to the Recovery point objective assessment in the BIA.

## Administrator view for configuring impact category and ratings

BCM administrators configure the assessment questionnaire to include one or more impact ratings such as **Low**, **Moderate**, or **High** for an impact category. The Impact Ratings related list is displayed in the Impact Category record as shown in the example.![Administrator view for the impact category.](../image/impact-category-admin-view.png)

BCM administrators specify the threshold of non-tolerance for the impact ratings according to impact category. The disruption duration for the first non-tolerable impact category is selected for the recovery time objective \(RTO\). The impact ratings have the specified values:

-   Low = 1
-   Moderate = 2
-   High = 3

The rating for the impact category is calculated based on the disruption duration as shown in the example.

![An example to show the calculation of impact category results.](../image/BIAImpactCategoryResults.png "Calculating the impact category")

Based on the configuration set up by BCM administrator, the questions are displayed in the **Recovery point objective assessment** tab as shown in the example.

![Recovery point objective assessment.](../image/rpo-assessment-questions-1.png)

## Calculation of RPO score for the BIA with examples

Consider the scenario where each question response has a numeric value. The application calculates the category score for each RPO impact category based on the highest response value.

![Calculation.](../image/rpo-score-for-BIA-step-a.png)

The application selects the highest category score from all the RPO categories. In the example, the highest category score is 40.

![Category score.](../image/rpo-score-for-BIA-step-b.png)

The application uses the Score Timeframe Mapping, defined at the template level, to determine the appropriate timeframe value. In the example, the category score is 40, which falls between the lower and upper threshold scores. The timeframe mapped to this score is "Immediately." Therefore, the system-calculated RPO value is "Immediately."

![Calculated RPO value.](../image/rpo-score-for-BIA-step-c.png)

## Recovery time objective assessment

If you are the business user, you can estimate the recovery time objective for your business services and processes by responding to the Recovery time objective assessment in the **Assessments** tab. The questions are displayed in the **Recovery time objective assessment** tab according to the configuration set up by BCM administrators. A sample Recovery time objective assessment is shown in the example.

![Recovery time objective assessment.](../image/rto-assessment-questions.png)

## Calculation of RTO score for the BIA with examples

Consider the scenario where each question response is assigned a numeric value. The application identifies the highest tolerable value for each RTO Impact category.

![Tolerable value for each RTO.](../image/rto-score-for-BIA-step-a.png)

The application then calculates the “Tolerable downtime” value for each RTO Impact category as the Impact rating with a value higher than the highest tolerable value. If no value exists, the application uses the maximum RTO value \(that is defined at the Impact category\) as the “Tolerable downtime.” The system calculates the RTO score based on the lowest “Tolerable downtime” value from all RTO impact categories.

**Note:** RTO cannot be calculated when the recovery tier doesn’t exist for the “Tolerable downtime” value.

In the example, the RTO score based on the lowest “Tolerable downtime” value is 8 Hours.

![Calculated RTO value.](../image/rto-score-for-BIA-step-b.png)

## Sample RTO calculation

Consider the scenario for another sample RTO calculation. BCM administrator has configured an intolerable impact rating for the Revenue impact category and defined the intolerable impact. If you are the business impact analysis owner, you must identify the timeline at which the revenue impact may go beyond $1M. See the sample RTO calculation for different scenarios as shown in the table.

<table id="table_zsm_2y2_3xb"><thead><tr><th>

Scenario

</th><th>

Non-tolerable impact

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scenario 1

</td><td>

In the Impact Ratings table, the **Tolerable** field is set to **false**.

</td><td>

If the administrator has specified that Low regulatory impact is non-tolerable, its corresponding disruption duration is set as the recovery time objective \(RTO\).

 In this example, the disruption duration for the **01 - Low** impact rating is set to 4 hours. Therefore, the recovery time objective \(RTO\) for the impact category is above 4 hours.

 Even if the moderate impact disruption duration is shorter, the calculation selects the value from the first alphanumerically sorted impact rating that has the **Tolerable** field set to **false**.

</td></tr><tr><td>

Scenario 2

</td><td>

In the Impact Ratings table, the **Tolerable** field is set to **false**.

</td><td>

If the administrator has specified that Moderate regulatory impact is non-tolerable, its corresponding disruption duration is set as the recovery time objective \(RTO\).

 In this example, the disruption duration for **02 - Moderate** impact is set to 24 hours. Therefore, the recovery time objective \(RTO\) for the impact category is above 24 hours.

</td></tr><tr><td>

Scenario 3

</td><td>

In the Impact Ratings table, the **Tolerable** field is set to **false**.

</td><td>

If the administrator has specified that High regulatory impact is non-tolerable, its corresponding disruption duration is set as the recovery time objective \(RTO\) as shown in the example. ![Administrator view for the impact category.](../image/impact-category-admin-view.png)

 In the tabular example, the disruption duration for **03 - High** impact is set to 72 hours. Therefore, the recovery time objective for the impact category is above 72 hours.

</td></tr><tr><td>

Scenario 4

</td><td>

The **Tolerable** field for the Low, Moderate, and High impact ratings is set to **true**.

</td><td>

If the administrator has set all the impact ratings as tolerable, the value specified in the **Maximum RTO value** field in the template is selected as the recovery time objective \(RTO\).

 In the example, the administrator has set all the impact ratings as tolerable. Therefore, the recovery time objective \(RTO\) is one month according to the value specified in the **Maximum RTO value** field.![Maximum RTO value.](../image/maximum-rto-value.png)

</td></tr></tbody>
</table>-   **Calculation of overall impact assessment result for a BIA**

    When you update the **Disruption Duration** of an impact category, the RTO of the BIA is automatically updated. The RTO of the BIA is set as the lowest tolerable downtime from each impact category. For example, consider a BIA having four impact categories – Legal, Reputation, Workforce, and Regulatory. When you update the disruption duration value of the legal impact category, then the RTO value of the BIA is recalculated based on the lowest tolerable disruption duration from each impact category. The Recovery Tier varies from organization to organization and is set based on the recalculated RTO value.

    |RTO value|Recovery Tier|
    |---------|-------------|
    |Immediate|Mission Critical|
    |1 Hour|Mission Critical|
    |4 Hours|Mission Critical|
    |8 Hours|Business Critical|
    |24 Hours|Business Critical|
    |72 Hours|Essential|
    |1 Week|Essential|
    |2 Weeks|Non-Essential|
    |1 Month|Non-Essential|


**Parent Topic:**[Structured workflows for BIAs](bia-tasks-performed-by-bia-owner.md)

