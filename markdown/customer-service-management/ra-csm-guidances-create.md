---
title: Create a guidance in Recommended Actions
description: Create a guidance that you can select when creating a recommendation in Recommended Actions.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Creating guidance and field recommendation in Recommended Actions, Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Create a guidance in Recommended Actions

Create a guidance that you can select when creating a recommendation in Recommended Actions.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, or admin

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Action Types** &gt; **Guidances**.

2.  Create a guidance.

    1.  Select **New** in the Guidances list.

    2.  In the **Name** field, enter a name for the guidance.

    3.  In the **Description** field, enter a brief description of the guidance.

    4.  Make the guidance available to multiple agents working on the case by selecting the **Action available to multiple users** check box.

        When this option isn’t selected, only one agent can work on any guidance. When the first agent works on the guidance and the state is in-progress, completed, or error, the other agents can't see this guidance.

    5.  Select **Allow users to re-run the guidance** to enable agents to go back to the previous node or edit the previous nodes in the runtime experience of a decision tree.

        This field is only displayed when the Guided Decisions Experience plugin \(sn\_ga\_exp\) is installed.

    6.  Select **Hide completed guidance** to hide the guidance recommended for a case resolution.

        In other words, the completed guidance in the View my response section of a Decision Tree is not displayed for the agent.

        **Note:** This field is visible only when the Guided Decision Experience plugin is installed. You may need to configure the form to add this field.

    7.  Select **Submit**.

3.  Open the guidance that you want to update.

4.  Create one or more inputs for the guidance.

    Inputs are the variables or information that the system needs to perform the guidance. You can use inputs in multiple places such as the guidance preview experience and the guidance actions.

    1.  In the Guidance Input tab, select **New**.

    2.  In the **Label** field, enter a name for the input.

    3.  In the **Type** field, select the field type of the input.

        Depending on the field type that you select, you might need to configure additional settings. For example, if you select Reference as the field type, you need to select a reference table.

    4.  If the guidance input requires an action by the agent, such as adding information to a field, select the **Is form field** check box.

    5.  Enter a **Default value**.

    6.  Select **Submit**.

5.  Create one or more outputs for the guidance.

    Outputs are the desired result of the guidance action. For example, if a guidance action creates a case task, the output of that action can return a reference to the case task that was created.

    1.  In the Guidance Output tab, select **New**.

    2.  In the **Label** field, enter a name for the output.

    3.  In the **Type** field, select the field type of the output.

        Depending on the field type that you select, you might need to configure additional settings. For example, if you select Reference as the field type, you need to select a reference table.

    4.  Enter a **Default value**.

    5.  Select **Submit**.

6.  Configure the detail experience for the guidance in the Detail Experience tab.

    The detail experience is a message that is displayed for guidances that opens in the contextual side panel or in a subtab.

    1.  In the **Title** field, add a title for the guidance in the detailed view.

    2.  In the **Guidance Message** field, provide a message for the detail view.

7.  Select **Submit**.


