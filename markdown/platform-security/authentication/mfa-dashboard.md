---
title: MFA Dashboard
description: View the different MFA metrics to understand the MFA adoption and usage.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Multi-factor authentication, Authentication, Access Management]
---

# MFA Dashboard

View the different MFA metrics to understand the MFA adoption and usage.

The MFA enhances security by requiring an additional verification step during the login process. The MFA Dashboard helps you to monitor and manage MFA settings for your organization. This dashboard provides an overview of MFA user enrollment, privileged admins who haven't opted MFA, and compliance. You can use it to ensure that all users have MFA enabled for enhanced security.

To access the MFA Dashboard, navigate **All** &gt; **Multi-factor Authentication** &gt; **MFA Dashboard**.

![MFA Dashboard](../images/mfa-dashboard.png)

**Note:** You must enable MFA to view the metrics. For more information, see [Multi-factor Authentication system properties](../reference/mfa-properties.md).

Following are the types of metrics displayed on the MFA Dashboard:

-   [User Metrics](mfa-dashboard.md#section_qkr_l2c_cfc)
-   [Login Metrics](mfa-dashboard.md#section_byk_42c_cfc)

## User Metrics

The following table provides details of the User Metrics in the MFA Dashboard.

<table id="table_bwy_g2c_cfc"><thead><tr><th>

Metrics

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Users enrolled in Multi-factor Authentication \(MFA\)

</td><td>

The percentage of users who can perform username-password based login and enrolled in MFA. This metric provides an insight on the adoption of MFA by the users over a period of time.**Note:** Ideally, the score should gradually increase and should be 100% over a period of time \(Refreshed once a day to collect records for a day before\).

</td></tr><tr><td>

Privileged admins without Multi-factor Authentication \(MFA\)

</td><td>

Privileged admins not using MFA is a significant risk to platform security. It’s recommended that you get these people using MFA. **Note:** Privileged admins are the users who have at least one role from the sys\_icenter\_role\_config table. \(Refreshed once a day to collect records for a day before\).

</td></tr></tbody>
</table>## Login Metrics

The following table provides details of the Login Metrics in the MFA Dashboard.

<table id="table_bdy_r2c_cfc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Multi-factor Authentication \(MFA\) factors used

</td><td>

Classification of MFA factors used during the username-password based login.

</td></tr><tr><td>

User-password logins without Multi-factor Authentication \(MFA\)

</td><td>

The percentage of username-password based logins without MFA. This metric provides an insight on the adoption of MFA over a period of time. **Note:** Ideally, the score should gradually decrease and should be zero over a period of time \(Refreshed once a day to collect records for a day before\).

</td></tr></tbody>
</table>