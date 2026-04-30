---
title: MFA enforcement timeline
description: FAQ related to MFA enforcement timelines and why it’s important.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Frequently asked questions - MFA enforcement, MFA enforcement, Multi-factor authentication, Authentication, Access Management]
---

# MFA enforcement timeline

FAQ related to MFA enforcement timelines and why it’s important.

1.  When is MFA enforced?

    According to the MFA policy, eligible users who haven’t completed the MFA setup has a 30-day self-enrollment period. The behavior is controlled using the system property `glide.authenticate.multifactor.self_enrolment_period`. The property's default value is 30 days. It can be updated to a maximum of 90 days.

    All internal users \(users who don’t have a `snc_external` role\) logging in with local or LDAP authentication must set up MFA within 30 days of their first successful login. During this time, you can log in normally but see a message at the time of login to enroll in MFA.

    ![Enrollment message](../images/mfa-enrolment-message.png)

    After 90 days of upgrading to Yokohama or a later release, if an internal user \(user without the `snc_external` role\) logs in with local or LDAP authentication for the first time, they’ll be required to use MFA immediately. You don't have the 30-day MFA self-enrollment window. This period is governed by a system property:`glide.authenticate.multifactor.enforcement.max_relaxation_period`. The maximum value for this property is 270 days.

2.  How can the MFA enforcement timeline adjusted?
    -   By updating the value of the property `glide.authenticate.multifactor.self_enrolment_period`, admins can provide a smaller or larger self-enrollment window. Set the property value to 0. The users are required to complete the MFA setup after their first login attempt with local or LDAP login after upgrading to Yokohama or a later release. The maximum duration of the self-enrollment window can be 90 days. Property value set higher than 90 will be treated as 90.
    -   By updating the value of the property `glide.authenticate.multifactor.enforcement.max_relaxation_period` admin can decide how many days post upgrade to the Yokohama or a later release you get the MFA self-enrollment window.
3.  How are end users informed about this upcoming change?

    End users performing local or LDAP authentication who will be enforced with MFA will see an information message after logging in. The same message is available when users visit their profile.

    |On the User Profile|On Employee Service Center|
    |-------------------|--------------------------|
    |![Message on the User Profile](../images/mfa-enrolment-message-profile.png)|![Message on the Employee Center](../images/mfa-enrolment-message-employee.png)|

    This message won’t appear for non-admin users performing SSO logins. The admin role will see a different information message after a successful login irrespective of the authentication method used for logging in.

    ![Message for Admin](../images/mfa-enrolment-message-admin.png)

    This message continues to be displayed until one of the admins acknowledges the update by setting the `glide.authenticate.multifactor.enforcement.acknowledged` property value to true.

    ![Glide Property to turn off the message](../images/mfa-enrolment-message-glide-property.png)

4.  How to turn off the message displayed to end users about completing the MFA setup when they log in?

    Admins can update the value of the `glide.authenticate.multifactor.enforcement.show_user_info_message` system property to false to turn off the MFA enrollment information message shown to end users after login.

5.  How to turn off the message displayed to administrators about the MFA enforcement?

    The information message regarding MFA enforcement shown to admin users after login, stops appearing when one of the admins acknowledges it by updating the value of the `glide.authenticate.multifactor.enforcement.acknowledged` system property to true.

6.  There's already an MFA policy defined using adaptive authentication based on the security needs of my organization in the instance. Is the policy impacted by the mandate?

    No, if the instance already has an active Adaptive authentication—MFA context policy, the new default secure MFA policy isn’t enforced. If the instance had MFA property enabled \(`glide.authenticate.multifactor`\) but the MFA policy wasn’t active, then the default secure MFA policy for enforcing MFA for all internal users \(users who don’t have `snc_external` role\) performing user name and password-based local or LDAP login is enabled.


