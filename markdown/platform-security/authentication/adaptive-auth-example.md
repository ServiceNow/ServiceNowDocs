---
title: Adaptive authentication configuration
description: Use these example steps to configure adaptive authentication on an instance.Create a criteria record to use as a policy input for your adaptive authentication policy.Create a policy to deny access to user groups defined in your group filter criteria.Configure the Post Authentication Policy Context to use your new policy. When configured, your instance denies access to users within the group defined in the filter criteria record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/adaptive-auth-example.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure properties, Adaptive authentication, Authentication, Access Management]
---

# Adaptive authentication configuration

Use these example steps to configure adaptive authentication on an instance.

To use this tutorial, you must have an instance with Adaptive Authentication activated. For details on this process, see [Activate adaptive authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/adaptive-authentication-plugin.md).

The example guides you through creating a new policy and applying it to an instance. In this tutorial you will:

-   **Create a filter criteria record**

    Create a group filter criteria record to use as an input for your policy. This record allows your policy to determine access based on a user's group. In these steps you define the group or groups the policy uses to determine access.

-   **Create a policy**

    Create a policy that determines whether a user can access the instance. This policy uses the group filter criteria record you create as an input. In these steps you also define policy conditions that define how the policy uses the policy input to determine user access.

-   **Configure a policy context**

    Configure the **Post Authentication Policy Context** to use your new policy. When configured, your instance denies access to users within the group defined in the filter criteria record.


## Create a filter criteria record

Create a criteria record to use as a policy input for your adaptive authentication policy.

### Before you begin

Role required: adaptive\_auth\_admin

To deny access to your instance based on user groups, you must create a group filter criteria record. This record defines a user group or a set of user groups that your policy can grant or deny access. In this example, you create a group filter criteria record for a single user group.

For details on user groups and how they are used in your instance, see [Exploring user administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/exploring-user-administration.md).

### Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Filter Criteria** &gt; **Group Criteria**.

2.  Select **New** to create a new record.

3.  In the **Name** field, enter a name for your record.

    For example, `Denied Groups`.

4.  In the **Description** field, enter a brief description.

    For example, `User groups denied access to the instance`.

5.  In the **Groups for criteria** list, double-click \(or use the keyboard shortcut\) **Insert a new row...**.

6.  Enter the name of a user group, or select the reference icon \(\[Omitted image "search.png"\] Alt text: Reference icon\) to select a group from a list.

    To create a new user group for your filter criteria, select the reference icon \(\[Omitted image "search.png"\] Alt text: Reference icon\), and then select the **New** button. For more details on creating user groups, see [Create a user group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAGroup.md).

7.  After you have added your user group, select **Submit** to save your criteria record.

    \[Omitted image "adaptive-auth-example-1.png"\] Alt text: Completed group filter criteria record.


## Create a policy

Create a policy to deny access to user groups defined in your group filter criteria.

### Before you begin

Role required: adaptive\_auth\_admin

### Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **All Policies**.

2.  In the **Policies** list, select **New**.

3.  In the **Name** field, enter a name for your record.

    For example, `Deny by Group`.

4.  In the **Description** field, enter a brief description.

    For example, `User groups denied access to the instance`.

5.  Select and hold \(or right-click\) the form header and select **Save**.

    After saving, the **Policy Inputs** and **Policy Conditions** lists display on the form.

6.  In the **Policy Inputs** list, select **Edit**.

7.  In the list collector, add the filter criteria created in the previous steps to your policy.

    \[Omitted image "policy\_filter-add.png"\] Alt text: List collector with a selected filter criteria record

8.  Select **Save**.

    The instance saves the policy input and the policy record displays again.

9.  In the **Policy Conditions** list, select **New**.

10. In the **Label** field, create a label for this condition, for example `Deny by group`.

11. In the **Description** field, enter a brief description.

    For example, `Deny access to users in Denied Groups`.

12. In the **Condition** field, select the filter criteria you created in the previous steps, then select **is**, and **true** to complete the condition.

    \[Omitted image "policy-condition-complete.png"\] Alt text: Completed policy condition record

13. Select **Save**.


## Configure a policy context

Configure the Post Authentication Policy Context to use your new policy. When configured, your instance denies access to users within the group defined in the filter criteria record.

### Before you begin

Role required: adaptive\_auth\_admin

### Procedure

1.  **Adaptive Authentication** &gt; **Auth Policy Contexts** &gt; **Post Authentication Context**.

    You must use the **Post Authentication Context** because the policy used in this tutorial must evaluate what group a user is in. This information is only available after the user enters their credentials.

2.  In the **Default Policy** field, select `Deny Policy`.

    This selection grants access to users by default, and only denies access when the policy conditions evaluate to true.

3.  In the **Deny Policy** field, select the policy you created in the previous steps.

4.  Select **Update** to save the policy context record.


