---
title: Activate Trusted Mobile app
description: Activate adaptive authentication with trusted mobile app by using the authentication policy and filter conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/activate-trusted-mobile-app.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Adaptive authentication for Trusted Mobile apps, Adaptive authentication, Authentication, Access Management]
---

# Activate Trusted Mobile app

Activate adaptive authentication with trusted mobile app by using the authentication policy and filter conditions.

## Before you begin

Make sure the Adaptive Authentication \(**com.snc.adaptive\_authentication**\) plugin is installed.

Role required: adaptive\_auth\_admin

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **Properties**.

2.  On the Adaptive Authentication Properties page, enable the following properties:

    -   Enable the Authentication Policy \(**glide.authenticate.auth.policy.enabled**\)
    -   Enable Device Trust Flow \(**glide.authenticate.preauth.allow.trusted.device**\)
    \[Omitted image "enable-mobile-trust.png"\] Alt text: Adaptive Authentication Properties

    **Note:** To disable the device trust flow property, you must remove the conditions with trusted mobile filter. Otherwise, an error message is displayed to remove the conditions.

3.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Auth Policy Contexts** &gt; **Pre Authentication Context**.

4.  Define the conditions in the Pre Authentication context.

    For more information, [Pre authentication context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/pre-auth-context.md).

    **Note:** By default, the policy condition is **Deny Policy**. You can change to **Allow Policy**. These policies are direct opposites.

    -   With the **Allow Policy**, all users are denied access by default, and it only allows access when the allow access policy conditions are true.
    -   With the **Deny Policy**, all users are allowed access by default, and it only denies access when the deny access policy conditions are true.
    In the Policy Input, the policy input **Trusted Mobile App** is a policy input for the trusted mobile app.

    \[Omitted image "trusted-device-filter.png"\] Alt text: Auth Policy Context

5.  In the Policy Conditions, create the condition by clicking **New**.

6.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Name of the condition|
    |Description|Description of the condition|
    |Application|Application scope for this record.|
    |Condition|Conditions based on AND and OR. Because the Auth Policy is **Allow Policy**, the condition for Trusted Mobile App is set true in the example shown on the image.|

    \[Omitted image "filter-condition.png"\] Alt text: Condition

7.  Click **Submit**.


## Result

The policy input and filter conditions are created for the Trusted Device feature. Users can proceed with using the Trusted Device feature to access the ServiceNow instance from untrusted networks by using the Now Mobile app. For more information, see [Register a trusted device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/register-trusted-device.md).

