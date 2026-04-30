---
title: Configure an authentication policy
description: Configure an authentication policy to define inputs and conditions to used to grant access to an instance or enforce multi-factor authentication.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication policies, Adaptive authentication, Authentication, Access Management]
---

# Configure an authentication policy

Configure an authentication policy to define inputs and conditions to used to grant access to an instance or enforce multi-factor authentication.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **All Policies**.

    **Note:** To see examples of completed policies, you can review these policies on your instance:

    -   DEMO POLICY - Allow Local Login for Admins from the Trusted IP Range only
    -   DEMO POLICY - Allow Local Login for Admins only
    -   DEMO POLICY - Restrict Username and Password based Authentication for specific users
2.  Click the **New** button to create a new policy record.

3.  In the **Policy** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of your policy.|
    |Application|The scoped application for the policy. This field is filled automatically with the current application.|
    |Description|Description of the policy|
    |Active|Whether the policy is active.|

4.  From the **Policy Inputs** tab, click **Edit**.

5.  Select one or more filter criteria from the **Collection** list and move them to **Policy Inputs List** of **Allow Access Policy** list.

    ![sample filter criteria for allow access policy](../images/filter-criteria-allow-access-policy.png)

    **Note:** For information on creating your own filter criteria to use in this section, see [Filter criteria](../concept/adaptive-auth-filter-criteria.md).

6.  From the **Policy Conditions** tab, click **New**.

7.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Label|Name to identify the condition.|
    |Description|Description of the condition.|
    |Condition|Logical combination of multiple policy inputs \(filter criteria\) that is used to evaluate authentication requests. For example, you can create conditions that allow only contractors from a list of trusted IP addresses.|

8.  Repeat step 7 to create additional policy conditions.

    **Note:** If you create multiple policy conditions, the final output of the access policy depends on the logical OR output of the all policy conditions. This means the policy will evaluate to true if any one of your policy conditions is met.

9.  Click **Save**.


