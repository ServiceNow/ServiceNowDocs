---
title: Create an email notification using the Notification agent
description: Create an email notification using the Notification agent in Now Assist by describing your requirements in natural language, instead of navigating forms or writing scripts.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-20"
reading_time_minutes: 1
breadcrumb: [Notification agent, Now Assist in Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an email notification using the Notification agent

Create an email notification using the Notification agent in Now Assist by describing your requirements in natural language, instead of navigating forms or writing scripts.

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

6.  Select **Create a new notification**, or enter a natural language prompt.

    Example prompts:

    -   `Notify the approver when an [BU name] request is pending approval.`
    -   `Notify the assignee when an [BU name] task is due.`
    **Note:**

    The agent supports two intents, creating a new notification or editing an existing notification. If the intent is unclear, the agent prompts you to select one.

7.  If the agent asks clarifying questions, provide the requested details to help it generate accurate notifications.

8.  Review the notification details that are displayed.

9.  Select one of the following options:

    -   **No, looks good** to create notification with the current details
    -   **Yes, I'd like to make changes** to modify the notification details
10. If you selected **Yes, I'd like to make changes**, enter the updates when prompted.

    Now Assist revises the notification and displays the updated details.

11. Review the updated notification details and select **Confirm**.

    Now Assist creates the notification and displays a success message.


