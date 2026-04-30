---
title: Automated Test Framework roles
description: Automated Test Framework is installed with these roles.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Automated Test Framework reference, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Automated Test Framework roles

Automated Test Framework is installed with these roles.

## ATF test administrator \[atf\_test\_admin\]

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and contact your account representative.

Create or edit Automated Test Framework properties. Has permission to:

-   View the tests page
-   Create/edit/delete tests
-   Create/edit/delete test steps
-   View the step config page
-   View the test runner page
-   View the test suite results, test results and result items pages
-   Execute user tests
-   View, create, edit, delete and execute test suites
-   Create/edit step config records
-   Create/edit Automated Test Framework properties

-   **Contains Roles**

    List of roles contained within the role.

    -   impersonator
    -   personalize\_dictionary
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevate to a privileged role](https://www.servicenow.com/docs/access?context=t_ElevateToAPrivilegedRole&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

    No.

-   **Special considerations**

    None.


## ATF test designer \[atf\_test\_designer\]

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and contact your account representative.

View Automated Test Framework properties only \(can't create or edit properties\). Has permission to:

-   View the tests page
-   Create/edit/delete tests
-   Create/edit/delete test steps
-   View the step config page
-   View the test runner page
-   View the test suite results, test results and result items pages
-   Execute user tests
-   View, create, edit, delete and execute test suites
-   View Automated Test Framework properties

-   **Contains Roles**

    List of roles contained within the role.

    impersonator

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Subscription**

    Whether the role is a chargeable user role that requires allocation of users with this role to subscriptions.

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevate to a privileged role](https://www.servicenow.com/docs/access?context=t_ElevateToAPrivilegedRole&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

    No.

-   **Special considerations**

    None.


## ATF workspace designer \[atf\_ws\_designer\]

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and contact your account representative.

View or set the basic or mutual authentication needed for REST endpoints that require authentication.

-   **Contains Roles**

    List of roles contained within the role.

    -   atf\_test\_designer
    -   web\_service\_admin
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Subscription**

    Whether the role is a chargeable user role that requires allocation of users with this role to subscriptions.

    No.

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevate to a privileged role](https://www.servicenow.com/docs/access?context=t_ElevateToAPrivilegedRole&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

    No.

-   **Special considerations**

    None.


**Parent Topic:**[Automated Test Framework reference](../concept/atf-ref-overview.md)

