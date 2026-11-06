---
title: High assurance for SSO login
description: Establish a high assurance session for SSO login with ServiceNow continuous authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/high-assurance-sso-logins.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [High assurance, Continuous Authentication \(CA\), Zero Trust Access, Access Management]
---

# High assurance for SSO login

Establish a high assurance session for SSO login with ServiceNow continuous authentication.

A high assurance session is a session that requires a user to verify their identity and authenticate with a specific identity or Identity Providers for a specific time frame.

ServiceNow continuous authentication \(CA\) feature enables you to create policies that create a high assurance session to the users who access personally identifiable information \(PII\), sensitive data, or restrict the access to explicit data that you want to protect.

When the user re-authenticates, there's a high assurance session that is established, which provides the ability for the users to access the data protected by the CA administrator based on the CA policy configuration.

You can create CA policies to verify user identity and authenticate users who access the data that you've protected. You can configure the CA policy and provide the Identity Providers details in the Identity Providers record to establish high assurance session.

\[Omitted image "ca-tab.png"\] Alt text: Continuous Authentication - tab information

The users who are performing SSO-based login \(SAML or OIDC\) and whenever there is an attempt to access the protected data, re-authentication screen is prompted with the same SSO that was used by the user during the initial login.

\[Omitted image "ca-sso-screen.png"\] Alt text: SSO - Screen

After successful SSO authentication, the protected data is displayed to the users for a certain time frame. You can configure the properties to change the time limit based on your requirements. To learn more, see [High assurance session with continuous authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/high-assurance-ca.md).

Performing re-authentication with SSO login \(SAML or OIDC\) creates a high assurance session establishing a secure and trusted connection with the identities \(users\) who are accessing the protected data.

A high assurance session established for the user is limited to the High Assurance session length \(**glide.zta.high\_assurance.session.timeout**\) system property. If the high assurance session time exceeds the property length, the user is prompted for re-authentication or step-up authentication.

**Related topics**  


[High assurance session with continuous authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/high-assurance-ca.md)

[Pre-work for Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/pre-work-ca.md)

[Configure Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/configure-ca.md)

