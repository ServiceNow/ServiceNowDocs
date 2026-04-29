---
title: Assessment metrics
description: In the Assessments application, a metric is a trait or value used to evaluate assessable records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment metrics

In the Assessments application, a metric is a trait or value used to evaluate assessable records.

Depending on the metric method, a metric can be used as either of the following:

-   A question on assessment questionnaires, to obtain a subjective value such as how much people enjoy using each cell phone offered in the service catalog.
-   A script that queries the database, to obtain an objective value such as the number of incidents related to each cell phone.

Each metric is associated to one [metric category](../reference/r_CategoryMetrics.md) and can be used to evaluate assessable records for that category only. For example, the Support Rating category contains metrics that measure the quality of vendors' customer support services. One metric addresses the quality of product documentation. Others address the strength of the user community, self-service options, online training, and other support services. Each metric has a numeric weight value to indicate its importance relative to other metrics in the same category.

Assessment administrators can create and administer metrics and [metric templates](../reference/r_MetricTemplates.md), which define reusable sets of answer options for metrics used as assessment questions. If you decide to use metric templates, you may want to create them before you create metrics.

**Note:** Changes to assessment metrics and metric templates are reflected in assessment questionnaires and results, even if users have saved responses already. If possible, avoid changing the original meaning of a metric question, the data type, or any metric templates in use by existing assessments.

-   **[Create an assessment metric for a category](../task/t_CreateAMetric.md)**  
After you create a category, create metrics you can use to evaluate the assessable records for that category.

**Parent Topic:**[Assessment administrator tasks](c_AssessmentProcess.md)

**Related topics**  


[Update a metric minimum and maximum value to match a template](../task/t_UpdAMetrMinMaxValToMatchATmplate.md)

