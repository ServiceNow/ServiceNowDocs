---
title: Post-authentication context
description: The Post Authentication policy context defines how and when a policy is enforced during the login process. The policy used in this context executes after your users see a login screen.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication policy contexts, Adaptive authentication, Authentication, Access Management]
---

# Post-authentication context

The Post Authentication policy context defines how and when a policy is enforced during the login process. The policy used in this context executes after your users see a login screen.

## Post-authentication context record

Policies in the post-authorization context execute after your users enter their credentials or SSO response. Your instance allows or denies access based on your selected policy. Because your users have identified themselves via their login credentials, the policy can use user information such as role or group to determine whether to grant access.

Use the fields in the Post-authentication policy context record to define how your instance uses your policy.

<table id="table_otz_ngr_2qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the policy context. This field is static and cannot be changed.

</td></tr><tr><td>

Description

</td><td>

Description of the context

</td></tr><tr><td>

Default Policy

</td><td>

Defines the default behavior of this context when evaluating the policy. Select from the following options.-   **Allow Policy**

Denies access to all users by default, and only allows access when the conditions the policy selected in the **Allow Policy** field evaluate to true.

-   **Deny Policy**

Allows access to all users by default, and only denies access when the conditions the policy selected in the **Deny Policy** field evaluate to true.


</td></tr><tr><td>

Allow Policy

</td><td>

The policy used for this context uses. This field appears only when the **Default Policy** field is set to **Allow Policy**.

</td></tr><tr><td>

Deny Policy

</td><td>

The policy used for this context uses. This field appears only when the **Default Policy** field is set to **Deny Policy**.

</td></tr></tbody>
</table>## Policy inputs and conditions

The **Policy Input** and **Policy Conditions** tabs display the inputs and conditions of the policy selected in the **Allow Policy** or **Deny Policy** field. These tabs serve as a reference, but cannot be used to change the policy inputs or conditions. To modify your policy settings, navigate to the policy using the reference icon \(![Reference icon](../images/reference-icon.png)\) next to the **Allow Policy** or **Deny Policy** field.

This example shows a post-authentication policy context record configured to deny access by default. The context uses a policy called **Deny access policy**. That policy has a set of inputs and conditions that are displayed in the **Policy Input** and **Policy Condition** tabs.

![Post-authentication policy context record](../images/pre-auth-context.png "Post-authentication policy context form")

