---
title: High assurance session with continuous authentication
description: Establish a high assurance session with ServiceNow continuous authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/high-assurance-ca.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Continuous Authentication \(CA\), Zero Trust Access, Access Management]
---

# High assurance session with continuous authentication

Establish a high assurance session with ServiceNow continuous authentication.

A high assurance session is a security measure to establish a secure and trusted connection with the identities \(users\) who access data and are verified with a high degree of confidence.

ServiceNow provides high assurance through robust authentication methods that enforce re-authentication using methods such as Multi-factor Authentication \(MFA\) and Single Sign On \(SSO\) while the users try to access sensitive data.

When the user re-authenticates or performs step-up authentication \(MFA\), there's a high assurance session that is established, which provides the ability for the users to access the data protected by the continuous authentication \(CA\) administrator based on the CA policy configuration.

Following are the re-authentication methods used to establish High-assurance based on the type of login:

-   [High Assurance for SSO login](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/high-assurance-sso-logins.md)
-   [High Assurance for non-SSO login](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/high-assurance-non-sso-logins.md)

High assurance session created by the user is valid based on the High Assurance session length \(**glide.zta.high\_assurance.session.timeout**\) determined by the CA administrator.

The high assurance session can be customized based on your requirements by setting the **High Assurance** system properties.

<table id="table_tfb_2l2_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

High Assurance session length \(**glide.zta.high\_assurance.session.timeout**\)

</td><td>

Length of the high assurance session, after which end-users must re-authenticate. Default: 30 minutes.**Note:** The value must be between 1 and 480.

</td></tr><tr><td>

Default high-assurance session length upon login

</td><td>

Duration in minutes for the default high-assurance session length upon user login. Default value: 5 minutes.**Note:** This property is only applicable for non-SSO logins.

</td></tr><tr><td>

Configure end-user display message \(**glide.zta.high\_assurance.session.message**\)

</td><td>

Message displayed to end-users for re-authentication. Default message: `One or more resources require additional authentication due to a policy created by your administrator`.

</td></tr><tr><td>

Total times failed authentication before user account lock-out \(**glide.zta.high\_assurance.session.max.login.failed\_attempts**\)

</td><td>

Maximum failed authentication attempts before users are logged out.**Note:** The value must be between 3 and 10.

</td></tr></tbody>
</table>## High assurance session as a preemptive measure

Users who work with high privilege data such as financial transactions, government information, personally identifiable information \(PII\), can establish a high assurance session as a preemptive measure to avoid frequent authentication notification during their logged in session.

High assurance session can be created by themselves. To create a high assurance session, select **User Profile** &gt; **Profile**. In the Related Links section, select **Create High-Assurance Session**. Verify your identity to create a high assurance session.

\[Omitted image "ca-high-assurance-profile.png"\] Alt text: High-Assurance Session from the user profile

**Related topics**  


[Exploring Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/explore-continuous-auth.md)

[Pre-work for Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/pre-work-ca.md)

[Configure Continuous Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/configure-ca.md)

