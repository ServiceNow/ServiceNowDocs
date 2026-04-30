---
title: Edit an email notification using the Notification agent
description: Edit an email notification using the Notification agent in Now Assist by describing your requirements in natural language, instead of navigating forms or writing scripts.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 1
breadcrumb: [Notification agent, Now Assist in Notifications, Configure core features, Administer]
---

# Edit an email notification using the Notification agent

Edit an email notification using the Notification agent in Now Assist by describing your requirements in natural language, instead of navigating forms or writing scripts.

## Before you begin

The Notification agent may produce inconsistent results when used with the Now LLM model. Confirm the notification details before deployment.

**Note:** The Notification Agent requires the Implementation Agent \(IA\) Orchestration framework and is not supported as a standalone feature.

Role required: admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  In the **Manage your products** section, select **View product overview** on the relevant product card.

3.  In the **Configuration insights** section, select **Configure**.

    The configure page opens in the Configuration Console.

4.  Select **Notifications** under the business unit you want to configure \(for example, Legal, Workplace Services, or Finance for Core Business Suite\).

5.  Select **Configure with Now Assist**.

    Now Assist opens the conversational panel, detects the current page context, and invokes the Notification Agent.

6.  Select **Edit an existing notification**.

    **Note:**

    The agent supports two intents, creating a new notification or editing an existing notification. If the intent is unclear, the agent prompts you to select one.

7.  When prompted, enter the name of the email notification.

    Now Assist loads the notification record and displays a link for review.

8.  Enter the changes you want to make.

    Example prompts:

    -   `Modify the condition to trigger when priority is High.`
    -   `Trigger the notification when the record is updated.`
    Now Assist processes your updates and displays the revised notification details.

9.  Review the updated notification details and confirm.

    Now Assist saves the changes and displays link to the updated notification.

10. If further modifications are needed, specify any additional changes.


