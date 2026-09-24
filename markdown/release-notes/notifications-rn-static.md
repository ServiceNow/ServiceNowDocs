---
title: Notifications release notes
description: The ServiceNow Notifications application enables you to create, manage, and send custom notifications in workflows for important events, actions, and alerts. See the following sections for release notes by version.This release enhances the Intent to Action framework, adds an inbound email channel for sensitive data redaction, includes source mailbox information in inbound email headers, and enables viewing original emails associated with bounced email addresses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/notifications-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow AI Platform administration release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Notifications release notes

The ServiceNow® Notifications application enables you to create, manage, and send custom notifications in workflows for important events, actions, and alerts. See the following sections for release notes by version.

## About Notifications

-   Keep users informed by sending email or SMS notifications about specific activities in the system, such as updates to incidents or change requests.
-   Control when notifications are sent, who receives them, and what content they contain.
-   Improve communication efficiency with email digests that consolidate multiple notifications into a single message.

See [Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/notifications.md) for more information.

## Activation and other requirements

-   **Activation information**

    Notifications is a ServiceNow AI Platform® feature that is active by default.

    Install Notifications Email Agents by requesting it from the ServiceNow® Store. Visit the [ServiceNow Store](https://store.servicenow.com/store) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    The Notification Agent requires the Implementation Agent \(IA\) Orchestration framework and is not supported as a standalone feature.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/now-platform-admin-rn-landing.md)

## Brazil Early Availability

This release enhances the Intent to Action framework, adds an inbound email channel for sensitive data redaction, includes source mailbox information in inbound email headers, and enables viewing original emails associated with bounced email addresses.

### What's changed

-   **Omnichannel intent detection and resolution**

    Enable omnichannel intent detection and resolution using a global intent library.

-   **Inbound email privacy policy configuration**

    Sensitive data redaction for inbound emails is now supported through a dedicated inbound email channel in Privacy Policy Advanced Configuration.

-   **Source mailbox identification for inbound emails**

    Identify the source mailbox using information included in inbound email headers.

-   **[View original bounced emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/email-bounce.md)**

    The original email associated with a bounced email address can now be viewed from the Bounce Email Address Logs record.


