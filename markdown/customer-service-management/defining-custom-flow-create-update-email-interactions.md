---
title: Define a custom flow to create or update email interactions
description: Define email-related business processes using Workflow Studio. This tool enables you to manage emails along with your customer service processes through a visual interface without having to design or request complex scripts.Create an interaction record to capture customer details.Modify existing interaction records, verifying that all email communication details are updated.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Email Interaction for CSM, Email Interaction for CSM, Email Interaction for CSM]
breadcrumb: [Configure flows for incoming emails, Email Interaction, Email channel, Configure, Enable communication channels, Configure, Customer Service Management]
---

# Define a custom flow to create or update email interactions

Define email-related business processes using Workflow Studio. This tool enables you to manage emails along with your customer service processes through a visual interface without having to design or request complex scripts.

## Create an interaction

Create an interaction record to capture customer details.

### Before you begin

Role required: workspace\_admin, awa\_agent, sn\_customerservice\_consumer\_agent, or sn\_customerservice\_agent

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Create a flow.

    1.  Select **Flows**.

    2.  Select **New**.

    3.  Select **Flow**.

    4.  In the **Flow name** field, enter the flow name.

    5.  Select the application scope from the Application list.

    6.  In the **Description** field, enter the description.

    7.  Select **Show additional properties**.

        To know more about additional properties, see [Create a flow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

    8.  Select **Build flow**.

3.  Create a trigger.

    1.  Select **Add a Trigger**.

    2.  Search and select **Application**.

    3.  Select **Inbound Email**.

    4.  Select Email conditions with **AND** operator.

        -   Select **Type** is **received**.
        -   Select **Receive type** is **New**.
        -   Select **To** contains **customerservice@example.com**.
        **Note:** **customerservice@example.com** is a sample email address. Specify the actual email address that should be configured as the default for creating email interactions.

    5.  Leave the Reply Record Type as empty.

    6.  Select **Done**.

4.  Select **Add an Action, Flow Logic, or Subflow** and select any of the following.

    -   Action
    -   Flow Logic
    -   Subflow
    **Note:** After you have created action entries, you can select multiple actions using **Select multiple**.

5.  Add error handler.

    1.  To enable the error handling, slide the **ERROR HANDLER** toggle switch.

    2.  Select **Add an Action, Flow Logic, or Subflow** and select any of the following.

    -   Action
    -   Flow Logic
    -   Subflow
6.  Verify the email flow and modify it if necessary.

7.  Select **Save**.

8.  Select **Activate**.

9.  From the confirmation dialog box, select **Activate**.


**Related topics**  


[Create a flow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

## Update an interaction

Modify existing interaction records, verifying that all email communication details are updated.

### Before you begin

Role required: admin, workspace\_admin, awa\_agent, sn\_customerservice\_consumer\_agent, or sn\_customerservice\_agent

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Create a flow.

    1.  Select **Flows**.

    2.  Select **New**.

    3.  Select **Flow**.

    4.  In the **Flow name** field, enter the flow name.

    5.  Select the application scope from the Application list.

    6.  In the **Description** field, enter the description.

    7.  Select **Show additional properties**.

        To know more about additional properties, see [Create a flow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

    8.  Select **Build flow**.

3.  Create a trigger.

    1.  Select **Add a Trigger**.

    2.  Search and select **Application**.

    3.  Select **Inbound Email**.

    4.  Select Email conditions with **AND** operator.

        -   Select **Type** is **received**.
        -   Select **Receive type** is **Reply**.
    5.  Leave the Reply Record Type as empty.

    6.  Select **Done**.

4.  Select **Add an Action, Flow Logic, or Subflow** and select any of the following.

    -   Action
    -   Flow Logic
    -   Subflow
    **Note:** After you have created action entries, you can select multiple actions using **Select multiple**.

5.  Add error handler.

    1.  To enable the error handling, slide the **ERROR HANDLER** toggle switch.

    2.  Select **Add an Action, Flow Logic, or Subflow** and select any of the following.

    -   Action
    -   Flow Logic
    -   Subflow
6.  Verify the email flow and modify it if necessary.

7.  Select **Save**.

8.  Select **Activate**.

9.  From the confirmation dialog box, select **Activate**.


**Related topics**  


[Create a flow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

