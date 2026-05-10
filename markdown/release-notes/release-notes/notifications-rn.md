---
title: Notifications release notes
description: The ServiceNow Notifications application enables you to create, manage, and send custom notifications in workflows for important events, actions, and alerts. Notifications was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Notifications release notes

The ServiceNow® Notifications application enables you to create, manage, and send custom notifications in workflows for important events, actions, and alerts. Notifications was enhanced and updated in the Australia release.

## Notifications highlights for the Australia release

-   Integrate personal corporate mailboxes with in ServiceNow to send and receive emails.
-   Send outbound emails from the ServiceNow instance using Microsoft Graph.
-   Encrypt inbound email attachments in CLE-enabled tables and decrypt them for outbound emails.
-   Enhanced inbound email classification to support thread-index header for emails generated via Microsoft or Microsoft Outlook ecosystem.
-   Deliver critical push notifications even when users are logged out.
-   Create and modify email notifications and email templates using natural language prompts through the Notification Agent.

See [Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/notifications.md) for more information.

## New in the Australia release

-   **[User mailbox integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/personal-corporate-mailbox.md)**

    Enable agents to integrate their personal corporate mail boxes to send and receive emails.

-   **[Granular admin roles required to secure the instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/granular-admin-roles-notifications.md)**

    The granular admin role enables developers and administrators to complete administrative configuration tasks for Notifications without requiring the full admin role.

-   **[Notification agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/notification-creation-agent.md)**

    The Notification agent enables platform administrators to create and modify email notifications and templates using natural language prompts, reducing the need of navigating complex forms &amp; scripts.


## UI changes

-   **[Create an email client template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAnEmailClientTemplate.md)**

    Added a check box for the email client template.

-   **[Configure templates for personal corporate mailboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-personal-corporate-mailbox.md)**

    Added a new **From Generation Type** for the User Email Addresses for email client templates.

-   **[Integrate personal corporate mailbox for receiving emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/integrate-corporate-email-receiving.md)**

    Added the Forwarding Address option for the email account type.


## Changed in this release

-   **[Sending email using Microsoft Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/send-email-using-ms-graph.md)**

    Connect Microsoft email accounts using Microsoft Graph within the ServiceNow instance for sending outbound emails.

-   **[Email threading for inbound reply email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_InboundEmailActions.md)**

    Enable classification of inbound emails by using the thread-index header for emails originating from Microsoft or Microsoft Outlook ecosystem.

-   **[Column Level Encryption for email attachments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/cle-for-email-attachments.md)**

    Attachments from inbound emails are now encrypted when stored in CLE-enabled tables and decrypted when sent in outbound emails, ensuring secure access without requiring scripting.

-   **[Enable push notifications for logged-out users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/enable-notifications-logged-out-users.md)**

    Push notifications can now be configured to be sent to users even when they are logged out, ensuring critical updates are not missed.


## Activation information

Notifications is a ServiceNow AI Platform feature that is active by default.

Install Notifications Email Agents by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

The Notification Agent requires the Implementation Agent \(IA\) Orchestration framework and is not supported as a standalone feature.

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

