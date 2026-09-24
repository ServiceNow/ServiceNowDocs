---
title: Updated hardening settings for baseline version 9.0
description: Some hardening settings have been updated with the release of Security Center baseline version 9.0.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/updated-hardening-settings-for-baseline-version-nine.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 41
breadcrumb: [Updated hardening settings, Baseline versions, Hardening settings, Platform Security]
---

# Updated hardening settings for baseline version 9.0

Some hardening settings have been updated with the release of Security Center baseline version 9.0.

<table id="table_baseline_v8_changes"><thead><tr><th>

Documentation

</th><th>

Updates

</th></tr></thead><tbody><tr><td>

[Disable AJAXEvaluate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-ajaxevaluate.md)

</td><td>

Default value -   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Enforce field-level ACLs on records created from the filtered list view UI query string](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-field-level-acls-on.md)

</td><td>

-   Short description
    -   \(Old\)

Enforce field-level ACLs on records created from the query string of the Filtered List view UI of a table

    -   \(New\)

Enforce field ACLs on records created from Filtered List view UI query string

-   Functional impact
    -   Old

When com.glide.acl\_check\_all\_filter\_on\_new is set to true, then ACLs may prevent fields included in the filter query string from affecting the value of fields in a created record when the creation is triggered from the list view UI of a table. However, this previous behavior was incorrect as it bypassed ACLs and allowed user without creation access to a field to modify its value.

    -   New

When the com.glide.acl\_check\_all\_filter\_on\_new is set to true, ACLs are enforced for fields included in the filter query string during record creation from the list view UI. This prevents users without create access from modifying protected fields through filter parameters.


</td></tr><tr><td>

[Escape XML markup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-escape-xml.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Turn off verbose SQL error messages for import processor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-turn-off-verbose-sql-error-messages-for-import-processor.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Require authorization for excel requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-excel-request-authorization.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enable protected tables plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-protected-tables-plugin.md)

</td><td>

-   Remediation
    -   \(Old\)

Set the Glide Property com.glide.security.protected\_table.enabled to true. This requires a user with the security\_admin role.

    -   \(New\)

Enable table protection through the guided activation flow:

        1.  Navigate to the Protected Tables plugin's guided activation flow.
        2.  Complete the activation process to enable table protection. Only users with the security\_admin role can activate this control.
Important: Don't enable this control by directly editing the property com.glide.security.protected\_table.enabled outside that guided activation flow.

Default protected tables: syslog, syslog\_transaction, sys\_outbound\_http\_log, sysevent, sys\_audit, sys\_push\_notification, protected\_table\_configuration, syslog\_app\_scope

To extend protection to additional tables, configure insert, update, and delete protection rules for each additional table and operation in the Protected Table Configuration list.

-   Security risk
    -   Old

Log integrity must be maintained to allow discovery of malicious activity.

    -   New

When disabled \(the default\), Protected Tables protections don't apply, allowing maintenance-role users to modify or delete critical audit and security logs without detection. An attacker with maintenance credentials could tamper with syslog, sys\_audit, and sysevent entries to cover malicious activity and evade forensic investigation. Disabling this property compromises the audit trail needed to detect and investigate security incidents.

-   Functional impact
    -   Old &lt;blank&gt;
    -   New

Enabling the com.glide.security.protected\_table.enabled property causes create, update, and delete attempts on tables in the Protected Table Configuration list to be evaluated. Depending on that table's configured protection level, the attempt is blocked, logged, or ignored. The level shipped per table is not fixed. It depends on how long the Protected Tables plugin has been installed, so confirm the actual values on your instance rather than assuming a table is blocking. One exception holds everywhere: insert attempts on sysevent are never blocked or logged, since normal processing inserts sysevent records continuously. A refused attempt shows the message "Modifications to &lt;table&gt; have been refused due to the Protected Table configuration. Please contact your system administrator." Any integration or business rule currently writing to or deleting from a blocking table will start failing once this property is enabled.

-   Default value
    -   Old &lt;blank&gt;
    -   New

false


</td></tr><tr><td>

[Enable Jelly JS interpolation protection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-jelly-js-interpolation-protection.md)

</td><td>

-   Functional impact
    -   Old &lt;blank&gt;
    -   New

Enabling this property causes the platform to reject Jelly JavaScript expressions that aren't explicitly recognized as safe or marked as SAFE. Instance owners should test custom UI pages, macros, and portal widgets that use Jelly-interpolated JavaScript expressions after making this change, and confirm that legitimate expressions continue to render as expected. Custom Jelly content that relies on dynamic, unmarked expressions may need to be updated to use the SAFE designation to continue functioning.

-   Default value
    -   Old &lt;blank&gt;
    -   New

true in Australia and newer, false prior

-   Fallback value
    -   Old

false

    -   New

true in Australia and newer, false prior


</td></tr><tr><td>

[Restrict permissions for CMDB model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-restrict-permissions-cmdb-model.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-chat-server-debugging.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-chat-server-debugging.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Escape scripts in scratchpad](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-escape-scratchpad.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Disable locked form elements debugging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-locked-form-elements-debugging.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Configure service portal widgets table allow list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-configure-service-portal-widgets-table-allow-list.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

'' \(empty string\)


</td></tr><tr><td>

[Minimize session activity timeout duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-activity-timeout.md)

</td><td>

-   Description
    -   \(Old\)

This property determines the user session timeout. This determines how long a user session stays active. If glide.ui.session\_timeout is not set to the recommended value of "60" minutes or less, then the session may stay valid for long even without activity. This could provide too large of a time window to enable session hijacking attacks.

    -   \(New\)

The glide.ui.session\_timeout property controls the inactive session timeout for authenticated users, specified in minutes. If this property is not set to the recommended value of 30 minutes or less, the session may remain valid for extended periods without user activity.

A long session timeout allows inactive sessions to remain valid for extended periods, increasing the chance that an attacker could hijack the session before it expires.

-   Remediation
    -   \(Old\)

Ensure the property glide.ui.session\_timeout is set to 60 or less.

    -   \(New\)

1. Navigate to /sys\_properties\_list.do on the instance.

2. Ensure the glide.ui.session\_timeout property does not exist in the sys\_properties table or is set to 30 minutes or less.

-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Reducing the glide.ui.session\_timeout property lowers the amount of idle time allowed before a user's session ends automatically, requiring re-authentication. Users who leave a session idle longer than the configured value \(for example, while completing a long form, waiting on an approval, or stepping away between tasks\) will be logged out and must sign in again.

Administrators should verify that long-running interactive workflows still complete comfortably within the new timeout window. Confirm that any automation or integration currently relying on a long-lived interactive UI session is migrated to a dedicated authentication method such as OAuth or a service account.

-   Dependencies and prerequisites
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The glide.ui.session\_timeout property is capped by the static property glide.ui.max\_session\_timeout, which limits the maximum effective value to 1440 minutes.

-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

integer

-   Default value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

30


</td></tr><tr><td>

[Set automatic token cleanup for token credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-set-automatic-token-cleanup-for-token-credentials.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true, 7


</td></tr><tr><td>

[Prevent impersonating user from viewing application data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-prevent-impersonating-user-from-viewing-application-data.md)

</td><td>

Plugin applicability-   \(Old\) &lt;blank&gt;
-   \(New\)

sn\_opp\_market, sn\_jny, sn\_imt\_vaccine, sn\_imt\_health\_test, sn\_hr\_core, sn\_egd\_goals, sn\_egd\_core, sn\_egd\_act, sn\_em, sn\_talent\_aia, sn\_ecn


</td></tr><tr><td>

[Require authorization for JSONv2 request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-jsonv2-request-authorization.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Implement the x-frame-options: SAMEORIGIN security header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-x-frame-options-sameorigin.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Maximize reset password SMS complexity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-reset-password-sms-complexity.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

6


</td></tr><tr><td>

[Limit integrations' active session life span](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-limit-integrations-active-session-life-span.md)

</td><td>

-   Description
    -   \(Old\)

This configuration will enforce max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes and the value of zero will disable timing out the active sessions. A larger maximum lifespan could allow an attacker to persist in a stolen session for longer, increasing the scope of a security incident. This particular property is limited to integrations that have low-privilege access to an instance.

    -   \(New\)

The **glide.integrations.active.session.life\_span** property enforces the maximum lifespan on active integration HTTP sessions, regardless of session inactivity. The configured value is in minutes. A value of zero disables the lifespan limit entirely, allowing sessions to persist indefinitely until the inactive timeout fires. This particular property is limited to integrations that have low-privilege access to an instance.

A larger maximum lifespan allows an attacker to persist a stolen session for longer, increasing the scope of a security incident.

-   Remediation
    -   \(Old\)

Set the Glide Property 'glide.integrations.active.session.life\_span' to a value greater than 0 and less than or equal to 720.

    -   \(New\)

1. Navigate to /sys\_properties\_list.do on the instance.

2. Ensure the **glide.integrations.active.session.life\_span** property exists and is set to a value greater than 0 and less than or equal to 720 minutes.

-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Integration sessions that exceed the configured lifespan are silently invalidated and reissued a new session ID. The integration user sees no error, but any session-scoped state accumulated during that session is lost and starts fresh.

-   Dependencies and prerequisites
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This control interacts with the **glide.integration.session\_timeout** property, which controls the integration idle-session timeout duration. The platform requires the active session maximum lifespan to be greater than or equal to the integration idle timeout. If the active session lifespan is configured to a value lower than the idle-session timeout, the platform automatically increases the effective lifespan to match the idle-session timeout and logs a warning message.


</td></tr><tr><td>

[Limit concurrent sessions across all nodes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-limit-concurrent-sessions-across-all-nodes.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Minimize reset password SMS expiry duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-reset-password-sms-expiracy.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

5


</td></tr><tr><td>

[Double check inbound transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-double-check-inbound-transactions.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

true


</td></tr><tr><td>

[Disable soap fault stack trace display](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-soap-fault-stack-trace-display.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

false


</td></tr><tr><td>

[Limit Invalid Password Reset Attempts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-reset-password-request-max-attempts.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

3


</td></tr><tr><td>

[Anti-CSRF token validation time](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-anti-csrf-token-validation-time.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

86400


</td></tr><tr><td>

[Require CAPTCHA for guest walk-up experience in customer service application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-require-captcha-for-guest.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

true


</td></tr><tr><td>

[Require authorization for csv requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-require-authorization-for-csv-requests.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

true


</td></tr><tr><td>

[Enable Identity and Access Audit tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-identity-and-access-audit-tool.md)

</td><td>

Configuration name-   \(Old\)

glide.identity.security.audit.enabled

-   \(New\)

glide.identity.security.audit.enabled, com.glide.security.audit


</td></tr><tr><td>

[Disable public access to favorites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-public-access-to-favorites.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

false


</td></tr><tr><td>

[Proactively invalidate sessions after defined durations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-proactively-invalidate-inactive-sessions.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

false


</td></tr><tr><td>

[Escape JavaScript \[Updated in Security Center 1.3\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-escape-javascript.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

true


</td></tr><tr><td>

[Enable HTTP Only Cookie Flag](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-http-only-cookie-flag.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

true


</td></tr><tr><td>

[Enforce SOAP request strict security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-soap-request-strict-security.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

true


</td></tr><tr><td>

[Block rooted or jailbroken mobile devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-block-rooted-or-jailbroken-mobile-devices.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

false


</td></tr><tr><td>

[Enforce strict elevate privilege](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-strict-elevate-privilege.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

true


</td></tr><tr><td>

[Enable the hardened java security manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-the-hardened-java-security-manager.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

com.glide.sys.security.ContextualSecurityManager


</td></tr><tr><td>

[Disable legacy JQuery behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-legacy-jquery-behavior.md)

</td><td>

Default value-   \(Old\)

&lt;blank&gt;

-   \(New\)

false


</td></tr><tr><td>

[Enable account recovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-account-recovery.md)

</td><td>

-   Description
    -   \(Old\)

This property controls the account recovery feature, which binds the ability to bypass single sign-on to specifically designated administrators. If "glide.sso.acr.enabled" is not set to the recommended value of "true", then the local interactive log-ins \(username or password based\) will be remain enabled when single sign-on is enabled on the instance.

    -   \(New\)

The glide.sso.acr.enabled property controls whether the Account Recovery \(ACR\) feature is available on an instance configured for Single Sign-On \(SSO\) authentication. When set to the recommended value of "true", the platform blocks turning on multi-SSO until account recovery is enabled. At least one user account must be enrolled for it. It also confines any session authenticated through the recovery path to writing only SSO- and account-recovery-related configuration. This preserves a controlled, auditable path back into the system for users who lose access to their normal SSO credentials.

-   Security risk
    -   \(Old\)

Eliminating local interactive log-ins reduces the potential for unauthorized access to the instance.

    -   \(New\)

Without an account recovery path, a user who loses access to their normal sign-in method has no supported way back into the system. That gap commonly pushes administrators and help desks toward manual, ad hoc identity verification workarounds to restore access. Those workarounds are a well-known target for social engineering and account takeover because they bypass the organization's standard authentication controls. Leaving a recovery path unavailable increases the risk of unauthorized account access and loss of control over who can regain entry to affected accounts.

-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Enabling this control doesn't disable SSO. It requires that an account-recovery path exist and restricts write access on a recovery-authenticated session to SSO- and recovery-related properties only. Admin users that have never configured account recovery, or that have zero users enrolled, will be blocked from turning on Multi-SSO until at least one user opts in. Users may test the Multi-SSO activation flow and the account-recovery login flow when removing or disabling ACR-enrolled users.

-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Boolean

-   Default value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

true


</td></tr><tr><td>

[Enforce strict user image upload](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-strict-user-image-upload.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Verify certificate chain and hostname](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-verify-certificate-chain-and-hostname.md)

</td><td>

-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the com.glide.communications.httpclient.verify\_hostname property is set to true, an outbound HTTPS connection is rejected if the remote host's certificate doesn't match the requested hostname or its certificate chain can't be validated. Outbound integrations to hosts with a mismatched or misconfigured certificate will fail to connect once this property is set to true.

-   Dependencies and prerequisites
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The "com.glide.communications.httpclient.verify\_hostname" property governs hostname and certificate chain validation independently of the "com.glide.communications.httpclient.verify\_revoked\_certificate" property, the overall gate for certificate revocation checking.

-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Boolean


</td></tr><tr><td>

[Minimize session window timeout duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-window-timeout.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

15


</td></tr><tr><td>

[Maximize reset password verification delay duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-reset-password-verification-delay.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

1000


</td></tr><tr><td>

[Log session audit events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-log-session-audit-events.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Ensure archive table ACLs are checked](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-ensure-archive-table-acls-are-checked.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enforce HTML sanitization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-check-unsanitized-html.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

enforce


</td></tr><tr><td>

[Enable CAPTCHA for external user registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-captcha-external-user-registration.md)

</td><td>

-   Rule Script: Script has been updated to improve detection accuracy
-   Default value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

true


</td></tr><tr><td>

[Require AJAXGlideRecord ACL checking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enabling-ajaxgliderecord-acl-checking.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Require Minimum and Maximum Password Length](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-set-minimal-password-length.md)

</td><td>

Rule script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable password reset policy checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-password-reset-policy-checks.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enforce oauth state parameter validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-oauth-state-parameter-validation.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Restrict Global App Development by Role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-restrict-global-app-development-by-role.md)

</td><td>

ODefault value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Restrict knowledge bases access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-restrict-knowledge-bases-access.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Timeout guest sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-timeout-guest-sessions.md)

</td><td>

-   Description
    -   \(Old\)

Use the glide.guest.session\_timeout system property to control the inactive session timeout for unauthenticated users. By default, the value of this property is 30 minutes. If there are availability concerns from persisting too many sessions in memory, the value of this property can be lowered to 5. Avoid setting this property greater than 30, as large timeout values increase the number of sessions persisted by the instance, and may cause minor availability concerns.

Avoid setting this property greater than 30. Large timeout values increase the number of sessions persisted by the instance, and may cause minor availability concerns.

    -   \(New\)

The **glide.guest.session\_timeout** property controls the inactive session timeout for unauthenticated \(guest\) users, specified in minutes. New instances are provisioned with a default of 5 minutes. If the property does not exist in the sys\_properties table, the effective value defaults to 0. When set to 0, the guest-specific override is turned off and the session instead uses the general UI session timeout \(**glide.ui.session\_timeout**\).

Setting the **glide.guest.session\_timeout** property greater than 30 minutes increases the number of sessions persisted by the instance, which may cause minor availability concerns.

-   Remediation
    -   \(Old\)

Ensure the Glide Property 'glide.guest.session\_timeout' is configured to the default value of 30. In the rare case there are availability concerns from persisting too many sessions in memory, the value of this property can be lowerered to 5.

    -   \(New\)

1. Navigate to /sys\_properties\_list.do on the instance.

2. Ensure the **glide.guest.session\_timeout** property exists and is set to a value greater than 0 and less than or equal to 30 minutes.

-   Dependencies and prerequisites
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The **glide.guest.session\_timeout** property interacts with the **glide.ui.session\_timeout** property. When **glide.guest.session\_timeout** is set to 0, guest sessions don't receive an independent idle timeout — they fall back to using **glide.ui.session\_timeout** instead.

-   Default value
    -   \(Old\)

30

    -   \(New\)

5


</td></tr><tr><td>

[Restrict flow context read access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-restrict-flow-context-read-access.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Minimize external user registration link expiration duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-external-user-registration-link-expiration.md)

</td><td>

-   Rule Script: Script has been updated to improve detection accuracy
-   Default value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

3


</td></tr><tr><td>

[Require authorization for SCHEMA requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-schema-request-authorization.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enable IAM and boundary checks for Amazon Bedrock access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-multiple-permission.md)

</td><td>

Short description-   \(Old\)

Enable multiple \(permission policy and boundary\) checks to ensure that the Role is privileged in AWS/Bedrock

-   \(New\)

Enable IAM and Boundary Checks for Amazon Bedrock access


</td></tr><tr><td>

[Enable UserCookie version 3.1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-usercookie-version-3-1.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Limit guest's active session life span](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-limit-guests-active-session-life-span.md)

</td><td>

-   Description
    -   \(Old\)

This configuration will enforce max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes and the value of zero will disable timing out the active sessions. This particular property is limited to Guest users, which have low privilege access to an instance.

    -   \(New\)

The **glide.guest.active.session.life\_span** property enforces a maximum lifespan on active guest HTTP sessions, regardless of the session activity. The configured value is in minutes. A value of zero disables the lifespan limit entirely, allowing sessions to persist indefinitely until the inactive timeout fires. Guest users are unauthenticated users who access the instance without logging in.

-   Rule script: Script has been updated to improve detection accuracy
-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Guest HTTP sessions that exceed the configured lifespan are silently invalidated and reissued a new session ID. The guest user sees no error or logout screen, but any session-scoped state \(for example, in-progress form data, embedded portal widget context, or session-based rate limiting\) accumulated during that session is lost and starts fresh. Legitimate guest users on long-running but otherwise idle browser tabs may need to reload the page after the configured interval elapses.

-   Dependencies and prerequisites
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This control interacts with the **glide.guest.session\_timeout** property, which controls the guest idle-session timeout duration. The platform requires the active session maximum lifespan to be greater than or equal to the idle timeout. If the active session lifespan is configured to a value lower than the idle-session timeout, the platform automatically increases the effective lifespan to match the idle-session timeout and logs a warning message.

-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

integer


</td></tr><tr><td>

[Configure service portal widgets allow list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-configure-service-portal-widgets-allow-list.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

''


</td></tr><tr><td>

[Require authorization for XML output requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-xml-output-authorization.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enforce production instance behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-production-instance-behavior.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Restrict HR case updates from personal emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-restrict-hr-case-updates-from.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Restrict JSONP requests to trusted URLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-restrict-jsonp-requests-to-trusted-urls.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Minimize reset password request success window duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-reset-password-request-success-window.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

1440


</td></tr><tr><td>

[Activate role based multi-factor authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-role-based-multi-factor-authentication.md)

</td><td>

-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Users assigned the admin, security\_admin, or user\_admin role will be prompted for a second authentication factor at login, and their password. Users without one of these roles are unaffected.

-   Dependencies and prerequisites
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

For role-based MFA enforcement to take effect, **glide.authenticate.multifactor** must be set to "true" and **multi\_factor\_criteria** must be active.

-   Default value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

false,"The multi\_factor\_criteria table record with sys\_id d427668b73003300fdbd04fbc4f6a7b6 is shipped in a zbooted instance but is not set to active"


</td></tr><tr><td>

[Require authorization for RSS requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-rss-request-authorization.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Apply domain separation on dot walked fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-apply-domain-separation.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Disable logger for low privilege users in script sandbox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-glide-security-logger-no-loggining-for-sandbox.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Maximum allowed attachment size](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-max-allowed-attachment-size.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

1024


</td></tr><tr><td>

[Maximize reset password request unlock window duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-reset-password-request-unlock-window.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

1440


</td></tr><tr><td>

[Require authorization for PDF requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-require-authorization-for-pdf-requests.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enable antivirus scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-antivirus-scan.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Prevent empty ACL creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-prevent-empty-acl-creation.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Disable Multi-SSO debugging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-multisso-debugging.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Escape Excel formulas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-escape-excel-formula.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Disable JavaScript tags in embedded HTML](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-allow-javascript-tags-in-embedded-html.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Prevent usage of 3DES keys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-prevent-usage-of-3des-keys.md)

</td><td>

Dependencies &amp; prerequisites-   \(Old\) &lt;blank&gt;
-   \(New\)

The property **glide.security.3des.removal\_job\_status** acts as a readiness gate. The scheduled job walks through deactivating/rotating out old 3DES static keys, and that job reports its progress via this status property. Until that job reports it's done \(KEYS\_DEACTIVATED or RESUPPLIED\), it's not yet possible to flip **glide.security.3des.static\_keys\_usable** to false, because doing so prematurely could break decryption of data still encrypted with those static keys.


</td></tr><tr><td>

[Restrict downloadable MIME types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-downloadable-mime-type-denylist.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Prevent inactive users from logging in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-prevent-inactive-users-from-logging-in.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enable HTML sanitizer within Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-html-sanitizer.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enable policy based session access for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-policy-based-session-access-for-mobile.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enable report view ACLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-report-view-acls.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Restricted Binding functionality in Case Bearer authorization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-restricted-binding-functionality-in-case-bearer-authorization.md)

</td><td>

-   Rule script: Script has been updated to improve detection accuracy
-   Default value
    -   \(Old\)

false

    -   \(New\)

true


</td></tr><tr><td>

[Maximize reset password request retry window duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-reset-password-request-retry-window.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

1440


</td></tr><tr><td>

[Deny by default with empty ACLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-security-manager-default-deny.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

deny


</td></tr><tr><td>

[Disable unauthenticated published reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-unauthenticated-published-reports.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Minimize SMTP Recipient Quantity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-max-smtp-recipients.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

100


</td></tr><tr><td>

[Clear pasteboard when app backgrounds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-require-clearing-pasteboard-when-backgrounding-mobile-application.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Restrict uploaded MIME types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-upload-mime-type-restriction.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enable ACLs for Encoded Query in Simple List Widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-acls-for-encoded-query-in-simple-list-widget.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Require Authorization for XSD Requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-xsd-request-authorization.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enable SMS code notification for enrollment and verification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-sms-code-notification-for-enrollment-and-verification.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Use of secure insert multiple operation within import set API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-use-of-secure-insert-multiple-operation-within-import-set-api.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Define restricted downloadable MIME types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-downloadable-mime-types.md)

</td><td>

-   Description
    -   \(Old\)

If glide.ui.attachment.download\_mime\_types does include dangerous MIME types such as text/html, image/svg ,image/svg+xml,application/xml, then dangerous files could be rendered inline in the browser, which could lead to Cross Site Scripting attacks \(XSS\). This property is the list of comma-separated attachment mime types, which won't render inline in the browser. For example, including text/html forces HTML files to be downloaded to the client as attachments rather than viewed inline in the browser. Maintaining this list properly prevents cross-site scripting attacks. If the glide.ui.attachment.download\_mime\_types system property doesn't include dangerous MIME types such as "text/html, image/svg,image/svg+xml,application/xml", then dangerous files could be rendered inline in the browser. This can lead to Cross Site Scripting \(XSS\) attacks. This check is only relevant when glide.ui.attachment.force\_download\_all\_mime\_types is set to false. This property is a list of comma-separated attachment MIME types, which don't render inline in the browser. For example, including text/html forces HTML files to be downloaded to the client as attachments rather than viewed inline in the browser.

    -   \(New\)

If the glide.ui.attachment.download\_mime\_types property doesn't include dangerous MIME types such as text/html, image/svg, image/svg+xml, application/xml, and application/xhtml+xml, then those dangerous files could be rendered inline in the browser, which could lead to Cross-Site Scripting \(XSS\) attacks. This property is a comma-separated list of attachment MIME types that are downloaded to the client and don't render inline in the browser. For example, including text/html forces HTML files to be downloaded to the client as attachments rather than viewed inline in the browser. Maintaining this list properly by including all dangerous MIME types prevents Cross-Site Scripting attacks. Note: This property's protection is only relevant when the glide.ui.attachment.force\_download\_all\_mime\_types property is set to false.

-   Fallback value
    -   \(Old\)

text/html,image/svg,image/svg+xml,application/xml

    -   \(New\)

''


</td></tr><tr><td>

[Verify certificate revocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-verify-certificate-revocation.md)

</td><td>

-   Functional impact
    -   \(Old\)

&lt;blank&gt;

    -   \(New\)

When the com.glide.communications.httpclient.verify\_revoked\_certificate is set to true, every outbound HTTP request over TLS has its certificate checked for revocation using OCSP or CRL, as governed by the other properties in this family. When this property is set to "false", no revocation checking is performed at all for outbound TLS connections, regardless of how the other certificate-revocation properties are configured.

-   Data type
    -   \(Old\)

&lt;blank&gt;

    -   \(New\)

Boolean

-   Default value
    -   \(Old\)

&lt;blank&gt;

    -   \(New\)

true


</td></tr><tr><td>

[Honor admin override ACLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-honor-admin-override-acls.md)

</td><td>

-   Description
    -   \(Old\)

ACLs are evaluated cumulatively. If there are a number of ACLs on any given field and the Admin Overrides option is false \(not selected\) on one of them, then the effective admin overrides for all the ACLs are considered to be false. This causes admins to be unable to pass even the ACL where the override should be in effect. If "glide.security.admin.override.accessterm" is not set to the recommended value of "true" then, even if one of the ACL terms under the ACL rule is "Admin overrides" false, the entire rule evaluates to false.

    -   \(New\)

The "glide.security.admin.override.accessterm" property controls how the platform decides whether an administrator can bypass an access rule when a resource \(a table, a field\) has more than one access rule applied to it. Each individual access rule can be configured to grant or deny an admin override on its own. When this property is set to its recommended value of true, the per-rule setting is honored individually. A rule explicitly configured to deny an admin override still blocks the administrator even if another rule on the same resource permits one. When set to "false", the bypass decision is instead made at a broader, combined level. This can let an administrator through even though one of the applicable rules was specifically configured to block the override.

-   Security risk
    -   \(Old\)

ACLs with conflicting "Admin overrides" settings may cumulatively evaluate to false, potentially preventing administrators from accessing fields they should have access to and inadvertently causing denial of access to critical data.

    -   \(New\)

When access checks are evaluated coarsely, a privileged user can access a resource despite rules set to deny override. This allows the most restrictive protection to be ignored in favor of a more permissive rule on the same resource. Protected data can be set to readable or writable, risking unauthorized access to sensitive information.

-   Functional impact
    -   \(Old\)

&lt;blank&gt;

    -   \(New\)

Changing this property to true affects only elevated-admin access decisions on resources governed by more than one access rule; regular users and single-rule resources see no behavior change. After the change, test contextual security scenarios where an admin role is granted access to a field or record through multiple layered rules, confirming that a rule explicitly configured to deny override still blocks the admin as expected. No service availability impact is expected since the change only tightens an authorization decision path.

-   Data type
    -   \(Old\)

&lt;blank&gt;

    -   \(New\)

Boolean

-   Default value
    -   \(Old\)

&lt;blank&gt;

    -   \(New\)

true

-   Fallback value
    -   \(Old\)

true

    -   \(New\)

false


</td></tr><tr><td>

[Set safe content security policy for SVG files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-set-safe-content-security-policy-for-svg-files.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Check UI action conditions before execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-check-ui-action-conditions-before-execution.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Disable inbound emails for locked out users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-inbound-emails-locked-out-users.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Rotate HTTP session identifiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-rotate-http-session-identifiers.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Escape jelly script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-escape-jelly.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Set Xframe options to prevent embedding third-party websites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-xframe-options.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

sameorigin


</td></tr><tr><td>

[Require authorization for WSDL request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-wsdl-request-authorization.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Minimize absolute session timeout duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-absolute-session-timeout.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

30


</td></tr><tr><td>

[Limit the policy-based mobile refresh token interval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-limit-policy-based-session-access-mobile-refresh.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

1800


</td></tr><tr><td>

[Control lockout time for invalid password reset attempts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-reset-password-request-max-attempts-window.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

1440


</td></tr><tr><td>

[Limit max subscriptions per user per day](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-limit-max-subscriptions-per-user-per-day.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

500


</td></tr><tr><td>

[Restrict access to emails with empty target table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-restrict-access-to-emails-with-empty-target-table.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Enable CAPTCHA in password reset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-captcha-in-password-reset.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Validate SOAP content type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-soap-content-type-checking.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Disable secure cookie debugging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-secure-cookie-debugging.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Limit max comments per user per day](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-limit-max-comments-per-user-per-day.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

500


</td></tr><tr><td>

[Validate remote host](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-validate-remote-host.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Require authorization for data broker rest API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-data-broker-rest-api-authorization.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Require authorization for script requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-script-request-authorization.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Disallow infected file download](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disallow-infected-files-download.md)

</td><td>

-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Users can download non-scanned attachments if the antivirus service is down or unreachable.

-   Default value
    -   \(Old\)

true

    -   \(New\)

false


</td></tr><tr><td>

[Require authentication by default for client-callable script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-privacy-on-client-callable-script-includes.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Enforce relative links](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-relative-links.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Require obfuscation of mobile app UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-mobile-app-ui-obfuscation.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Restrict access to GlideSystemUserSession scriptable API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-glidesystemusersession-scriptable-api.md)

</td><td>

Default value-   \(Old\)

true

-   \(New\)

false


</td></tr><tr><td>

[Enable work order management query rules for service organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-work-order-management-query-rules.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Enforce device encryption and passcode requirements \[New in Security Center 1.3\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-device-encryption-and-passcode-requirements.md)

</td><td>

Default value-   \(Old\) &lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Require authorization for SOAP requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-soap-request-authorization.md)

</td><td>

-   Technical Configuration Name
    -   \(Old\)

glide.basicauth.required.soap, glide.soap.require\_ws\_security

    -   \(New\)

glide.basicauth.required.soap,glide.soap.require\_ws\_security

-   Rule script: Script has been updated to improve detection accuracy
-   Security risk
    -   \(Old\)

Unauthenticated access to SOAP export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.

    -   \(New\)

When set to false, both properties allow unauthenticated SOAP requests to map to the guest user and execute without credential validation, enabling unauthorized data export and system operations.

-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Disabling either property relaxes SOAP request authentication requirements. Basic auth and/or WS-Security validation is set to optional, allowing unauthenticated or weakly-authenticated SOAP requests to proceed.

-   Data tyype
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Boolean

-   Default value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

true,false

-   Fallback value
    -   \(Old\)

true,true

    -   \(New\)

true,false


</td></tr><tr><td>

[Enforce application specific ACLs only for application data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-application-specific-acls-only-for-application-data.md)

</td><td>

Added two properties: sn\_tf, sn\_lco\_cmn

</td></tr><tr><td>

[Disable SQL error messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disabling-sql-error-messages.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Minimize entity expansion threshold for GlideXMLUtil scriptable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-setting-entity-expansion-threshold.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

3000


</td></tr><tr><td>

[Disable GlideRecord scope fencing legacy behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-gliderecord-scope-fencing-legacy-behavior.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Restrict Impersonation to Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-restrict-impersonation-to-admin.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Restrict email domains for external user registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-external-user-registration-email-domain-allowlist.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Remove remember me](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-remove-remember-me.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Disable email OTP for multi-factor authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-email-otp-for-multi-factor-authentication.md)

</td><td>

-   Functional impact
    -   \(Old\)&lt;blank&gt;
    -   \(New\)

Users who rely solely on the email one time passcode as their multi-factor authentication method will no longer see that option on the MFA validation screen. They must enroll an alternative factor such as an authenticator app, a hardware security key, or SMS before this property is turned off, otherwise they may be unable to complete login until an administrator enrolls an alternative factor for them.

-   Data type
    -   \(Old\)&lt;blank&gt;
    -   \(New\)

Boolean

-   Default value
    -   \(Old\)&lt;blank&gt;
    -   \(New\)

true


</td></tr><tr><td>

[Disable outbound SSLv2/SSLv3 connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disabling-sslv2-sslv3.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Log user impersonation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-log-user-impersonation.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enable ACLs to Control Live Profile Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-acls-to-control-live-profile-details.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

ACL


</td></tr><tr><td>

[Deny unauthorized access to request items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-deny-unauthorized-access-to-request-items.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

deny


</td></tr><tr><td>

[Sanitize All Translated HTML Fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-sanitize-all-translated-html-fields.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Disable creating users from incoming emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-restrict-emails-by-domain.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Restrict performance monitoring access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-performance-monitoring-acl.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Require write access to access service catalog add item page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-require-write-access-to-access-service-catalog-add-item-page.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Block access for delegated developers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-block-access-for-delegated-developers.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enforce strict security of session cookies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-secure-session-cookies.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enforce field ACLs for inbound query requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-field-acls-for-inbound-query-requests.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Minimize reset password request expiration duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-reset-password-request-expiration.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

10


</td></tr><tr><td>

[Enforce URL allowlist check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-url-allowlist-check.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true,""


</td></tr><tr><td>

[Limit UI active session life span](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-limit-ui-active-session-life-span.md)

</td><td>

-   Functional impact
    -   \(Old\)

Enforces max life-span on active authenticated HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero will disable timing out the active sessions. The max life-span must be more than inactive timeout glide.ui.session\_timeout \(default 30 minutes\).

    -   \(New\)

Authenticated UI sessions that exceed the configured lifespan are explicitly logged out. The session cookies are cleared and the session is invalidated, forcing the user to re-authenticate, rather than silently reissuing a new session ID as occurs with guest and integration sessions. Users must re-authenticate to continue working, even if they were actively using the platform when the session expired.

-   Dependencies and prerequisites
    -   \(Old\)&lt;blank&gt;
    -   \(New\)

This control interacts with the "glide.ui.session\_timeout" property, which controls the UI idle-session timeout duration. The platform requires the active session maximum lifespan to be greater than or equal to the idle timeout. If the active session lifespan is configured to a value lower than the idle-session timeout, the platform automatically increases the effective lifespan to match the idle-session timeout and logs a warning message.

-   Default value
    -   \(Old\)&lt;blank&gt;
    -   \(New\)

0


</td></tr><tr><td>

[Require authorization for import requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-import-request-authorization.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enforce password reset on API requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-password-reset-on-api-requests.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Disable external content URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-external-content-url.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Enforce security rules to sharing dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-security-rules-to-sharing-dashboards.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

false


</td></tr><tr><td>

[Require authorization for unload requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-require-authorization-for-unload-requests.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Disable adding default roles to skill ACLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-disable-adding-default-roles-to-skill-acls.md)

</td><td>

Functional impact

 -   old

Certain roles may be prevented from using skills if they do not satisfy an existing access control. These two property configurations will ensure certain roles always retain a base level of access to all skills.

-   New

When the com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl property is set to false, roles are no longer automatically granted access to generative AI skill ACLs — any role that needs to execute a skill must satisfy the skill's own access control instead of relying on an automatically-added default role. The related "com.glide.one\_extend.default\_roles\_for\_skill\_acl" property, which lists which roles get auto-added when com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl is set to true, has no effect while it is set to false.


</td></tr><tr><td>

[Require authorization for XML requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-xml-request-authorization.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Require authorization for API requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-api-request-authorization.md)

</td><td>

Default value-   \(Old\)&lt;blank&gt;
-   \(New\)

true


</td></tr><tr><td>

[Enforce OCSP check on network error](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-ocsp-check-on-network-error.md)

</td><td>

Functional impact

 Old: &lt;blank&gt;

 New: When the com.glide.communications.httpclient.ocsp\_allow\_network\_error property is set to false, an outbound HTTPS connection is not established if the OCSP responder becomes unreachable due to a network error, such as a timeout or DNS failure. Administrators should monitor OCSP responder availability after making this change, as any outbound integration with a temporarily unreachable OCSP responder will fail to connect.

 Dependencies and prerequisites

 Old: &lt;blank&gt;

 New: The com.glide.communications.httpclient.ocsp\_allow\_network\_error property has no effect unless the com.glide.communications.httpclient.verify\_revoked\_certificate property, the overall gate for certificate revocation checking, is set to true.

 Data type

 Old: &lt;blank&gt;

 New: Boolean

 Default value

 Old: &lt;blank&gt;

 New: true

</td></tr></tbody>
</table>**Parent Topic:**[Updated hardening settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/hardening-settings-updated.md)

