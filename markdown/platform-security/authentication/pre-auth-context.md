---
title: Pre authentication context
description: The pre authentication policy context defines how and when a policy is enforced during the login process. The policy used in this context executes before your users see a login screen.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Authentication policy contexts, Adaptive authentication, Authentication, Access Management]
---

# Pre authentication context

The pre authentication policy context defines how and when a policy is enforced during the login process. The policy used in this context executes before your users see a login screen.

## Pre authentication context record

Policies in the pre authentication context execute when a user first accesses the instance, before they see a login screen.

You can use the pre authentication context to allow or deny access before your users are prompted for login credentials based on your selected policy. Because these policies evaluate before a user enters any information, those policies can’t take criteria such as a user's roles or groups into account.

Use the fields in the **Pre Authentication policy context** record to define how your instance uses your policy.

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
</table>**Note:**

You can only use the IP Filter, Trusted Mobile App Filter, and Location Filter criteria in the Pre Authentication Policy Context.

## Policy inputs and conditions

The **Policy Input** and **Policy Conditions** tabs display the inputs and conditions of the policy selected in the **Allow Policy** or **Deny Policy** field. These tabs serve as a reference, but can’t be used to change the policy inputs or conditions. To modify your policy, navigate to the policy using the reference icon \(![Reference icon](../images/reference-icon.png)\) next to the **Allow Policy** or **Deny Policy** field.

This example shows a pre authentication policy context record configured to deny access by default. The context uses a policy called **Deny access policy**. That policy has a set of inputs and conditions that are displayed in the **Policy Input** and **Policy Condition** tabs.

**Note:**

-   Only IP-Based filters, Location based filters, or Trusted Mobile App filter can be used in the pre authentication policy context.
-   Whenever there's a pre authentication set with non absolute conditions or filter criteria, you're displayed with an error message stating that the policy or context can’t be configured. It's recommended to validate all the inputs for the pre authentication context before executing it to the instance.

    For example: If the administrator is outside the trusted network and configures pre authentication context with IP ranges, if the IP ranges are mismatched with the current session of the admin, the admin is blocked.


![Pre-authentication policy context record](../images/pre-auth-context.png "Pre authentication policy context form")

