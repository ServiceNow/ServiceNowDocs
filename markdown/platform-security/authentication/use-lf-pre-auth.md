---
title: Use Location Filter in Pre Authentication Context
description: Use the location filter criteria created in the Pre Authentication Context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/use-lf-pre-auth.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Use Location Filter criteria, Location filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Use Location Filter in Pre Authentication Context

Use the location filter criteria created in the Pre Authentication Context.

## Before you begin

Role required: adaptive\_auth\_admin

Plugin required: **Zero Trust - Location Based Access** \(`com.snc.zero_trust_location_access`\).

A Location Filter with the countries that you want to restrict access to the users based on the location must be created. For more information, see [Create location filter criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/create-location-filter-criteria.md).

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Auth Policy Context** &gt; **Pre Authentication Context**.

    When a policy is chosen in the pre authentication policy context:

    -   Selecting the Deny access policy as the default policy allows the access to all users by default and only denies access when the policy conditions defined in the deny access policy evaluate to true.
    -   Selecting the Allow access policy as the default policy denies the access to all users by default and only allows access when the policy conditions defined in the allow access policy evaluate to true.
    The example shows how you can restrict the logins from the specified locations. You can choose the Deny Access and the associated policy \(Deny Access\) as the Pre Authentication policy and specify the policy inputs and conditions.

    \[Omitted image "deny-policy-location.png"\] Alt text: Deny Policy Location

2.  Select the information icon and then select **Open Record** to open the **Deny Policy** record.

    **Note:** The example described in this task is **Deny Policy**. You can also use **Allow Policy** and set the conditions accordingly to control the logins.

3.  In the Deny Access Policy, under the Policy Inputs section, select **New**.

    \[Omitted image "deny-policy-location-filter.png"\] Alt text: Deny Access Policy

4.  Add the Location Filter input and **Save**.

    For example, APAC Region.

    \[Omitted image "location-filter-criteria-input.png"\] Alt text: APAC Region Filter

    The filter is added as **Policy Inputs**.

5.  Select the Policy Conditions tab and select **New**.

6.  In the Conditions page, provide the label, conditions, and set it to true.

    \[Omitted image "condition-location-filter.png"\] Alt text: Condition

    **Note:**

    -   In this example, the selection of true as a condition implies that the user logging from the configured regions won’t be able to log in to the instance.
    -   If the condition is set to false, then only users from configured regions can log in to the instance and the other users won’t be able to log in to the instance.
7.  Select **Submit**.

    The users selecting the instance link and logging from the configured countries are displayed an error message about the access denial \(error message configured by their administrators on the policy properties page\).


