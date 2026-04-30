---
title: Security Event Notifications
description: View, manage, and analyze the default security event notification policies on your ServiceNow instance, as well as access the functionality to create custom policies.
locale: en-US
release: zurich
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Security monitoring console, Security Center, Platform Security]
---

# Security Event Notifications

View, manage, and analyze the default security event notification policies on your ServiceNow instance, as well as access the functionality to create custom policies.

Access Security Event Notifications from the Security Center homepage by opening the **Security Monitoring Console** in the **Security Consoles** section, then selecting the **Security Event Notifications** tab.

![Security events notifications](../images/security-event-notifications-overview.png)

Customize and create notification policies that trigger email notifications when users perform actions in the ServiceNow AI Platform that might be insecure or require admin monitoring.

Admins can customize the values for the default policies, clone, and edit default policies or create their own custom ones.

## Security policies

The Security Event Notifications console displays important information regarding the security policies on your instance. This table includes columns displaying:

<table id="table_gfh_dbt_wbc"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the security event notification policy.

</td></tr><tr><td>

Status

</td><td>

The status of a policy can be either active or inactive.

</td></tr><tr><td>

Updated

</td><td>

The date and time of when the policy was last updated.

</td></tr><tr><td>

Updated by

</td><td>

The user that updated a policy.

</td></tr><tr><td>

Last triggered on

</td><td>

The date and time the policy last ran.

</td></tr><tr><td>

Triggered count last week

</td><td>

The number of triggers a policy generated the past 7 days.

</td></tr><tr><td>

Percentage change

</td><td>

The rate of change for weekly triggers, calculated as a percentage.**Note:** For example, if this policy triggers an average of 5 notifications a week and it triggered 10 times last week, that would be a percentage increase of 100%.

</td></tr></tbody>
</table>Select a policy on the table to view more detail, including an overview, settings, and notification history. Select the **New custom policy** button to create a custom policy tailored to your organization's use cases.

## Manage security banner announcements

Select **Manage announcement settings** to control whether admins receive banner notifications on this instance. For information on these announcements, see [Security banner announcements](scc-banner.md).

-   **[Create custom security event notification policies](../task/create-a-policy.md)**  
Learn how to create custom security event notifications that are specific to your organization's needs. This enables you to monitor actions taken by users and groups on your instance and generate notifications for potential security risks.
-   **[Modify security event notification policies](../task/modify-security-event-notification-policies.md)**  
Learn how to modify the settings of your security event notification policies.
-   **[Configure preferences for security event notification policies](../task/configure-preferences-for-security-event-notifications.md)**  
Discover how to customize security event notification policies in Security Center to align with your organization's specific needs.
-   **[Security Event Notifications history](security-event-notifications-history.md)**  
Explore the complete history of security event notifications on your instance.

**Parent Topic:**[Security monitoring console](sc-monitor-console.md)

