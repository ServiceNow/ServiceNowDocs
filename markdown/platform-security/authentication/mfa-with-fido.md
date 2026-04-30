---
title: FIDO2 as an MFA factor
description: You can configure FIDO2 as an MFA factor policy to enforce MFA for yours.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [MFA factor policies, MFA verification methods, Configure MFA, Multi-factor authentication, Authentication, Access Management]
---

# FIDO2 as an MFA factor

You can configure FIDO2 as an MFA factor policy to enforce MFA for yours.

FIDO2 is a password-less authentication standard that enables users to authenticate using a physical security key or biometric authentication. It provides a more secure alternative to traditional MFA methods, reducing the risk of phishing and other cyberattack.

The FIDO2 factor policy enhancement provides a secure authentication method to your multi-factor authentication \(MFA\) policies. You can configure FIDO2 as an MFA factor policy option, providing a higher level of security compared to traditional methods like Email and SMS.

![MFA- Biometric or Hardware keys](../images/biometirc-mfa.png)

You can configure FIDO2 factor policy and when the users satisfies the factor policy condition, the during log in to ServiceNow, FIDO2 setup is displayed for the users who haven't already added registered Hardware key or Biometric on their profile.

If the registration is completed, then second factor validation screen is displayed to log in.

**Note:** FIDO2 can also be self-enrolled by the users. To know more about how to self-enroll, see [Set up Multi-factor authentication on your user profile](../task/mfa-setup-profile.md).

## Key Benefits

The following are some of the key benefits of using FIDO2 as an MFA factor:

-   **Exclusive FIDO2 Authentication**

    Ensure high-privilege accounts can only authenticate using FIDO2's strong authentication capabilities \(biometrics, passkeys, or hardware security keys\).

-   **Exclusion of less secure methods**

    Suppress other authentication methods when FIDO2 is the only matching policy.

-   **Forced enrollment**

    Require users to register a FIDO2 key if not already enrolled.

-   **Granular control**

    Apply strict enforcement to specific roles or groups using policy-based targeting.


As a higher-security factor, FIDO2 has exclusive enforcement capabilities. When it's the only matching policy for a user:

-   Overrides other enroll-enrolled factors.
-   Forces FIDO2 registration, if the user isn’t enrolled.
-   Becomes the exclusive authentication option.

## Example Configurations and User Behaviors

The following table illustrates how different user scenarios are handled based on their roles and enrolled factors.

Example Factor Policy Conditions:

-   **FIDO2 Factory Policy**: Condition is "ITIL role should be true".
-   **EMAIL Factor Policy**: Condition is "ASSET role should be true".

<table id="table_pvx_pgx_bgc"><thead><tr><th>

Example user

</th><th>

Has roles

</th><th>

Already enrolled factors

</th><th>

Matching policies

</th><th>

Behavior

</th></tr></thead><tbody><tr><td>

andrew.och

</td><td>

**ITIL**

</td><td>

None

</td><td>

FIDO2

</td><td>

User is redirected to MFA setup with FIDO2 only. After registration, FIDO2 is the only authentication option.

</td></tr><tr><td>

abel.tuter

</td><td>

**ITIL**

</td><td>

Authenticator

</td><td>

FIDO2

</td><td>

User is redirected to MFA setup with FIDO2 only, even if the user has Authenticator as self-enrolled factor.**Note:** If the user hasn't registered to any MFA factor, then the user is redirected to MFA setup with FIDO2.

</td></tr><tr><td>

aileen.motterm

</td><td>

**ASSET**

</td><td>

Authenticator

</td><td>

Email

</td><td>

Sees Email and Authenticator options during log in. The user can choose either factor or optionally register FIDO2.

</td></tr><tr><td>

abraham.lincoln

</td><td>

**ASSET**, **ITIL**

</td><td>

Authenticator

</td><td>

Email and FIDO2

</td><td>

Sees Email and Authenticator option during log in. The user can register FIDO2 during validation. After registration, the user can see all the 3 factors.

</td></tr></tbody>
</table>By configuring FIDO2 as an MFA factor policy, you can significantly enhance the security of your authentication processes.

