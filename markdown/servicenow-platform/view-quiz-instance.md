---
title: View a quiz instance
description: View an instance to verify that quiz instances were created, to check the state of a quiz instance, or to reassign a quiz instance. A quiz instance represents one questionnaire assigned to one user.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Quizzes, Quizzes, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View a quiz instance

View an instance to verify that quiz instances were created, to check the state of a quiz instance, or to reassign a quiz instance. A quiz instance represents one questionnaire assigned to one user.

## Before you begin

Role required: admin or assessment\_admin

## Procedure

1.  Navigate to **All** &gt; **Quizzes** &gt; **Quiz Instances**.

    The following submodules are available based on the state of the instances:

    -   **Ready to take**: Displays quiz instances that the user can take. By default, these instances are sorted in ascending order by the **Number** field.
    -   **In progress**: Displays quiz instances that are in progress. By default, these instances are sorted in ascending order by the **Number** field.
    -   **Completed**: Displays quiz instances that are complete. By default, these instances are sorted in descending order by the **Taken on** field.
    -   **Cancelled**: Displays quiz instances that are canceled. By default, these instances are sorted in ascending order by the **Number** field.
    -   **All**: Displays quiz instances in all states. By default, these instances are sorted in ascending order by the **Number** field.
2.  From the required submodule, click a quiz instance.

    By default, the fields listed in the following table are displayed for all submodules other than the **Completed** submodule.

    **Note:** When you select an instance in the **Completed** submodule, you are redirected to the User's Response page.

3.  In the form, fill the fields.

<table id="table_qcz_2vg_mbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically generated record number.

</td></tr><tr><td>

Metric type

</td><td>

Metric type of this quiz.

</td></tr><tr><td>

Due Date

</td><td>

Date by which the quiz instance should be completed. The system populates the due date based on the **Assessment duration** of the associated quiz definition, which is set to 14 days by default.The quiz due date is not enforced in the base system. If you want to enforce the due date, consider using a workflow or other mechanism to send survey recipients reminders when a survey is overdue.

</td></tr><tr><td>

State

</td><td>

State of the quiz.

</td></tr><tr><td>

Assigned to

</td><td>

User that the quiz instance is assigned to. This field becomes read-only when the state is **In progress**, **Complete**, or **Canceled**.

</td></tr><tr><td>

Domain

</td><td>

Domain associated with the instance.

</td></tr><tr><td class="sub-head" colspan="2">

Related Link

</td></tr><tr><td>

View User's Response

</td><td>

Shows a read-only version of the survey responses completed by the user.

</td></tr><tr><td class="sub-head" colspan="2">

Related List

</td></tr><tr><td>

Assessment Instance Questions

</td><td>

All instance question records that store user response values for each question on the quiz questionnaire. The following columns are relevant to quiz:-   **Category**: Displays the quiz categories the questions belong to.
-   **Metric**: Displays the quiz questions.


</td></tr></tbody>
</table>
**Parent Topic:**[Using Quizzes](../concept/using-quizzes.md)

**Related topics**  


[bundle-platadm.c_ScheduleEvents]

