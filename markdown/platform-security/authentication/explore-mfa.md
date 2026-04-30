---
title: Exploring Multi-factor authentication
description: Multi-factor Authentication \(MFA\) is an authentication method that requires users to provide information other than their basic credentials.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Exploring Multi-factor authentication

Multi-factor Authentication \(MFA\) is an authentication method that requires users to provide information other than their basic credentials.

ServiceNow provides MFA options such as setting up an authenticator app, biometric, passkey or hardware security key, SMS and email for authentication. You can use FIDO2 authenticator, passkeys, biometric authenticators, and hardware security keys as Multi-factor Authentication \(MFA\) factor without requiring an authenticator app setup.

![MFA screen](../images/new-mfa.png)

If the user has completed the setup using any one factor, they can still go to their profile page and complete the remaining factors setup.

## Activate MFA

Activate the **Integration - Multifactor Authentication** \(com.snc.integration.multifactor.authentication\) plugin to begin using MFA on an instance. MFA is activated by default on ServiceNow.

## Multi-factor criteria

Use multi-factor criteria to determine which users and roles must use two-step multi-factor verification. You can use one of these criteria or a combination of them to suit your business needs.

-   **User-based multi-factor criteria**

    Use user-based multi-factor criteria to select individual users who are required to log in using MFA. Administrators update the **Enable Multifactor Authentication** field on a user record to enable or disable MFA requirements for a user. For details on this process, see [Configure user-based multi-factor criteria](../task/t_RequireMultifactorAuthForAUser.md).

-   **Role-based multi-factor criteria**

    Use role-based multi-factor criteria to require MFA login for all users assigned to a specific role. The **Role-based multi-factor authentication** record on the **Multi-factor Criteria** \[multi\_factor\_criteria\] table contains the list of roles that require an MFA login. For details on maintaining this list, see [Configure role-based multi-factor criteria](../task/mfa-role-criteria.md).

-   **Adaptive authentication policy-based multi-factor criteria**

    Use adaptive authentication to determine when your instance requires MFA. Adaptive authentication uses authentication policies to evaluate criteria like a user's IP address or user groups. For details on the adaptive authentication feature, see [Adaptive authentication](adaptive-authentication.md).


## Multi-factor authentication methods

The users can use the following options in addition to their user name and password to fulfill multi-factor authentication requirements. The users can setup MFA factors such as Authenticator applications, Biometric scanners, Hardware Keys, and SMS independently.

<table id="table_bhf_4bw_ypb"><tbody><tr><td>

Authenticator applications

 An authenticator application is third-party software that generates temporary passcodes. Users can use these passcodes along with their password to log in into an instance that requires multi-factor authentication \(MFA\). For more detail on these applications, see [Authenticator Applications](mfa-auth-app.md).

 Follow the instructions on the screen to set-up the authenticator application.

</td><td>

![Authenticator](../images/auth-app.png)

</td></tr><tr><td>

Biometric scanners

 Biometric authenticators use fingerprint or facial recognition to identify users. Your users can use these authenticators on their devices as part of the multi-factor login process. For details on registering biometric authenticators, see [Register a biometric authenticator](../task/mfa-setup-bio-auth.md).

</td><td>

![Biometrics icon](../images/biometric-2.png)

</td></tr><tr><td>

Hardware Keys

 Hardware keys are physical hardware that you can use to authenticate. Hardware keys are inserted into a port on your device to provide authentication. For details on registering hardware keys, see [Register a hardware security key](../task/mfa-setup-hardware-key-auth.md).

</td><td>

![Hardware key icon](../images/hardware-key.png)

</td></tr><tr><td>

SMS

 Admin can configure ServiceNow instance to require users who attempt to log in to the instance using SMS based OTP.

 When users attempt to log in to ServiceNow, SMS OTP is sent to the mobile number associated with the sys\_user record. Users can enter the six-digit verification code that it sent to the mobile device and verify their identity.

 For more information, see [Multi-factor authentication with SMS](mfa-with-sms.md).

</td><td>

![SMS](../images/sms.png)

</td></tr><tr><td>

Email

 Admin can configure ServiceNow instance to require users who attempt to log in to the instance using Email based OTP.

 When users attempt to log in to ServiceNow, Email OTP is sent to the email address of the user. Users can enter the six-digit verification code that it sent to the email address and verify their identity.

 For more information, see [Multi-factor authentication with Email](mfa-with-email.md).

</td><td>

![Email](../images/email.png)

</td></tr></tbody>
</table>## Multi-factor authentication properties

Use multi-factor authentication properties to enable, disable, and configure MFA on your instance. For details on these properties, see [Multi-factor authentication system properties](../reference/mfa-properties.md).

