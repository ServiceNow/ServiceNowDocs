---
title: Add an authentication policy to an authentication policy context
description: Add an authentication policy to one of the authentication policy contexts. The authentication context uses the policy inputs and conditions to determine whether uses are granted access to the instance, or whether MFA is enforced for your users.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication policies, Adaptive authentication, Authentication, Access Management]
---

# Add an authentication policy to an authentication policy context

Add an authentication policy to one of the authentication policy contexts. The authentication context uses the policy inputs and conditions to determine whether uses are granted access to the instance, or whether MFA is enforced for your users.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Auth Policy Contexts**, and select one of the entries depending on your needs.

    -   **Pre Authentication Context**

        Use the pre-authorization context to evaluate your policy before the user sees the login screen. Users are granted or denied access based on this evaluation.

    -   **Post Authentication Context**

        Use the post-authorization context to evaluate your policy after the user enters their login credentials. Users are granted or denied access based on this evaluation. Because this evaluation takes place after the instance identifies the user, policies in this context can make their evaluation based on user data, such as their role or group.

    -   **MFA Context**

        Use the MFA context to determine whether a user must use multi-factor authentication when logging in.

    -   **Session Validation Context**

        Use the session validation context to evaluate the IP-Address that are set based on the conditions defined as a filter and allows access to the instance within a session.

2.  In the **Default Policy** field, select a value.

    The value in this field determines how the context uses the outcome of your policy's conditions.

    The available options in this field depend on the selected context. For details on these contexts, see [Authentication policy contexts](../concept/auth-policy-contexts.md).

3.  Assign a policy to the context.

    The name of the field depends on which context you have selected.

    -   **Pre-authentication and Post-authentication context**

        These contexts have a **Deny Policy** or **Allow Policy** field, depending on the selection in the **Default Policy** field.

    -   **MFA context**

        This context has a **Step-Up MFA Policy** or **Step-Down MFA Policy** field, depending on the selection in the **Default Policy** field.

    -   **Session validation context**

        This context has a **Allow Policy** or **Deny Policy** field, depending on the selection in the **Default Policy** field.

4.  Click **Update**.

    After updating the record, you can see your policy's inputs and conditions in the **Policy Input** and **Policy Conditions** tabs.


