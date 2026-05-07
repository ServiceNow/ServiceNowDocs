---
title: Multiple Proactive Triggers rules and actions
description: The Proactive Triggers feature uses rules and actions to trigger context-specific Virtual Agent conversations with end users on the web client.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Proactive Triggers, Proactive Triggers, Manage people and work, Conversational Interfaces]
---

# Multiple Proactive Triggers rules and actions

The Proactive Triggers feature uses rules and actions to trigger context-specific Virtual Agent conversations with end users on the web client.

An admin enables the [Proactive Triggers](../task/enable-proactive-triggers.md) feature.

An admin then creates rules and defines actions that are triggered by those rules. Admins can create multiple rules and actions. They also specify the end user that the rules and actions apply to.

Multiple rules can be defined with the same trigger type references \(for example, catalog item, knowledge, portal home, URL\) as long as the **Order** and **Delay time** settings are different. Multiple rules defined on the same trigger type references let you layer messages based on how long the end user is on the page.

A rule can include more than one action, but ensure that you apply the action to different users in the **Applies to** fields.

If you have errors when you create a rule, check the following fields to see if there's a conflict:

**Tip:** The error message that appears includes a link that you can select to help you identify the conflicts.

![Error message link.](../image/conflict-error-message-link.png "Error message example")

-   **Trigger type**
-   **Delay time**
-   **Order**

It may be necessary to clear the rule's history for the rule to function as anticipated. When you set your rule's **Frequency** field to **Once per user** and you want to run the rule again, you must clear the history. Clearing the history lets you apply the rule again for that user. To clear the rule's history, select **Clear History** on the rule's Proactive Rule form. After the history clears, an admin must reactivate the rule.

![Clear History.](../image/ci-proactive-triggers-new-rule-button.png "Clear History example")

**Related topics**  


[Manage Proactive Triggers](manage-proactive-triggers-2.md)

