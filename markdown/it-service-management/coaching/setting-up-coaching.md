---
title: Setting up Coaching and surveys
description: To take full advantage of Coaching, configure the Coaching application and set up surveys.
locale: en-US
release: xanadu
product: Coaching
classification: coaching
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Coaching, IT Service Management]
---

# Setting up Coaching and surveys

To take full advantage of Coaching, configure the Coaching application and set up surveys.

## Setting up Coaching

Configure Coaching to start assessing and coaching trainees.

1.  Set up Coaching [roles](../reference/coaching-roles.md) and groups to identify Coaching users, coaches, and admins.
2.  Define an assessment trigger on the Coaching Opportunity form.
3.  Identify training content that is provided as part of a training or virtual coaching.
4.  Configure virtual coaches to add to a coaching opportunity.
5.  Set up surveys to provide feedback on the coaching experience so you can make improvements.

## Setting up surveys

You can obtain feedback for both the coach and the trainee by creating surveys that are accessed from a Coaching Assessment form that has been resolved or closed.

-   Survey taken by trainee to provide feedback on the coach
-   Survey taken by coach to provide feedback on the trainee

Access the [Survey designer](https://www.servicenow.com/docs/access?context=c_SurveyDesigner&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for Coaching by navigating to **Survey** &gt; **Survey Designer**.

Access the Coaching [Survey definitions](https://www.servicenow.com/docs/access?context=c_SurveyDefinitions&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) by navigating to **Coaching** &gt; **Coaching Surveys**.

## Coaching Properties

<table id="table_u2w_jh5_fnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_coaching.kb\_article\_duration

</td><td>

Number of days to read the knowledge article. The admin \(sn\_wfo.admin\) sets the number of days for the trainee to complete reading the article. The number of days is converted to the due date for the trainee to complete the training. It is calculated from the current date taking the trainee's time zone into consideration.-   **Type:**Integer
-   **Default value:**5

</td></tr><tr><td>

sn\_coaching.exclude\_weekends\_on\_training\_due\_date

</td><td>

Excludes weekends when the due date is set for trainees to complete training.-   **Type:**true \| false
-   **Default value:**true

</td></tr></tbody>
</table>-   **[Define trigger conditions for a coaching opportunity](../task/create-coaching-opportunity.md)**  
Use the Coaching Opportunity form to define a critical moment in a process on which a user can be coached. A coaching opportunity consists of the relationship between a process that can be improved, and coaches and trainees.
-   **[Identify and add course items for a virtual coach](../task/identify-learning-content.md)**  
Define filters and add course items for automated virtual coaching. When a coaching assessment is triggered, the course items are automatically attached to the assessment.
-   **[Create a survey and associate with a Coaching opportunity](../task/create-survey-coaching-opportunity.md)**  
Create a survey for coaches or trainees to assess the training quality. Add a question bank to the survey. Associate the survey with a coaching opportunity to provide feedback when the coach completes the coaching assessment.

**Parent Topic:**[Coaching](coaching-landing.md)

