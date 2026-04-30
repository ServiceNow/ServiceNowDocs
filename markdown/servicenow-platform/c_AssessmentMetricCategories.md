---
title: Assessment metric categories
description: In the Assessments application, a metric category represents a theme for evaluating assessable records in a given metric type.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [View an assessment metric category, Assessment administrator tasks, Use, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment metric categories

In the Assessments application, a metric category represents a theme for evaluating assessable records in a given metric type.

Each category has a numeric weight value to indicate its importance relative to other categories. Within a category, records called metrics are the traits or values used to evaluate assessable records. For example, there are many categories within the **Vendor** metric type, including Support Rating, which contains metrics that measure the quality of vendors' customer support services. Assessable records must be associated to categories to be eligible for evaluation. Assessment administrators create categories and manage which assessable records each category is associated to.

## Weight categories and metrics

When you create a metric category or metric, you must specify a weight, a numeric value that indicates the importance of the category or metric relative to other categories and metrics.

The greater the weight value, the more important the item is. The system uses weight values in [assessment result](../reference/r_AssessmentResults.md) calculations. Consider these recommendations when choosing weight values.

-   Determine a weighting scale and use it consistently. In general, use a scale with a small numeric range. A standard 1-10 scale is usually appropriate, where 1 is least and 10 most important. Understand that increasing the maximum value of a weighting scale impacts all related result calculations.
-   Use the same weighting scale for metric categories and metrics. Though there is no limitation, consider using the same or very similar weighting scales for both categories and metrics to make it easier to remember which values to use. A scale of 1-10 is an effective and simple weighting system, but may not be suitable for all organizations.

**Note:** If you do not want to use weighting, set the same weight value for all categories and metrics. The default weight value is 10.

-   **[Create a category for assessable records](../task/t_CreateACategoryAR.md)**  
After you create a metric type and generate assessable records, create categories for the themes you are interested in using to evaluate the assessable records.
-   **[Assessable record associations](../reference/r_ManageAssessablRecordAssociation.md)**  
Only the assessable records associated to a category can be evaluated using metrics in that category. Manage which assessable records you evaluate for each category by creating and removing the associations.
-   **[Delete a category](../task/t_DeleteACategory.md)**  
When you delete a category, the system also deletes the associated category users and stakeholders.

**Parent Topic:**[View an assessment metric category](../task/t_CreateAnAssessmentCategory.md)

**Related topics**  


[Assessment metrics](c_AssessmentMetrics.md)

[Create an assessment metric for a category](../task/t_CreateAMetric.md)

[Create an assessment metric definition](../task/t_CreateAMetricDefinition.md)

[Metric templates](../reference/r_MetricTemplates.md)

[Update a metric minimum and maximum value to match a template](../task/t_UpdAMetrMinMaxValToMatchATmplate.md)

