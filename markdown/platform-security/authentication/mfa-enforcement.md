---
title: Multi-factor Authentication enforcement
description: MFA is enforced for non-SSO logins to ServiceNow starting with the Yokohama release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/mfa-enforcement.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Multi-factor authentication, Authentication, Access Management]
---

# Multi-factor Authentication enforcement

MFA is enforced for non-SSO logins to ServiceNow starting with the Yokohama release.

MFA enhances security by requiring users to provide two or more forms of evidence to prove their identity during login. MFA protects accounts from threats like phishing and account takeovers.

MFA is a critical security tool against various identity takeover-related attacks. ServiceNow enforces MFA by default post-Yokohama upgrade and making it required for non-SSO log ins \(users performing login with only username and password or LDAP based authentication\) to help improve the security posture and reduce the risk of breaches.

MFA enforcement is carried out through an MFA policy that is activated by default from Yokohama or upgrade to Yokohama. The MFA is enforced if the **Enforce MFA for non-SSO logins** policy is `Active` and honored through the MFA Context.

**Note:**

-   The policy is enabled for all **non-snc\_external** users performing local \(username and password\) or LDAP based authentication.
-   The instance admin can modify the enforcement scope by changing the MFA context policy, policy criteria, or policy conditions.

Here's more details about MFA enforcement:

-   Enforced to all production and non-production instances.
-   Enforced to all the **non-snc\_external** users and **non-SSO** login.
-   Integration with Basic auth and OAuth resource owner password credential grant does not require MFA from Yokohama.

To learn more about the changes due to enforcement, see [Changes due to the multi-factor authentication enforcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/changes-mfa-enforcement.md).

To learn more about MFA, see [Exploring Multi-factor Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/explore-mfa.md).

## Clear an entry from the enforcement table

Integration accounts that aren't marked as Web Service Access Only and make API calls appear in the enforcement table. To clear an entry, open Security Center, go to **Security Metrics** &gt; **Authentication** &gt; **Integration Accounts without Web Service Access Only Flag enabled**, and select the hybrid user record. Then choose one of the following actions:

-   **Enable Web Service**: converts the account to a web service access only account. Use this when the account is an integration that makes API calls.
-   **Mark as Interactive**: use this when the account isn't supposed to make API calls. The account is cleared from the enforcement table.

**Related topics**  


[Configuring multi-factor authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/configure-mfa.md)

[Using Multi-factor authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/mfa-use.md)

[MFA enforcement properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/mfa-enforcement-properties.md)

[Troubleshooting multi-factor authentication enforcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/troubleshoot-mfa-enforcement.md)

[Frequently asked questions - Multi-factor Authentication enforcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/faq-mfa.md)

