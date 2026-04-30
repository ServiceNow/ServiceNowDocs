---
title: Assign the Code Signing Administrator Role
description: Assign the Code Signing Administrator role to a user to access the Code Signing configuration experience.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Code Signing, Code Signing, Platform Security]
---

# Assign the Code Signing Administrator Role

Assign the Code Signing Administrator role to a user to access the Code Signing configuration experience.

## Before you begin

Roles required:

-   admin
-   security\_admin

**Important:** The user that is assigned the Code Signing Administrator role must be in the Global scope.

## Procedure

1.  Select a non-production instance to use as your Trusted non-production instance \(TNPI\).

    The TNPI is used to create jobs, sign records, and perform other necessary tasks before enabling signature validation on your Protected Production Instance \(PPI\).

2.  Navigate to **All** &gt; **Code Signing** &gt; **Code Signing Role Administration**.

3.  Grant a user the Code Signing Administrator role by moving a user from the **Available Users** list to the **Selected User\(s\)** list.

4.  Select **Save**.

    **Important:** The user assigned to the role must log out and lot in again to perform Code Signing tasks.


## Result

The selected user has the Code Signing Admin role. A user with this role can access the Code Signing configuration experience, and assign other Code Signing roles to users.

To learn more about Code Signing roles, see [Roles installed with Code Signing](../reference/cs-role-landing.md#).

**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

