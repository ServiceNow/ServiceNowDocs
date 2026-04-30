---
title: Troubleshooting MFA enforcement
description: Troubleshooting information due to the MFA enforcement.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [MFA enforcement, Multi-factor authentication, Authentication, Access Management]
---

# Troubleshooting MFA enforcement

Troubleshooting information due to the MFA enforcement.

ServiceNow enforces MFA by default post-Yokohama upgrade and making it mandatory for non-SSO logins \(users performing login with only username and password or LDAP based authentication\) to ensure a better security posture and reduce the risk of breaches.

MFA enforcement is carried though a MFA policy that is activated by default from Yokohama or upgrade to Yokohama. Following are some of the troubleshooting task that you can perform if there's any change to the MFA behavior:

-   Debug using the troubleshooting tools
-   Navigate to the Log location and Debug properties
-   Understand the MFA scenarios based on your users experience while using MFA
-   Understand the MFA issue due to upgrade from a previous release

## Debug MFA

Use the either of the following tools or a combination to understand the debug information:

-   **Splunk** - to see the debug logs.
-   System logs or Node logs.
-   **HAR** logs to analyze the debug logs for the MFA.

## Log location and Debug properties

Navigate to the following location to know more about logs:

-   For system logs, navigate to **All** &gt; **System Log** &gt; **System Logs**.
-   For node logs, navigate to **All** &gt; **System Logs** &gt; **Utilities** &gt; **Node Log File Browser**.

The system debug logs and instance node logs are required for the debug purpose. Following are the debug properties that are required to be enabled:

-   `glide.webauthn.debug.enabled`
-   `glide.log.default_log_debug`
-   `glide.authenticate.policy.debug`
-   `glide.authenticate.hybrid_user_tracking.debug`

## MFA issue based on scenarios

-   **Scenario 1: User is not able to login using any of their second factor**

    Reset the MFA for the your users and delete the old user records from the following tables:

    -   `user_multifactor_auth`
    -   `sys_user_public_credential`
    -   `sys_user_multi_factor_setup`
-   **Scenario 2: Admin is not able to login using any of their second factor**

    Another user with admin access can reset the MFA for any blocked admin user. If still the issue exist, reach out to ServiceNow Support.

-   **Scenario3: Error observed during the MFA Setup or Validation**

    Check the warning "Associated Error Codes/Warning: Your 6-digit verification code is incorrect. Try again with the correct code".

    Perform the following steps:

    -   In case of TOTP Authenticator App, if the date and time of the Authenticator MFA device and instance are not in sync \(±30 sec\), then the TOTP code is not accepted. Verify the device and instance date and time.
    -   In case of email, configure the user level notification, outbound email configuration, and user correctly in the `sys_user` table.
    -   In case of SMS, configure the Twillio or other SMS service provider integration correctly and set to active. Verify if the user's mobile number is configured correctly in the `sys_user` table.

