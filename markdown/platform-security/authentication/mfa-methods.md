---
title: MFA verification methods
description: ServiceNow's MFA supports verification methods such as Authenticator App, Fast IDentity Online 2 \(FIDO2\) and Time-based One-Time Password \(TOTP\).
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Multi-factor authentication, Multi-factor authentication, Authentication, Access Management]
---

# MFA verification methods

ServiceNow's MFA supports verification methods such as Authenticator App, Fast IDentity Online 2 \(FIDO2\) and Time-based One-Time Password \(TOTP\).

The users can use the following options in addition to their user name and password to fulfill multi-factor authentication requirements. The users can setup MFA factors such as Authenticator applications, Biometric scanners, Hardware Keys, and SMS independently.

## Authenticator Applications

An authenticator application is third-party software that generates temporary passcodes. Users can use these passcodes along with their password to log in into an instance that requires multi-factor authentication \(MFA\). For more detail on these applications, see [Authenticator Applications](mfa-auth-app.md).

![Authenticator](../images/auth-app.png)

## Hardware Keys and Biometric scanners \(Web Authentication\)

The **Integration - Web Authentication** \(com.snc.integration.webauthn\) plugin allows hardware key or biometric reader authentication on your instance.

Biometric authenticators use fingerprint or facial recognition to identify users. Your users can use these authenticators on their devices as part of the multi-factor login process. For details on registering biometric authenticators, see [Register a biometric authenticator](../task/mfa-setup-bio-auth.md).

![Biometrics icon](../images/biometric-2.png)

Hardware keys are physical hardware that you can use to authenticate. Hardware keys are inserted into a port on your device to provide authentication. For details on registering hardware keys, see [Register a hardware security key](../task/mfa-setup-hardware-key-auth.md).

![Hardware key icon](../images/hardware-key.png)

## Passkey

Passkey authentication is a secure, password less method of log in, where the users use a passkey by unlocking their device with a biometric sensor, PIN, or pattern.

## SMS

Admin can configure ServiceNow instance to require users who attempt to log in to the instance using SMS based OTP.

When users attempt to log in to ServiceNow, SMS OTP is sent to the mobile number associated with the sys\_user record. Users can enter the six-digit verification code that it sent to the mobile device and verify their identity. For more information, see [Multi-factor authentication with SMS](mfa-with-sms.md).

![SMS](../images/sms.png)

## Email

Admin can configure ServiceNow instance to require users who attempt to log in to the instance using Email based OTP.

When users attempt to log in to ServiceNow, Email OTP is sent to the email address of the user. Users can enter the six-digit verification code that it sent to the email address and verify their identity. For more information, see [Multi-factor authentication with Email](mfa-with-email.md).

![Email](../images/email.png)

**Related topics**  


[Web Authentication - MFA](web-authentication-mfa.md)

[MFA verification methods](mfa-methods.md)

[Multi-factor authentication with Email](mfa-with-email.md)

