---
title: External roles in self-registration
description: To prevent inadvertently providing access to external users, you can assign the snc\_external role to all external users.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate External User Self-Registration, Self-register to ServiceNow instance, Authentication, Access Management]
---

# External roles in self-registration

To prevent inadvertently providing access to external users, you can assign the snc\_external role to all external users.

External users that self-register must be assigned the snc\_external role, which has the least privileges. The snc\_external role indicates that the user is external to your organization and should not have any access to resources unless explicitly allowed through ACLs for the snc\_external role or additional roles that inherit the snc\_external role.

By default, users with the snc\_external role cannot access:

-   Tables without the role that inherits the snc\_external role or the public role.
-   Non-record type resources, such as processors and UI pages without the snc\_external role or a role that inherits the snc\_external role.
-   Platform Analytics dashboards.

Beginning with the Paris release, you must enable an exclude-list property to enforce the explicit assignment of snc\_external roles. For information about enabling the property, see [Prevent future internal role assignments for external users](https://www.servicenow.com/docs/access?context=fix-csm-external-user-roles-task4&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

