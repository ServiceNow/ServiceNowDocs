---
title: MFA types
description: FAQ related to MFA types and why it’s important.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Frequently asked questions, MFA enforcement, Multi-factor authentication, Authentication, Access Management]
---

# MFA types

FAQ related to MFA types and why it’s important.

1.  What are the types of verification methods that are available for MFA with ServiceNow?

    ServiceNow base system supports these verification methods.

    1.  Passkey
    2.  TOTP Authenticator apps such as Google Authenticator, Okta verify, Microsoft Authenticator, Authy, DUO
    3.  Biometric Authenticator \(FIDO2\) such as Windows Hello, Apple Touch ID, Face ID, android fingerprint sensor.
    4.  Hardware Security Keys \(FIDO2\) such as YubiKey, Thetis
    5.  Email One-time password \(OTP\)
    6.  SMS OTP - Multi-factor authentication with SMS com.snc.authentication.sms\_mfaplugin installation and factor configuration are required to enable SMS OTP-based MFA.
2.  Can a user configure multiple MFA factors or verification methods?

    Yes, you can enroll for multiple MFA factors by visiting their user profile. For example, you can enroll a laptop with biometric authenticator, use the mobile phone with a passkey, and have an authenticator app setup.

3.  What steps do users must perform to complete the MFA setup?

    User can perform either of the following MFA options.

    ![MFA screen](../images/new-mfa.png)

    Refer the [Multi-factor authentication](mfa-landing.md) documentation for more information about MFA setup.

4.  Can the SMS and Email OTP-based MFA limited to certain users?

    Admin can set up MFA factor policies for email and SMS OTP-based MFA factors to limit these factors to certain user groups or roles.

5.  The users don’t have a mobile phone where they can set up an authenticator app. How can these users enable MFA?

    From the Xanadu release onwards, you can use a Biometric authenticator, passkeys, FIDO2 hardware security keys, and email OTP-based MFA without requiring an authenticator app setup on the mobile phone.

6.  As an end user how to set up MFA?

    Refer the [Using Multi-factor authentication](mfa-use.md) documentation for more information about MFA setup.


