---
title: Log Export Service roles
description: Log Export Service is installed with these roles.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Log Export Service \(LES\), Platform Security]
---

# Log Export Service roles

Log Export Service is installed with these roles.

## Application admin \[sn\_logstoanalytics.admin\]

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and contact your account representative.

This role is installed along with the LES application and allows a non-admin to use the application.

-   **Contains Roles**

    List of roles contained within the role.

    None.

-   **Groups**

    List of groups this role is assigned to by default.

    None.

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see[Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md).

    No.

-   **Special considerations**

    None.


## System administrator \[admin\]

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and contact your account representative.

Admin role is required for the setup of the LES store application.

-   **Contains Roles**

    List of roles contained within the role.

    -   sn\_templated\_snip.template\_snippet\_admin
    -   sn\_employee.admin
    -   taxonomy\_admin
    -   sn\_ace.ace\_user
    -   sn\_hr\_sp.esc\_admin
-   **Groups**

    List of groups this role is assigned to by default.

    None.

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md).

    No.

-   **Special considerations**

    None.


**Parent Topic:**[Log Export Service \(LES\)](../concept/les-landing-page.md)

