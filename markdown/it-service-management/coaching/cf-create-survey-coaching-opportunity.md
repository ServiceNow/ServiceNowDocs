---
title: Create a survey and associate with a Coaching opportunity
description: Create a survey for coaches or trainees to assess the training quality. Add a question bank to the survey. Associate the survey with a coaching opportunity to provide feedback when the coach completes the coaching assessment.
locale: en-US
release: australia
product: Coaching
classification: coaching
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up, Configure, Coaching, IT Service Management]
---

# Create a survey and associate with a Coaching opportunity

Create a survey for coaches or trainees to assess the training quality. Add a question bank to the survey. Associate the survey with a coaching opportunity to provide feedback when the coach completes the coaching assessment.

## Before you begin

Role required: sn\_coaching.admin

## Procedure

1.  Create a survey to associate with a coaching opportunity.

    **Note:** If you already have a survey that you want to associate with a coaching opportunity, go to the Associate a survey with a coaching opportunity step.

    1.  Navigate to **All** &gt; **Coaching** &gt; **Administration** &gt; **Survey Designer**.

    2.  In the **Name** field, enter the name for the coaching survey.

    3.  Select the **Configuration** tab.

    4.  In the **Survey Owners** field, select **Coaching Admin**.

    5.  In the **Description** field, enter a description for the survey.

    6.  In the **Source table** field, select Coaching Assessment \[sn\_coaching\_assessment\].

    7.  In the **Duration** field, enter the length of time recipients are given to complete the survey.

    8.  Select **Save**.

    For more information on configuring a survey, see [Survey Designer Configuration form](https://www.servicenow.com/docs/access?context=survey-design-config-form&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

2.  Create a question bank for the survey.

    1.  Navigate to **All** &gt; **Surveys** &gt; **Question Bank**.

    2.  In the **Assessment Metric Categories** list, select **New.**

    3.  In the **Name** field, enter a name for the question bank and then select and hold \(or right-click\) the form header and select **Save**.

    4.  In the Assessment Metrics related list, select **New**.

    5.  In the Survey Question form, enter the name, question, and data type, and select **Submit**.

    For more information on creating or updating a question bank, see [Survey questions](https://www.servicenow.com/docs/access?context=c_SurveyQuestion&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

3.  Associate the question bank with the survey.

    1.  Navigate to **All** &gt; **Coaching** &gt; **Administration** &gt; **Coaching Surveys**.

    2.  In the Assessment Metric Types list, select the survey you have created.

    3.  In the Metric Categories related list, select **New Category from Bank**.

    4.  Select the question bank you have created and select **Add selected**.

    5.  Select **Update**.

4.  Associate a survey with a coaching opportunity.

    1.  Navigate to **All** &gt; **Coaching** &gt; **Coaching Opportunities**.

    2.  Select the Surveys related list.

    3.  Do any of the following:

        -   To add a survey to be taken by the coach, in the **Survey taken by Coach** field, using the search icon select the survey.
        -   To add a survey to be taken by the trainee, in the **Survey taken by Trainee** field, using the search icon select the survey.
        For more information on the coaching opportunities, see [Define trigger conditions for a coaching opportunity](cf-create-coaching-opportunity.md).


**Parent Topic:**[Setting up Coaching and surveys](../concept/cf-setting-up-coaching.md)

