---
title: High Assurance session with Continuous Authentication
description: Establish high assurance session for with ServiceNow's continuous authentication.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Continuous Authentication \(CA\), Zero Trust Access, Access Management]
---

# High Assurance session with Continuous Authentication

Establish high assurance session for with ServiceNow's continuous authentication.

A high assurance session is a security measure to establish a secure and trusted connection with the identities \(users\) who access data and are verified with a high degree of confidence.

ServiceNow's High assurance is achieved through robust authentication methods which enforces re-authentication using methods such as Multi-factor Authentication \(MFA\) and Single Sign On \(SSO\) while the users try to access data that are sensitive.

When the user re-authenticates or perform step-up authentication \(MFA\), there's a high assurance session that is established, which provides the ability for the users to access the data protected by the CA administrator based on the CA policy configuration.

Following are the re-authentication methods used to establish High-assurance based on the type of login:

-   [High Assurance for SSO login](high-assurance-sso-logins.md)
-   [High Assurance for non-SSO login](high-assurance-non-sso-logins.md)

High assurance session created by the user is valid based on the High Assurance session length \(**glide.zta.high\_assurance.session.timeout**\) determined by the CA administrator.

The high assurance session can be customized based on your requirement by setting the **High Assurance** system properties:

<table id="table_tfb_2l2_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

High Assurance session length \(**glide.zta.high\_assurance.session.timeout**\)

</td><td>

Specify the high assurance session length, after which the end-users should re-authenticate. Default: 30 minutes.**Note:** The value must be between 1 and 480.

</td></tr><tr><td>

Default high-assurance session length upon login

</td><td>

Specify the duration in minutes for the default high-assurance session length upon user login. Default value: **5** minutes.**Note:** This property is only applicable for non-sso logins.

</td></tr><tr><td>

Configure end-user display message \(**glide.zta.high\_assurance.session.message**\)

</td><td>

Specify the message that is displayed to the end-user for re-authentication. Default message: `One or more resources require additional authentication due to a policy created by your administrator`.

</td></tr><tr><td>

Total times failed authentication before user account lock-out \(**glide.zta.high\_assurance.session.max.login.failed\_attempts**\)

</td><td>

Set the maximum failed authentication attempts before the users are logged out.**Note:** The value must be between 3 and 10.

</td></tr></tbody>
</table>## High assurance session as a Preemptive measure

Users who work with high privilege data such as financial transactions, government information, PII, can establish high assurance session as a preemptive measure to avoid frequent authentication notification during their logged in session.

High assurance session can be created by the themselves. To create a high assurance session, select **User Profile** &gt; **Profile**. In the **Related Links** section, select **Create High-Assurance Session**. Verify your identity to create a high assurance session.

![High-Assurance Session from the user profile](../images/ca-high-assurance-profile.png)

**Related topics**  


[Explore Continuous Authentication](explore-continuous-auth.md)

[Pre-work for Continuous Authentication](pre-work-ca.md)

[Configure Continuous Authentication](../task/configure-ca.md)

