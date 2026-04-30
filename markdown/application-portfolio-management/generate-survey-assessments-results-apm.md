---
title: Generate survey assessments and view the results within Enterprise Architecture
description: Within Enterprise Architecture you can assign an assessment questionnaire to a user who uses a business application and get the feedback about the application.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Create or edit an indicator to assess an application, Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Generate survey assessments and view the results within Enterprise Architecture

Within Enterprise Architecture you can assign an assessment questionnaire to a user who uses a business application and get the feedback about the application.

## Before you begin

**Important:**

Starting with the Xanadu release, the application indicators module is moved to the Enterprise Architecture Workspace. To learn more, see [Regenerate capability indicator scores on-demand in Enterprise Architecture Workspace](eaw-task/eaw-regenerate-capability-indicator-scores-in-eaw.md) and [Regenerate application indicator scores on-demand in Enterprise Architecture Workspace](eaw-task/eaw-regenerate-indicator-score.md).

To know more about indicators, see [Configure indicators](../concept/eaw-concept/eaw-configure-indicators.md).

Role required: sn\_apm.apm\_admin

## About this task

Enterprise Architecture integrates with Assessments and Surveys to evaluate business applications and business capabilities based on assessment metric types. Application indicators that are sourced from assessments can only be assessed using the assessment metric.

An **assessment metric** is a trait or value that is used to evaluate a business application. Related metrics are grouped under an **assessment metric category**, which can be used to evaluate business applications for that category only. Whereas a **metric type** can comprise many metric categories that define a set of criteria an organization uses to evaluate its business applications.

For example, an organization may employ assessment metric types such as customer satisfaction, business value, technical risk, and functional fit to evaluate its business applications. Further, the organization can assess a group of business applications based on one assessment metric category, such as CSAT category for customer satisfaction. Within this CSAT category, you can define an actual assessment metric such as a question in an assessment questionnaire, **How likely is it that you would recommend this application to others?**

Your business application is the assessable record and it’s linked to a metric type. Use the custom UI to set conditions based on the columns of the business application table that meet your criteria and filter the applications. Select either a user group or selective users as target assessors and send out the questionnaires for them to take the survey. View the assessments and their status in the **Assessment Instances**, and the results in the **Metric Category Results** tabs of the **Indicator** related lists.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **Application Indicators**.

2.  Select open an indicator whose data source is assessments.

3.  Select the **Generate Assessments** button.

4.  To filter the business applications that should be assessed, set your conditions in the **Field**, **Operator**, and **Value** fields of the condition builder in the Generate Assessment UI that opens up.

    ![UI to set filter conditions on applications and select users to send the assessment.](../image/APMAssessmentIntegration.png "Generate Assessment UI")

    Your filter criteria are applied on all records in the business application \[cmdb\_ci\_business\_app\] table and you can filter applications by any column of the table.

5.  To add a dependent condition, select **AND** or **OR** next to the condition.

6.  To add a top-level condition or multiple filter criteria, select the **New Criteria** button.

7.  To clear existing filter conditions and set a new condition, select the **Clear All** button.

8.  Select users in the **Select Target Assessors** region to send the assessment questions.

    You can either select a user group or move individual application users to the Assessors list.

9.  Select **Send Assessments**.

10. Select **OK** to confirm in the Send Assessment dialog box.

    The user can view and take the assigned assessments by navigating to **Self-Service** &gt; **My Assessments &amp; Surveys**.

    For more information, see [Take a survey](https://www.servicenow.com/docs/access?context=t_TakeASurvey&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    After the user submits the assessments, the **State** of the assessment instance in the **Assessments Instances** tab changes to **Complete**.

11. Select the **Assessments Instances** tab to view the instances of assessments that have been created, the total number of assessments that have been sent out to users who fit in the filter criteria, and the status of the assessment instances.

    Each occurrence of a questionnaire assigned to one user is an assessments instance.

    **Note:**

    The indicator score and the corresponding application score are calculated only when all the users in the assessment group have completed the assessment.

12. Select the **Metric Category Results** tab to view the weight, rating, and normalized value of each business application that was assessed by the user or the user group.

    For more information, see [View an assessment category result](https://www.servicenow.com/docs/access?context=t_ViewACategoryResult&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) to know how the assessment results are calculated.


**Parent Topic:**[Create or edit an indicator to assess an application](create-application-indicators.md)

