---
title: Fix external user role assignments
description: You may have external users \(contacts or consumers\) on your instance that have been assigned internal roles. If so, you can use the Customer Service Management guided setup to evaluate and correct these role assignments as needed.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [User management, Set up your environment, Configure, Customer Service Management]
---

# Fix external user role assignments

You may have external users \(contacts or consumers\) on your instance that have been assigned internal roles. If so, you can use the Customer Service Management guided setup to evaluate and correct these role assignments as needed.

Because external users with internal roles can result in access issues, it’s recommended that external users only be assigned external roles.

Use the tasks in the Fix External User Role Assignment category guided setup category to evaluate the contacts and consumers with the following role assignments:

-   The snc\_internal role only.
-   The snc\_internal role and one or more external roles.
-   The snc\_internal role and one or more additional internal roles.
-   The snc\_internal role and one or more additional internal and external roles.

Review the list of users in each group and tag those users with incorrect role assignments. Then run the scheduled job to fix the role assignments.

**Note:** You can also review and update external user roles using a query-based list. For more information, see [KB0829930](https://support.servicenow.com/kb_view.do?sysparm_article=KB0829930).

## Using guided setup to fix external user role assignments

With the csm\_guided\_setup\_user role, you can use guided setup to fix external user role assignments.

1.  Navigate to **Customer Service** &gt; **Administration** &gt; **Guided Setup**.
2.  On the Getting Started page of the guided setup, select **Get Started**.
3.  In the Fix External User Role Assignment category, select **Get Started**.

    The Fix External User Role Assignment page opens with a list of tasks to evaluate groups of external users.

4.  To perform a task, select **Configure**.

    This button opens the page in your instance where the configuration is completed.


## Fix External User Role Assignment tasks

The following table describes the different configuration tasks in the Fix External User Role Assignment category.

<table id="table_tth_54l_mlb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

External users with possible non-intentional internal role assignment

</td><td>

It's a set of contacts and consumers with the following role assignments:-   The snc\_internal role only.
-   The snc\_internal role and one or more external roles.

You must not assign internal roles to external users. Review the contacts in this list and fix the role assignment as needed.

</td></tr><tr><td>

External users with possible intentional internal role assignments

</td><td>

It's a set of contacts and consumers that have the following role assignments:-   The snc\_internal role and one or more additional internal roles.
-   The snc\_internal role and one or more additional internal and external roles.

You must not assign both internal and external roles to the same user. Review the users in this list and fix the role assignment as needed.

</td></tr><tr><td>

External users with intentional internal role assignments

</td><td>

It's a set of contacts and consumers that have the snc\_internal role that is contained by another role.You must not assign internal roles to external users. Review the users in this list and fix the role assignments as needed.

</td></tr><tr><td>

Avoid such role assignments in future

</td><td>

To help prevent external users from being assigned the snc\_internal role in the future, enable the following property: **glide.security.explicit\_roles.enable\_internal\_user\_blacklist**

 Select **Configure** to navigate to the property and verify that the value is true. If false, set the value to true.

</td></tr></tbody>
</table>