---
title: Create rules and actions for Proactive Triggers
description: Create rules and related actions for Proactive Triggers. These rules and their related actions determine the messages that end users see on the ServiceNow portal.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Proactive Triggers, Proactive Triggers, Manage people and work, Conversational Interfaces]
---

# Create rules and actions for Proactive Triggers

Create rules and related actions for Proactive Triggers. These rules and their related actions determine the messages that end users see on the ServiceNow portal.

## Before you begin

[Enable the Proactive Triggers feature](enable-proactive-triggers.md), and review the list of default rules included with Proactive Triggers.

Role required: sn\_pt.proactive\_admin or admin

## About this task

Select a default rule in the Proactive Triggers rules list to see how the default rule is defined. Admins or proactive admins can use these rules, change them, or create rules. After a rule is created, the admin creates one or more actions that are triggered by the rule. Actions define the messages that end users see based on the rule and the next steps available for the end users to take. For examples of default rules and action types, see [Exploring Proactive Triggers](../concept/proactive-triggers.md).

## Procedure

1.  Navigate to **Conversational Interfaces** &gt; **Settings** &gt; **General**, and then select **View All** next to Proactive Triggers **Rules**.

    The list of default rules included with Proactive Triggers is displayed.

2.  Select **New** to display the Proactive Rule form.

3.  On the Proactive Rule form, fill in the fields.

    For a description of the field values, see [Proactive Rule form](../reference/proactive-rule-new-record-form.md).

4.  Select **Submit**.

    The rule is created and is displayed in the list of available rules.

5.  Select the newly created rule, and then go to the Proactive Actions related list.

6.  Select **New** and, when prompted, choose the action type for the rule.

    |Action type|Description|
    |-----------|-----------|
    |Message only|End users see an HTML pop-up message.|
    |Message that launches a virtual agent topic|End users see an HTML pop-up message that directs them to an available Virtual Agent topic.|
    |Message that launches a selection of virtual agent topics|End users see an HTML pop-up message with up to three suggested action buttons that direct them to a relevant Virtual Agent topic.|

    **Note:** If you've created [Live Agent rules](create-rule-actions.md#), you can only select Message action types for those rules.

7.  On the Proactive Action form, fill in the fields.

    For a description of the field values, see [Proactive Action form](../reference/proactive-action-new-record-form.md).

8.  If you select the **Message that launches a selection of virtual agent topics** action type, work with the following default list columns on the Proactive Action Virtual Agent Topic Controls related list to determine the button display order:

    |Column|Description|
    |------|-----------|
    |Label|The button label that appears to end users. Double-click \(or use the keyboard shortcut\) the value to enter a button label up to a maximum of 40 characters. Leave this value empty if you want to have the label auto-populate with the topic title.|
    |Topic|The Virtual Agent topic that end users interact with after they’ve selected the button. Double-click \(or use the keyboard shortcut\) the value to enter or search for a Virtual Agent topic.|
    |Active|The active status of the rule action. A rule needs at least one active action for the rule to be triggered. Double-click \(or use the keyboard shortcut\) to select either **true** or **false**. Leave this value empty to auto-populate this value to **true**.|
    |Order|The button order that is displayed on end users’ screens. Double-click \(or use the keyboard shortcut\) to enter the button preference order. Leave this value empty if you want to auto-populate with the next available order number that increments by one.|

    **Note:** Up to three buttons can appear in the proactive message.

9.  Select **Submit**.

    The Proactive action is created.

    You can create additional rules and actions as needed. For information about using multiple rules and actions, see [Multiple Proactive Triggers rules and actions](../concept/multiple-rules-and-actions.md).

    You can localize the language for end users by making entries to the Translated Text table. For more information about making entries to the Translated Text table, see [Translating text fields](https://www.servicenow.com/docs/access?context=c_UseTranslatedText&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


## Result

The triggering rules and actions are ready for you to validate and test.

