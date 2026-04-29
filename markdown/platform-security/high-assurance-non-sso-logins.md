---
title: High Assurance session for non-SSO login
description: Establish high assurance session for non-SSO logins \(local or LDAP\) using ServiceNow's continuous authentication.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [High Assurance, Continuous Authentication \(CA\), Zero Trust Access, Access Management]
---

# High Assurance session for non-SSO login

Establish high assurance session for non-SSO logins \(local or LDAP\) using ServiceNow's continuous authentication.

A high assurance session is a session that requires a user to verify their identity and authenticate with a specific identity or Identity Providers for a specific time frame.

ServiceNow's continuous authentication \(CA\) feature enables you to create policies that creates a high assurance session to the users who access Personally Identifiable Information \(PII\), sensitive data, or restrict the access to explicit data that you want to protect.

When the user perform step-up authentication \(MFA\), there's a high assurance session that is established, which provides the ability for the users to access the data protected by the CA administrator based on the CA policy configuration.

You can create CA policies to verify the users identity and authentication the users to access the data that you've protected. The users who are performing non- SSO based login \(local or LDAP\) and whenever there is an attempt to access the protected data, step-up authentication \(MFA\) screen is prompted to the users.

![MFA-SMS](../images/mobile-screen-mfa.png)

After successful authentication, the protected data is displayed to the users for a certain time frame. You can configure the properties to change the time limit based on your requirement. To know more, see [High Assurance session with Continuous Authentication](high-assurance-ca.md).

**Note:** If the users haven't setup MFA, it is compulsory to complete the setup.

Performing step up authentication \(MFA\), creates a high assurance session establishing a secure and trusted connection with the identities \(users\) who are accessing the protected data.

An high assurance session established for the user is limited to the High Assurance session length \(**glide.zta.high\_assurance.session.timeout**\) system property. If the high assurance session time exceeds the property length, the user is prompted for re-authentication or step up authentication.

**Related topics**  


[High Assurance session with Continuous Authentication](high-assurance-ca.md)

[Pre-work for Continuous Authentication](pre-work-ca.md)

[Configuring Continuous Authentication](../task/configure-ca.md)

