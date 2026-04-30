---
title: Prevent a role from being delegated
description: You can prevent roles from being delegated to users.
locale: en-US
release: zurich
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Delegating roles, Managing roles, User admin, Configure core features, Administer]
---

# Prevent a role from being delegated

You can prevent roles from being delegated to users.

## Before you begin

Role required: admin

## About this task

By default, the following roles can’t be delegated.

-   admin
-   public
-   role\_delegator

    **Note:** A user with the role\_delegator role can’t delegate this role to other group members.


## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Roles**.

2.  Open the role.

3.  Configure the form to add the **Grantable** or **Can delegate** fields.

4.  Clear the check box for one or both of these fields.

5.  Select **Update**.


**Parent Topic:**[Delegating roles](../concept/c_DelegateRoles.md)

