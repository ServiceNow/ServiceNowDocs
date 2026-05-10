---
title: Define rules to process incoming emails
description: Define your email-related business processes using Inbound Email Flows. Manage emails along with your customer service processes through a visual Flow Designer interface without having to design or request complex scripts.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure process rules for incoming emails, Email to case, Email channel, Enable communication channels, Configure, Customer Service Management]
---

# Define rules to process incoming emails

Define your email-related business processes using Inbound Email Flows. Manage emails along with your customer service processes through a visual **Flow Designer** interface without having to design or request complex scripts.

## Before you begin

Role required: admin, sn\_customerservice\_manager

## About this task

Email flows use conditional logic to incorporate multiple business processes into one flow. When designing inbound email flows, note the following:

-   The execution order of the inbound email flows takes a higher precedence than inbound actions. For example, if an email flow executes, it prevents the execution of inbound actions.
-   The user who sends an email should have the necessary roles to perform the operations specified in the flow. Otherwise the system stops the operation.

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


[Building flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flows.md)

[Building custom actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/actions.md)

