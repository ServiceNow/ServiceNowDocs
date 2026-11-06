---
title: High assurance session for non-SSO login
description: Establish a high assurance session for non-SSO logins \(local or LDAP\) with ServiceNow continuous authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/high-assurance-non-sso-logins.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [High assurance, Continuous Authentication \(CA\), Zero Trust Access, Access Management]
---

# High assurance session for non-SSO login

Establish a high assurance session for non-SSO logins \(local or LDAP\) with ServiceNow continuous authentication.

A high assurance session is a session that requires a user to verify their identity and authenticate with a specific identity or Identity Providers for a specific time frame.

ServiceNow continuous authentication \(CA\) feature enables you to create policies that create a high assurance session to the users who access personally identifiable information \(PII\), sensitive data, or restrict the access to explicit data that you want to protect.

When the user performs step-up authentication \(MFA\), there's a high assurance session that is established, which provides the ability for the users to access the data protected by the CA administrator based on the CA policy configuration.

You can create CA policies to verify the users identity and authentication the users to access the data that you've protected. The users who are performing non- SSO based login \(local or LDAP\) and whenever there is an attempt to access the protected data, step-up authentication \(MFA\) screen is prompted to the users.

\[Omitted image "mobile-screen-mfa.png"\] Alt text: MFA-SMS

After successful authentication, the protected data is displayed to the users for a certain time frame. You can configure the properties to change the time limit based on your requirements. To learn more, see [High assurance session with continuous authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/high-assurance-ca.md).

**Note:** If users haven't set up MFA, they must complete the setup.

Performing step-up authentication \(MFA\) creates a high assurance session establishing a secure and trusted connection with the identities \(users\) who are accessing the protected data.

A high assurance session established for the user is limited to the High Assurance session length \(**glide.zta.high\_assurance.session.timeout**\) system property. If the high assurance session time exceeds the property length, the user is prompted for re-authentication or step-up authentication.

**Related topics**  


[High assurance session with continuous authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/high-assurance-ca.md)

[Pre-work for Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/pre-work-ca.md)

[Configure Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/configure-ca.md)

