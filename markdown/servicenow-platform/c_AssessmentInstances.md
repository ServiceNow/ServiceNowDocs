---
title: Assessment instances
description: An assessment instance represents one occurrence of a questionnaire assigned to one user.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scheduled assessments, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment instances

An assessment instance represents one occurrence of a questionnaire assigned to one user.

The system generates assessment instances only when the required conditions are met, as described in [Scheduled assessments](c_ScheduledAssessments.md) and [On-demand assessments](c_OnDemandAssessments.md), and there are non-scripted metrics in at least one category.

When the system generates scheduled assessments for a metric type, each assessment instance contains questions about assessable records and categories related to the stakeholder to which it is assigned.

Example:

Recall that there can be multiple stakeholder records associated with one user record. Minh Leclare is a stakeholder for these items related to the **Vendor** metric type:

|Assessable record|Category|
|-----------------|--------|
|Amazon|User Satisfaction|
|Acme|User Satisfaction|
|Acme|Reliability|
|Cisco|Reliability|

When the system generates a scheduled assessment, Minh is assigned one assessment instance to evaluate Amazon, Acme, and Cisco by answering questions from the categories as a stakeholder. Assuming that there are three questions in the User Satisfaction category and six questions in Reliability, Minh's questionnaire contains three questions about Amazon, nine questions about Acme, and six questions about Cisco.

When the system generates an on-demand assessment [for a specific assessable record](../task/t_GenOnDemandAssessOneAssessRec.md), the assessment instance contains questions about that assessable record and all its associated categories. When the system generates an on-demand assessment [for a metric type](../task/t_GenOnDemandAssessMultAssessRec.md), the assessment instance contains questions about all that metric type's assessable records and their associated categories.

**Parent Topic:**[Scheduled assessments](c_ScheduledAssessments.md)

