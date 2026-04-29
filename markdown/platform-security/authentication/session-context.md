---
title: Session validation context
description: Use the Session Validation Context as an additional layer of protection against session or cookie hijacking.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Authentication policy contexts, Adaptive authentication, Authentication, Access Management]
---

# Session validation context

Use the Session Validation Context as an additional layer of protection against session or cookie hijacking.

You can use the Session Validation Context with the [Adaptive authentication](adaptive-authentication.md) policy framework. The framework uses authentication policies to evaluate authentication requests and then either denies or allows access based on policy inputs and conditions.

The Session Validation Context policy can be used in conjunction with post auth policy, where an admin can enforce IP restrictions to certain or all users during the logged in session.

The Session Validation Context feature evaluates the IP-addresses based on the conditions you set and allows access to the instance within a session. The Session Validation Context outcome is set based on selecting **Allow Policy** as this policy terminates the user session immediately unless one of the policy conditions defined in the allow access policy evaluates to true.

**Note:** The Session Validation Context for an authentication policy can only be with **Allow Policy**.

The Session Validation Context works based on the following mechanism:

-   Captures the user's IP address on session creation from user request and stores it in the session and database.
-   Rejects a request when its IP address differs from that in the session or outside of the customer defined valid IP ranges you defined.

**Note:** The Session Validation Context is:

-   Available only for authenticated users.
-   Not applicable for guest user sessions or native mobile apps.
-   Optional and based on the requirement that it can be configured.
-   Executed only for the post-login requests.

## Benefits of Session Validation

The Session Validation Context has the following benefits:

-   Restricts access to ServiceNow® when hijackers copy a user's session cookies from one device to another to impersonate the session.
-   Restricts the user's session access if they're using an insecure network.
-   Configures the various rules and IP ranges by user group or role for user logins.

## Session Validation context record

Policies in the session validation context execute post-login requests.

Use the fields in the session validation policy context record to define how your instance uses your policy.

<table id="table_otz_ngr_2qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the policy context. This field is static and can’t be changed.

</td></tr><tr><td>

Description

</td><td>

Description of the context.

</td></tr><tr><td>

Default Policy

</td><td>

Defines the default behavior of this context when evaluating the policy. Select from the following options.-   **Allow Policy**

Denies access to all users by default, and only allows access when the conditions in the **Allow Policy** field evaluate to true.

-   **Deny Policy**

Allows access to all users by default, and only denies access when the conditions in the **Deny Policy** field evaluate to true.


</td></tr><tr><td>

Allow Policy

</td><td>

The policy used for this context. This field appears only when the **Default Policy** field is set to **Allow Policy**.

</td></tr><tr><td>

Deny Policy

</td><td>

The policy used for this context. This field appears only when the **Default Policy** field is set to **Deny Policy**.

</td></tr></tbody>
</table>You can choose the **Session Validation Policy** as Allow Policy or Deny Policy based on the policy input and policy conditions.

**Note:** You can only use the IP, Role, and Group filter criteria for Session Validation policy.

## Policy inputs and conditions

The **Policy Input** and **Policy Conditions** tabs display the inputs and conditions of the policy selected in the **Allow Policy** or **Deny Policy** field. These tabs serve as a reference; but they can’t be used to change the policy inputs or conditions. To modify your policy, navigate to the policy using the reference icon next to the **Allow Policy** or **Deny Policy** field.

