---
title: User Metrics
description: User Metrics displays the user MFA enrollment trends on ServiceNow.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [MFA Dashboard, Multi-factor authentication, Authentication, Access Management]
---

# User Metrics

User Metrics displays the user MFA enrollment trends on ServiceNow.

User Metrics on the MFA Dashboard are as follows:

-   [Users enrolled in Multi-factor Authentication \(MFA\)](user-metrics.md#section_oxp_4vx_w2c)
-   [Privileged admins without Multi-factor Authentication \(MFA\)](user-metrics.md#section_qgd_rvx_w2c)

## Users enrolled in Multi-factor Authentication \(MFA\)

The percentage of users who can perform username-password based login and enrolled in MFA. This metric provides an insight on the adoption of MFA by the users over a period of time.

![Users enrolled in MFA](../images/mfa-dashboard-users-enrolled.png)

**Note:** Ideally, the score should gradually increase and should be 100% over a period of time \(Refreshed once a day to collect records for a day before\).

## Privileged admins without Multi-factor Authentication \(MFA\)

Privileged admins not using MFA is a significant risk to platform security. It’s recommended that you get these people using MFA.

![Privileged admins without MFA](../images/mfa-dashboard-privileged-admins.png)

**Note:** Privileged admins are the users who have at least one role from the **sys\_icenter\_role\_config** table. \(Refreshed once a day to collect records for a day before\).

