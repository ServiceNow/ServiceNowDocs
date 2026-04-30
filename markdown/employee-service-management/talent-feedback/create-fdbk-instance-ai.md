---
title: View survey instance
description: A survey instance represents one questionnaire assigned to one user. You view an instance to verify that survey instances were created, to check the state of a survey instance, or to reassign a survey instance.
locale: en-US
release: zurich
product: Talent Feedback
classification: talent-feedback
topic_type: task
last_updated: "2026-03-01"
reading_time_minutes: 1
breadcrumb: [Using Employee feedback collection AI agent, Use, Talent Feedback, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# View survey instance

A survey instance represents one questionnaire assigned to one user. You view an instance to verify that survey instances were created, to check the state of a survey instance, or to reassign a survey instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **Survey Instances**.

    The following sub-modules are available based on the state of the instances:

    -   **Ready to take**: Displays survey instances that are ready to be taken by the user. By default, these instances are sorted in ascending order by the **Number** field.
    -   **In progress**: Displays survey instances that are in progress. By default, these instances are sorted in ascending order by the **Number** field.
    -   **Completed**: Displays survey instances that are complete. By default, these instances are sorted in descending order by the **Taken on** field.
    -   **Cancelled**: Displays survey instances that are cancelled. By default, these instances are sorted in ascending order by the **Number** field.
    -   **All**: Displays survey instances in all states. By default, these instances are sorted in ascending order by the **Number** field.
2.  Open a survey instance from the required sub-module.

    By default, you can view the following fields in the [Survey Instance form](https://www.servicenow.com/docs/access?context=survey-instance-form&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for all sub-modules other than **Completed**.

    -   **Number**
    -   **Metric type**
    -   **Due date**
    -   **Taken on**
    -   **Assigned to**
    **Note:**

    -   When you open an instance in the **Completed** sub-module, you are redirected to the User's Response page.
    -   Each survey instance is stored as a record on the Assessment Instance \[asmt\_assessment\_instance\] table with a modified view for survey use.

