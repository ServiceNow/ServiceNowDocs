---
title: Configure the Propose Solution UI action and declarative action
description: Add generative AI-specific functionality to the Case form by configuring the Propose Solution UI action and declarative action that are included with the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# Configure the Propose Solution UI action and declarative action

Add generative AI-specific functionality to the Case form by configuring the Propose Solution UI action and declarative action that are included with the Now Assist for Customer Service Management \(CSM\) application.

## Before you begin

Role required: admin

## About this task

The Customer Service Management application includes a Propose Solution UI action that agents can use to propose a solution for a customer service case.

The Now Assist for Customer Service Management \(CSM\) application includes the following actions that provide generative AI-specific functionality. Agents can use these actions to propose solutions that include AI-generated resolution notes:

-   Propose Solution declarative action: Generates resolution notes in CSM Configurable Workspace.
-   Propose Solution UI action: Generates resolution notes in Core UI.

**Note:** These actions are inactive by default.

To use the generative AI functionality, you must deactivate the Propose Solution UI action for Customer Service Management and then activate the Propose Solution UI action and declarative action for Now Assist for CSM. After being activated, these actions are available to customer service agents for assigned cases that are in the Open state.

## Procedure

1.  Deactivate the Propose Solution UI action for the Customer Service Management application.

    1.  Navigate to **All** &gt; **System Definition** &gt; **UI Actions** to display the UI Actions list.

    2.  Configure the list to show the Application column.

        For more information on how to configure a list, see [Configure the list layout](https://www.servicenow.com/docs/access?context=t_ConfigureTheListLayout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

    3.  Filter the list to display **Propose Solution** in the **Name** field.

    4.  Select the Propose Solution UI action for the Customer Service application.

    5.  Clear the **Active** check box.

    6.  Select **Save**.

        The system returns you to the UI Actions list.

2.  Activate the Propose Solution UI action for the Now Assist for CSM application to use this functionality in Core UI.

    1.  From the UI Actions list, select the Propose Solution UI action for the Now Assist for CSM application.

    2.  Select the **Active** check box.

    3.  Select **Save**.

        The system returns you to the UI Actions list.

3.  Enable the Propose Solution declarative action for the Now Assist for CSM application to use this functionality in CSM Configurable Workspace.

    1.  Navigate to the **sys\_declarative\_action\_assignment.list** to display the Action Assignments list.

    2.  In the Action label column, select **Propose Solution**.

    3.  Enable the **Active** check box.

    4.  Select **Save**.

        The system returns you to the Action Assignments list.


