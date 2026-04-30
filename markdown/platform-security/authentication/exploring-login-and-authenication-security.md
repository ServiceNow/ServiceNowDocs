---
title: Exploring Login and authentication security
description: Configure login security options to control access to your instance.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Login and authentication security, Local Authentication, Authentication, Access Management]
---

# Exploring Login and authentication security

Configure login security options to control access to your instance.

## Security options

You can control several aspects of user login and authentication security:

<table id="table_nxm_qlz_k1b"><thead><tr><th>

Feature

</th><th>

Description

</th><th>

Related topics

</th></tr></thead><tbody><tr><td>

Log in and log out controls

</td><td>

Control several dimensions of the log in and log out process for users, such as specifying a landing page that the user sees upon login and control how users log out.

</td><td>

-   [Defining login scenarios](../../login/task/t_LoginScenarios.md)
-   [Configuring the logout confirmation prompt](../task/t_EnableTheLogoutConfirmPrompt.md)
-   [Installation exits](../../../script/server-scripting/reference/r_InstallationExits.md)
-   [Specify lockout for failed login attempts](../task/t_LockoutForFailedLogins.md)

</td></tr><tr><td>

Authentication security

</td><td>

Control the password reset process and features like the Remember Me option. You can also use IP address-based controls for access to the instance and implement a nonce to be used with single sign-on digest authentication.

</td><td>

-   [Configuring your password policy](../../../integrate/authentication/task/set-your-password-policy.md)
-   [Password Reset](c_SelfServicePasswordReset.md)
-   [Remember me](../../login/concept/c_ChSetRemMeChkbxCookie.md#)
-   [IP range based authentication](../../login/concept/c_IPRangeBasedAuthentication.md)
-   [Implementing a nonce](../../login/concept/c_ImplementingANonce.md)

</td></tr></tbody>
</table>