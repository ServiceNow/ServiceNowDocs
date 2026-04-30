---
title: Exploring Multi-factor authentication
description: Multi-factor Authentication \(MFA\) is an authentication method that requires users to provide information other than their basic credentials.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [MFA, Multi-factor authentication, multifactor auth, Multi-factor]
breadcrumb: [Multi-factor authentication, Authentication, Access Management]
---

# Exploring Multi-factor authentication

Multi-factor Authentication \(MFA\) is an authentication method that requires users to provide information other than their basic credentials.

MFA is a security process that require a user to provide two or more different verification factors to access a service or account. It adds an extra security layer of protection to your service beyond just a password, which makes harder for unauthorized individuals to gain access.

By requiring multiple factors, MFA significantly enhances security and helps protect against various cyber threats, including phishing and identity theft. Here's some insight about how MFA works:

-   First factor: User using their username and password for login.
-   Second factor: User is prompted for a second factor that’s with the user \(An identity verification method such as an authenticator app or security key\).

**Note:**

-   MFA is activated by default on ServiceNow.
-   MFA is enabled using **glide.authenticate.multifactor** property. If you wish to disable this property, you must provide a business justification about why you want to disable MFA.

![MFA screen](../images/new-mfa.png)

ServiceNow's MFA supports verification methods such as Authenticator App, Fast IDentity Online 2 \(FIDO2\), Passkey, and Time-based One-Time Password \(OTP\). Following are the details of available verification methods:

-   **Authenticator App**: Apps that generate unique, temporary verification codes. For example: Otka, Google Authenticator, Microsoft Authenticator, etc.
-   **FIDO2**: Physical devices that use public-key cryptography to validate user identities. For example: Hardware Keys \(YubiKey\), Biometric scanners \(Apple's Touch ID\).
-   **Passkey**: Log in with a passkey by unlocking the device with a biometric sensor, PIN, or pattern.
-   **OTP**: Secret key and the current time to generate a unique password that is only valid for a short period of time. For example: SMS \(OTP\) and Email \(OTP\).

You can use MFA along with the following:

-   Local Database Authentication \(native ServiceNow authentication\) or [LDAP integration](../../ldap/concept/c_LDAPIntegration.md)
-   SSO SAML or SSO OIDC. For more information, see [Multi-Provider Single sign-on \(SSO\)](../../single-sign-on/concept/c_MultipleProviderSingleSignOn.md).

**Related topics**  


[MFA verification methods](mfa-methods.md)

[Multi-factor authentication system properties](../reference/mfa-properties.md)

