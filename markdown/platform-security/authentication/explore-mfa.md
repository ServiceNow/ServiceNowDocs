---
title: Exploring Multi-factor Authentication
description: Multi-factor Authentication \(MFA\) is an authentication method that requires users to provide information other than their basic credentials.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [MFA, multi-factor authentication, multi-factor auth, multi-factor]
breadcrumb: [Multi-factor authentication, Authentication, Access Management]
---

# Exploring Multi-factor Authentication

Multi-factor Authentication \(MFA\) is an authentication method that requires users to provide information other than their basic credentials.

MFA is a security process that requires a user to provide two or more different verification factors to access a service or account. It adds an extra security layer of protection to your service beyond just a password, which makes it harder for unauthorized individuals to gain access.

By requiring multiple factors, MFA significantly enhances security and helps protect against various cyberthreats, including phishing and identity theft. Here's some insight about how MFA works:

-   **First factor**: The user using their user name and password for login.
-   **Second factor**: The user is prompted for a second factor that’s with the user \(An identity verification method such as an authenticator app or security key\).

Further, these factors can be typically categorized into secured and less-secured based on their level of protection against common security threats.

-   Secured Factors:
    -   FIDO \(Fast Identity Online\): This factor uses hardware tokens or biometric authentication methods, providing a high level of security by confirming that the user has a physical device or unique biometric trait to verify their identity.
    -   **TOTP \(Time-Based One-time Password\):** This factor generates a one-time password that is valid for a short period, usually 30 seconds. It’s typically delivered through a mobile app, adding an extra layer of security by requiring the user to have access to a specific device and app.
-   Less-Secured Factors:
    -   **EMAIL:** This factor sends a verification code or link to the user's email address. While convenient, it’s less secure because email accounts can be compromised.
    -   **SMS:** This factor sends a verification code via text message to the user's phone number. It’s also less secure due to the potential for SIM swapping and other mobile phone vulnerabilities.

To enhance security, it’s recommended to prioritize the use of secured factors like FIDO and TOTP over less-secured factors like EMAIL and SMS.

**Note:**

-   MFA is activated by default on ServiceNow.
-   MFA is enabled using **glide.authenticate.multifactor** property. If you want to disable this property, you must provide a business justification about why you want to disable MFA.

![MFA screen](../images/new-mfa.png)

ServiceNow's MFA supports verification methods such as Authenticator App, Fast IDentity Online 2 \(FIDO2\), Passkey, and time-based One-time Password \(OTP\). Following are the details of available verification methods:

-   **Authenticator App**: Apps that generate unique, temporary verification codes. For example: Okta, Google Authenticator, Microsoft Authenticator, and so on
-   **FIDO2**: Physical devices that use public-key cryptography to validate user identities. For example: Hardware Keys \(YubiKey\), Biometric scanners \(Apple's Touch ID\).
-   **Passkey**: Log in with a passkey by unlocking the device with a biometric sensor, PIN, or pattern.
-   **OTP**: The secret key and the current time to generate a unique password that is only valid for a short period. For example: SMS \(OTP\) and Email \(OTP\).

You can use MFA along with the following:

-   Local Database Authentication \(native ServiceNow authentication\) or [Lightweight Directory Access Protocol integration](../../ldap/concept/c_LDAPIntegration.md)
-   SSO SAML or SSO OIDC. For more information, see [Multi-Provider single sign-on \(SSO\)](../../single-sign-on/concept/c_MultipleProviderSingleSignOn.md).

**Related topics**  


[Multi-factor Authentication verification methods](mfa-methods.md)

[Multi-factor Authentication system properties](../reference/mfa-properties.md)

