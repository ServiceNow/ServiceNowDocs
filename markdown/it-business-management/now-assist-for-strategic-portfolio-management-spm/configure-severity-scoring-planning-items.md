---
title: Update severity scoring configuration for portfolio insights
description: Configure the severity thresholds and scoring factors that determine how planning items are classified as critical, medium, or low risk, so that Portfolio insights generates recommendations based on your organization's risk criteria.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 4
breadcrumb: [Configure, Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Update severity scoring configuration for portfolio insights

Configure the severity thresholds and scoring factors that determine how planning items are classified as critical, medium, or low risk, so that Portfolio insights generates recommendations based on your organization's risk criteria.

## Before you begin

Role required: sn\_align\_core.apw\_admin

**Note:** Default severity thresholds and scoring factors are preconfigured for portfolio insights. Update these settings only if your organization's risk criteria differ from the defaults.

For example, the following default values apply to the Delayed planning items category:

-   Default `severityThresholds` configuration: `{ "severityThresholds": { "critical": { "minScore": 10 }, "medium": { "minScore": 5 }, "low": { "minScore": 1 } }`

-   Default `scoringFactors` configuration: `"scoringFactors": { "scheduleDelay": { "enabled": true, "pointsPerDay": 0.5, "maxPoints": 10 }, "priority": { "enabled": true, "weights": { "High": 3, "Medium": 1, "Low": 0 } }, "dependencyImpact": { "enabled": true, "pointsPerDownstreamDependency": 1, "maxPoints": 6 }, "financialRisk": { "enabled": true, "benefitThreshold": 100000, "pointsIfAboveThreshold": 3, "maxPoints": 3 } } }`


## About this task

Severity scoring determines how the Portfolio insights skill classifies planning items and surfaces root causes and recommended actions. Each planning item receives an overall risk score based on weighted scoring factors — scheduled delay, priority, dependency impacts, and financial risk. The score is then evaluated against configurable thresholds to assign a severity level.

Severity levels are color-coded for quick identification: red for critical, yellow for medium, and green for low. The color assignments are fixed and cannot be changed.

Configuration is managed in the Insight topic configuration table using records with type set to **Portfolio**.

The insights are generated for the following categories for a portfolio plan:

-   Delayed planning items - Planning items delayed beyond planned end date
-   Date misalignment - Planned vs Approved date misalignment
-   Delayed start - Planning items with delayed starts

**Note:**

-   For Delayed planning items insights, root causes and recommendations are generated from the top 15 delayed planning items, ranked by severity score.
-   For Delayed start insights, only planning items whose planned start date falls within the last 30 days are included.

**Important:** This topic covers severity scoring configuration for the Delayed planning items category. The same steps apply to the Delayed start and Date misalignment categories.

## Procedure

1.  Navigate to **All** &gt; **sn\_spm\_gen\_ai\_insight\_topic.list**.

    A list of Insight topic table records appear.

2.  In the **Type** column, right-click **Portfolio** and select **Show Matching** to show only records with the type set to **Portfolio**.

    ![Show the Portfolio Insight topic table records.](../images/update-severity-scoring-for-planning-items.png)

    After applying the filter, the following three insight topic table records appear.

    ![Insight topic table records portfolio insights](../images/insight-topic-table-portfolio-insights.png)

3.  Next to an Insight topic record, select preview icon to open the record.

    For example, select Preview Delayed Planning Item record icon to view the Delayed Planning Items record.

4.  In the `severityThresholds` section of the **Default topic config** field, set the score range for each severity level according to your organization's risk criteria.

    ![Default delayed planning items record.](../images/default-delayed-planning-items-record.png)

    |Severity level|Description|
    |--------------|-----------|
    |Critical|Planning items whose risk score meets or exceeds the critical threshold. Displayed in red.|
    |Medium|Planning items whose risk score falls between the critical and low thresholds. Displayed in yellow.|
    |Low|Planning items whose risk score falls below the medium threshold. Displayed in green.|

    Default `severityThresholds` configuration: `{ "severityThresholds": { "critical": { "minScore": 10 }, "medium": { "minScore": 5 }, "low": { "minScore": 1 } }`

5.  In the `scoringFactors` section of the **Default topic config** field, set the weight for each factor that contributes to the overall risk score according to your organization's risk criteria.

    |Scoring factor|Description|
    |--------------|-----------|
    |Scheduled delay|Contributes to the risk score based on the number of days a planning item is delayed beyond its planned end date. The score is calculated as 0.5 points per day delayed, up to a maximum of 10 points.|
    |Priority|Contributes to the risk score based on the priority assigned to the planning item: High \(3 points\), Medium \(1 point\), or Low \(0 points\).|
    |Dependency impacts|Contributes to the risk score based on the number of downstream dependent planning items affected by the delay, up to a maximum of 6 points.|
    |Financial risk|Contributes to the risk score based on the financial exposure associated with the planning item. Planning items with a benefit above the threshold receive additional points, up to a maximum of 3 points.|

    Default `scoringFactors` configuration: `"scoringFactors": { "scheduleDelay": { "enabled": true, "pointsPerDay": 0.5, "maxPoints": 10 }, "priority": { "enabled": true, "weights": { "High": 3, "Medium": 1, "Low": 0 } }, "dependencyImpact": { "enabled": true, "pointsPerDownstreamDependency": 1, "maxPoints": 6 }, "financialRisk": { "enabled": true, "benefitThreshold": 100000, "pointsIfAboveThreshold": 3, "maxPoints": 3 } } }`

6.  Save the configuration record.

    The updated severity thresholds and scoring factor weights are applied when Portfolio insights next generates insights for planning items in the portfolio plan.


## What to do next

To verify that the configuration is working as expected, open a portfolio plan that contains planning items with known delays and confirm that the severity classifications reflect the thresholds you set. For details, see [View portfolio insights for a portfolio plan in Strategic Planning Workspace or Portfolio Planning Workspace using Now Assist for SPM](view-portfolio-insights.md).

