---
title: Troubleshooting multi-factor authentication enforcement
description: Resolve issues caused by MFA enforcement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/troubleshoot-mfa-enforcement.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [MFA enforcement, Multi-factor authentication, Authentication, Access Management]
---

# Troubleshooting multi-factor authentication enforcement

Resolve issues caused by MFA enforcement.

ServiceNow enforces MFA by default post-Yokohama upgrade and makes it required for non-SSO logins \(users performing login with only username and password or LDAP based authentication\) to help improve security posture and reduce the risk of breaches.

MFA enforcement is carried out through an MFA policy that is activated by default from Yokohama or upgrade to Yokohama. The following are some of the troubleshooting tasks that you can perform if there's any change to the MFA behavior:

-   Debug using the troubleshooting tools
-   Navigate to the Log location and debug properties
-   Understand the MFA scenarios based on your users experience while using MFA
-   Understand the MFA issue due to upgrade from a previous release

## Debug MFA

Use any of the following tools or a combination to understand the debug information:

-   System logs or Node logs.
-   **HAR** logs to analyze the debug logs for the MFA.

## Log location and debug properties

Navigate to the following location to learn more about logs:

-   For system logs, navigate to **All** &gt; **System Log** &gt; **System Logs**.
-   For node logs, navigate to **All** &gt; **System Logs** &gt; **Utilities** &gt; **Node Log File Browser**.

The system debug logs and instance node logs are required for the debug purpose. The following debug properties must be enabled:

-   `glide.webauthn.debug.enabled`
-   `glide.log.default_log_debug`
-   `glide.authenticate.policy.debug`
-   `glide.authenticate.hybrid_user_tracking.debug`

## MFA issue based on scenarios

-   **Scenario 1: User can't log in using any of their second factor**

    Reset MFA for your users and delete the old user records from the following tables:

    -   `user_multifactor_auth`
    -   `sys_user_public_credential`
    -   `sys_user_multi_factor_setup`
-   **Scenario 2: Admin can't log in using any of their second factor**

    Another user with admin access can reset the MFA for any blocked admin user. If the issue still exists, contact ServiceNow Support.

-   **Scenario 3: Error observed during the MFA setup or validation**

    Check the warning "Associated Error Codes/Warning: Your 6-digit verification code is incorrect. Try again with the correct code".

    Perform the following steps:

    -   In case of TOTP Authenticator App, if the date and time of the Authenticator MFA device and instance are not in sync \(±30 sec\), then the TOTP code is not accepted. Verify the device and instance date and time.
    -   In case of email, configure the user level notification, outbound email configuration, and user correctly in the `sys_user` table.
    -   In case of SMS, configure the Twilio or other SMS service provider integration correctly and set to active. Verify if the user's mobile number is configured correctly in the `sys_user` table.
-   **Scenario 4: An integration account appears in the enforcement table**

    Integration accounts that aren't marked as Web Service Access Only and make API calls appear in the enforcement table. In Security Center, select the account and choose **Enable Web Service** to convert it to a web service access only account, or **Mark as Interactive** if it isn't supposed to make API calls. For more information, see [Multi-factor Authentication enforcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/mfa-enforcement.md).


