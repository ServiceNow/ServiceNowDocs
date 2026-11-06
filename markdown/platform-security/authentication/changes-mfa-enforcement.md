---
title: Changes due to the Multi-factor Authentication enforcement
description: Information about the changes that are expected due to the MFA enforcement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/authentication/changes-mfa-enforcement.html
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [MFA enforcement, Multi-factor authentication, Access Management]
---

# Changes due to the Multi-factor Authentication enforcement

Information about the changes that are expected due to the MFA enforcement.

MFA enforcement changes that are expected as follows:

-   No impact on integration.
-   Users who have already enrolled MFA continue to be challenged with MFA during local login.
-   If a user has not set up MFA yet, after the Yokohama upgrade, they’ll be initially exempted from undergoing MFA for a certain period during which they can enroll MFA.
-   If the user fails to self-enroll, then they have MFA enforced on the completion of the exemption period \(default 30 days\) and must set up MFA.
-   After 90 Days, MFA will be enforced by default. There will be no self-enrollment period for first-time logins after 90. Administrators can configure this period.

As an administrator, you can prepare for the MFA enforcement based on the following:

-   Review the MFA Context Policy configuration and adjust the policy conditions according to your business requirements.
-   Add the exempted group provided by default, if there are any other users who must be exempted.
-   Review the MFA Enforcement Properties and adjust based on your requirements. To learn more, see [Multi-factor Authentication enforcement properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/mfa-enforcement-properties.md).

## MFA enforcement scenario after 30 days of the MFA enforcement

-   **Scenario 1 for Acme Corp**: In the instance, if the user doesn’t have an active MFA policy. Imagine Sarah uses local authentication to access an instance. On upgrading to the Yokohama release during login, a message to enroll in MFA is displayed. There's 30 days to complete this setup. If Sarah doesn’t complete the setup, after 30 days, the account requires MFA to log in, and won’t be able to access it until MFA is set up.
-   **Scenario 2 for Acme Corp**: In the instance, Anita was already MFA along with local authentication. Anita continues to require MFA without the 30-day self-enrollment window.
-   **Scenario 3 for Acme Corp**: In the instance, Olivia uses Single Sign-On \(SSO\) for authentication. There's no impact on the login experience, and Olivia isn’t enforced for MFA.
-   **Scenario 4 for Globex Corp**: In the instance, if a user already had an MFA policy requiring - MFA for all local login attempts outside the company’s trusted network. On upgrading to the Yokohama or a later release, MFA enforcement behavior for user logins remain the same.

## Changes on upgrade to Zurich

When you upgrade to Zurich, a fix script runs if both of the following were true before the upgrade:

-   The **glide.authenticate.auth.policy.enabled** property was set to `false`.
-   A Pre or Post Authentication Policy Context was configured.

The script makes the following changes:

-   Sets the **Default Policy** of the context to **Deny Policy**. See [Authentication policy contexts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/auth-policy-contexts.md) for what each option means.
-   Points the context to an inactive placeholder policy, **Demo Post Auth policy** or **Demo Pre Auth policy**, in place of the policy you configured.
-   Sets **glide.authenticate.auth.policy.enabled** to `true`.
-   Sets **glide.authenticate.multifactor** to `true` and rewrites several **glide.authenticate.multifactor.\*** properties. See [Multi-factor Authentication enforcement properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/mfa-enforcement-properties.md).
-   Schedules a job that deletes existing MFA enrollment data. Users must enroll in MFA again.

The result depends on the instance. An upgrade can change a Production instance and leave a Sub-production instance unchanged if the Sub-production instance already had **glide.authenticate.auth.policy.enabled** set to `true`.

After the upgrade, a policy you configured can stop being enforced. For example, an IP allow list might stop applying to SSO logins. Re-associate your policy with the context to restore it.

To confirm what the upgrade changed, search the system log for `fix_mfa_enforcement`. You can also check **Upgrade History** for `z_fix_mfacontext_upgrade`.

