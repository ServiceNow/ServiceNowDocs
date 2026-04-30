---
title: Create a delegate
description: Delegation admins \(delegation\_admin\) can delegate tasks from one employee to another using Granular Delegate.
locale: en-US
release: xanadu
product: Granular Delegation
classification: granular-delegation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Granular Delegation, Granular Delegation, Employee Service Management]
---

# Create a delegate

Delegation admins \(delegation\_admin\) can delegate tasks from one employee to another using **Granular Delegate**.

## Before you begin

Role required: delegation\_admin

Ensure that the delegate user \(the person to whom tasks will be reassigned\) has the necessary roles to complete those tasks.

## Procedure

1.  Navigate to **All** &gt; **Granular Delegation** &gt; **Create New Delegate**.

2.  Fill in the form.

<table id="table_klq_cg2_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

User \(delegator\) who delegates service tasks to a delegate.

</td></tr><tr><td>

Starts

</td><td>

Date when service delegation begins.

</td></tr><tr><td>

Delegate

</td><td>

User authorized as delegate.

</td></tr><tr><td>

Ends

</td><td>

Date when service delegation ends.

</td></tr><tr><td>

All notifications

</td><td>

Option to send the delegate a copy of all notifications you receive during the delegation period. Select this option when you want the delegate to receive the delegation notification. For example, you want the delegate to receive notifications about activity stream or record updates. It is set to False by default to avoid concerns around getting notifications that has critical and sensitive data. **Note:** Notifications with the **Exclude Delegates** option enabled override the True setting of this option. Use the **Exclude Delegates** option to prevent delegates from seeing confidential or protected information.

</td></tr><tr><td>

Meeting invitations

</td><td>

Option to forward delegates meeting invitations. Select this option to forward the delegate any meeting invitations the instance generates or receives for you. It is set to False by default.

</td></tr></tbody>
</table>3.  Select **Save**.

    The **Delegation Rules** related list appears.

4.  Select **Edit** to assign delegation rules to a delegate.

    You can use condition filters to search for delegation rules.

5.  Select delegation rules under the **Collection** column you want to assign to a delegate and move them to the **Delegation Rules List** column.

6.  Select **Save**.

    The **Granular Delegate** form returns.


