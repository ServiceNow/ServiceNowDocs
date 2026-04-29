---
title: Structured workflows for Business Impact Analysis
description: Business impact analysis helps you to predict the consequences of a disruption on a business process or business function.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Structured workflows for Business Impact Analysis

Business impact analysis helps you to predict the consequences of a disruption on a business process or business function.

A business process is a set of tasks done by a business organization to deliver a business service or product to customers. When a business process in disrupted, the impact to the organization can be huge in terms of revenue and reputation. Business impact analysis \(BIA\) is performed to identify and prioritize critical processes, quantify or qualify the impacts, and identify recovery dependencies. Ideally, business impact analysis on critical processes must be performed annually.

The assessment of a business critical process disruption helps you to estimate the consequential impact on your business revenue, legal issues, workforce disruption, or business reputation. It also enables you to identify the dependencies of your business process on business applications, technology, or vendors that might be affected. This analysis gathers the information needed to develop recovery strategies.

![Business impact analysis overview](../image/BIAImpactAssessmentView.png "Business impact analysis overview")

## Impact ratings for your business impact analysis

The Business Continuity Management \(BCM\) administrator of your organization defines the impact ratings for your business impact analysis \(BIA\) and decides if the impact is tolerable for your business process. For more information on the impact ratings, see [Configure an impact rating to assess an impact category](../task/configure-impact-rating-bcp.md). According to the configuration set up by BCM administrator, the questions are displayed in the **RTO Impact Assessment** tab.

Consider the example where BCM administrator has configured an intolerable impact rating for the Revenue impact category. BCM administrator has defined what qualifies to be an intolerable impact. As a BIA owner, you must identify the timeline at which the revenue impact may go beyond $1M.![BIA impact rating.](../image/BIA-intolerable-impact.png)

## Multiple impact ratings for an impact category

If your BCM administrator has configured the assessment questionnaire to include multiple impact ratings for an impact category, the impact category ratings are displayed in the Impact Category view as shown in the example.![Administrator view for the impact category.](../image/impact-category-admin-view.png)

BCM administrators specify a threshold of non-tolerance for the impact ratings, per impact category. The disruption duration for the first non-tolerable impact category is selected for the recovery time objective \(RTO\). The impact ratings have the specified values:

-   Low = 1
-   Moderate = 2
-   High = 3

See the example for the sample RTO calculation.

![An example to show the calculation of impact category results.](../image/BIAImpactCategoryResults.png "Example to show the calculation of impact category")

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

 Even if the moderate impact disruption duration is shorter, the calculation will select the value from the first alphanumerically sorted impact rating that has the **Tolerable** field set to **false**.

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

 In the example, the administrator has set all the impact ratings as tolerable. Therefore, the recovery time objective \(RTO\) is one month as per the value specified in the **Maximum RTO value** field.![Maximum RTO value.](../image/maximum-rto-value.png)

</td></tr></tbody>
</table>-   **Calculation of category score from impact analysis questions for an impact category that contributes to Recovery Point Objective \(RPO\)**

    If the impact category contributes to **RPO**, then evaluate each impact analysis question in that RPO category based on the value of your data like business critical, operation critical, business essential, or operation essential. The maximum value among all the questions of that RPO is considered as the Category Score of that Impact Category and stored in the Impact Category Results table \[sn\_bia\_category\_result\].

-   **Calculation of overall impact assessment result for a BIA**

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


