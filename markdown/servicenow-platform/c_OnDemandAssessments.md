---
title: On-demand assessments
description: On-demand assessments can be generated for metric types with the Schedule type field set to On demand.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Assessment administrator tasks, Use, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# On-demand assessments

On-demand assessments can be generated for metric types with the Schedule type field set to On demand.

For the system to properly generate on-demand assessments, the metric type must be active and published. The metric type must also be associated to at least one metric category. That metric category must be associated to one or more of each of the following items:

-   Assessable record
-   Metric

By default, an assessment administrator can generate an on-demand assessment for one assessable record or [multiple assessable records](../task/t_GenOnDemandAssessMultAssessRec.md).

-   **[Generate an on-demand assessment](../task/t_OnDemandAssessment.md)**  
Use on-demand assessments to familiarize yourself with the basic assessment process and test your questionnaires using minimal configuration.
-   **[Generate an on-demand assessment for one assessable record](../task/t_GenOnDemandAssessOneAssessRec.md)**  
When you generate an on-demand assessment from the Assessable Record form, the resulting assessment contains questions from the categories associated to the assessable record.
-   **[Generate an on-demand assessment for multiple assessable records](../task/t_GenOnDemandAssessMultAssessRec.md)**  
When you generate an on-demand assessment from the Assessment Metric Type form, the resulting assessment contains questions from all categories associated to any assessable records for the metric type.
-   **[Generate an assessment with the on-demand API](../task/t_GenAssessmentOnDemandAPI.md)**  
The Assign Assessment buttons call an API to generate on-demand assessments.

**Parent Topic:**[Assessment administrator tasks](c_AssessmentProcess.md)

**Related topics**  


[Assessment generation](c_AssessmentGeneration.md)

[Scheduled assessments](c_ScheduledAssessments.md)

[Generate an on-demand assessment for multiple assessable records](../task/t_GenOnDemandAssessMultAssessRec.md)

[View an assessment instance](../task/t_ViewAnAssessmentInstance.md)

[Clean up assessment data](../task/t_CleanUpAssessmentData.md)

