---
title: Authentication
description: The authentication category covers the main elements of modern authentication to confirm an entity and its claims are authentic and correct, resistant to impersonation and prevent interception of passwords.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Hardening settings, Platform Security]
---

# Authentication

The authentication category covers the main elements of modern authentication to confirm an entity and its claims are authentic and correct, resistant to impersonation and prevent interception of passwords.

The ASVS standard builds on the [NIST 800-63b \(https://pages.nist.gov/800-63-3/sp800-63b.html\)](https://pages.nist.gov/800-63-3/sp800-63b.html) specification for this section.

Authentication includes password policy, controls and storage, proper implementation of authenticators and proper implementation of out of band or one time verifiers.

-   **[Activate role-based multi-factor authentication \[Updated in Security Center 1.3\]](sc-activate-role-based-multi-factor-authentication.md)**  
Use the **glide.authenticate.multifactor** property to enforce role-based multi-factor authentication \(MFA\) for all users assigned to specific roles.
-   **[Activate role based multi-factor authentication](sc-role-based-multi-factor-authentication.md)**  
Use the **glide.authenticate.multifactor** property to enforce role-based multi-factor authentication \(MFA\) for all users assigned to specific roles.
-   **[Anti-CSRF token \(instance security hardening\)](../../security/reference/anti-csrf-token.md)**  
Use the **glide.security.use\_csrf\_token** property to ensure the use of a secure token to identify and validates incoming requests, which in turn are used to prevent these attacks.
-   **[Control Lockout Time for Invalid Password Reset Attempts](sc-reset-password-request-max-attempts-window.md)**  
The **password\_reset.request.max\_attempt\_window** property controls the number of minutes a user must wait to reset or change their password after exceeding the maximum number of unsuccessful attempts that is set with the **password\_reset.request.max\_attempt** property.
-   **[Disable creating users from incoming emails](sc-restrict-emails-by-domain.md)**  
Use the **glide.user.trusted\_domain** property to specify the comma-separated list of trusted domains used in the creation of users from incoming emails.
-   **[Disable password-less authentication](sc-disable-password-less-authentication.md)**  
Use the **glide.login.no\_blank\_password** property to prevent users from logging into the NOW platform with blank passwords, or by leaving the **Password** field empty.
-   **[Disable resource owner password credentials \(ROPC\) in OAuth 2 token grants \[New in Security Center 7.0\]](sc-disable-resource-owner-password-credentials-ropc-in-oauth-2-token-grants.md)**  
Prevent Resource Owner Password Credentials \(ROPC\) from granting OAuth 2 tokens.
-   **[Do not apply password policy at login \[Updated in Security Center 1.5 and removed in 2.0\]](sc-do-not-apply-password-policy-at-login.md)**  
Manage how password complexity is handled in your instance.
-   **[Enable account recovery](sc-account-recovery.md)**  
The **glide.sso.acr.enabled** property controls the account recovery feature.
-   **[Enable CAPTCHA for customer registration](sc-enable-captcha-for-customer-registration.md)**  
Reduce the risk of requests by malicious bots by enabling CAPTCHA for customer registration.
-   **[Enable a deny-list password validation check](sc-enable-blacklisted-passwords-validation-check.md)**  
Manage the deny-list passwords in the Excluded Password table.
-   **[Enable CAPTCHA for External User Registration](sc-enable-captcha-external-user-registration.md)**  
The **sn\_ext\_usr\_reg.captchaEnabled** controls if CAPTCHA will be validated for external user registration.
-   **[Enable CAPTCHA in password reset](sc-enable-captcha-in-password-reset.md)**  
Use the **password\_reset.captcha.ignore** property to enable or disable requiring a CAPTCHA challenge when a user resets their password.
-   **[Enable email OTP for multi-factor authentication](sc-enable-email-otp-for-multi-factor-authentication.md)**  
Manage how two-factor authentication is applied on your instance.
-   **[Enable password reset policy checks](sc-enable-password-reset-policy-checks.md)**  
Use the **glide.enable.password\_policy** property to enable password policy checks whenever a user changes their password using the user interface.
-   **[Enable relay state in SAML requests to prevent replay attacks](sc-enable-relay-state-in-saml-requests-to-prevent-replay-attacks.md)**  
Reduce the risk of replay attacks by enabling relay state in SAML requests to help prevent replay attacks.
-   **[Enable SMS code notification for enrollment and verification](sc-sms-code-notification-for-enrollment-and-verification.md)**  
The **password\_reset.sms.use\_notify** property controls the usage of SMS code notifications for password reset.
-   **[Enable SSL in LDAP authentication \[Updated in Security Center 1.5 and 2.0\]](sc-enable-ssl-in-ldap-authentication.md)**  
Manage the encryption of LDAP authentication requests on your instance.
-   **[Enforce current password policy compliance requirements on login](sc-enforce-current-password-policy-compliance-requirements-on-login.md)**  
Reduce the risk of brute force account login by enforcing current password policy compliance requirements on login.
-   **[Enforce device encryption and passcode requirements \[New in Security Center 1.3\]](sc-enforce-device-encryption-and-passcode-requirements.md)**  
The **glide.sg.device\_encryption\_enabled** property enforces the Federal Information Processing Standard \(FIPS 140-2\) Encryption. Mobile device encryption and passcode ensure that an unauthorized user cannot access the content of a device even if the device is physically obtained.
-   **[Limit Invalid Password Reset Attempts](sc-reset-password-request-max-attempts.md)**  
The **password\_reset.request.max\_attempt** is used to control the maximum number of unsuccessful attempts that a user can reset or change their password before being locked out for a specified period of time.
-   **[Limit Allowed Number of Failed Login Attempts Before Lockout](sc-managing-failed-login-attempts.md)**  
Two script actions are available that enable a site administrator to manage the number of times a user can provide an incorrect password before being locked out from the ServiceNow AI Platform. You can enable either of these script actions to manage failed login attempts.
-   **[Maximize failed login unlock timeout duration \[Updated in Security Center 1.3\]](sc-managing-unlock-timeout-after-failed-logins.md)**  
A script action is available that enables site administrators to manage the number of times a user can provide an incorrect password before being locked out from the ServiceNow AI Platform. You can enable this script action to manage failed login attempts.
-   **[Maximize reset password request retry window duration](sc-reset-password-request-retry-window.md)**  
The **password\_reset.request.retry\_window** property controls the number of minutes before the count for password reset attempts refreshes.
-   **[Maximize reset password request unlock window duration](sc-reset-password-request-unlock-window.md)**  
The **password\_reset.request.unlock\_window** property controls the number of minutes a user must wait to start a reset request after the last successful unlock account action.
-   **[Maximize reset password SMS complexity](sc-reset-password-sms-complexity.md)**  
The **password\_reset.sms.default\_complexity** property controls the minimum required SMS code verification size required during password reset.
-   **[Maximize reset password SMS pause window duration](sc-reset-password-sms-pause-window.md)**  
Manage the time duration in minutes that a user must wait before they can request a new password reset code.
-   **[Maximize reset password verification delay duration](sc-reset-password-verification-delay.md)**  
Configure the delay, in milliseconds, that a user must wait before submitting a new password reset request.
-   **[Minimize external user registration link expiration duration](sc-external-user-registration-link-expiration.md)**  
Manage the number of days that a registration link can be accessed.
-   **[Minimize reset password max SMS per day](sc-reset-password-max-sms-per-day.md)**  
Manage the maximum number of SMS codes sent for verification per day by user.
-   **[Minimize failed login attempts for high assurance sessions](sc-minimize-failed-login-attempts-for-high-assurance-sessions.md)**  
Decrease the likelihood of a brute force attack by minimizing failed login attempts for high assurance sessions.
-   **[Minimize reset password request expiration duration](sc-reset-password-request-expiration.md)**  
The **password\_reset.request.expiry** denotes the time period in minutes during which a user must perform the password reset process.
-   **[Minimize reset password request success window duration](sc-reset-password-request-success-window.md)**  
The **password\_reset.request.success\_window** property controls the number of minutes a user must wait to reset or change their password again after successfully resetting the password. The user will be blocked to reset the password again for the specified duration.
-   **[Minimize reset password SMS expiry duration](sc-reset-password-sms-expiracy.md)**  
Control the number of minutes remaining before the SMS code expires.
-   **[Minimize one-time out of band verifier lifetime duration \[Updated in Security Center 1.3\]](sc-short-one-time-out-of-band-verifier-lifetime.md)**  
Manage the time duration for out-of-band verifiers.
-   **[Minimize SAML notBefore or notOnOrAfter constraint duration \[Updated in Security Center 1.3 and 1.5\]](sc-saml-notbefore-or-notonorafter-constraint.md)**  
Configure this property to add a grace period in which SAML requests and responses are considered valid.
-   **[Notify users during password reset/change process \[Removed in Security Center 1.5\]](sc-password-reset-change-notification-process.md)**  
Use this property to enable end users to reset or change passwords using a self-service process.
-   **[Prohibit Use of KBA as Single Factor for AI Voice](sc-prohibit-use-of-kba-as-single-factor-for-ai-voice.md)**  
Use a system property to prevent Knowledge Based Authentication \(KBA\) from being the only factor of authentication required to authenticate to the platform for AI voice.
-   **[Reduce allowed bypasses for multifactor setup](sc-reduce-allowed-bypasses-for-multifactor-setup.md)**  
Decrease the window of time an account is at risk of compromise by reducing allowed bypasses for multifactor setup.
-   **[Remove credentials from Welcome page](sc-remove-credentials-welcome-page.md)**  
Modify the default content on the Welcome page to remove the default credentials.
-   **[Require CAPTCHA for guest walk-up experience in customer service application](sc-require-captcha-for-guest-walk-up-experience-in-customer-service-application.md)**  
The CAPTCHA for the Guest Walk-up experience prevents unauthenticated guest users to create bookings by requiring users to complete a CAPTCHA verification.
-   **[Require obfuscation of classic mobile app UI \[Updated in Security Center 1.3\]](sc-classic-mobile-app-ui-obfuscation.md)**  
Use the **glide.ui.m.blur\_ui\_when\_backgrounded** property to obfuscate all fields from the snapshot as the image is saved during the backgrounding process.
-   **[Require obfuscation of mobile app UI](sc-mobile-app-ui-obfuscation.md)**  
Configure the **glide.sg.blur\_ui\_when\_backgrounded** property so that the UI of the app is blurred when the app is running in the background.
-   **[Require Minimum and Maximum Password Length](sc-set-minimal-password-length.md)**  
Set minimum and maximum password lengths to avoid compliance issues and reduce the risk of a successful brute force attack
-   **[Set OTP lifetime for password reset to 1 hour \[Updated in Security Center 2.0\]](sc-set-otp-lifetime-for-password-reset-to-12-hours-or-less.md)**  
Control the time duration of the link in the password reset email.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

