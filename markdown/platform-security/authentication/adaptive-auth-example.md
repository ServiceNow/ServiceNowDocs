---
title: Tutorial: Configure adaptive authentication
description: Use these example steps to configure adaptive authentication on an instance.Learn how to create a criteria record to use as a policy input for your adaptive authentication policy.Learn how to create a policy to deny access to user groups defined in your group filter criteria.Configure the Post Authentication Policy Context to use your new policy. When configured, your instance denies access to users within the group defined in the filter criteria record.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure adaptive authentication properties, Adaptive authentication, Authentication, Access Management]
---

# Tutorial: Configure adaptive authentication

Use these example steps to configure adaptive authentication on an instance.

To use this tutorial, you must have an instance with Adaptive Authentication activated. For details on this process, see [Activate adaptive authentication](../task/adaptive-authentication-plugin.md).

The example guides you through creating a new policy and applying it to an instance. In this tutorial you will:

-   **Create a filter criteria record**

    Create a group filter criteria record to use as an input for your policy. This record allows your policy to determine access based on a user's group. In these steps you define the group or groups the policy uses to determine access.

-   **Create a policy**

    Create a policy that determines whether a user can access the instance. This policy uses the group filter criteria record you create as an input. In these steps you also define policy conditions that define how the policy uses the policy input to determine user access.

-   **Configure a policy context**

    Configure the **Post Authentication Policy Context** to use your new policy. When configured, your instance denies access to users within the group defined in the filter criteria record.


## Create a filter criteria record

Learn how to create a criteria record to use as a policy input for your adaptive authentication policy.

### Before you begin

Role required: admin

To deny access to your instance based on user groups, you must create a group filter criteria record. This record defines a user group or a set of user groups that your policy can grant or deny access. In this example, you will create a group filter criteria record for a single user group.

For details on user groups and how they are used in your instance, see [Exploring user administration](https://www.servicenow.com/docs/access?context=exploring-user-administration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Filter Criteria** &gt; **Group Criteria**.

2.  Click **New** to create a new record.

3.  In the **Name** field, enter a name for your record.

    For example, `Denied Groups`.

4.  In the **Description** field, enter a brief description.

    For example, `User groups denied access to the instance`.

5.  In the **Groups for criteria** list, double-click **Insert a new row...**.

6.  Enter the name of a user group, or click the reference icon \(![Reference icon](../images/search.png)\) to select a group from a list.

    If you want to create a new user group for your filter criteria, click the reference icon \(![Reference icon](../images/search.png)\), and then click the **New** button. For more details on creating user groups, see [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

7.  After you have added your user group, click **Submit** to save your criteria record.

    ![Completed group filter criteria record.](../images/adaptive-auth-example-1.png)


## Create a policy

Learn how to create a policy to deny access to user groups defined in your group filter criteria.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **All Policies**.

2.  In the **Policies** list, click **New**.

3.  In the **Name** field, enter a name for your record.

    For example, `Deny by Group`.

4.  In the **Description** field, enter a brief description.

    For example, `User groups denied access to the instance`.

5.  Right-click the form header and click **Save**.

    After saving, the **Policy Inputs** and **Policy Conditions** lists display on the form.

6.  In the **Policy Inputs** list, click **Edit**.

7.  In the list collector, add the filter criteria created in the previous steps to your policy.

    ![List collector with a selected filter criteria record](../images/policy_filter-add.png)

8.  Click **Save**.

    The instance saves the policy input and displays the policy record displays again.

9.  In the **Policy Conditions** list, click **New**.

10. In the **Label** field, create a label for this condition, for example `Deny by group`.

11. In the **Description** field, enter a brief description.

    For example, `Deny access to users in Denied Groups`.

12. In the **Condition** field, select the filter criteria you created in previous steps, then select **is**, and **true** to complete the condition.

    ![Completed policy condition record](../images/policy-condition-complete.png)

13. Click **Save**.


## Configure a policy context

Configure the Post Authentication Policy Context to use your new policy. When configured, your instance denies access to users within the group defined in the filter criteria record.

### Before you begin

Role required: admin

### Procedure

1.  **Adaptive Authentication** &gt; **Auth Policy Contexts** &gt; **Post Authentication Context**.

    You must use the **Post Authentication Context** because the policy used in this tutorial must evaluate what group a user is in. This information is only available after enters their credentials.

2.  In the **Default Policy** field, select `Deny Policy`.

    This selection grants access to users by default, and only denies access when the policy conditions evaluate to true.

3.  In the **Deny Policy** field, select the policy you created the previous steps.

4.  Click **Update** to save the policy context record.


