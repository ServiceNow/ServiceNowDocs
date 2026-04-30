---
title: Configure preferences for security event notification policies
description: Discover how to customize security event notification policies in Security Center to align with your organization's specific needs.
locale: en-US
release: yokohama
product: Security Center
classification: security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Security Event Notifications, Security monitoring console, Security Center, Platform Security]
---

# Configure preferences for security event notification policies

Discover how to customize security event notification policies in Security Center to align with your organization's specific needs.

## Before you begin

Role required: admin

## About this task

The **Policy settings** page is where you can customize the settings for a security event notification policy. Here, you can adjust options related to when the policy runs, the conditional logic, and the notifications that are sent.

## Procedure

1.  In Security Center, select **Notifications**.

2.  Under the Security policies table, select a security event notification policy that you want to configure.

    For example, **Send notification when high privileged role is granted**.

3.  Select **Policy settings**.

4.  Configure the policy settings.

<table id="table_xdj_3gf_wbc"><thead><tr><th>

Label

</th><th>

What to configure

</th></tr></thead><tbody><tr><td>

**When to run**

</td><td>

**Trigger**: The event that starts the policy.

</td></tr><tr><td>

**Conditions**

</td><td>

The conditional logic and conditions to apply to your policies.

 -   **Condition logic**: two options
    -   **All conditions must be met to trigger this policy**: all conditions need to be valid for the policy to send notifications.
    -   **Any of the conditions must be met to trigger this policy**: notifications will be sent if any one of the conditions is valid.
-   **Add Condition**: Select Add Condition and provide the appropriate values for it.
 You can remove a condition by selecting **Remove condition**.

</td></tr><tr><td>

**Notifications**

</td><td>

The email body and email recipients:-   **Notification**: Select one of the predefined notification templates. See [Create a custom email for security event notifications](create-custom-email-for-security-event-notifications.md) for more information.
-   **Add Notification**: Select Add Notification.
-   **Groups**: Select the group who should receive the notification.
-   **Users**: Select the users who should receive the notification.
You can remove a notification by selecting **Remove notification**.

</td></tr></tbody>
</table>    **Note:** If you want to make a policy inactive, select **Deactivate**. If you want to replicate a policy, select the down arrow next to the **Update** \(![Update button.](../images/update-ui-image.png)\) button.

5.  Select **Update** to save your settings.


-   **[Create a custom email for security event notifications](create-custom-email-for-security-event-notifications.md)**  
Learn how for creating a custom email for security event notifications by configuring new notifications, setting triggers, defining recipients, and crafting email content with dynamic event fields.

**Parent Topic:**[Security Event Notifications](../concept/security-policies.md)

