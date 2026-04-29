---
title: Tutorial: Configuring session validation
description: Configure session validation within the Adaptive Authentication framework to provide as an additional layer of protection for session or cookie hijacking.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Session validation context, Authentication policy contexts, Adaptive authentication, Authentication, Access Management]
---

# Tutorial: Configuring session validation

Configure session validation within the Adaptive Authentication framework to provide as an additional layer of protection for session or cookie hijacking.

## Before you begin

Role required: adaptive\_auth\_admin

Plugin required: **Adaptive Authentication** \(com.snc.adaptive\_authentication\)

To configure Session Validation, you must perform the following steps:

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **All Policies**.

2.  Select the **Session Validation Policy** in the Policies \(`sys_authentication_policy_list.do`\) page.

3.  Select **Policy Inputs**.

    1.  Select **New** or **Edit**.

    2.  Choose the kind of Policy Input \(Filter Criteria\) that you want to create.

        Available options are IP, Role, and Group Filter Criteria. Let's choose **IP Filter Criteria**.![IP Filter Criteria](../images/use-ip-session-context-filter.png)

    3.  Fill the form with the filter details and provide the **IP Range**.

        ![IP Filter Criteria](../images/ip-range-session-context.png)

        To learn more about how to create an IP Filter, see [Create IP filter criteria](create-ip-filter-criteria.md).

    4.  Select **Submit**.

4.  Select **Policy Conditions** on the Session Validation Policy page.

    1.  Select **New**.

    2.  Fill the form and set the Condition for the Policy Input.

        **Note:** You can set the conditions to `true` or `false` based on the configuration of the policy input. In this example, it is set to `true`. Setting the condition to true in this case allows only the user with the configured IP address to log in.

        ![Condition](../images/condition-session-context.png)

5.  Select the `Active` check box to activate the policy after the Session Validation Policy is set up with policy inputs and conditions.

    ![Activate Session Context](../images/activate-session-context.png)

6.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **Properties** and enable the Session Validation property.

    ![Session Validation property](../images/session-context.png)

7.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Auth Policy Contexts** &gt; **Session Validation Context**.

8.  Set the Default Policy to **Allow Policy** or **Deny Policy** to set the session validation context according to the policy input and policy conditions.

    **Note:** By default:

    -   The Session Validation context is set to **Allow Policy**.
    -   Allow Policy is selected as **Session Validation Policy**.
    -   The Session Validation Context for an authentication policy can only be with **Allow Policy**.
    ![Policy Context](../images/policy-session-context.png)


## Result

The configuration evaluates the login session based on the following:

-   Restricts access to the ServiceNow® instance when hijackers copy a user's session cookies from one device to another to impersonate a session.
-   Restricts the user's session access if they're using an insecure network.

