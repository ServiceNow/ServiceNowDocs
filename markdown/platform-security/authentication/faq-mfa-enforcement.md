---
title: MFA enforcement requirements – What and Why
description: FAQ related to MFA enforcement and why it’s important.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Frequently asked questions, MFA enforcement, Multi-factor authentication, Authentication, Access Management]
---

# MFA enforcement requirements – What and Why

FAQ related to MFA enforcement and why it’s important.

1.  What is the MFA?

    Multi-factor Authentication \(MFA\) is a security process that requires you to provide two or more forms of verification before they can access an account or system. To learn more, see [Exploring Multi-factor Authentication](explore-mfa.md).

2.  Why is the MFA enforcement mandate?

    MFA is mandated to protect your account and data security. Cyberthreats are ever-changing, and passwords alone no longer provide sufficient protection against unauthorized access.

    -   With MFA enabled, even if attackers have your password, the attackers still need a second form of verification. This additional layer significantly blocks most unauthorized attempts, keeping your information more secure.
    -   Setting MFA as the default, minimize the risk of security breaches and safeguarding your account automatically. This means you get enhanced peace of mind without having to make any extra security decisions.
3.  Why is it important to enable MFA?

    Enabling MFA boosts your account security. Passwords alone aren't enough because passwords can be exposed in data breaches. With MFA, even if someone knows your password, they can't access your account without a second verification step.

4.  Why does ServiceNow require MFA?

    ServiceNow is mandating MFA to protect you from these threats. It's a simple yet effective way to reduce unauthorized access. By requiring MFA, there's a strong layer of protection to every account, reducing security risks for you and all users.

5.  What is the MFA requirement for existing customers?

    For existing customers upgrading their instance to the Yokohama or a later release:

    -   If the instance doesn’t already have the **Adaptive Authentication** – [Multi-factor Authentication context](mfa-auth-context.md) turned on, automatically it’s enabled as a default MFA policy.
    -   All the internal users \(users who don’t have snc\_external role\) logging in with local or LDAP authentication must set up MFA within 30 days of their first successful login. During this time, you can log in normally but see a message at the time of login to enroll in MFA.
    -   After 30 days, MFA will be required by default, and users won’t be able to log in without completing the MFA setup.
6.  What is the MFA requirement for new customers?

    For any instance using the Yokohama release or later, MFA is enabled by default for all internal users. It also applies to users who don’t have the `snc_external` role and are logging in with local or LDAP authentication. From the first login, the users are required to set up and use MFA.


