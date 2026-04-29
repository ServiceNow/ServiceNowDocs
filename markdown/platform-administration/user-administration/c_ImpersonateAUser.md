---
title: Impersonating users
description: Administrators are able to impersonate other authenticated users, a feature primarily used for testing.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitoring user activity, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Impersonating users

Administrators are able to impersonate other authenticated users, a feature primarily used for testing.

This function enables the administrator to access the system exactly as the impersonated user, including identical menus and modules. All actions performed by the administrator during impersonation are recorded as if they were executed by the impersonated user.

![Impersonation example](../image/imperson_general.png)

## Impersonation limitations

When you impersonate a user, all scope-protected roles and encryption module roles are supported if the **Impersonation** option is configured in the module access policy. See [Create a module access policy](https://www.servicenow.com/docs/access?context=create-module-access-policy&version=australia&pubname=australia-platform-security&ft:locale=en-US) for details.

Impersonating a user enables access to scope-protected and encryption roles, as defined in the access policy. However, if impersonating a user with an admin role, access to certain features and modules is limited unless the impersonator already possesses those roles.

Impersonating a user with an application-specific admin role, like Human Resources admin or Security Incident Response, limits access to certain features such as security incidents and profile information, unless these roles are already assigned to the impersonating admin. This restriction extends to certain modules and applications in the navigation bar, and admins can’t change the password of users with application admin roles.

The following actions or conditions cause a user impersonation to end:

-   The user impersonates a different user
-   The user session ends, for example after a user logs out of their instance

    **Note:** When an administrator starts impersonating a user, the 'Impersonate Begin' event is logged in the system log. Similarly, the 'Impersonate End' event is recorded when impersonation concludes under one of the two conditions listed above.


## Impersonation requirements

The user account to be impersonated must have a user ID. You can find this ID in the User \[sys\_user\] record for the account. If this value is missing, the message `The user you selected could not be impersonated` appears.

You need several different accounts to test the system.

-   An admin account to do work
-   An information technology infrastructure library \(ITIL\), or similar, account to test as a technician
-   An ESS account to test as an end user

More logins may be required to adequately test the system.

**Note:** If you try to impersonate a user who is either locked out or inactive, the system will automatically log you out if you initiate an action or select a link. Remember that all changes made during impersonation only apply to that session. To help ensure accuracy, log out and then log back in after completing the impersonation.

## Mobile impersonation

Mobile impersonation is available on ServiceNow mobile apps. For information on mobile impersonations, see [Mobile impersonation](https://www.servicenow.com/docs/access?context=mobile-impersonation&version=australia&pubname=australia-mobile&ft:locale=en-US).

-   **[Manage the visibility of the impersonation feature](manage-the-visibility-of-the-impersonation-feature.md)**  
Before users can impersonate another user, an administrator must make the feature visible.
-   **[Impersonate a user](../task/t_ImpersonateAUserInUI16.md)**  
You can select a user or enter a different user name to perform an impersonation.
-   **[Impersonation logs](c_LogImpersonations.md)**  
Impersonations are logged in the system log.
-   **[User impersonation auditing](impersonation-audits.md)**  
User impersonation auditing creates a structured, dedicated audit trail for every impersonation session.

**Parent Topic:**[Monitoring user activity](../../roles/concept/user-admin-tools-landing.md)

