---
title: Using Granular Delegation
description: Employees can use Granular Delegation to delegate their tasks to another eligible employee.You can delegate an assigned task to another employee from your Employee Center.Use the Granular Delegates list to view a list of employees that you have delegated your tasks to. You can also delegate your tasks to another employee as an alternative to using the Employee Center.Use Granular Delegates list to view granular delegate records for the logged in user or employees that have delegated tasks to you.You can use Granular Delegation to delegate tasks from ServiceNow mobile.You can delegate tasks to other eligible users from the ServiceNow mobile.You can use the ServiceNow mobile to view tasks delegated to you.
locale: en-US
release: zurich
product: Granular Delegation
classification: granular-delegation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Granular Delegation, Employee Service Management]
---

# Using Granular Delegation

Employees can use Granular Delegation to delegate their tasks to another eligible employee.

## Delegate on-demand tasks

You can delegate an assigned task to another employee from your Employee Center.

### Before you begin

Role required: none

You can also delegate an assigned task from the ServiceNow® mobile. For more information, see [Using granular delegation on ServiceNow mobile](granular-delegation-use.md#).

**Note:** You must create delegation rules before you can delegate on-demand tasks. For more information, see [Create delegation rules](../task/create-delegation-rules.md).

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  Select your login name or picture at the top, right corner.

3.  Select **Profile**.

4.  Scroll down to the **My Delegates** section and select the **Add Delegate** button.

5.  Fill in the form.

<table id="table_vzv_ttp_pnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delegate

</td><td>

The name of the person you are delegating your tasks to.

</td></tr><tr><td>

Start date

</td><td>

Select the **Show calendar** icon \(![Select date and time icon](../../../human-resources/image/select-date-time-icon.png)\) and select the date you want delegations to start.

</td></tr><tr><td>

End date

</td><td>

Click the **Show calendar** icon \(![Select date and time icon](../../../human-resources/image/select-date-time-icon.png)\) and select the date you want delegations to end.

</td></tr><tr><td>

Duties

</td><td>

Select the duties you want to assign to the delegate for the time period you select.If your admin organized the duties into categories, the categories are listed before the individual duties. When you select a category, all of the duties in that category are selected.

</td></tr></tbody>
</table>    **Note:** Setting up delegation does not automatically delegate the existing active tasks of delegator prior to the delegation start date. Tasks are delegated only in the following cases:

    -   A new case is assigned to the delegator between the delegation start and end dates.
    -   An existing case of the delegator updated during the delegation period.
6.  Select **Submit**.

    **Note:** You can also navigate to **Granular Delegation** &gt; **My Delegates** and select **New**, or **Granular Delegation** &gt; **Create New Delegate** to assign your tasks to another employee. For more information, see [View my delegates](granular-delegation-use.md#).

7.  Select the edit icon, then select **Remove delegate** to remove the delegate

8.  Select the down arrow icon \[![Employee Center - Down arrow icon to show active delegations](../image/esc-down-arrow-icon.png) to view a list of delegates you have assigned your tasks to.

9.  Select the edit icon to remove delegates when you have multiple delegates.


## View my delegates

Use the **Granular Delegates** list to view a list of employees that you have delegated your tasks to. You can also delegate your tasks to another employee as an alternative to using the Employee Center.

### Before you begin

-   Role required: any role with access to task tables such as HR Task \[sn\_hr\_core\_task\]
-   Create one or more Delegation Rule records
-   Verify that your delegate has access to the records specified by your delegation rules

**Note:** Admins can use the **Create New Delegate** form to assign tasks from a delegator to a delegate. For more information, see [Create a delegate](../task/create-delegation-admin.md).

### Procedure

1.  Navigate to **All** &gt; **Granular Delegation** &gt; **My Delegates**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_urd_3v2_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

User \(delegator\) who delegates service tasks to a delegate.

</td></tr><tr><td>

Delegate

</td><td>

User you want to delegate tasks to.

</td></tr><tr><td>

Starts

</td><td>

Date when service delegation begins.

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
</table>4.  Select **Save**.

5.  From the **Delegation Rules** related list, select **Edit**.

6.  Select the delegation rules records you authorize this delegate to have.

7.  Select **Save**.

    The **Granular Delegate** form returns.

8.  Select **Update**.


## View delegations assigned to me

Use **Granular Delegates** list to view granular delegate records for the logged in user or employees that have delegated tasks to you.

### Before you begin

-   Role required: any role with access to task tables such as HR Task \[sn\_hr\_core\_task\]
-   Create one or more Delegation Rule records
-   Verify that your delegate has access to the records specified by your delegation rules

### Procedure

1.  Navigate to **All** &gt; **Granular Delegation** &gt; **Delegated to Me**.

    A list of delegation records assigned to you appears.

2.  To view a delegation record, select the date link under the **Starts** column.

3.  To view the user record of the delegator, select the user link under the **User** column.

4.  To create a new the delegation, select **New**.

5.  Fill in the form.

<table id="table_klq_cg2_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

Logged in user \(delegator\) who delegates service tasks to a delegate.

</td></tr><tr><td>

Starts

</td><td>

Date when service delegation begins. The default is the current date and time.

</td></tr><tr><td>

Delegate

</td><td>

User you want to delegate tasks to.**Note:** The default value is the logged in user. You need to change this to the user you are delegating tasks to.

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
</table>6.  Select **Save**.

    The **Delegation Rules** related list appears.

7.  Select **Edit** to assign delegation rules to a delegate.

    You can use condition filters to search for delegation rules.

8.  Select delegation rules under the **Collection** column you want to assign to a delegate and move them to the **Delegation Rules List** column.

9.  Select **Save**.

    The **Granular Delegate** form returns.


## Using granular delegation on ServiceNow mobile

You can use Granular Delegation to delegate tasks from ServiceNow® mobile.

To delegate your tasks using the ServiceNow® mobile:

-   Select your HR profile
-   Add a delegate
-   Add details of the delegation
-   Submit the delegation

For more information on the ServiceNow® mobile application, see [ServiceNow Mobile](https://www.servicenow.com/docs/access?context=mobile-config-navigation&version=zurich&pubname=zurich-mobile&ft:locale=en-US).

### Delegate tasks using the ServiceNow mobile

You can delegate tasks to other eligible users from the ServiceNow® mobile.

#### Before you begin

Role required: sn\_hr\_core.case\_writer

#### Procedure

1.  Navigate to the **All** &gt; **ServiceNow mobile home page**.

2.  Select the HR profile icon in the top, right corner.

    ![Granular Delegation Mobile - Home page](../image/gd-mobile-home.png)

3.  Select the edit icon \(![Edit icon](../image/esc-edit-button.png)\).

    ![Granular Delegation mobile - Add delegate](../image/gd-mobile-add-delegate.png)

4.  Select the **Add a Delegate** button.

5.  Fill in the form.

<table id="simpletable_dld_b2r_spb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delegate

</td><td>

Person authorized as a delegate.Select a person you want to delegate your duties to.

</td></tr><tr><td>

Start date

</td><td>

Date when the service delegation begins.

</td></tr><tr><td>

End date

</td><td>

Date when the service delegation ends.

</td></tr><tr><td>

Duties

</td><td>

The duties you want to delegate. A list of duties appears after you select **Duties**.Select the duties you want to delegate and a check mark appears next to the duty.

</td></tr></tbody>
</table>6.  Select **Submit**.

    Your Employee Profile appears. To see a list of people you have delegated tasks to, select the **Delegates** tab.


### View tasks delegated to you on the ServiceNow mobile

You can use the ServiceNow® mobile to view tasks delegated to you.

#### Before you begin

Role required: sn\_hr\_core.case\_writer

Notification of delegated tasks are sent to your email address if your HR profile contains that information. For more information, see [Use HR Profile](../../../human-resources/concept/c_HRProfileRecords.md).

**Note:** If your company uses Connect, you can choose what notifications you receive. For more information on notifications, see [Enable or disable Connect notifications globally](https://www.servicenow.com/docs/access?context=t_EnableDisableConnectNotifications&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

#### Procedure

1.  Navigate to the mobile **All** &gt; **Home** &gt; **My Tasks**.

    A list of tasks delegated to you appears.


