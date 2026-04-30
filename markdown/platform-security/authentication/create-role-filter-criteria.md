---
title: Create role filter criteria
description: Role filter criteria allows you to filter users based on the roles. You can configure an authentication policy to allow or deny access to a list of user roles.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Role Filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Create role filter criteria

Role filter criteria allows you to filter users based on the roles. You can configure an authentication policy to allow or deny access to a list of user roles.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Filter Criteria** &gt; **Role Filter Criteria**.

2.  Click **New**.

3.  On the form, fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the role.|
    |Application|Scope of the application.|
    |Description|Short description of the role.|

    ![Role filter criteria form](../images/role-filter-criteria-2.png "Example role filter criteria record")

4.  From the **Roles for criteria**, double-click **Insert a new row**.

5.  Create a condition for a specific role using the Condition Builder.

    For example, you can create a condition that allows only users with admin, itil, or snc\_internal roles. For more information about Condition Builder, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    **Note:** Currently, Dot-walking is not supported in Role filter criteria.

    ![Role filter criteria sample.](../images/role-filter-criteria.png)


