---
title: Monitoring user activity
description: Learn about the tools available to administrators for monitoring users on their instance.
locale: en-US
release: yokohama
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Monitoring user activity

Learn about the tools available to administrators for monitoring users on their instance.

## User administration tools

In addition to storing information on a user, user accounts are also associated to groups and roles. Your instance uses groups and roles to determine which records and features an individual may access.

-   **Impersonation**

    Administrators can select user records for impersonation. Use this feature to experience the instance as another user, with that user's preferences and permissions. User impersonation can be a valuable tool for testing and troubleshooting. For more information on impersonation, see [Impersonating users](../../users-and-groups/concept/c_ImpersonateAUser.md).

-   **Investigating user account activity**

    At any time there is a need to review specific user behavior, below are the recommended steps on how to review the transaction logs and event logs:

    -   Locate the IP address of successful/failed login for a particular ServiceNow user for their instance
    -   Modify the time frame of the search
    -   Limiting the scope of the search by user name
    -   View successful/failed login attempts
    For more information about investigating user activity, see the [How to investigate user account activity \[KB0564981\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564981) article in the Now Support Knowledge Base.

-   **User sessions**

    With user session management, and administrator can view and terminate individual user sessions, lock out users from the instance, and make users inactive. For details on managing user sessions, see [Managing user sessions](../../user-sessions/concept/c_ManageUserSessions.md#).

    User records are also associated with transaction logs. Administrators can use these logs to track all browser activity for an instance.


-   **[Impersonating users](../../users-and-groups/concept/c_ImpersonateAUser.md)**  
Administrators are able to impersonate other authenticated users, a feature primarily used for testing.
-   **[Managing user sessions](../../user-sessions/concept/c_ManageUserSessions.md#)**  
The ServiceNow AI Platform provides the ability to view and terminate individual user sessions, lock out users from the system, and make users inactive.
-   **[Non-interactive sessions](../../users-and-groups/concept/c_NonInteractiveSessions.md#)**  
The Non-Interactive Sessions plugin creates a distinction between interactive and non-interactive users.

**Parent Topic:**[Configure ServiceNow AI Platform core features](../../general/concept/config-now-platform-core-features.md)

