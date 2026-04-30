---
title: Multi-factor authentication with SMS
description: Multi-factor authentication \(MFA\) with SMS as a factor for your authentication.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [MFA verification methods, Configure Multi-factor authentication, Multi-factor authentication, Authentication, Access Management]
---

# Multi-factor authentication with SMS

Multi-factor authentication \(MFA\) with SMS as a factor for your authentication.

Admin can configure ServiceNow instance to require users who attempt to login the instance using SMS based OTP.

When users attempt to login to ServiceNow, SMS OTP is sent to the mobile number associated with the sys\_user record. User's can enter the six-digit verification code that it sent to the mobile device and verify their identity.

You can configure MFA with SMS using the out of the box Twilio as well. For more information, see [Multi-factor authentication Providers](multi-factor-authentication-providers.md).

![MFA-SMS](../images/mobile-screen-mfa.png)

Further the MFA with SMS can be controlled based on the policy input and conditions using filter criteria. Following are the types of filter criteria:

-   [IP Filter Criteria](../task/create-ip-filter-criteria.md)
-   [Role Filter Criteria](../task/create-role-filter-criteria.md)
-   [Group Filter Criteria](../task/create-group-filter-criteria.md)

