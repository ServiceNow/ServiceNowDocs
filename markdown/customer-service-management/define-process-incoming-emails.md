---
title: Define rules to process incoming emails
description: Define your email-related business processes using inbound email flows. This enables you to manage emails along with your customer service processes through a visual Flow Designer interface without having to design or request complex scripts.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-09-19"
reading_time_minutes: 1
breadcrumb: [Creating rules for incoming emails that create and assign cases, Configuring the email channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Define rules to process incoming emails

Define your email-related business processes using inbound email flows. This enables you to manage emails along with your customer service processes through a visual **Flow Designer** interface without having to design or request complex scripts.

## Before you begin

Role required: admin, sn\_customerservice\_manager

## About this task

Email flows use conditional logic to incorporate multiple business processes in one flow. When designing inbound email flows, note the following:

-   The execution order of the inbound email flows take a higher precedence than inbound actions \(that is if an email flow executes, it prevents execution of inbound actions\).
-   The user who sends an email should have the necessary roles to perform operations specified in the flow or the operation will stop.

## Procedure

1.  Create an inbound email flow.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    2.  Select one of the following flows.

        -   **Create Case from Email**: Creates a case when a user sends a new email.
        -   **Update Case via Reply**: Updates a case when you use the reply option.
    3.  Select **Edit Flow**.

    4.  Select the **Inbound Email** trigger.

    5.  Modify the default email filter conditions or select **New Criteria** to add conditions.

    6.  Select a Reply Record Type table.

    7.  Select **Done**.

2.  Edit the flow.

    1.  Select an existing action and expand it.

    2.  Provide information for the action or select the add icon \(+\) to add a new action, flow logic, or subflow.

    3.  Select **Done**.

3.  Finalize the rule.

    1.  Verify the email flow and modify it if necessary.

    2.  Select **Save**.

    3.  Select **Activate**.

4.  Select **Activate**.

    The defined inbound email flow is activated.


**Related topics**  


[Building flows](https://www.servicenow.com/docs/access?context=flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

[Building custom actions](https://www.servicenow.com/docs/access?context=actions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

