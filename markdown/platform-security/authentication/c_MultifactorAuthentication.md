---
title: Configuring MFA, supported methods, and workflow
description: MFA, also known as two-step verification, is a security requirement that users enter more than one set of credentials to access an instance.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Configuring MFA, supported methods, and workflow

MFA, also known as two-step verification, is a security requirement that users enter more than one set of credentials to access an instance.

The basic level of authentication to an instance is local database authentication where a user enters their user name and password. MFA gives administrators and users the ability to require a second level of authentication.

The second level of authentication can be based on the following:

-   A passcode from an authentication app
-   A hardware key
-   A biometric authenticator, such as a fingerprint reader or facial recognition.
-   An SMS or Email

![MFA Options](../images/MFA-options.png)

As an administrator, you can set-up MFA for individual users or all the users in a specific role. You can also enable your users to opt and use MFA.

## Activation

The **Integration - Multifactor Authentication** \(com.snc.integration.multifactor.authentication\) plugin is installed by default on your instance but must be enabled by an administrator using a system property. For details, see [Multi-factor authentication system properties](../reference/mfa-properties.md).

**Note:** After cloning an instance, you must re-enable MFA on the cloned instance. For more information, you can refer these KB articles [KB0657100](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0657100), [KB0860689](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0860689),[KB0825390](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0825390), [KB0779908](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0779908), [KB0717367](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0717367), [KB0727991](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0727991).

## Supported authentication methods

You can use MFA with the following authentication methods:

-   Local Database Authentication \(native ServiceNow authentication\)
-   [LDAP integration](../../ldap/concept/c_LDAPIntegration.md)
-   SSO SAML
-   [SSO OIDC](mfa-sso.md)

## Multi-factor authentication set up workflow

-   **Administrator enables multi-factor authentication**

    The **Integration - Multifactor Authentication** \(com.snc.integration.multifactor.authentication\) plugin is activated on your instance by default. To begin using MFA, administrators must enable MFA using a system property. Once enabled, administrators select users or roles that require MFA logins.

    For more detail on administrator set up for MFA, see [Multi-factor authentication \(MFA\)](mfa-config-landing.md).

-   **Users log in using an authentication app**

    The users are prompted to use MFA options for the log in. Users can choose either of the options to complete MFA and if any user has completed the setup using any one factor, they can still go to their profile page and complete the remaining factors setup if they want to.


## Web Authentication

Activate **Integration - Web Authentication** \(com.snc.integration.webauthn\) to allow hardware key or biometric reader authentication on your instance.

<table id="table_wdw_nyp_dpb"><tbody><tr><td>

![Hardware key icon](../images/hardware-key.png)

</td><td>

Hardware keys are physical hardware that you can use to authenticate. Hardware keys are inserted into a port on your device to provide authentication. For details on registering hardware keys, see [Register a hardware security key](../task/mfa-setup-hardware-key-auth.md).

</td></tr><tr><td>

![Biometrics icon](../images/biometric-2.png)

</td><td>

Biometric authenticators use fingerprint or facial recognition to identify users. Your users can use these authenticators on their devices as part of the multi-factor login process. For details on registering biometric authenticators, see [Register a biometric authenticator](../task/mfa-setup-bio-auth.md).

</td></tr></tbody>
</table>## SMS or Email \(One-time password\)

To enable users to log in to a ServiceNow instance and smoother experience on the go, MFA is supported with SMS and Email.

<table id="table_gdm_b2g_dvb"><tbody><tr><td>

![SMS](../images/sms.png)

</td><td>

Admin can configure ServiceNow instance to require users who attempt to login the instance using SMS based OTP.

 When users attempt to login to ServiceNow, SMS OTP is sent to the mobile number associated with the sys\_user record. User's can enter the six-digit verification code that it sent to the mobile device and verify their identity.

 For more information, see [Multi-factor authentication with SMS](mfa-with-sms.md).

</td></tr><tr><td>

![Email](../images/email.png)

</td><td>

Admin can configure ServiceNow instance to require users who attempt to login to the instance using Email based OTP.

 When users attempt to login to ServiceNow, Email OTP is sent to the email address associated to the user. User's can enter the six-digit verification code that it sent to the email address and verify their identity.

 For more information, see [Multi-factor authentication with Email](mfa-with-email.md).

</td></tr></tbody>
</table>