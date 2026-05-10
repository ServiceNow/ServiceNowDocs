---
title: Configure a quiz
description: You can configure an entire quiz.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a quiz, Quiz designer, Using Quizzes, Quizzes, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a quiz

You can configure an entire quiz.

## Before you begin

Role required: assessment\_admin, survey\_creator, or admin

## About this task

The values you enter and select on this page are applied to the entire quiz.

## Procedure

1.  In the quiz designer, click **Configuration** and then fill in the fields as described in the table.

<table id="table_dwb_gwh_br"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Check box for enabling the distribution of this quiz to recipients.

</td></tr><tr><td>

Description

</td><td>

Description of this configuration or the quiz to which it is attached.

</td></tr><tr><td>

Introduction

</td><td>

Introductory content to display on quizzes. You can add a welcome message or background information about the quiz.

</td></tr><tr><td>

Owners

</td><td>

Owners of the quiz. You can add a user with the survey\_creator, survey\_admin, or assessment\_admin role.

</td></tr><tr><td>

Signature

</td><td>

\[Optional\] Acknowledgement by a quiz recipient of requirements, admonitions, or expectations related to a quiz.

</td></tr><tr><td>

Return URL

</td><td>

Destination address of a web page that is presented to users after they submit a completed quiz. When a return URL is configured, the **End note** content does not appear.

</td></tr><tr><td>

End note

</td><td>

Content that is displayed to recipients after they submit a completed quiz. You can add a thank you message, follow-up instructions, or other applicable information. End notes are not displayed if a **Return URL** is specified.

</td></tr><tr><td>

Duration

</td><td>

Amount of time that recipients are given to complete this quiz, starting from the time that the quiz is generated. The default duration is 14 days.

</td></tr><tr><td>

Manager

</td><td>

Assessment manager for this quiz. These users are only responsible for managing the quiz process and not the results. The system notifies the manager when submissions for this quiz are past due.

</td></tr><tr><td>

Notify manager if overdue

</td><td>

Check box for sending [email notifications](t_ChangeTheOrderOfAnAnswer.md) to a recipient's manager when that user fails to submit an assigned quiz before the due date.

</td></tr><tr><td class="sub-head" colspan="2">

Related Links

</td></tr><tr><td>

Show Benchmarks

</td><td>

Opens the Benchmarks Dashboard that provides visibility into your key performance indicators \(KPIs\) and trends.**Note:**

-   This related link is available only for survey\_admin, assessment\_admin and survey\_reader with bm\_viewer role.
-   You must opt in to Benchmarks to view the dashboard. See [Enable Benchmarks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/benchmarks/t_EnableBench.md)
-   This is applicable only for a published quiz.


</td></tr></tbody>
</table>
**Parent Topic:**[Create a quiz](t_CreateaQuiz.md)

