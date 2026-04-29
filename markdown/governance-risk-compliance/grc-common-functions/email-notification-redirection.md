---
title: GRC notification redirection
description: When you receive notifications for GRC records, you're directed to either the workspace view or classic view based on your access permissions and role. This feature enables you to work directly in the appropriate interface without manual navigation.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# GRC notification redirection

When you receive notifications for GRC records, you're directed to either the workspace view or classic view based on your access permissions and role. This feature enables you to work directly in the appropriate interface without manual navigation.

## How it works

When you select a link in a notification, the system determines where to direct you based on your workspace access:

-   If you have access to a workspace, you're directed to the workspace view of the record.
-   If you don't have workspace access, you're directed to the classic view of the record.
-   If you have access to multiple workspaces, you're directed to the workspace view of the record in the workspace that takes precedence based on your administrator's configuration.

## Benefits

-   You remain in your preferred interface without having to switch manually between workspace and classic views.
-   You have a consistent experience across notifications and workspaces.
-   Reduced confusion and fewer steps when accessing records.
-   If your workspace access can't be determined, you're directed to the classic view so that you can still access records from notifications.

-   **[Configure GRC notification redirection](../task/configure-email-notification-redirection.md)**  
Create notification routing rules that automatically direct users to workspace view or classic view based on their access permissions.
-   **[Modify email notifications to use notification redirection](../task/modify-email-notifications-to-use-notification-redirection.md)**  
Update email notifications to use the notification redirection framework so users are automatically directed to the appropriate view based on their workspace access.

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

**Related topics**  


[Configure GRC notification redirection](../task/configure-email-notification-redirection.md)

