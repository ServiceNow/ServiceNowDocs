---
title: MFA \(Multi-Factor Authentication\) context
description: The MFA \(Multi-Factor Authentication\) policy context uses a policy to define how and when MFA is enforced during the login process.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Authentication policy contexts, Adaptive authentication, Authentication, Access Management]
---

# MFA \(Multi-Factor Authentication\) context

The MFA \(Multi-Factor Authentication\) policy context uses a policy to define how and when MFA is enforced during the login process.

## MFA context record

The MFA \(Multi-Factor Authentication\) policy context defines whether your users must provide a second form of authentication when logging in. This context does not deny access to your instance as the post-authentication and pre-authentication policies. The policy you select in this context takes precedence over user or role-based configurations for multi-factor authentication.

To access the MFA context, navigate to **All** &gt; **Multi-factor Authentication** &gt; **MFA Context**.

Use the fields in the Post-authentication policy context record to define how your instance uses your policy.

**Note:**

-   If the default policy is **Step-Up MFA Policy**, users will be shown with Multi-factor Authentication if policy configured in **Step-Up MFA Policy** evaluates to true. Policy takes precedence over the user or role based configuration.
-   MFA with SSO login will only be available if `glide.authenticate.mfa.with.multisso.enabled` Property is set to true.
-   You can navigate to the Authentication Policy record to Add or Edit the 'Policy Input\(s\)' to the referenced Policy field \(**Step-Up MFA Policy** or **Step-Down MFA Policy**\).

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

Defines the default behavior of this context when evaluating the policy. Select from the following options.-   **Step-Up MFA Policy**

Enforces MFA to users when the policy conditions defined in the **Step-Up MFA Policy** field evaluate to true.

-   **Step-Down MFA Policy**

Enforces MFA by default. MFA is not enforced only when the policy conditions defined in the **Step-Down MFA Policy** field evaluate to true.


</td></tr><tr><td>

Step-Up MFA Policy

</td><td>

The policy used for this context uses. This field appears only when the **Default Policy** field is set to **Step-Up MFA Policy**.

</td></tr><tr><td>

Step-Down MFA Policy

</td><td>

The policy used for this context uses. This field appears only when the **Default Policy** field is set to **Step-Down MFA Policy**.

</td></tr></tbody>
</table>## Policy inputs and conditions

The **Policy Input** and **Policy Conditions** tabs display the inputs and conditions of the policy selected in the **Step-Up MFA Policy** or **Step-Down MFA Policy** field. These tabs serve as a reference, but cannot be used to change the policy inputs or conditions. To modify your policy settings, navigate to the policy using the reference icon \(![Reference icon](../images/reference-icon.png)\) next to the **Step-Up MFA Policy** or **Step-Down MFA Policy** field.

**Note:** Policy conditions can be created from here, but as a good practise it is recommended to add new policy conditions from policy page.

This example shows an MFA context record configured using a step-up MFA policy. This default policy means that MFA is enforced only when the conditions defined in the policy evaluate to true. The context uses a policy called **Step-Up MFA policy**. That policy has a set of inputs and conditions that are displayed in the **Policy Input** and **Policy Condition** tabs.

![MFA policy context record](../images/mfa-auth-context.png "MFA policy context form")

