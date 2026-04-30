---
title: Multi-factor Authentication enforcement
description: Enforcement of MFA for non-SSO logins to ServiceNow from the Yokohama release.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Multi-factor authentication, Authentication, Access Management]
---

# Multi-factor Authentication enforcement

Enforcement of MFA for non-SSO logins to ServiceNow from the Yokohama release.

MFA enhances security by requiring users to provide two or more evidence to prove their identity during login. MFA protects accounts from threats like phishing and account takeovers.

MFA being a critical security tool against various identity takeover-related attacks. ServiceNow enforces MFA by default post-Yokohama upgrade and making it mandatory for non-SSO log ins \(users performing login with only username and password or LDAP based authentication\) to ensure a better security posture and reduce the risk of breaches.

MFA enforcement is carried though a MFA policy that is activated by default from Yokohama or upgrade to Yokohama. The MFA is enforced the **Enforce MFA for non-SSO logins** policy is `Active` and honored through the MFA Context.

**Note:**

-   The policy is enabled for all **non-snc\_external** users performing local \(username and password\) or LDAP based authentication.
-   The instance admin can modify the enforcement scope by changing the MFA context policy, policy criteria, or policy conditions.

Here's more details about MFA enforcement:

-   Enforced to all production and non-production instances.
-   Enforced to all the **non-snc\_external** users and **non-SSO** login.
-   Integration with Basic auth and OAuth resource owner password credential grant does not require MFA from Yokohama.

To know more about the changes due to enforcement, see [Changes due to the MFA enforcement](changes-mfa-enforcement.md).

To know more about MFA, see [Exploring Multi-factor authentication](explore-mfa.md).

**Related topics**  


[Configure Multi-factor authentication](configure-mfa.md)

[Using Multi-factor authentication](mfa-use.md)

[MFA enforcement properties](mfa-enforcement-properties.md)

[Troubleshooting MFA enforcement](troubleshoot-mfa-enforcement.md)

[Frequently asked questions - MFA enforcement](faq-mfa.md)

