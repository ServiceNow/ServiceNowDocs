---
title: Use Location Filter Post Authentication Context
description: Use the location filter criteria created in the Post Authentication Context.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Tutorial: Use Location Filter criteria, Location Filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Use Location Filter Post Authentication Context

Use the location filter criteria created in the Post Authentication Context.

## Before you begin

Role required: adaptive\_auth\_admin

Plugin required: **Zero Trust - Location Based Access** \(`com.snc.zero_trust_location_access`\).

Create a Location Filter with the countries that you want restrict access to the users based on the location. For more information, see [Create Location filter criteria](create-location-filter-criteria.md).

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Auth Policy Context** &gt; **Post Authentication Context**.

    When a policy is chosen in the post authentication policy context:

    -   Selecting the Deny access policy as the default policy allows the access to all users by default and only denies access when the policy conditions defined in the deny access policy evaluate to true.
    -   Selecting the Allow access policy as the default policy denies the access to all users by default and only allows access when the policy conditions defined in the allow access policy evaluates to true.
    The example shows on how you can configure a `itil` users with a condition to only access the instance from the specified location \(US\). And the `itil` users can’t log in from other countries.

    After users providing their credentials on the login page. You can choose the Allow Access and the associated policy \(Allow Access\) as the Post Authentication policy and specify the policy inputs and conditions.

2.  Select the information icon and then select **Open Record** to open the **Allow Policy** record.

    **Note:** The example described in this task is **Allow Policy**. You can also use **Deny Policy** and set the conditions accordingly to control the log in.

3.  In the Allow Access Policy, under the Policy Inputs section, select **New**.

    ![Add Post auth](../images/edit-post-auth.png)

4.  Add the Role Filter criteria and Location Filter criteria.

    1.  Adding Role Filter criteria:

        -   Create Role Filter Input as `itil`.![Itil Post Auth](../images/itil-post-auth.png)
        -   Create Role Filter Condition and set it to `true`.![Role condition](../images/itil-post-auth-condition.png)
        For more information on how to create role filter criteria, see [Create role filter criteria](create-role-filter-criteria.md).

    2.  Adding Location Filter criteria:

        -   Create Location Filter Input. Add United States in the Locations.![Ading Location](../images/itil-post-auth-US.png)
        -   Create Location Filter Condition and set it to `true`.![Location Filter Condition](../images/itil-post-auth-US-condition.png)
        For more information on how to create role filter criteria, see [Create Location filter criteria](create-location-filter-criteria.md).

        The Allow Access Policy shows the Policy Inputs and Conditions that are created in the previous steps:

        -   Policy Inputs: itil, itil user from US
        -   Policy Conditions: itil user login, itil user from US condition.
        ![Policy Input and Conditions](../images/post-auth-policy-condition.png)

        **Note:**

        -   In this example, the selection of true as a condition implies that the `itil` users logging from the configured country \(US\) are able to log in to the instance.
        -   If the condition is set to false, then the `itil` users from the configured country \(US\) won’t be able to log in to the instance and the other users won’t be able to log in to the instance.
5.  Select **Submit** or **Update** to update the Post Authentication Context.

    The `itil` users selecting the instance link, specifying their credential and then logging outside the configured country \(US\) is displayed an error message about the access denial \(error message configured by their administrators on the policy properties page\).


