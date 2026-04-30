---
title: Email service
description: The Email Service API provides endpoint to install the Email API on the instance.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Creating an email account, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email service

The Email Service API provides endpoint to install the Email API on the instance.

By default, Email Service only allows admin users to access the [Email API](https://www.servicenow.com/docs/access?context=email-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US). Administrators can [grant access to the Email API](../task/grant-access-to-email-api.md) by:

1.  Adding an access control for creating records in the Email \[sys\_email\] table linked to the email\_api\_send role.
2.  Assigning the email\_api\_send role to the non-admin user.
3.  Verifying the non-admin user has read access to the notification target table. For example, an email notification for an incident, requires read access to the Incident table.

Non-admin users with the email\_api\_send role can access the Email API from the [REST API Explorer](https://www.servicenow.com/docs/access?context=use-REST-API-Explorer&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

-   **[Create a system address filter](../../../administer/notification/task/create-system-address-filter.md)**  
Define how email address filters apply to inbound and outbound email.

**Parent Topic:**[Creating an email account](../../../administer/notification/concept/using-email-admin.md)

