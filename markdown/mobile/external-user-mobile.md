---
title: Mobile external users
description: Define external users to have availability to access your instance, but without access to all the capabilities allocated to internal users. External users are usually third parties, contractors, or external agents. External users are not employees of your organization.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Mobile external users

Define external users to have availability to access your instance, but without access to all the capabilities allocated to internal users. External users are usually third parties, contractors, or external agents. External users are not employees of your organization.

External users can perform tasks like view knowledge base articles, create, edit and manage incidents, and use Virtual Agent chat, without affecting the security of the instance. The snc\_external role is assigned to external users and specifies that such users have fewer privileges. For more information on the snc\_external role and how it is defined, see [External roles in self-registration](https://www.servicenow.com/docs/access?context=external-roles-self-registration&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) and [Explicit roles in CSM](https://www.servicenow.com/docs/access?context=explicit-roles-in-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Functionality not available to mobile external users

The following is a list of different functionalities and capabilities not available to external users on mobile.

-   **Zing search** - The search bar is not displayed for screens that use Zing search. For AI Search, the search bar is displayed.
-   **Charts** - Both Performance Analytics and reporting charts are not displayed.
-   **Attachments** - By default, external users are not able to view, edit, or upload attachments. To enable external users to view, edit, or upload attachments, set the **allow\_snc\_external\_attachment\_access** mobile property to `true`. For more information, see [Enable external users to access attachments](../task/enable-ext-users-attach-access.md).
-   **Offline** - Mobile offline mode is not available. External users without an internet connection cannot continue to work from a mobile device.
-   **Debug drawer** - The ability to display performance-related data via the debug drawer, is not available.
-   **Impersonate user** - External users cannot use the mobile impersonation functionality.

