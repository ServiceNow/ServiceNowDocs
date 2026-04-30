---
title: Configure task count for your next tasks widget
description: You can configure how many tasks you want to see in your next tasks widget.
locale: en-US
release: yokohama
product: Journey Designer
classification: journey-designer
topic_type: task
last_updated: "2025-04-18"
reading_time_minutes: 1
breadcrumb: [Employees view and complete journeys, Journey view for an employee, Managers, mentors, and employees work with journeys in the Employee Center, Using Journey designer, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure task count for your next tasks widget

You can configure how many tasks you want to see in your next tasks widget.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System definition** &gt; **Script includes**.

2.  Search for the `jnySNC` script include entry in the name field and select it.

3.  Edit the following script to change the number of tasks you want shown on your next tasks widget.

    ```
    //tasks limit
    jnySNC.MY_JOURNEY_NEXT_TASKS_LIMIT = 10;
    ```

    **Note:** Here the number of tasks limit is set to 10, you can update it to any number you'd like.


**Parent Topic:**[Employees view and complete journeys](jny-dsgnr-employee-journey-tasks.md)

