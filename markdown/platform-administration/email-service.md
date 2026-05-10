---
title: Email service
description: The Email Service API provides endpoint to install the Email API on the instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email service

The Email Service API provides endpoint to install the Email API on the instance.

By default, Email Service only allows admin users to access the [Email API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/email-api.md). Administrators can [grant access to the Email API](../task/grant-access-to-email-api.md) by:

1.  Adding an access control for creating records in the Email \[sys\_email\] table linked to the email\_api\_send role.
2.  Assigning the email\_api\_send role to the non-admin user.
3.  Verifying the non-admin user has read access to the notification target table. For example, an email notification for an incident, requires read access to the Incident table.

Non-admin users with the email\_api\_send role can access the Email API from the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/use-REST-API-Explorer.md).

-   **[Create a system address filter](../../../administer/notification/task/create-system-address-filter.md)**  
Define how email address filters apply to inbound and outbound email.

**Parent Topic:**[Creating an email account](../../../administer/notification/concept/using-email-admin.md)

