---
title: Updated hardening settings for baseline version 8.0
description: Some hardening settings have been updated with the release of Security Center baseline version 8.0.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: concept
last_updated: "2026-03-13"
reading_time_minutes: 117
breadcrumb: [Updated hardening settings, Baseline versions, Hardening settings, Platform Security]
---

# Updated hardening settings for baseline version 8.0

Some hardening settings have been updated with the release of Security Center baseline version 8.0.

<table id="table_baseline_v8_changes"><thead><tr><th>

Documentation

</th><th>

Updates

</th></tr></thead><tbody><tr><td>

[Disable legacy JQuery behavior](../reference/sc-legacy-jquery-behavior.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.jquery.legacy" is not set to the recommended value of "false", then older prepatched JQuery versions are used which will introduce unpatched vulnerabilities in the library. When false, integrates the JQuery 1.12.3 and 2.2.3 security patches. The system property is a failsafe in case any organizations depend on the non-patched versions of angularJS to run their custom implementations.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This could potentially lead to security risks arising from attacks on vulnerabilities discovered in outdated JQuery library versions.


</td></tr><tr><td>

[Enforce Query ACLs for SubLists, List Counts and Widget Data Tables](../reference/sc-enforce-query-acls-for-sublists-list-counts-and-widget-data-tables.md)

</td><td>

Rule Script updated to improve detection accuracy.

</td></tr><tr><td>

[Enable antivirus scan](../reference/sc-enable-antivirus-scan.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "com.glide.snap.enable\_scan" is not set to the recommended value of "true", then antivirus scanning is disabled.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Users may download malicious files leading to desktop and session compromise.


</td></tr><tr><td>

[Timeout Guest Sessions](../reference/sc-timeout-guest-sessions.md)

</td><td>

-   Description
    -   \(Old\)

Control the inactive session timeout for unauthenticated users with the "glide.guest.session\_timeout" system property. Raise the value of this property to extend the period of time your instance persists sessions beyond the default of 30 minutes. Avoid excessively large timeout values, which can increase the number of sessions persisted by the instance, and cause minor availability concerns.

    -   \(New\)

Use the glide.guest.session\_timeout system property to control the inactive session timeout for unauthenticated users. By default, the value of this property is 30 minutes. If there are availability concerns from persisting too many sessions in memory, the value of this property can be lowered to 5. Avoid setting this property greater than 30, as large timeout values increase the number of sessions persisted by the instance, and may cause minor availability concerns.

-   Remediation
    -   \(Old\)

Ensure the Glide Property 'glide.guest.session\_timeout' is set to a default value of 30. It may be desirable to lower this value to 5 in rare cases of availability concerns on the instance.

    -   \(New\)

Ensure the Glide Property 'glide.guest.session\_timeout' is configured to the default value of 30. In the rare case there are availability concerns from persisting too many sessions in memory, the value of this property can be lowerered to 5.

-   Security Risk
    -   \(Old\)

Large timeout values can increase the number of concurrent sessions on your instance, causing minor availability concerns.

    -   \(New\)

Avoid setting this property greater than 30. Large timeout values increase the number of sessions persisted by the instance, and may cause minor availability concerns.

-   Functional Impact
    -   \(Old\)

Small timeout values can result in an undesirable user experience as sessions expire too rapidly.

    -   \(New\)

Small timeout values can result in an undesirable user experience as sessions expire too rapidly. If there are availability concerns from persisting too many sessions in memory, the value of this property can be lowered to 5.


</td></tr><tr><td>

[Require authorization for data broker rest API \[Updated in Security Center 1.3\]](../reference/sc-data-broker-rest-api-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.basicauth.required.databrokerrestapiprocessor" is not set to the recommended value of "true", then basic authorization is not required for all inbound Data Broker Rest API requests.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This could lead to unauthenticated information disclosure from the instance.


</td></tr><tr><td>

[Configure event management assignment group admin roles \[New in Security Center 1.5\]](../reference/sc-configure-event-management-assignment-group-admin-roles.md)

</td><td>

-   Short Description
    -   \(Old\)

Configure Event Managment Assignment Group Admin Roles

    -   \(New\)

Configure Event Management Assignment Group Admin Roles

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The Glide Property 'evt\_mgmt.connector\_assignment\_group\_admin\_roles' contains comma separated string signifying the role names that have admin access over the assignment group field in connector instances.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Changing the default roles in this list may open up unauthorized users to altering event integrations on the instance.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Changing the default roles in this list may prevent previously authorized users from altering event integrations on the instance.

-   Dependencies and Prerequisites
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Application - Event Management

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

String

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

admin,evt\_mgmt\_admin,sn\_sow\_srm.srm\_admin


</td></tr><tr><td>

[Enable report view ACLs](../reference/sc-enable-report-view-acls.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The following property is responsible for implementing a check of report\_view ACLs for published reports. If "glide.report.report\_view.check\_published" is not set to the recommended value of "true", then checking of report\_view ACLs for published reports is disabled.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This could potentially leak sensitive data to unauthenticated users.


</td></tr><tr><td>

[Disable AJAXEvaluate](../reference/sc-disable-ajaxevaluate.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The AjaxEvaluator processor executes these scripts in sandbox however there are several additional properties which can allow the scope of activities in the sandbox to expand or be turned off entirely. In a worst case scenario a user can easily execute scripts as an admin privilege.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.script.allow.ajaxevaluate" is not set to the recommended value of "false", then the system API can be vulnerable to Client script execution through AJAX calls.


</td></tr><tr><td>

[Maximize reset password verification delay duration](../reference/sc-reset-password-verification-delay.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "password\_reset.verification.delay" is not set to the recommended value of "1000" or more, then password reset verification codes will be susceptable to brute force attacks.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The milliseconds delay limits the ability of a malicious actor to attempt to guess users identification or verification details, by using automation tools \("bots"\).


</td></tr><tr><td>

[Prevent inactive users from logging in](../reference/sc-prevent-inactive-users-from-logging-in.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property 'glide.authenticate.only.allow.active.user.login' is not set to 'true', users in the sys\_user table marked inactive can still login to the instance. Users may be marked inactive if they no longer have permission to login \(such as during termination from a company\).

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Inactive users may still access the instance and any data they could previously access.


</td></tr><tr><td>

[Enable High Security Plugin](../reference/sc-high-security-plugin.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The High Security plugin, activated by default, creates more than 900 different configurations to control the level of security on your instance. These configurations enable strict access control, input validation, and output encoding. It separates user functionality from access control management functionality through requiring administrators to explictly elevate into a "security\_admin" role before making access control changes.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Critical parts of the instance may be exposed to unauthorized access or manipulation.


</td></tr><tr><td>

[Activate Limit Concurrent Sessions Plugin](../reference/sc-limit-concurrent-sessions-plugin.md)

</td><td>

-   Short Description
    -   \(Old\)

Limit Concurrent Sessions Plugin

    -   \(New\)

Activate Limit Concurrent Sessions Plugin

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The Limit Concurrent Sessions plugin \(com.glide.limit.concurrent.sessions\) allows an administrator to limit the number of active sessions per user/role. It is recommended this plugin be enabled and configured to reduce the likelihood of session hijacking. If this plugin is enabled and configured, there will be a limit to the number of open sessions that can be hijacked.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Higher numbers of active concurrent sessions creates security risk by increasing the attack surface for account compromise, making it harder to detect unauthorized access and enforce session accountability across devices and locations.

-   Plugin Applicability
    -   \(Old\)

Limit Concurrent Sessions Plugin

    -   \(New\) &lt;blank&gt;

</td></tr><tr><td>

[Proactively Invalidate Sessions After Defined Durations](../reference/sc-proactively-invalidate-inactive-sessions.md)

</td><td>

-   Short Description
    -   \(Old\)

Proactively Invalidate Inactive Sessions

    -   \(New\)

Proactively Invalidate Sessions After Defined Durations

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When glide.active.session.timeout.invalidate.session isnot set to true, there's a small interval of time where a timed-out session isn't invalidated proactively before the Tomcat container invalidates the session. The duration of this time interval is dependent on additional properties representing differing use cases. glide.ui.active.session.life\_span: The value of this property defines the time, in minutes, before a UI session is invalidated. glide.guest.active.session.life\_span: The value of this property defines the time, in minutes, before a guest session is invalidated. glide.integrations.active.session.life\_span: The value of this property defines the time, in minutes, before an integrations session is invalidated.

-   Remediation
    -   \(Old\)

Ensure the Glide Property 'glide.active.session.timeout.invalidate.session' exists and is set to the value 'true'. If the property does not appear in the sys\_properties table, add a new record.

    -   \(New\)

Ensure that the property "glide.active.session.timeout.invalidate.session" is set to true.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If a session is hijacked, an attacker may be able to use a session during this small period.


</td></tr><tr><td>

[Enable policy based session access for mobile](../reference/sc-enable-policy-based-session-access-for-mobile.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The Zero Trust - Policy Based Session Access plugin allows security admins to reduce user access in a session based on IP, Location, Identity provider attributes and user attributes using adaptive authentication policies. When this property is enabled \(set to 'true'\), then users logging in via mobile device will have their roles restricted as configured by the plugin policies.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Instance admins may wish to restrict high privileged access when users login via mobile device, possible indicating an unsafe environment for sensitive operations.


</td></tr><tr><td>

[Enable work order management query rules for service organizations](../reference/sc-enable-work-order-management-query-rules.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When set to 'true', rules/filters from sn\_query\_rule table will be used to determine read access to Field Service Management-related tables \(Work Order and Work Order Task\) to the logged in user through query business rules and read ACLs. When 'false', the records won't be filtered based on query rules. Query business

rules add additional security validations. Specifically, this property will filter records for agents, qualifiers, and dispatchers based on their assigned territory or territory membership. It is best practice to follow the principle of least privilege when reading records.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

There may be increased risk of data exposure from Field Service Management tables.


</td></tr><tr><td>

[Disable SQL error messages](../reference/sc-disabling-sql-error-messages.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.db.loguser" is not set to the recommended value of "false", then sensitive server-side error messages could be displayed to end-users. Error messages can include stack traces and information about the structure of the database that could provide an attacker the knowledge needed to perform successful SQL Injection should the preconditions exist.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Messages can include stack traces and database structure details, which attackers can leverage to craft targeted SQL injection attacks if other vulnerabilities exist. Exposing internal error information increases the risk of exploitation.


</td></tr><tr><td>

[Set guest user for soap requests](../reference/sc-set-guest-user-for-soap-requests.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Use the com.glide.soap.guest\_user glide property to control the access level of unauthenticated SOAP requests. If this property isn't set to the recommended value of soap.guest or is set to a user with limited privileges, then SOAP requests execute on behalf of this user.

-   Remediation
    -   \(Old\)

Ensure the property "com.glide.soap.guest\_user" is set to "soap.guest".

    -   \(New\)

Ensure the property is set to soap.guest to ensure an appropriate level of access for unauthenticated SOAP requests.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated SOAP requests can allow unauthorized access if not properly restricted. Evaluating these requests against a minimally privileged user helps reduce the risk of exposing sensitive operations. Failure to enforce this control may result in elevated access and compromise system integrity.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

SOAP requests are restricted to the permissions of the soap.guest user. If an integration relies on a resource that does not have the appropriate ACLs for soap.guest, those requests will result in permission denials.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

String User ID \(user\_name\) of a user in the sys\_user table

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

soap.guest


</td></tr><tr><td>

[Required JMS connection factories](../reference/sc-required-jms-connection-factories-plugin-applicability-mid-server.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls the Java Messaging Service \(JMS\) connection factories that the MID Server can use. It is intended for a few select factories needed by plugins for JMS activity or action. Including additional factories could be a step in a chain of attack for vulnerabilities such as JNDI insertion that rely on capabilities an attacker can leverage in allowed factories. To prevent the possibility of any leveraged vulnerability, do not include factories beyond the necessary defaults.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Expanding the set of Java Messaging Service \(JMS\) connection factories beyond the necessary defaults introduces a significant risk because it increases the attack surface for exploitation techniques such as JNDI injection. Allowing additional factories can enable attackers to leverage insecure configurations or vulnerabilities in messaging components as part of a broader attack chain, potentially leading to remote code execution or system compromise. Restricting factories to only those required by core functionality is essential to maintain a secure posture.


</td></tr><tr><td>

[Require obfuscation of mobile app UI](../reference/sc-mobile-app-ui-obfuscation.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.sg.blur\_ui\_when\_backgrounded" is not set to the recommended value of "true", then the mobile app's UI is visible when viewed from the app switcher once the app has been backgrounded.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Blurring mobile backgrounding screenshots provides a higher level of confidentiality and privacy on the local device by blurring this view when backgrounded.


</td></tr><tr><td>

[Enforce device encryption and passcode requirements \[New in Security Center 1.3\]](../reference/sc-enforce-device-encryption-and-passcode-requirements.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property 'glide.sg.device\_encryption\_enabled' is set to true, the ServiceNow mobile app will check that device encryption is enabled and that device passcode is enabled. If encryption or passcode is not enabled, the user will not be allowed to log into the instance on mobile. This property enforces FIPS 140-2 Encryption. Mobile device encryption and passcode are important security features for ensuring an unauthorized user cannot access the content of the device even if the device is physically obtained.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This creates a risk that sensitive data stored or accessed through the mobile app could be exposed if the device is lost, stolen, or compromised. Without encryption and passcode enforcement, unauthorized users can gain physical access to confidential information, undermining compliance with FIPS 140-2 and weakening overall data protection.


</td></tr><tr><td>

[Enable protected tables plugin](../reference/sc-enable-protected-tables-plugin.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property 'com.glide.security.protected\_table.enabled' is set to 'true', The Protected Tables plugin will be utilized to prevent higher privilege users on an instance from tampering with log tables. The following logging tables will have special protections when this property is set to 'true': syslog \(config not modifiable\) syslog\_transaction sys\_outbound\_http\_log sysevent sys\_audit sys\_push\_notification protected\_table\_configuration \(config not modifiable\) syslog\_app\_scope

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Log integrity must be maintained to allow discovery of malicious activity.


</td></tr><tr><td>

[Enforce read ACLs on report views](../reference/sc-enforce-read-acls-on-report-views.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property "glide.report.report\_view.read\_acl", when set to "enforce", enforces the READ ACL \(table level\) on reporting functions when there is no Report View ACL on the table/field.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

ACLs could be bypassed, leading to potential sensitive information disclosure.


</td></tr><tr><td>

[Restrict access to GlideSystemUserSession scriptable API](../reference/sc-access-glidesystemusersession-scriptable-api.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The methods "gs.addErrorMessageNoSanitizationMessaging\(\)" and "gs.addInfoMessageNoSanitization\(\)" are used within the scripting environment for logging and notifications. Both of these are available in the sandbox if this property is not set to the recommended value of "false". The sandbox is a low privileged scripting environment available to unauthenticated and no role users. Both of these methods can be used to display unsanitized input to a user.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Displaying unsanitized input to the user is dangerous, as unsanitized input may contain dangerous code that runs in the user's browser. This can be utilized for traditional reflected XSS attacks. Reflected XSS attacks can be used in multiple scenarios, including session hijacking.


</td></tr><tr><td>

[Enable SMS code notification for enrollment and verification](../reference/sc-sms-code-notification-for-enrollment-and-verification.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property "password\_reset.sms.use\_notify" controls usage SMS code notification for enrollment and verification. If "password\_reset.sms.use\_notify" is set to the recommended value "true", then user will be notifed for password reset for SMS verification method and new device enrollment. Using

SMS code notification for enrollment and verification is more secure that default email notification.

-   Remediation
    -   \(Old\)

Ensure the property "password\_reset.sms.expiry" is set to "true".

    -   \(New\)

Ensure the property "password\_reset.sms.use\_notify" is set to "true".

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Email-based notifications are generally less secure because they are more susceptible to account compromise and phishing attacks. Using SMS for verification provides stronger assurance of user identity and reduces the risk of unauthorized password resets or fraudulent device enrollments.


</td></tr><tr><td>

[Do not use demo certificates for active SAML configurations](../reference/sc-do-not-use-demo-certificates-active-saml-configurations-plugin.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The demo certificates provided by ServiceNow should not be used in production SAML configurations. The certificates are common among all instances with known passphrase. If one of the SAML properties utilizing a certificate keystore is active \(require\_signed\_authnrequest, require\_signed\_logoutrequest or encrypt\_assertion\) then the demo data must not be used. Since demo data is shared among all instance, there is no integrity garuntee of requests signed with shared certificates.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Messages encrypted by the IDP could be decrypted by any actor, if intercepted.


</td></tr><tr><td>

[Enable email OTP for multi-factor authentication](../reference/sc-enable-email-otp-for-multi-factor-authentication.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property "glide.authenticate.multifactor.email.otp.enabled" controls if a token for the second authentication factor can be sent via email. Email is considered a weak MFA factor which an attacker is more likely to gain access into for defeating MFA. If the property is false: 1. The user will not see email OTP option on the MFA validation screen. If the property is true:

2. The email factor is shown in cases where the email factor policy is inactive and no other 2fa registered. 3. The email factor is shown if the email factor policy is active and evaluated to true. 4. The email factor is not shown if the email factor policy is active and evaluated to false.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

An attacker may successfully bypassing MFA when they have the user's password.


</td></tr><tr><td>

[Enable UserCookie version 3.1](../reference/sc-enable-usercookie-version-3-1.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

UserCookie v3 is generated only when property glide.ui.secure.cookies.use\_kmf is disabled. UserCookie v3 is not secure due to storing secret key for HMAC in source code and identical for all customers. By setting the property "glide.ui.secure.cookies.use\_kmf" to "true" UserCookie v3.1 will be used and secret key will be stored in security storage such as KMF.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This creates a significant risk of session hijacking, as attackers who obtain or reverse-engineer the key can forge authentication cookies and impersonate users.


</td></tr><tr><td>

[Enable Jelly JS interpolation protection for nested expressions](../reference/sc-enable-jelly-js-interpolation-protection-for-nested-expressions.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property allows a customer to turn on or off interpolation protection specifically for nested Jelly expressions. Interpolation protection ensures that when Jelly expressions are used in JavaScript, they must be deemed safe by either falling under certain categories OR being marked as SAFE in the expression itself. This property was added to protect against possibly dangerous Jelly expressions which are nested in another Jelly expression.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unprotected interpolated jelly expression may result in a malicious actor sending a crafted GET parameter to a Jelly page and cause the contents of that parameter to be evaluated as server-side JavaScript with admin privileges.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Boolean

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

true


</td></tr><tr><td>

[Escape XML markup](../reference/sc-escape-xml.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property escapes XML values at the parser level for the user interface. It prevents reflected and stored cross-site scripting attacks. This property is not applicable in Service Portal.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.ui.escape\_text" is not set to the recommended value of "true", then XML values will not be escaped at the parser level for the user interface; this will leave jelly templates susceptible to reflected and stored cross site scripting attacks.


</td></tr><tr><td>

[Disable GlideRecord Scope Fencing Legacy Behavior](../reference/sc-enable-gliderecord-scope-fencing-legacy-behavior.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

GlideRecord provided cross scope create/update access to tables that were not configured with that level of access. In order to prevent customers from having applications broken when this scoped access behavior was patched, the property glide.record.legacy\_cross\_scope\_access\_policy\_in\_script was created. When 'true', cross scope access falls back onto legacy behavior \(insecure\). This property disables scope fencing, allowing scoped apps to access global script interfaces.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

It is best security practice to have scope fencing restrictions in place. Scoping ensures applications can only access resources with explicit access or within their scope, following the principle of least privilege. Disabling this feature could lead to confidentiality, availability, and integrity impacts.


</td></tr><tr><td>

[Remove remember me](../reference/sc-remove-remember-me.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls the Remember Me check box from the login page to prevent login information from being cached when set to true. If the value is set to false, caching of authentication information is allowed and the "Remember Me" checkbox is displayed.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This increases the risk of unauthorized access if the device is shared, lost, or compromised, as cached credentials can allow attackers to bypass authentication.


</td></tr><tr><td>

[Disable outbound SSLv2/SSLv3 connections](../reference/sc-disabling-sslv2-sslv3.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls the desired transport encryption protocol. If "glide.glide.outbound.sslv3.disabled" is not set to the recommended value of "true", then outbound MID server connections such as REST and SOAP requests will use SSL as the transport protocol. SSL was proven to be insecure in 2014.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

SSLv3 has been proven insecure since 2014 due to vulnerabilities like POODLE, making it susceptible to man-in-the-middle attacks and data interception. Allowing SSLv3 undermines transport encryption and exposes sensitive data in transit, violating modern security standards.


</td></tr><tr><td>

[Disable creating users from incoming emails](../reference/sc-restrict-emails-by-domain.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

An administrator can set an email property to automatically create users from incoming emails. If set this property to the insecure value, the instance will automatically create users from incoming email. Each user created will have the same hardcoded default password which makes bypassing authentication through brute force easier.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Allowing automatic user creation without strong password controls undermines authentication security and increases the likelihood of system compromise.


</td></tr><tr><td>

[Minimize SMTP Recipient Quantity](../reference/sc-max-smtp-recipients.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property specifies the maximum number of recipients the instance can list in the To: line for a single email notification. Notifications that would exceed this limit instead create duplicate email notifications addressed to a subset of the recipient list. Each email notification has the same maximum number of recipients.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This can lead to resource exhaustion and potentially cause a Denial of Service \(DoS\) condition on the email subsystem or the instance itself. Limiting recipient counts is essential to prevent abuse and maintain system performance and availability.


</td></tr><tr><td>

[Enable password reset policy checks](../reference/sc-enable-password-reset-policy-checks.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Use the glide.enable.password\_policy property to customize password strength validation rules for the Change Password form. Customize the length and complexity values to match your organization's security policy. If "glide.enable.password\_policy" is not set to the recommended value of "true", then password standards will not be enforced.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Enforcing password complexity is critical to maintaining strong authentication and reducing exposure to account takeover.


</td></tr><tr><td>

[Require clearing pasteboard when backgrounding mobile application](../reference/sc-require-clearing-pasteboard-when-backgrounding-mobile-application.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The "glide.sg.clear\_pasteboard\_when\_backgrounded" property controls if text copied from ServiceNow mobile app is kept in the clipboard and pasteboard after the app is in background mode.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This creates a risk of sensitive information disclosure, as clipboard data can be accessed by other applications on the device, potentially exposing credentials, PII, or confidential business data. Enforcing this property helps prevent unintended data leakage across apps.


</td></tr><tr><td>

[Restrict permissions for CMDB model](../reference/sc-restrict-permissions-cmdb-model.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property is an additional access control to the CMDB model. If "csm\_cmdb\_model.customer\_visible\_flag" is not set to the recommended value of "true", then any user with the sn\_esm\_user role and out of the box ACLs will have permissions to the CMDB model. Note that this role tends to be granted to external users.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

External users could unwillingly be given permissions to the CMDB model.


</td></tr><tr><td>

[Disable JavaScript tags in embedded HTML](../reference/sc-allow-javascript-tags-in-embedded-html.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.ui.security.codetag.allow\_script" is not set to the recommended value of "false", then this property allows rendered HTML in journal fields and forms which opens room for XSS attacks. Malicious HTML needs to be put between code tags for example \[code\]\[/code\].

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Uncontrolled JavaScript risks Cross-Site Scripting \(XSS\) attacks, enabling malicious actors to inject and execute harmful scripts in the user's browser. Such

attacks can lead to session hijacking, credential theft, and compromise of sensitive data.


</td></tr><tr><td>

[Restrict performance monitoring access](../reference/sc-performance-monitoring-acl.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.security.diag\_txns\_acl" is not set to the recommended value of "true", then All users \(authenticated or not\) have access to diagnostic pages such as stats.do, xmlstats.do, threads.do and replication.do pages. These endpoints are intended to be used for monitoring instance health.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Information exposed by performance monitoring endpoints may be useful to attackers.


</td></tr><tr><td>

[Configure Service Portal Widgets Table Allow List](../reference/sc-configure-service-portal-widgets-table-allow-list.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The Glide Property 'glide.service\_portal.widget.table\_allow\_list' contains the list of tables allowed to be accessed by unauthenticated users through Service Portal widgets that make use of the additional security checks provided in the SNCACLWidgetUtil script include. This property is only enforced if the Glide Property 'glide.service\_portal.widget.enforce\_public\_check' is 'true'. There may be unauthenticated information disclosure if unnecessary tables are listed in this property. Table ACLs will still be evaluated as previously occurred.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated users may gain access to sensitive data through Service Portal widgets, potentially leading to information disclosure despite existing table ACLs.

-   Fallback Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

''


</td></tr><tr><td>

[Honor Admin Override ACLs](../reference/sc-honor-admin-override-acls.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

ACLs are evaluated cumulatively. If there are a number of ACLs on any given field and the Admin Overrides option is false \(not selected\) on one of them, then the effective admin overrides for all the ACLs are considered to be false. This causes admins to be unable to pass even the ACL where the override should be in effect. If "glide.security.admin.override.accessterm" is not set to the recommended value of "true" then, even if one of the ACL terms under the ACL rule is "Admin overrides" false, the entire rule evaluates to false.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

ACLs with conflicting "Admin overrides" settings may cumulatively evaluate to false, potentially preventing administrators from accessing fields they should have access to and inadvertently causing denial of access to critical data.


</td></tr><tr><td>

[Require XMLdoc2 entity validation with allowlist](../reference/sc-xmldoc2-entity-validation-with-entity-expansion.md)

</td><td>

Short Description

 -   \(Old\)

Require XMLdoc2 entity validation with allowlistDisable Entity Expansion

-   \(New\)

Require XMLdoc2 entity validation with allowlist


</td></tr><tr><td>

[Enforce oauth state parameter validation](../reference/sc-enforce-oauth-state-parameter-validation.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The "glide.oauth.state.paramater.required system" property enables the "State" parameter to be required in an OAuth request for authorization code flow. Beginning in the Madrid release, the system property "glide.oauth.state.parameter.required" adds a "State" parameter for an OAuth request. For zbooted instances, the property is true. For upgraded instances, the property is not present, so the "State" parameter is not enabled. The "State" parameter is a string value, and should not contain special characters. The State parameter cannot be empty or " ". Not enabling the "State" parameter to "true" ensures that an attacker cannot perform CSRF attacks during authentication can allow an attacker to perform operations as the victim.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Not enabling the glide.oauth.state.parameter.required property in OAuth authorization code flow increases the risk of Cross-Site Request Forgery \(CSRF\) attacks, potentially allowing attackers to impersonate users and perform unauthorized actions.


</td></tr><tr><td>

[Limit max comments per user per day](../reference/sc-limit-max-comments-per-user-per-day.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "sn\_kb\_social\_qa.max\_comments\_per\_user\_daily" is not set to the recommended value of "500" or less, then there will be no restriction on number of QA comments per day.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Too many comments could lead to resource exhaustion.


</td></tr><tr><td>

[../reference/sc-disable-chat-server-debugging.md](../reference/sc-disable-chat-server-debugging.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.cs.debug" is not set to the recommended value of "false", then chat server messages logging is enabled. Setting the property value to true enables logging chat server messages on system logs. As a lot of log messages are generated, it is advised to enable it only when troubleshooting chat server. After troubleshooting, the property should be disabled to avoid clogging system logs. Setting the property to false, which is also the default value does not log chat server messages on system logs.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This could lead to unintended sensitive information leak through system logs.


</td></tr><tr><td>

[Configure Service Portal Widgets Allow List](../reference/sc-configure-service-portal-widgets-allow-list.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The Glide Property 'glide.service\_portal.widget.allow\_list' determines the list of widgets that are allowed to attempt to access any table on the instance. ACLs for those tables will still be enforced. If there are misconfigured empty ACLs on tables on the instance, widgets in this list may allow access to those tables, leading to information disclosure. This property is only enforced if the widget makes use of SNCACLWidgetUtil, and the Glide Property 'glide.service\_portal.widget.enforce\_public\_check' is set to 'true'.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated users may gain unintended access to sensitive table data via Service Portal widgets, resulting in potential information disclosure.

-   Fallback Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

''


</td></tr><tr><td>

[Minimize external user registration link expiration duration](../reference/sc-external-user-registration-link-expiration.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "sn\_ext\_usr\_reg.Reg\_link\_expiration\_days" is not set to the recommended value of "3", then a registration link could be used by someone other than the intended user if the link is discovered later in time.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Longer expiration windows weaken account provisioning security and create opportunities for unauthorized account creation or impersonation.


</td></tr><tr><td>

[Prevent verbose HTTP request logging](../reference/sc-prevent-verbose-http-request-logging.md)

</td><td>

Description

 -   \(Old\)

The two properties glide.outbound\_http\_log.override and glide.outbound\_http\_log.override.level

work together to control the level of logging for outbound HTTP requests. When glide.outbound\_http\_log.override is set to "true", the log level for requests and

responses is controlled by glide.outbound\_http\_log.override.level . If the override level is set to "all" or "elevated", then request and response headers are logged

-   \(New\)

The two properties glide.outbound\_http\_log.override and glide.outbound\_http\_log.override.level work together to control the level of logging for outbound HTTP requests. When glide.outbound\_http\_log.override is set to "true", the log level for requests and responses is controlled by glide.outbound\_http\_log.override.level . If the override level is set to "all" or "elevated", then request and response headers are logged


</td></tr><tr><td>

[Enable CAPTCHA for External User Registration](../reference/sc-enable-captcha-external-user-registration.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "sn\_ext\_usr\_reg.captchaEnabled" is not set to the recommended value of "true", then CAPTCHA will not be validated for external user registration and could lead to automatic account creation attacks.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Enforcing CAPTCHA is critical to prevent bot-driven attacks and maintain the integrity of user onboarding.


</td></tr><tr><td>

[Apply domain separation on dot walked fields](../reference/sc-apply-domain-separation.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls whether join queries are given domain separated conditions or not, in order to ensure they apply domain separation functionality for dot walked fields.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Sensitive information could be disclosed that is not to be shared with a specific domain.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

There may be moderate functional impact to the instance if components are reliant on the unsafe cross domain queries. Instances should be tested in non-production environments before enabling.


</td></tr><tr><td>

[Disable unauthenticated published reports](../reference/sc-disable-unauthenticated-published-reports.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.report.published\_reports.enabled" is not set to the recommended value of "false", then reports stored on the instance can be made visible without authentication.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Allowing unauthenticated access to sensitive data can cause inadvertent information disclosure to a malicious actor.


</td></tr><tr><td>

[Require authorization for JSONv2 request](../reference/sc-jsonv2-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.basicauth.required.jsonv2" is not set to the recommended value of "true", then this will disable Basic Authentication for JSONv2 format export processor. This also happens when combined with a wrong role within the guest\_user related property \(For example a high privileged user such as Admin\).

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated access to JSON export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.


</td></tr><tr><td>

[Require authorization for XML output requests](../reference/sc-xml-output-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.basicauth.required.xmloutputprocessor" is not set to the recommended value of "true", then basic authorization is not required for all inbound XMLOutputProcessor requests. This could lead to unauthenticated information disclosure from the instance.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated access to XML export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.


</td></tr><tr><td>

[Minimize reset password SMS expiry duration](../reference/sc-reset-password-sms-expiracy.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property "password\_reset.sms.expiry" denotes the number of minutes before the SMS code expires.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the value is too high, an attacker may guess the SMS code to reset the password.


</td></tr><tr><td>

[Prevent Unauthenticated Access to Virtual Agent Embedded Web Client](../reference/sc-publicly-exposed-virtual-agent-embedded-web-client.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The UI page sn\_va\_web\_client\_app\_embed , which is an embedded web client for Virtual Agent, contains the ACL marked 'true' in the sys\_public table Out of Box. It has been confirmed that there are use cases where public accessibility is needed however this is not a security best practice to set it to default publicly accessible.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Sensitive information may be exposed to unauthenticated users.


</td></tr><tr><td>

[Maximize reset password SMS pause window duration](../reference/sc-reset-password-sms-pause-window.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "password\_reset.sms.pause\_window" is not set to the recommended value of "2" minutes or greater, then a malicious user could initiate many password reset SMS codes in a brief window of time.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This increases the attacker's likelihood of predicting the SMS reset code.


</td></tr><tr><td>

[Maximize reset password request retry window duration](../reference/sc-reset-password-request-retry-window.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property "password\_reset.request.retry\_window" specifies the length of time before the count for password reset attempts refreshes.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the value is too low, then it will make brute forcing against password reset process attacks much faster.


</td></tr><tr><td>

[Double check inbound transactions](../reference/sc-double-check-inbound-transactions.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Property provides an extra layer of security on form submission / field updates by ensuring only users with the proper permissions are allowed to update a form. If "glide.security.strict.updates" is not set to the recommended value of "true", then updates are not strict meaning they are able to modify fields visible to them regardless of whether they have the appropriate permissions.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Users may be able to update form fields simply by having visibility into them—regardless of their actual permissions—creating a risk of unauthorized data modification and privilege escalation.


</td></tr><tr><td>

[Minimize reset password request expiration duration](../reference/sc-reset-password-request-expiration.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "password\_reset.request.expiry" is not set to the recommended value of "10" or less, then it increases the opportunity for someone else to guess and use the request and attempt to reset the password.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Short expiration windows are critical to reducing the opportunity for unauthorized password resets and maintaining account security.


</td></tr><tr><td>

[Limit Invalid Password Reset Attempts](../reference/sc-reset-password-request-max-attempts.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property "password\_reset.request.max\_attempt" dictates the maximum number of unsuccessful password reset attempts that can be taken before the user is locked out of password reset process. The lockout period is determined by the value in "password\_reset.request.max\_attempt\_window".

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the value is too high, then it could be possible to perform brute force attack against password reset process.


</td></tr><tr><td>

[Enable CAPTCHA in password reset](../reference/sc-enable-captcha-in-password-reset.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "password\_reset.captcha.ignore" is not set to the recommended value of "false", then a CAPTCHA challenge-response will not be used during the password reset process. CAPTCHAs help prevent automation attacks by prompting the user for a challenge-response that is not easily answered by automated systems.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the CAPTCHA is disabled, an attacker may be more successful during automated attacks against the password reset feature.


</td></tr><tr><td>

[Validate remote host](../reference/sc-validate-remote-host.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.update\_set.remote.check\_host" is not set to the recommended value of "true", then the Team Development Remote Instance test feature will allow an internal network port scan by providing positive/negative error messages.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

An attacker may enumerate all open ports on a given host or pull response data, leading to information leak or unauthorized data access.


</td></tr><tr><td>

[Rotate HTTP session identifiers](../reference/sc-rotate-http-session-identifiers.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.ui.rotate\_sessions" is not set to the recommended value of "true", then identifying information on a session is kept and not rotated between applications.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This increases the risk of session hijacking, as attackers could reuse session identifiers to gain unauthorized access.


</td></tr><tr><td>

[Set Xframe options to prevent embedding third-party websites](../reference/sc-xframe-options.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "com.glide.cs.embed.xframe\_options" is not set to the recommended value of "DENY" or "SAMEORIGIN", then content of the web application could be embedded in a third-party site using an ALLOW-FROM URI.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Allowing untrusted third-party sites could enable attacks such as clickjacking.

-   Fallback Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

''


</td></tr><tr><td>

[Enforce production instance behavior](../reference/sc-production-instance-behavior.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.installation.production" is not set to the recommended value of "true", then the instance is not treated as a production instance, permitting zboot and other potentially dangerous scripts.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Allowing a production instance to be evaluated as non-production can lead to information disclosure or denial of service.


</td></tr><tr><td>

[Enforce security rules to sharing dashboards](../reference/sc-enforce-security-rules-to-sharing-dashboards.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property 'glide.cms.dashboards.sharing\_with\_secure\_search' is not set to 'true', a user can share a dashboard to groups and roles that they do not personally have access to. This property enforces ACLs on searching the sys\_user, sys\_user\_role, and sys\_user\_group tables when sharing a dashboard.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Oversharing a dashboard may result in minor confidentiality impacts in cases where a user shares a dashboard with a user, group, or role that should not access to the dashboard.


</td></tr><tr><td>

[Implement the x-frame-options: SAMEORIGIN security header](../reference/sc-x-frame-options-sameorigin.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The following property controls the implementation of the security header X-Frame-Options: SAMEORIGIN. If "glide.set\_x\_frame\_options" is not set to the recommended value of "true", then an instance will be allowed to be framed in an iframe of another page.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This can lead to a clickjacking attack.


</td></tr><tr><td>

[Enable HTTP Only Cookie Flag](../reference/sc-http-only-cookie-flag.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.cookies.http\_only" is not set to the recommended value of "true", then the instance does not require the HTTPOnly attribute for sensitive cookies.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The HTTPOnly attribute is used to prevent attacks, such as cross-site scripting, because it doesn't allow access to the cookie using a client-side script, such as JavaScript.


</td></tr><tr><td>

[Prevent Empty ACL Creation](../reference/sc-prevent-empty-acl-creation.md)

</td><td>

-   Short Description
    -   \(Old\)

Prevent Empty ACL Creation

    -   \(New\)

Prevent Empty ACL Creation

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The glide.security.empty\_acl.popup\_window.enabled property controls whether users making form-based edits to ACL records \(sys\_security\_acl\)

can create, update, or save an invalid ACL that has an invalid data condition, script, security attribute, or roles list, or otherwise does not have any configured \(an "empty ACL"\). As of the Xanadu release, an empty ACL will completely deny access. On versions prior to Xanadu, empty an ACL will allow unconditional access. When the glide.security.empty\_acl.popup\_window.enabled property is set to a secure value of "true", attempts to create, update, or save an invalid or empty ACL will be blocked, and a clientside model will be provided to configure a role or security attribute for the ACL. If the property is insecurely set to any other value, then such attempts will be allowed and no client-side model will be displayed. Note: This property is case sensitive. A value of "True" \(capital "T"\) will be equivalent to "false". Additionally, this property will only function when the High Security \(com.glide.high\_security\) plugin is installed and active.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Misconfigured or empty Access Control Lists \(ACLs\) can unintentionally grant unrestricted access to sensitive data and system functionality. When ACLs lack proper conditions, roles, or security attributes, they fail to enforce authorization boundaries, enabling attackers or unauthorized users to bypass security controls. This can lead to data breaches, privilege escalation, and compromise of confidentiality, integrity, and availability across the platform.

-   Fallback Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

false


</td></tr><tr><td>

[Require authorization for XML requests](../reference/sc-xml-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.basicauth.required.xml" is not set to the recommended value of "true", then this will disable Basic Authentication for XML format export processor. This also happens when combined with a wrong role within the guest\_user related property \(For example a high privileged user such as Admin\). This will lead to unauthenticated access to instance data.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated access to XML export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.


</td></tr><tr><td>

[Enforce SOAP request strict security](../reference/sc-soap-request-strict-security.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.soap.strict\_security" is not set to the recommended value of "true", then users do not need a SOAP role to make requests of non-public pages when the high security or web service plugin is installed.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

An unauthorized user can get access to sensitive content/data on the target instance.


</td></tr><tr><td>

[Disable public access to favorites](../reference/sc-public-access-to-favorites.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.ui.magellan.favorites.allow\_public" is not set to the recommended value of "false", then all unauthenticated users can access Favorites of the same "Guest" user in the navigator.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated users are allowed to access and potentially manipulate the Favorites of the shared "Guest" user, increasing the risk of unauthorized UI customization, data exposure, and user interface misuse.


</td></tr><tr><td>

[Disable inbound emails for locked out users](../reference/sc-disable-inbound-emails-locked-out-users.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls inbound email actions for locked out users. If "glide.pop3.process\_locked\_out" is set to "True", there may be an information disclosure as inbound emails would be received by users with locked accounts.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Allows locked-out users to continue submitting inbound emails that may create records or trigger workflows, posing a security risk by enabling potentially unauthorized actions.


</td></tr><tr><td>

[Enable scoped admin application ACLs](../reference/sc-administer-scoped-admin-application-acls.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Determines whether an application administration apps can inherit global access control list \(ACL\) rules. Useful when there are no scoped admin application ACLs defined for the record scope.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.security.scoped\_administration.honor\_global\_acl" is not set to the recommended value of "true", then a low privilege user with permissions to the application could potentially access sensitive records.


</td></tr><tr><td>

[Log session audit events](../reference/sc-log-session-audit-events.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property 'glide.authenticate.session\_access.log\_audit\_event' is set to 'true', session audit events will be created in the sys\_session\_access\_audit table. Information logged will include user, session ID \(non-sensitive\), IP address, roles, and policies.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Information about who accessed a session will not be logged to assist in incident investigations.


</td></tr><tr><td>

[Minimize session activity timeout duration](../reference/sc-session-activity-timeout.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property determines the user session timeout. This determines how long a user session stays active. If "glide.ui.session\_timeout" is not set to the recommended value of "60" minutes or less, then the session may stay valid for long even without activity. This could provide too large of a time window to enable session hijacking attacks.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A long session timeout allows inactive sessions to remain valid for extended periods, increasing the chance that an attacker could hijack the session before it expires.


</td></tr><tr><td>

[Log user impersonation](../reference/sc-log-user-impersonation.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.sys.log\_impersonation" is not set to the recommended value of "true", then user-impersonating events will no longer be logged.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

ServiceNow's automated security detections and security investigation capabilities effectiveness will be reduced.

-   Fallback Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

false


</td></tr><tr><td>

[Enforce HTML Sanitization](../reference/sc-check-unsanitized-html.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property enforces sanitization behavior of translated\_html fields on a global level for field assignments.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "com.glide.security.check\_unsanitized\_html" is not set to the recommended value of "enforce", then an attacker could be able to execute arbitrary javascript in the victim's browser \(XSS attacks\).


</td></tr><tr><td>

[Disable local login for users with Single Sign-On \(SSO\) enabled](../reference/sc-disable-local-login-for-users-with-single-sign-on-sso-enabled.md)

</td><td>

Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Define active session timeout exception roles](../reference/sc-define-active-session-timeout-exception-roles.md)

</td><td>

Remediation

 -   \(Old\)

Configure the glide.active.session.timeout.exception.roles property to roles which should be exempt from active session timeouts. This property value is a comma separated list of roles. The default value is edge\_encryption,mid\_server,maint.

-   \(New\)

Configure the glide.active.session.timeout.exception.roles property to roles which must be exempt from active session timeouts. This property value is a comma separated list of roles. The default value is edge\_encryption,mid\_server,maint.


</td></tr><tr><td>

[Limit integrations' active session life span](../reference/sc-limit-integrations-active-session-life-span.md)

</td><td>

-   Technical Configuration Name
    -   \(Old\)

glide.integrations.active.session.life\_span

    -   \(New\)

glide.integrations.active.session.life\_span

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This configuration will enforce max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes and the value of zero will disable timing out the active sessions. This particular property is limited to integrations that have low-privilege access to an instance.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A larger maximum lifespan could allow an attacker to persist in a stolen session for longer, increasing the scope of a security incident.

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

0

-   Fallback Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

0


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Limit guest's active session life span](../reference/sc-limit-guests-active-session-life-span.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This configuration will enforce max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes and the value of zero will disable timing out the active sessions. This particular property is limited to Guest users, which have low privilege access to an instance.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A larger maximum lifespan could allow an attacker to persist a stolen session for longer, increasing the scope of a security incident.

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

0


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Enable CAPTCHA for customer registration](../reference/sc-enable-captcha-for-customer-registration.md)

</td><td>

Description

 -   \(Old\)

The property "sn\_customerservice.captchaEnabled" determines if CAPTCHA validation is enabled or disabled for customer registration on the Customer Service Management Portal.

-   \(New\)

The property "sn\_customerservice.captchaEnabled" determines if CAPTCHA validation is enabled or disabled for customer registration on the Customer Service Management Portal.


</td></tr><tr><td>

[Limit Allowed Number of Failed Login Attempts Before Lockout](../reference/sc-managing-failed-login-attempts.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The "SNC User Lockout Check" or "SNC User Lockout Check with Auto Unlock" script actions enable the administrator to manage the number of failed login attempts for a user. Two script actions are available that enable a site administrator to manage the number of times a user can provide correct password before getting locked out from the Now Platform. Additionally, the "glide.user.max\_unlock\_attempts" property controls the number of allowed failed login attempts. If the value of "glide.user.max\_unlock\_attempts" is increased above the recommended value of "5", it will increase the number of login attempts an attacker could make against a given user.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Allowing more attempts gives attackers additional opportunities to guess passwords, increasing the likelihood of unauthorized access and credential compromise. Proper lockout configuration is critical to maintaining strong authentication security.


</td></tr><tr><td>

[Enforce relative links](../reference/sc-enforce-relative-links.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The "glide.cms.catalog\_uri\_relative" property enforces relative links from the URI parameter on /ess/catalog.do. If "glide.cms.catalog\_uri\_relative" is not set to the recommended value of "true", then the URL will not be sanitized with the enforceRelativeURL\(url\) function. This property impacts the legacy Content Management System \(CMS\) which has been replaced with Service Portal.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Absolute URLs can pose a security risk when used as a part of parameter or a field value, thus redirecting the source page to an adversary-controlled website.


</td></tr><tr><td>

[Minimize Concurrent Interactive Sessions with Limit Concurrent Sessions Plugin](../reference/sc-glide-authenticate-limit-concurrent-interactive-sessions.md)

</td><td>

-   Short Description
    -   \(Old\)

Minimize Concurrent Interactive Session Quantity When Limit Concurrent Sessions Plugin Is Installed

    -   \(New\)

Minimize Concurrent Interactive Sessions with Limit Concurrent Sessions Plugin

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property "glide.authenticate.max.concurrent.interactive.sessions" controls the number of active sessions that can be open for a user when the Limit Concurrent Sessions \(com.glide.limit.concurrent.sessions\) plugin is enabled. It is recommended that this value be the default of "1" to reduce the number of sessions that can be left open for a user.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A greater number of open sessions means there are more sessions that can potentially be hijacked.


</td></tr><tr><td>

[Require authorization for SCHEMA requests](../reference/sc-schema-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.basicauth.required.schema" is not set to the recommended value of "true", then basic authorization is not required for all Inbound Table Schema Processor requests. The Inbound Table Schema Processor handles incoming schema requests for the platform.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Omitting authentication from this processor will lead to unauthenticated access to instance schema data.


</td></tr><tr><td>

[Block Expired Anti-CSRF Tokens](../reference/sc-block-expired-csrf-tokens.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property allows usage of an expired secure token to identify and validate incoming requests. This token is used to prevent cross-site request forgery attacks.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Allowing the use of previous or expired CSRF tokens exposes the application to replay attacks, enabling attackers to reuse valid requests and potentially perform unauthorized actions on behalf of legitimate users.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Boolean

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

false


</td></tr><tr><td>

[Set Automatic Token Cleanup for Token Credentials](../reference/sc-set-automatic-token-cleanup-for-token-credentials.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the property 'com.snc.platform.security.token.auth.cleanup' is set to the insecure value of 'false', expired API keys and HMAC secrets will not be deleted. This creates a potential for token reuse. If the token was expired due to leakage or compromise, reuse exposes the instance to anyone possessing the leaked token. Expired tokens are kept for the number of days defined by 'com.snc.platform.security.token.auth.days.expired.hmac\_secret.is.kept' and 'com.snc.platform.security.token.auth.days.expired.api\_key.is.kept'. Integers value of 0 and greater are valid values. A value of 0 would cause the expired tokens to be deleted in the same day. The default of 7 days, or fewer, is recommended.

-   Remediation
    -   \(Old\)

Ensure the property 'com.snc.platform.security.token.auth.cleanup' does not exist in the sys\_properties table or is set to 'true'. Ensure the properties 'com.snc.platform.security.token.auth.days.expired.api\_key.is.kept' and 'com.snc.platform.security.token.auth.days.expired.hmac\_secret.is.kept' do not exist in the sys\_properties table or are set to 7 or less, where 7 corresponds to the number of days.

    -   \(New\)

Ensure the property 'com.snc.platform.security.token.auth.cleanup' does not exist in the sys\_properties table or is set to 'true'. Ensure the properties 'com.snc.platform.security.token.auth.days.expired.api\_key.is.kept' and 'com.snc.platform.security.token.auth.days.expired.hmac\_secret.is.kept' do not exist in the sys\_properties table or are set to 7 or less, where 7 corresponds to the number of days.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A high number of days increases the exposure period for token reuse.


</td></tr><tr><td>

[Enable HTML Sanitizer within Virtual Agent](../reference/sc-enable-html-sanitizer.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls the whether the HtmlSanitizerService is enabled. If "com.glide.cs.html.sanitizer.enabled" is not set to "true", then a Stored Cross-Site Scripting \(XSS\) attack is possible in the VA web client.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

An XSS vulnerability can facilitate privilege escalation to higher-level roles, such as administrator, enabling broader lateral movement within the system.


</td></tr><tr><td>

[Enable HTTP response headers configuration](../reference/sc-enable-http-response-headers-configuration.md)

</td><td>

Description

 -   \(Old\)

Reduce the risk of cookie/session-related hijacking of web apps using a system property. If glide.http.headers\_config.enabled isn't set to true, then response header configurations defined in the HTTP Response Headers \[sys\_response\_header\] table aren't used. Security related HTTP response headers include Content Security Policy, which aids in XSS-related protections. For details on HTTP response headers, see HTTP Response Headers \(https://www.servicenow.com/docs/csh?topicname=http-response-header.html&amp;version=latest\).

-   \(New\)

Reduce the risk of cookie/session-related hijacking of web apps using a system property. If glide.http.headers\_config.enabled isn't set to true, then response header configurations defined in the HTTP Response Headers \[sys\_response\_header\] table aren't used. Security related HTTP response headers include Content Security Policy, which aids in XSS-related protections. For details on HTTP response headers, see HTTP Response Headers \(https://www.servicenow.com/docs/csh?topicname=http-response-header.html&amp;version=latest\).


</td></tr><tr><td>

[Prevent users from accepting warning to bypass CSRF validation](../reference/sc-prevent-users-from-accepting-warning-to-bypass-csrf-validation.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property prevents users from being able to accept a warning which allows a potentially malicious request to be sent to the instance. This warning appears when a POST request fails due to having a mis-matched anti-CSRF token belonging to one of the victim's other active sessions. If "glide.security.csrf.strict.validation.mode" is not set to the recommended value of "true", then an attacker can formulate a CSRF attack utilizing a leaked anti-CSRF token from a different active session belonging to the victim. A POST request to an instance contains an anti-CSRF token within "sysparm\_ck" or "XUserToken" which matches the user's current session. If the anti-CSRF token is instead tied to one of the user's other active sessions, the POST request will return a 302 redirection to security\_interceptor.do with a "Continue" button available to the user when this property is set to "false". Clicking this button will re-submit the request to the instance, except it will now having a valid anti-CSRF token. When this property is set to "true", the 302 redirection to the security\_interceptor.do page will not display a "Continue" button and the user will not be allowed to resubmit the request.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A successful CSRF attack will allow an attacker to effectively perform any operation that the victim is able to perform.


</td></tr><tr><td>

[Block access for delegated developers](../reference/sc-block-access-for-delegated-developers.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property determines whether a delegated developer can give assign roles to users through scripts. If "com.glide.sys.security.delegateddev.block\_grant\_roles" is not set to the recommended

value of "true", then a delegated developer could assign roles to any user. This could lead to unapproved privilege escalation.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Delegated developers may assign roles to any user via scripts, posing a significant security risk of unauthorized privilege escalation.


</td></tr><tr><td>

[Require Authorization for XSD Requests](../reference/sc-xsd-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The glide property "glide.basicauth.required.xsd" controls whether authentication is required in order to make a XSD request to an instance. If "glide.basicauth.required.xsd" is not set to the recommended value of "true", then authentication is disabled for XSD requests on the instance.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property allows unauthenticated access to XSD processor leaking sensitive information.


</td></tr><tr><td>

[Turn off verbose SQL error messages for import processor](../reference/sc-turn-off-verbose-sql-error-messages-for-import-processor.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If this property is false a verbose SQL error message is returned, potentially causing sensitive information disclosure.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If verbose SQL error messages are returned, sensitive information such as database structure, table names, or query details may be exposed. This information can be leveraged by attackers to craft targeted SQL injection attacks or exploit other vulnerabilities, increasing the risk of data breaches and system compromise. Limiting error detail is essential to prevent information disclosure that aids malicious activity.


</td></tr><tr><td>

[Escape scripts in scratchpad](../reference/sc-escape-scratchpad.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The scratchpad is an easy way to set information on the server that can be accessed in the browser. An admin can script anything to be on it, including arbitrary data from arbitrary records.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.ui.escape\_scratchpad" is not set to the recommended value of "true", then it is possible to execute malicious script like a cross-site scripting vulnerability.


</td></tr><tr><td>

[Require authorization for PDF requests](../reference/sc-require-authorization-for-pdf-requests.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.basicauth.required.pdf" is not set to the recommended value of "true", then this will disable Basic Authentication for PDF format export processor. This also happens when combined with a wrong role within the guest\_user related property \(For example a high privileged user such as Admin\). This will lead to unauthenticated access to instance data.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated access to PDF export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.


</td></tr><tr><td>

[Enable SNC access control plugin](../reference/sc-snc-access-control-plugin.md)

</td><td>

Remediation

 -   \(Old\)

Ensure the plugin "com.snc.snc\_access\_control" is activated. Read the documentation on activating at https://www.servicenow.com/docs/csh? topicname=t\_ActivateSNCAccessControl.html&amp;version=latest.

-   \(New\)

Ensure the plugin "com.snc.snc\_access\_control" is activated.


</td></tr><tr><td>

[Limit concurrent sessions across all nodes](../reference/sc-limit-concurrent-sessions-across-all-nodes.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property is meant to be used with the "Limit Concurrent Sessions" plugin. When this plugin is installed and configured, the number of open sessions can be limited per user. When this property is set, the number of sessions will be tracked across all nodes instead of a single application nodes.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If this property is not set to true, multiple sessions can be open across multiple nodes, increasing the likelihood of a successful session hijacking.

-   Plugin Applicability
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

com.glide.limit.concurrent.sessions


</td></tr><tr><td>

[Enable security jump start plugin \(ACL Rules\)](../reference/sc-security-jump-start-plugin-acl-rules.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Creates several important ACLs that validate the Access Controls on some of the key system tables within the Now Platform. These rules provide a jump-start on securing many system tables, making it easier for an organization to get an instance into production. The Security Jump Start \(ACL Rules\) plugin is installed automatically on all new instances.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Gaps in access control can allow unauthorized users to view, modify, or delete sensitive data, undermining data integrity, confidentiality, and compliance with organizational security policies.


</td></tr><tr><td>

[Ensure archive table ACLs are checked](../reference/sc-ensure-archive-table-acls-are-checked.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The 'glide.security.enable\_archive\_table\_acls' controls if ACLs added to archive tables are evaluated \(true\) or if only the ACLs of the original table \(i.e. the table the archive table was created from\) are evaluated \(false\). There is no reason for this property to not be true since the original table ACLs will be evaluated regardless of its value and since a customer can simply avoid additional ACLs for an archive table by not adding them.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the property is set to false, ACLs added to archived tables will be ignored, an action which is counterintuitive and may lead to authorization bypass.


</td></tr><tr><td>

[Disable Entity Expansion within the XMLDocument2 Streaming Parser](../reference/sc-disable-entity-expansion.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.stax.allow\_entity\_resolution" is not set to the recommended value of "false", then this property allow XML entities to be expanded during parsing by the streaming parser \(XMLDocument2\).

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

XML entity expansion can lead to attacks such as ability to read system files, and Denial of Service.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Boolean

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

false


</td></tr><tr><td>

[Restrict flow context read access](../reference/sc-restrict-flow-context-read-access.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property 'com.snc.process\_flow.reporting.require\_flow\_access' is set to a value of true, there is an additional access check for a user trying to read a flow context. A user must have access to the parent flow to be able to read the flow context.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

There may be minor information disclosure if this property is not set securely.


</td></tr><tr><td>

[Restrict downloadable MIME types](../reference/sc-downloadable-mime-type-denylist.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the property "glide.ui.attachment.force\_download\_all\_mime\_types" is set to true, then the "glide.ui.attachment.download\_mime\_types" property will be overridden so that all MIME types will be downloaded rather than rendered by the browser. For example, downloading text/html forces an HTML file to be downloaded to the client as a file rather than viewed inline in the browser, preventing a XSS attack.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

XSS can lead to easily attained privilege escalation to higher roles such as admin where more lateral movement can be taken.


</td></tr><tr><td>

[Minimize Entity Expansion Threshold for GlideXMLUtil Scriptable](../reference/sc-setting-entity-expansion-threshold.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls the maximum amount of entity expansion within an XML Parser. If "glide.xmlutil.max\_entity\_expansion" is not set to the recommended value of 3000 or less, then the GlideXMLUtil parsing scriptable may be vulnerable to denial of service attacks.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A Denial-of-Service \(DoS\) vulnerability poses a security risk by allowing attackers to overwhelm or crash a system, rendering it unavailable to legitimate users and potentially disrupting critical operations.


</td></tr><tr><td>

[Restrict Global App Development by Role](../reference/sc-restrict-global-app-development-by-role.md)

</td><td>

-   Short Description
    -   \(Old\)

Restrict Global App Development by Role

    -   \(New\)

Restrict Global App Development by Role

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property "sn\_g\_app\_creator.allow\_global" controls which users can create applications in the global scope using the Guided Application Creator. If "sn\_g\_app\_creator.allow\_global" is set to the recommended value of "false," users need the role "sn\_g\_app\_creator.global" to create an application in the global scope using Guided Application Creator. If "sn\_g\_app\_creator.allow\_global" is set to the insecure value of "true" then all users with only the base role "sn\_g\_app\_creator.app\_creator" can create an application in the global scope using Guided Application Creator. Applications in the global scope do not contain scope protections allowing a developer to access greater features and functions beyond a specific scope.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Limiting global application development to users with the additional role follows the principle of least privilege.


</td></tr><tr><td>

[Enable ACLs to Control Live Profile Details](../reference/sc-enable-acls-to-control-live-profile-details.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Use the glide.live\_profile.details property to designate whether a user should be able to view all detail fields, such as company name and phone numbers, in a live profile under the live feed feature. If "glide.live\_profile.details" is set to the value of "Hide", then no live profile information is visible to user. If it is set to show, all information is visible. When glide.live\_profile.details" is set to the value of "ACL", information is visible based on the user's profile ACLs.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Exposing sensitive user information such as company affiliation and contact details to unauthorized users increases the risk of data leakage and violating privacy controls if ACLs are not enforced.


</td></tr><tr><td>

[Set safe content security policy for SVG files](../reference/sc-set-safe-content-security-policy-for-svg-files.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property adds "script-src none" to the ContentSecurity-Policy header when SVGs are accessed via the ".iix" file extension, which prevents the exploitation of stored XSS from crafted file attachments stored within the instance.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Without this policy, a malicious actor could trick a user into running arbitrary JavaScript code in their web browser leading to consequences such as data exfiltration or session takeover.


</td></tr><tr><td>

[Enable Jelly JS Interpolation Protection](../reference/sc-enable-jelly-js-interpolation-protection.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property allows a customer to turn on or off interpolation protection. Interpolation protection ensures that when Jelly expressions are used in JavaScript, they must be deemed safe by either falling under certain categories OR being marked as SAFE in the expression itself. Without this mitigation enabled, a malicious actor can send a crafted GET parameter to a Jelly page and cause the contents of that parameter to be evaluated as server-side JavaScript with admin privileges.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.ui.jelly.js\_interpolation.protect" is not set to the recommended value of "true", then dangerous jelly expressions interpolated in JavaScript are allowed and user can execute code using jelly template.


</td></tr><tr><td>

[Require AJAXGlideRecord ACL checking](../reference/sc-enabling-ajaxgliderecord-acl-checking.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property toggles ACL validation for GlideAjax API calls. If "glide.script.secure.ajaxgliderecord" is not set to the recommended value of "true", then ACL validation will not be completed for GlideAjax requests.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This could lead to server-side resources being accessed by users without proper authorization.


</td></tr><tr><td>

[Enforce OCSP check on network error](../reference/sc-enforce-ocsp-check-on-network-error.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the glide property "com.glide.communications.httpclient.ocsp\_allow\_network\_error" is not explicitly set to the recommended value of false, and the OCSP \(Online Certificate Status Protocol\) check encounters a network-related issue—such as a timeout or failure to retrieve revocation data —the system will treat the OCSP validation as successful by default.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

An attacker using a revoked certificate could exploit this by simply omitting the OCSP response during a connection attempt. In such cases, the client would incorrectly accept the revoked certificate as valid, thereby undermining the integrity of the Public Key Infrastructure \(PKI\) and the trust model that underpins secure web communications. The use of revoked certificates is often indicative of malicious activity, unless attributable to temporary synchronization issues between certificate authorities and OCSP responders.


</td></tr><tr><td>

[Require authorization for excel requests](../reference/sc-excel-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.basicauth.required.excel" is not set to the recommended value of "true", then this will disable Basic Authentication for EXCEL format export processor. This also happens when combined with a wrong role within the guest\_user related property \(For example a high privileged user such as Admin\).

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated access to Excel export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.


</td></tr><tr><td>

[Use of secure insert multiple operation within import set API](../reference/sc-use-of-secure-insert-multiple-operation-within-import-set-api.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls whether GlideRecordSecure or GlideRecord is used for the Insert Multiple operation within Import Set API. If this property is set to "false", then GlideRecordSecure will be used to insert records and Table level ACLs will be evaluated. If this property is set to "true", then GlideRecord will be used to insert records and Table level ACLs will not be evaluated.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If this property is not set to the recommended value of "false", then a low privilege user may be able to insert data into tables outside the scope of their privileged roles.


</td></tr><tr><td>

[Minimize absolute session timeout duration](../reference/sc-absolute-session-timeout.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.ui.user\_cookie.max\_life\_span\_in\_days" is not set to the recommended value of "30" or other appropriate value, then a very long life session could be more vulnerable to session hijack attacks.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A long session lifespan extends the window of opportunity for attackers to hijack active sessions, increasing the likelihood of unauthorized access if credentials or session tokens are compromised.


</td></tr><tr><td>

[Disable locked form elements debugging](../reference/sc-disable-locked-form-elements-debugging.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.security.explain.write.locks" is not set to the recommended value of "False", then additional debug information is displayed on locked form elements.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Displaying debug information on locked form elements could lead to information disclosure.


</td></tr><tr><td>

[Deny unauthorized access to request items](../reference/sc-deny-unauthorized-access-to-request-items.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property defines a default behavior for the "retrieveAddress" API. When there are no roles given in property "glide.sc.req\_for.roles", the Client Callable Script Include 'ScriptServiceCatalogGetLocation' can be called by any unprivileged logged-in user and can retrieve the address of any other users in the system.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.sc.req\_for.roles.default" is not set to the recommended value of "deny" \(allow\) and the value of glide.sc.req\_for.roles is empty, then any user can request items for other users allowing unauthorized resource access.


</td></tr><tr><td>

[Check UI action conditions before execution](../reference/sc-check-ui-action-conditions-before-execution.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.security.strict.actions" is not set to the recommended value of "true", then there will be no validation on the table UI before execution. Setting this property to secure value will add an extra layer of security validation.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Users may perform operations they may not be authorized for— potentially leading to unauthorized data manipulation, privilege escalation, and bypassing of access controls designed to protect sensitive records.


</td></tr><tr><td>

[Sanitize All Translated HTML Fields](../reference/sc-sanitize-all-translated-html-fields.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property 'glide.translated\_html.sanitize\_all\_fields' is set to the value 'true', all translated\_html elements will be sanitized using an HTML sanitizer. When the property is set to 'false', an element will only be sanitized if a dictionary attribute, html\_sanitize, is set to true.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Sanitizing HTML elements is best practice to ensure an attacker cannot embed malicious content that may lead to Cross Site Scripting \(XSS\) attacks.


</td></tr><tr><td>

[Require write access to access service catalog add item page](../reference/sc-require-write-access-to-access-service-catalog-add-item-page.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property 'glide.sc.request.add\_item\_write\_access' is not set to 'true', any logged in user can access the Add Catalog Item UI page. This could result in unauthorized operations performed on catalog items.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This creates a risk of unauthorized modifications or additions to catalog items, potentially leading to service disruption, fraudulent requests, or exposure of sensitive data. Misconfigured access controls in catalog management can undermine system integrity.


</td></tr><tr><td>

[Restrict knowledge bases access](../reference/sc-restrict-knowledge-bases-access.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property is being used in the functionality of knowledge record user criteria security. If "glide.knowman.block\_access\_with\_no\_user\_criteria" is not set to the recommended value of "true", then knowledge bases without can read or can contribute user criteria become readable and writable by all users.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Knowledge bases lacking explicit "can read" or "can contribute" user criteria may become accessible and editable by all users, potentially leading to unauthorized access and modification of sensitive knowledge content.


</td></tr><tr><td>

[Activate role based multi-factor authentication](../reference/sc-role-based-multi-factor-authentication.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property enforces multi-factor authentication based on the roles assigned to the user. If this property is set to true, then it will enforce role-based multi-factor authentication for all users described in the multi\_factor\_criteria table. This table enforces multi-factor authentication based on the roles assigned to the user. If a user has been assigned "admin", "security\_admin" or "user\_admin" roles in the multi-factor roles list, MFA will be enforced.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Enforcing MFA based on roles strengthens authentication security and aligns with best practices for protecting privileged accounts.


</td></tr><tr><td>

[Verify certificate chain and hostname](../reference/sc-verify-certificate-chain-and-hostname.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property "com.glide.communications.httpclient.verify\_hostname" is not set to the secure value of "true", the hostname and certificate chain presented by remote hosts during a TLS connection initiated from the ServiceNow instance are not validated.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This could compromise the security of the TLS connection and allow person-in-the-middle attacks, where communications between two parties are intercepted. This may lead to sensitive data disclosure.


</td></tr><tr><td>

[Restrict uploaded MIME types](../reference/sc-upload-mime-type-restriction.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property is used to activate MIME type checking for uploads.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.security.file.mime\_type.validation" is not set to the recommended value of true, then MIME type validation for file attachments will not take place which could allow malicious file types to be uploaded.


</td></tr><tr><td>

[Disable soap fault stack trace display](../reference/sc-disable-soap-fault-stack-trace-display.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.soapfault.display\_stack\_trace" is not set to the recommended value of "False", then a stack trace in a SOAP fault detail element is displayed.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Displaying stack traces to users could lead to sensitive information disclosure.


</td></tr><tr><td>

[Validate SOAP content type](../reference/sc-soap-content-type-checking.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.soap.require\_content\_type\_xml" is not set to the recommended value of "true", then there is no validation for the SOAP request.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This lack of validation can enable Cross-Site Request Forgery \(CSRF\) attacks, allowing malicious actors to trick authenticated users into sending unauthorized SOAP requests.


</td></tr><tr><td>

[Enable ACLs for Encoded Query in Simple List Widget](../reference/sc-enable-acls-for-encoded-query-in-simple-list-widget.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property "glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list" is not set to "true", a user may be able to bypass ACLs evaluation on a query condition in Simple List Widget.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

It is best practice to evaluate ACLs within queries to ensure a user has access to the fields being queried to prevent unauthorized data leakage.


</td></tr><tr><td>

[Restrict Impersonation to Admin](../reference/sc-restrict-impersonation-to-admin.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property glide.sys.permissive.impersonate is set to a value of false , only users with the admin role may impersonate. When this value is set to true , users may be able to make

use of application components that expose impersonation APIs to impersonate a higher privileged user.

-   Remediation
    -   \(Old\)

Ensure the Glide Property glide.sys.permissive.impersonate is set to a value of false . If this property does not exist, the default value is false . This value is safe-overridable. If the property is set to false , it cannot be changed going forward.

    -   \(New\)

Ensure the Glide Property glide.sys.permissive.impersonate is set to a value of false . If this property does not exist, the default value is false . This value is safe-overridable. If the property is set to false , it cannot be changed going forward.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

May result in unauthorized resource access if these application components are misconfigured.


</td></tr><tr><td>

[Require authorization for WSDL request](../reference/sc-wsdl-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.basicauth.required.wsdl" is not set to the recommended value of "true", then this will disable Basic Authentication for WSDL requests. WSDL is a protocol that is used to describe web services such as instance table schemas, and is not a mechanism for sharing the data within tables. Setting this property to "true" allows for disclosure of table schemas to unauthenticated users.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated access to WSDL Requests, when combined with misconfigured guest user role, poses a risk of unauthorized table schema exposure.


</td></tr><tr><td>

[Restrict HR case updates from personal emails](../reference/sc-restrict-hr-case-updates-from-personal-emails-plugin-applicability-human-resources-scoped-app.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property 'sn\_hr\_core.restrict\_guest\_email' is not set to 'true', a user can send an email from a personal account referencing the HR case to be included in the worknotes. This could result in minor confidentiality or integrity issues if the personal email is compromised or communicating insecurely. An admin may want to restrict the ability of users to respond to HR cases via their personal email, since they cannot be confident of the user accessing the personal email account.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This creates a risk of minor confidentiality and integrity issues because personal email accounts may be insecure or compromised, and administrators cannot verify the identity or security posture of those accounts. Allowing this behavior weakens control over sensitive HR communications and increases exposure to data leakage.


</td></tr><tr><td>

[Anti-CSRF token validation time](../reference/sc-anti-csrf-token-validation-time.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Time in seconds for a secure token to expire. When the user session expires, the secure token expires with it, unless the "allowing reuse of expired tokens are allowed" property is enabled, and its within the time frame described by this property. This token is used to prevent cross site request forgery attacks. \(default is 86400 seconds or 1 day\)

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The time limit for a CSRF token to expire defines how long the token remains valid for verifying legitimate user requests; if set too long, it increases the risk that an attacker could reuse a stolen token to perform unauthorized actions, while a shorter expiration window reduces this risk by narrowing the attack window.


</td></tr><tr><td>

[Require authorization for SOAP requests](../reference/sc-soap-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The glide property 'glide.basicauth.required.soap' controls whether basic authentication is required to make a SOAP request to an instance. If 'glide.basicauth.required.soap' is not set to the recommended value of 'true', then unauthenticated users performing SOAP operations will be mapped to the soap.guest user. This may enable an unauthenticated user to perform operations on the instance as if a logged in user to the instance. There may be additional impact if the user define within 'com.glide.soap.guest\_user' is assigned additional roles.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated access to SOAP export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.


</td></tr><tr><td>

[Hide user comments on articles](../reference/sc-hide-user-comments-on-articles.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the Glide Property 'glide.knowman.show\_user\_feedback' is not set to 'never', feedback comments will be visible on knowledge articles to users with the roles defined in the Glide Property 'glide.knowman.show\_user\_feedback.roles'. Due to the potentially sensitive information in a feedback comment, an instance admin may not want the feedback to be visible.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If this property is not set to 'never', there could be confidentiality impacts if sensitive information is disclosed in feedback.


</td></tr><tr><td>

[Enforce Strict User Image Upload](../reference/sc-enforce-strict-user-image-upload.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.security.strict.user\_image\_upload" is not set to the recommended value of "true", then ACLs are not enforced on image uploads to the Photo field. When the property is set to true, the table ACLs are enforced when uploading photos, only allowing authorized users to upload an image.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

An unauthorized user may upload an image to another user's profile.


</td></tr><tr><td>

[Minimize session window timeout duration](../reference/sc-session-window-timeout.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property affects the expiry of the cookie. After each successful authentication, the cookie will expire after the number of days specified as the property value. If "glide.ui.user\_cookie.life\_span\_in\_days" is not set to the recommended value of 15 or less, then there is a higher risk that the cookie, if stolen, can be used for longer.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A longer life span increases the time window that a stolen cookie will be used.


</td></tr><tr><td>

[Require authorization for API requests](../reference/sc-api-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.basicauth.required.api" is not set to the recommended value of "true", then this will disable Basic Authentication on API request and will lead to unauthenticated access to instance data.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated access to API data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.


</td></tr><tr><td>

[Disable external content URL](../reference/sc-disable-external-content-url.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.ui.url.external.content" is not set to the recommended value of "false", then Connect chat will retrieve external link metadata in order to render richer content in messages with links to Youtube, news articles, images, etc.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This could lead to Server Side Request Forgery \(SSRF\) attacks.


</td></tr><tr><td>

[Enforce strict elevate privilege](../reference/sc-enforce-strict-elevate-privilege.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When this property is set to 'true', roles marked as "privileged" must always be manually elevated by an admin user upon new session creation in order for the user to be granted the role's capabilities. When 'false', roles marked as "privileged" are automatically elevated upon an admin user new session, and do not need to be manually elevated \(with exception of "security\_admin"\). Setting this property to secure value will add an extra layer of security validation to role elevation by privileged user.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This risks potential privilege misuse or accidental execution of highimpact actions. Requiring manual elevation adds a deliberate security checkpoint that helps prevent unauthorized or unintended access to sensitive capabilities.


</td></tr><tr><td>

[Disable MultiSSO Debugging](../reference/sc-disable-multisso-debugging.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls debug logging for multiSSO.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

MultiSSO debugging features could lead to unintended sensitive information leak.


</td></tr><tr><td>

[Enforce strict security of session cookies](../reference/sc-secure-session-cookies.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.ui.secure\_cookies" is not set to the recommended value of "true", then additional cookie security and strict cookie validation is not performed.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This could allow an attacker to bypass cookie validation leading to unauthorized resource access.


</td></tr><tr><td>

[Enable the hardened java security manager](../reference/sc-enable-the-hardened-java-security-manager.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property contains Java classname of current Java security manager. ServiceNow has standardized on the Contextual Security Manager. If "glide.security.manager" is not set to the recommended value of "com.glide.sys.security.ContextualSecurityManager", then the instance may be using an obsolete Java security manager which is missing expected hardening policies.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Without this hardening, it may be possible for a malicious actor with script execution access to achieve remote code execution on the instance.


</td></tr><tr><td>

[Restrict access to specific IP ranges plugin](../reference/sc-restrict-access-to-specific-ip-ranges-plugin.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This plugin when set to true restricts access to specific IP ranges. Unless public access is intended for the instance, administrators should limit access to their assigned IP net blocks. An exclusion list \(Deny\) or an inclusion list \(Allow\) of IP addresses can be created through IP Address Access Control \(ip\_access\_list.do\).

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Allowing unrestricted public access to a ServiceNow instance without properly configuring the IP Address Access Control plugin exposes the system to unauthorized access and potential exploitation from any IP address, undermining networklevel security and increasing the attack surface.


</td></tr><tr><td>

[Require authorization for unload requests](../reference/sc-require-authorization-for-unload-requests.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property performs authentication while retrieving data from tables/pages in the form of unload data on the instance. If "glide.basicauth.required.unl" is not set to the recommended value of "true", then this will disable Basic Authentication for the UNL format export processor. This also could be combined with a wrong role within the guest\_user related property, this will lead to unauthenticated access to instance data.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property may allow unauthenticated access to unload data exports—especially when combined with misconfigured guest user roles—creating a serious risk of unauthorized exposure of instance configuration and data.


</td></tr><tr><td>

[Require authorization for import requests](../reference/sc-import-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property performs this authentication while importing data sources into the instance tables/pages. It restricts any guest users who are currently accessing this data. If "glide.basicauth.required.importprocessor" is not set to the recommended value of "true", then unauthenticated users could access import processor. Additional access controls, ie ACLs, are still enforced, but this value allows a guest user import request to be processed and not summarily denied.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property may allow unauthenticated users to initiate import requests via the import processor, potentially bypassing initial authentication checks and increasing the risk of unauthorized data manipulation despite enforced ACLs.


</td></tr><tr><td>

[Require authorization for script requests](../reference/sc-script-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property determines if basic auth is required to invoke a scripted processor. Any records accessed by the scripted processor will still use other access controls, ie ACLs, before returning any data. If "glide.basicauth.required.scriptedprocessor" is not set to the recommended value of "true", then an attacker could access sensitive information such as an unauthenticated \(guest\) user attempting to access an email through the EmailDisplay sys\_processor.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property may allow unauthenticated users to invoke scripted processors, potentially exposing sensitive information despite existing ACLs.


</td></tr><tr><td>

[Enable contextual security plugin](../reference/sc-contextual-security-plugin.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The "Contextual Security: Role Management" plugin helps manage user groups and roles to protect information through role-based access controls. The plugin efficiently consolidates duplicate entries for inherited roles, and secures a record/information using create, read, write, and delete functionality. After it is installed and activated, the dictionary roles \(created by simple security manager\) are no longer tested. Instead, the Now Platform looks for ACL rules on fields and tables. It secures the data with the help of ACL rules instead of traditional, role-based dictionary rules implemented by simple security manager. Even if you configure the dictionary form and add roles to a dictionary entry, no change in rights occurs.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Failing to transition fully to ACL-based controls may leave sensitive data exposed due to overlooked or outdated dictionary role configurations.


</td></tr><tr><td>

[Enforce password reset on api requests](../reference/sc-enforce-password-reset-on-api-requests.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When a user is marked for "Password needs reset" they must provide a new password at the next authentication attempt. This property controls whether the password reset is mandatory before making API calls. If "glide.authenticate.api.user.reset\_password.mandatory" is not set to the recommended value of "true", then user accounts marked as "Password needs reset" can still perform most common operations by querying the table API through basic authentication.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This could allow information disclosure in the event that stale accounts are compromised.


</td></tr><tr><td>

[Disable logger for low privilege users in script sandbox](../reference/sc-glide-security-logger-no-loggining-for-sandbox.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.security.sandbox\_no\_logging" is set to "false", then logging will be available for low-privileged users using sandboxed scripts. This property controls Glide System's ability to log scripts being executed in the sandbox environment.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A low privileged user could inject logs allowing the malicious user to potentially obfuscate an attack.


</td></tr><tr><td>

[Require authentication by default for client-callable script includes](../reference/sc-privacy-on-client-callable-script-includes.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property makes sure that Client-Callable Script Includes, also known as Ajax Script Includes, are not automatically made available to nonauthenticated users. If "glide.script.ccsi.ispublic" is not set to the recommended value of "False", then it will allow Script Includes to be run as public scripts and allow unauthenticated users access to instance data.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Sensitive business logic or data is potentially exposed, increasing the risk of unauthorized access to instance resources.


</td></tr><tr><td>

[Enforce field ACLs for inbound query requests](../reference/sc-enforce-field-acls-for-inbound-query-requests.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the property "glide.export.query.enforce\_field\_acl" is set to "true", field ACLs will be checked against the incoming query, and reject the query if the user is unauthorized. If the property is false, ACLs will NOT be checked against incoming query and will continue to execute.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This can result in information disclosure to unauthorized parties.


</td></tr><tr><td>

[Limit UI active session life span](../reference/sc-limit-ui-active-session-life-span.md)

</td><td>

Functional Impact

 -   \(Old\)

Enforces max life-span on active authenticated HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero will disable timing out the active sessions. The max life-span should be more than inactive timeout glide.ui.session\_timeout \(default 30 minutes\).

-   \(New\)

Enforces max life-span on active authenticated HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero will disable timing out the active sessions. The max life-span must be more than inactive timeout glide.ui.session\_timeout \(default 30 minutes\).


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict access to emails with empty target table](../reference/sc-restrict-access-to-emails-with-empty-target-table.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.email.email\_with\_no\_target\_visible\_to\_all" is not set to the recommended value of false, then low level users will have access to emails which are not their own.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Emails that lack a specific target record may become visible to all users, resulting in unauthorized access to potentially sensitive communication and violating principles of least privilege and data confidentiality.


</td></tr><tr><td>

[Enable account recovery](../reference/sc-account-recovery.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls the account recovery feature which binds the ability to bypass single sign-on to specifically designated administrators. If "glide.sso.acr.enabled" is not set to the recommended value of "true", then the local interactive log-ins \(username or password based\) will be remain enabled when single signon is enabled on the instance.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Eliminating local interactive log-ins reduces the potential for unauthorized access to the instance.


</td></tr><tr><td>

[Require authorization for RSS requests](../reference/sc-rss-request-authorization.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls basic authorization for inbound RSS requests. If "glide.basicauth.required.rss" is not set to the recommended value of "true", then this will disable Basic Authentication for RSS format export processor. This also could be combined with a wrong role within the guest\_user related property, this will lead to unauthenticated access to instance data.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated access to RSS export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.


</td></tr><tr><td>

[Require authorization for csv requests \[Updated in Security Center 1.3\]](../reference/sc-require-authorization-for-csv-requests.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.basicauth.required.csv" is not set to the recommended value of "true", then this will disable Basic Authentication for CSV format export processor. This also happens when combined with a wrong role within the guest\_user related property \(Ex: high privileged role\). This will lead to unauthenticated access to instance data.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Unauthenticated access to CSV export data, when combined with misconfigured guest user role, poses a significant risk of unauthorized data exposure.


</td></tr><tr><td>

[Control Lockout Time for Invalid Password Reset Attempts](../reference/sc-reset-password-request-max-attempts-window.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The password\_reset.request.max\_attempt\_window property defines the number of minutes a user must wait to reset or change their password after exceeding the maximum number of unsuccessful attempts that is set with the password\_reset.request.max\_attempt property.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A value too low increases the risk of successfully brute forcing a password as a greater number of password reset attempts can be made.


</td></tr><tr><td>

[Maximize reset password SMS complexity](../reference/sc-reset-password-sms-complexity.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "password\_reset.sms.default\_complexity" is not set to the recommended value of "6" or greater, then a weak SMS validation token is used.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This increases the possibility of token guessing which could lead to account takeover.


</td></tr><tr><td>

[Minimize reset password max SMS per day](../reference/sc-reset-password-max-sms-per-day.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property "password\_reset.sms.max\_per\_day" denotes the maximum number of SMS codes sent for verification per day for a user.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the value is too high, it will be easier for attackers to brute force the SMS code.


</td></tr><tr><td>

[Require CAPTCHA for guest walk-up experience in customer service application](../reference/sc-require-captcha-for-guest-walk-up-experience-in-customer-service-application.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The captcha for the Guest Walk-up experience prevents unauthenticated guest users to create bookings by requiring users to complete a captcha verification. If captcha is not enabled, this could lead to automated creation of spam

appointments to overwhelm the system or fill up all available booking spots creating a Denial of Service attack.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This exposes the system to spam appointments and resource exhaustion attacks, potentially filling all available booking slots and causing a Denial of Service \(DoS\). Without CAPTCHA, the platform lacks a critical control to prevent automated abuse and maintain service availability.


</td></tr><tr><td>

[Minimize reset password request success window duration](../reference/sc-reset-password-request-success-window.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "password\_reset.request.success\_window" is not set to the recommended value of "1440" or less, then it increases the opportunity of someone else abusing the password reset functionality to gain unauthorized access to a user account.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Limiting the success window reduces the opportunity for abuse and strengthens account recovery security.


</td></tr><tr><td>

[Enable MID audit log](../reference/sc-enable-mid-audit-log-plugin-applicability-mid-server.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The MID Server command audit log tracks details such as the command name, command hash, name of credential used and execution status. When enabled, users with the agent\_security\_admin role can view these logs in the MID Server Command Audit Logs \[ecc\_agent\_command\_audit\_log\] table. Navigate to All &gt; MID Server &gt; Audit Logs &gt; Command Audit Logs to see this table.

-   Remediation
    -   \(Old\)

Set mid.log.command\_audit.enable to "true" in the ecc\_agent\_property table to turn on auditing for commands run by the MID server. See the following documentation for editng this mid server property: https://docs.servicenow.com/csh?topicname=mid-audit-log.html&amp;version=latest

    -   \(New\)

Set mid.log.command\_audit.enable property to true in the MID Server Properties \[ecc\_agent\_property\] table for each MID Server to turn on auditing for commands run by the MID Server. For more details on setting this property, see https://docs.servicenow.com/csh?topicname=midaudit-log.html&amp;version=latest

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

In the event of security investigation, this table can be used by incident response teams to audit the commands run on the MID server. Without this log, there might not be sufficient details to respond to situations such as unauthorized account use.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

None

-   CVSS Score
    -   \(Old\)

2.2

    -   \(New\)

4.4

-   Dependencies and Prerequisites
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This setting only applies to instances using an active Management, Instrumentation, and Discovery \(MID\) Server. A MID Server enables communication and movement of data between a ServiceNow instance and external applications, data sources, and services. Setting up a MID Server requires downloading the MID Server package on a Linux or Windows host, setting up the connection with the given ServiceNow instance and configuring additional settings. Information and references can be found at https://www.servicenow.com/docs/csh?topicname=mid-serverlanding.html&amp;version=latest. After it has been set up, a MID Server appears as a record in the MID Servers \[ecc\_agent\] table on connecting instance.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Boolean

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

false


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Enforce URL allowlist check](../reference/sc-enforce-url-allowlist-check.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.security.url.whitelist.strict\_check" is not set to the recommended value of "true" then all external URLs are allowed for redirection when "glide.security.url.whitelist" is empty. If "glide.security.url.whitelist" is not empty, then only external URLs in the whitelist are allowed. Thus either setting "glide.security.url.whitelist.strict\_check" to true OR ensuring "glide.security.url.whitelist" is set to a non-empty value with the allowed external URLs leaves the instance in a secure state.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If all external URLs are allowed for redirection, this could allow an attacker to redirect a user to a malicious website.


</td></tr><tr><td>

[Disable secure cookie debugging](../reference/sc-disable-secure-cookie-debugging.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.secure\_cookie.debug" is not set to the default value of "false", then debug messages in the SecureUserCookie and Cookie class are logged in localhost log.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Logging debug messages from the SecureUserCookie and Cookie class could lead to sensitive information disclosure.


</td></tr><tr><td>

[Minimize Allowed Attachment Size](../reference/sc-max-allowed-attachment-size.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property "com.glide.attachment.max\_size" controls the maximum size of uploaded attachment. Note: a real attachment size is calculated through multiplication 10241024value of property "com.glide.attachment.max\_size". If the value of property "com.glide.attachment.max\_size" is 1024 then the max allowed attachment size is 1Gb.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The platform can accept large files that could fill up storage or cause a denial of service.


</td></tr><tr><td>

[Enable email spam scoring and filtering](../reference/sc-email-spam-scoring-and-filtering.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The Email Filter \(com.glide.email\_filter\) plugin installs email filtering within the instance. This filtering identifies existing headers, which enables the administrator to decide what to do with the email based on the associated header. This plugin adds a header to each message. The header can be used for filtering within the instance. This feature is very helpful for filtering out spam. Note: Please make sure prerequisite properties "glide.email.read.active" is set to true, as this control only applies when inbound email is enabled.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Enabling and configuring email filtering is essential for reducing exposure to spam and maintaining system integrity.


</td></tr><tr><td>

[Disallow infected file download](../reference/sc-disallow-infected-files-download.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the property "com.glide.snap.infected\_download\_allowed" is set to "true", users can still download nonscanned attachments in the case that the antivirus service is down or unreachable.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A user may download a malicious file to their desktop.


</td></tr><tr><td>

[Block rooted or jailbroken mobile devices](../reference/sc-block-rooted-or-jailbroken-mobile-devices.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.sg.allow\_rooted\_jailbroken\_device" is not set to the recommended value of "false", then the mobile app will allow users to use the app from jailbroken or rooted mobile devices. Jailbroken or rooted mobile devices run untrusted code at the system level that can bypass the platform's security model which our mobile apps rely on. Setting "allow\_rooted\_jailbroken\_device" to "false" enables a limited client-side check to display an error message to the user if attempting to use the app from one of these devices. This configuration maps to MASVS v1.4.2 requirement 8.1 at R-level.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Allowing rooted or jailbroken mobile devices significantly increases the risk of credential theft, data leakage, and malicious code execution.


</td></tr><tr><td>

[Invalidate Session After OAuth Token Expiration \[New in Security Center 2.0\]](../reference/sc-invalidate-session-after-oauth-token-expiration.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When an OAuth access token is issued, the response includes a cookie. Users can use this cookie to continue using a session even after the OAuth token used to create that session expires. Use the glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled system property to prevent this.

-   Remediation
    -   \(Old\)

Ensure the Glide Property glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled is set to a

value of true. When the record does not exist in the sys\_properties table, the default is false. A record is created for newly provisioned instances.

    -   \(New\)

Ensure the glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled system property exists in the System Properties \[sys\_properties\] table, and is set to a value of true.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If an OAuth token is leaked or compromised, the lack of expiration would allow an attacker to use and extend the session via the created cookie. Malicious users can use sessions to access unauthorized resources and take unauthorized actions. Set this property to the secure value to eliminate this hidden session extension mechanism and reduce replay risk by enforcing token expiration.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Impact when set to true: Sessions end immediately when the access token expires. Cookies no longer refresh session validity. Clients must use refresh tokens or re-authenticate to obtain a new access token. Potential Breakage: Legacy clients or custom integrations relying on cookie-based session extension fail after token expiry. Long-running jobs without token renewal logic may encounter 401 errors. What Continues to Work: Standard OAuth flows with refresh tokens. Properly designed integrations that renew tokens proactively

-   CVSS Score
    -   \(Old\)

5.4

    -   \(New\)

6.8

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Boolean

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

true


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict XML external entities](../reference/sc-xml-entity-validation-url-allowlist.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Use the glide.xml.entity.whitelist.enabled and glide.xml.entity.whitelist system properties to prevent your instance from processing XML external entities from untrusted sources. XML external entity \(XXE\) attacks occur when a malicious actor modifies incoming XML to access data or interact with otherwise restricted systems. An attacker can use the Document Type Definition \(DTD\) to include arbitrary HTTP requests that the server may execute. This could lead to additional attacks using the server's trust relationship with other entities. To help prevent these attacks, the glide.xml.entity.whitelist.enabled system property limits the sources

from which your instance executes XML. Use the glide.xml.entity.whitelist property to define a set of trusted sources. The value for "glide.xml.entity.whitelist" set to "http://java.sun.com/j2ee/dtds/" is a reference to the DTDs \(Document Type Definitions\) provided by Java EE \(formerly known as J2EE\). This URL acts as a central point where standard DTDs for XML documents are located, which define the structure and legal elements and attributes of XML documents. NOTE: Values other than http://java.sun.com/j2ee/dtds/ can be included in the glide.xml.entity.whitelist property, but are unnecessary for the out of the box platform state. Review any additional values to determine if they are safe.

-   Remediation
    -   \(Old\)

Ensure the Glide Property "glide.xml.entity.whitelist" exists and is set to "http://java.sun.com/j2ee/dtds/" and the Glide Property "glide.xml.entity.whitelist.enabled" exists and is set to the value "true". If the properties do not appear in the sys\_properties table, add new records.

    -   \(New\)

Ensure that the glide.xml.entity.whitelist system property exists in the System Properties \[sys\_properties\] table, and is set to http://java.sun.com/j2ee/dtds/. Ensure that the glide.xml.entity.whitelist.enabled system property exists in the System Properties \[sys\_properties\] table and is set to the value true.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

An XML Eternal Entity \(XEE\) attack can allow attackers to exfiltrate data or perform unauthorized actions via crafted XML payloads.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

XML external entities from sources outside the whitelist will not be processed.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Comma-separated list, Boolean


</td></tr><tr><td>

[Limit max subscriptions per user per day](../reference/sc-limit-max-subscriptions-per-user-per-day.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "sn\_kb\_social\_qa.max\_subscriptions\_per\_user\_daily" is not set to the recommended value of "500" or less, then there will be no restriction on the maximum number of Social Q&amp;A questions to which a user can subscribe to in a day.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Too many subscriptions could lead to resource exhaution.


</td></tr><tr><td>

[Minimize Concurrent Interactive Sessions with Limit Concurrent Sessions Plugin](../reference/sc-glide-authenticate-limit-concurrent-interactive-sessions.md)

</td><td>

-   Short Description
    -   \(Old\)

Limit Concurrent Interactive Sessions When Limit Concurrent Sessions Plugin Is Installed

    -   \(New\)

Limit Concurrent Interactive Sessions with Limit Concurrent Sessions Plugin

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property is meant to be used with the Limit Concurrent Sessions \(com.glide.limit.concurrent.sessions\) plugin. When the plugin is active and the property is set to "false", a user can have any number of concurrent interactive sessions on an instance.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A greater number of open sessions means there is a great possibility for session hijacking to occur.


</td></tr><tr><td>

[Maximize reset password request unlock window duration](../reference/sc-reset-password-request-unlock-window.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property "password\_reset.request.unlock\_window" controls the number of minutes a user must wait to start a reset request after the last successful unlock account.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the value is too low, it increases the opportunity for a malicious actor from brute forcing the user's password using automated tools.


</td></tr><tr><td>

[Limit policy based session access mobile refresh token interval](../reference/sc-limit-policy-based-session-access-mobile-refresh.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property 'glide.authenticate.session\_access.mobile.refresh\_token\_interval' governs the length of time after which a mobile device user will be forced to re-authenticate. This only applies if the admin has configured the Identity Provider attributes \(which can vary for each login\) in

the session access policy and the user authenticates via Single Sign On. The property value is an integer in seconds. The recommended value is 1800 \(30 minutes\).

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A large value may grant a larger timeframe for session access to be hijacked by an attacker.


</td></tr><tr><td>

[Disable legacy JQuery UI usage](../reference/sc-disable-legacy-jquery-ui-usage.md)

</td><td>

Data Type

 -   \(Old\)

Boolean

-   \(New\)

String


</td></tr><tr><td>

[Prevent impersonating user from viewing application data](../reference/sc-prevent-impersonating-user-from-viewing-application-data.md)

</td><td>

-   Description
    -   \(Old\)

Use system properties to prevent an impersonating user from viewing application data. Prevent admin level from accessing the application specific data belonging to that user when impersonating an account. This permission can be set at the application level by creating a system property specific to the application. These system properties use the .impersonateCheck naming format \(for example sn\_hr\_core.impersonateCheck\). Create a system property with a value of true to prevent users from accessing the application-specific data belonging to another user when impersonating an account. NOTE: Not all applications are designed to work in this configuration or have a System Properties \[sys\_properties\] record for this purpose. The following scopes are configured to work with this property. sn\_opp\_market sn\_jny sn\_imt\_vaccine sn\_imt\_health\_test sn\_hr\_core sn\_egd\_goals sn\_egd\_core sn\_egd\_act sn\_em sn\_talent\_aia

    -   \(New\)

Use system properties to prevent an impersonating user from viewing application data. Prevent admin level from accessing the application specific data belonging to that user when impersonating an account. This permission can be set at the application level by creating a system property specific to the application. These system properties use the .impersonateCheck naming format \(for example sn\_hr\_core.impersonateCheck\). Create a system property with a value of true to prevent users from accessing the application-specific data belonging to another user when impersonating an account. NOTE: Not all applications are designed to work in this configuration or have a System Properties \[sys\_properties\] record for this purpose. The following scopes are configured to work with this property. sn\_opp\_market sn\_jny sn\_imt\_vaccine sn\_imt\_health\_test sn\_hr\_core sn\_egd\_goals sn\_egd\_core sn\_egd\_act

sn\_em sn\_talent\_aia sn\_ecn

-   Remediation
    -   \(Old\)

For each application with the .impersonateCheck property in the System Properties \[sys\_properties\] table, ensure the property value is set to true. These properties can only be modified by the scoped administrator for the specific application. Use this script to find which properties need to be updated or created on the instance:

var properties = \[ 'sn\_opp\_market.impersonateCheck', 'sn\_jny.impersonateCheck', 'sn\_imt\_vaccine.impersonateCheck', 'sn\_imt\_health\_test.impersonateCheck', 'sn\_hr\_core.impersonateCheck', 'sn\_egd\_goals.impersonateCheck', 'sn\_egd\_core.impersonateCheck',\]

\['sn\_egd\_act.impersonateCheck', 'sn\_em.impersonateCheck', 'sn\_talent\_aia.impersonateCheck' \]; var pm = new GlidePluginManager\(\); for \(var i = 0; i &lt; properties.length; i++\) \{ var property = properties\[i\]; var application = property.split\('.'\)\[0\]; var propertyValue = gs.getProperty\(property, 'false'\); if \(pm.isActive\(application\) &amp;&amp; propertyValue.toLowerCase\(\) != 'true'\) \{ gs.print\(property\); \} \}

    -   \(New\)

For each application with the .impersonateCheck property in the System Properties \[sys\_properties\] table, ensure the property value is set to true. These properties can only be modified by the scoped administrator for the specific application. Use this script to find which properties need to be updated or created on the instance:

var properties = \[ 'sn\_opp\_market.impersonateCheck', 'sn\_jny.impersonateCheck', 'sn\_imt\_vaccine.impersonateCheck', 'sn\_imt\_health\_test.impersonateCheck', 'sn\_hr\_core.impersonateCheck', 'sn\_egd\_goals.impersonateCheck', 'sn\_egd\_core.impersonateCheck', 'sn\_egd\_act.impersonateCheck', 'sn\_em.impersonateCheck', 'sn\_talent\_aia.impersonateCheck', 'sn\_ecn.impersonateCheck' \]; var pm = new GlidePluginManager\(\); for \(var i = 0; i &lt; properties.length; i++\) \{ var property = properties\[i\]; var application = property.split\('.'\)\[0\]; var propertyValue = gs.getProperty\(property, 'false'\); if \(pm.isActive\(application\) &amp;&amp; propertyValue.toLowerCase\(\) != 'true'\) \{ gs.print\(property\); \} \}

-   Functional Impact
    -   \(Old\)

Admin level users will not be able to impersonate another user and view that user's data in a specific application context.

    -   \(New\)

Admin level users are not able to impersonate another user and view that user's data in a specific application context.


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict unauthenticated access to attachments](../reference/sc-restrict-unauthenticated-access-attachments.md)

</td><td>

-   Description
    -   \(Old\)

Secure the images on your instance to prevent sensitive information leak. Images on your instance are accessible via urls that end in .iix. Set the glide.image\_provider.security\_enabled system property to true to prevent access to your images via these URLs. \[Note\] This property is not honored for images from the attachment table if the origin table is one of: Stationeries \[sysevent\_email\_style\] Welcome Page Sections \[sys\_home\] System Properties \[sys\_properties\]

    -   \(New\)

Use the glide.image\_provider.security\_enabled property restrict unauthenticated access to image attachments. If set to true, images are visible to any authenticated user but no unauthenticated user. If set to false, images are visible to anyone with a URL to the attachment. Thumbnails of an attached image maintain the same policy as the original attached image and are accessible to the same set of users as the original attached image. When this property is enabled, more fine grained access control for unauthenticated users is obtained through entries in the Security Allow/Deny List Entities \[sys\_security\_restricted\_list\] table and through the declaration of public KB articles for those images attached to KB articles. These exceptions to the default policy for unauthenticated users when this property is true are applied in the following order. Note in these exceptions, "parent table" refers to the table of the original image attachment from which a thumbnail is generated. 1. If the table of an attached image or parent table of a thumbnail image is deny-listed in the Security Allow/Deny List Entities \[sys\_security\_restricted\_list\] table, access is denied to the image/thumbnail. 2. If the table of an attached image or parent table of a thumbnail image is allow-listed in the Security Allow/Deny List Entities \[sys\_security\_restricted\_list\] table, access is granted to the image/thumbnail. 3. If the table of an attached image or parent table of a thumbnail image is included in a public KB article, access is granted to the image/thumbnail.

-   Remediation
    -   \(Old\)

Ensure the property "glide.image\_provider.security\_enabled" is set to "true".

    -   \(New\)

Ensure the property "glide.image\_provider.security\_enabled" is set to "true". If the property does not exist on the "sys\_properties" table, the default value is

"false".

-   Security Risk
    -   \(Old\)

Restriction should be applied for unauthenticated users as some attachments might contain sensitive information.

    -   \(New\)

If the property is set to false, image attachments are visible to anyone authenticated or unauthenticated with a URL to the attachment. This may lead to sensitive information leaks. To avoid these, set the property to true and ensure any exceptions to the default policy when the property is true are properly configured.

-   Functional Impact
    -   \(Old\)

No significant impact on the functionality. User experience might be affected because the user who formerly directly accessed .iix must go through authentication.

    -   \(New\)

If the property was previously false and then is set to true, unauthenticated users can no longer be able to access image attachments unless explicitly allowed using one of the exclusion procedures.


</td></tr><tr><td>

[Enable a deny-list password validation check](../reference/sc-enable-blacklisted-passwords-validation-check.md)

</td><td>

-   Technical Configuration Name
    -   \(Old\)

glide.enable.blacklist\_password

    -   \(New\)

glide.enable.blacklist\_password, blacklisted\_password

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Use the glide.enable.blacklist\_password property to monitor deny-list passwords. When the property is set to true, the user's password is checked against a specific list of deny-listed passwords. This denial prevents users from using a password from a set of breached passwords. You can maintain the list by inserting passwords into the Excluded Password \[blacklisted\_password\] table. ServiceNow provides a small, medium, or large password list that can be inserted to the Excluded Password table through the UI page found at All &gt; Password Policy &gt; Exclusion List Management. ServiceNow installs the small list of 5,000 passwords to new instances.

-   Remediation
    -   \(Old\)

Ensure the property "glide.enable.blacklist\_password" is set to "true".

    -   \(New\)

Ensure that the glide.enable.blacklist\_password system property is set to true and that the Excluded Password \[blacklisted\_password\] table contains a minimum of 5,000 records.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Attackers often target commonly used or previously exposed passwords. This can lead to account compromise through credential stuffing or brute-force attacks. Enforcing deny-listed password checks strengthens authentication security and reduces exposure to credential-based attacks.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Some users may have difficulty selecting a password.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Boolean

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

true


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Enforce application specific ACLs only for application data](../reference/sc-enforce-application-specific-acls-only-for-application-data.md)

</td><td>

-   Description
    -   \(Old\)

Control the behavior of application data residing in primary tables outside the application. When these properties have a value of true, only the application-specific ACLs are evaluated for access to the application data residing in these tables. Not all applications are designed to work in this configuration or use a System Property \[sys\_properties\] record for this purpose. These system properties use the glide.enforce\_security\_scope. naming format. For example, use the glide.enforce\_security\_scope.sn\_hr\_sp property for the Employee Center Core \(sn\_hr\_sp\) scope. The following application scopes contain this property: sn\_doc sn\_egd\_act sn\_egd\_core sn\_egd\_goals sn\_em sn\_gsm sn\_gsm\_info\_req sn\_gsm\_lic\_prmt sn\_gsm\_lic\_prmt\_ex sn\_gsm\_soc\_bnfts sn\_hc\_professional sn\_hr\_agent\_ws sn\_hr\_ai\_agents sn\_hr\_awa

sn\_hr\_core sn\_hr\_ef sn\_hr\_er sn\_hr\_gen\_ai sn\_hr\_hc sn\_hr\_le sn\_hr\_le\_ent sn\_hr\_mii\_base sn\_hr\_na\_galileo sn\_hr\_pad sn\_hr\_pj sn\_hr\_sp sn\_hr\_va sn\_hr\_ws sn\_imt\_health\_test sn\_imt\_tracing sn\_imt\_vaccine sn\_ja sn\_jny sn\_lg\_contracts sn\_lg\_matter sn\_lg\_ops sn\_opp\_market sn\_professional sn\_svc\_appl\_info sn\_svc\_appl\_pgm\_mg sn\_talent\_aia sn\_uni\_req sn\_uni\_task

    -   \(New\)

Control the behavior of application data residing in primary tables outside the application. When these properties have a value of true, only the application-specific ACLs are evaluated for access to the application data residing in these tables. Not all applications are designed to work in this configuration or use a System Property \[sys\_properties\] record for this purpose.

These system properties use the glide.enforce\_security\_scope. naming format. For example, use the glide.enforce\_security\_scope.sn\_hr\_sp property for the Employee Center Core \(sn\_hr\_sp\) scope. The following application scopes contain this property: sn\_doc sn\_egd\_act sn\_egd\_core sn\_egd\_goals sn\_em sn\_gsm sn\_gsm\_info\_req sn\_gsm\_lic\_prmt sn\_gsm\_lic\_prmt\_ex sn\_gsm\_soc\_bnfts sn\_hc\_professional sn\_hr\_agent\_ws sn\_hr\_ai\_agents sn\_hr\_awa sn\_hr\_core sn\_hr\_ef sn\_hr\_er sn\_hr\_gen\_ai sn\_hr\_hc sn\_hr\_le sn\_hr\_le\_ent sn\_hr\_mii\_base sn\_hr\_na\_galileo sn\_hr\_pad sn\_hr\_pj sn\_hr\_sp sn\_hr\_va sn\_hr\_ws sn\_imt\_health\_test sn\_imt\_tracing sn\_imt\_vaccine sn\_ja sn\_jny

sn\_lg\_contracts sn\_lg\_matter sn\_lg\_ops sn\_opp\_market sn\_professional sn\_svc\_appl\_info sn\_svc\_appl\_pgm\_mg sn\_talent\_aia sn\_uni\_req sn\_uni\_task sn\_egd\_lh sn\_ecn sn\_ni\_core sn\_hr\_voice\_aia

-   Remediation
    -   \(Old\)

For each application installed with the glide.enforce\_security\_scope property in the System Properties \[sys\_properties\] table, \(for example, glide.enforce\_security\_scope.sn\_hr\_core\), ensure the property value is set to true. These properties can only be modified by the scoped administrator for the specific application. If a sys\_properties record does not exist for the given application and respective property, it must be created. Use this script can to find which properties need to be updated or created on the instance: var properties = \[ 'glide.enforce\_security\_scope.sn\_uni\_task', 'glide.enforce\_security\_scope.sn\_uni\_req', 'glide.enforce\_security\_scope.sn\_svc\_appl\_info', 'glide.enforce\_security\_scope.sn\_professional', 'glide.enforce\_security\_scope.sn\_opp\_market', 'glide.enforce\_security\_scope.sn\_lg\_ops', 'glide.enforce\_security\_scope.sn\_lg\_matter', 'glide.enforce\_security\_scope.sn\_lg\_contracts', 'glide.enforce\_security\_scope.sn\_jny', 'glide.enforce\_security\_scope.sn\_ja', 'glide.enforce\_security\_scope.sn\_imt\_vaccine', 'glide.enforce\_security\_scope.sn\_imt\_tracing', 'glide.enforce\_security\_scope.sn\_imt\_health\_test', 'glide.enforce\_security\_scope.sn\_hr\_ws', 'glide.enforce\_security\_scope.sn\_hr\_va', 'glide.enforce\_security\_scope.sn\_hr\_sp', 'glide.enforce\_security\_scope.sn\_hr\_pj', 'glide.enforce\_security\_scope.sn\_hr\_pad', 'glide.enforce\_security\_scope.sn\_hr\_mii\_base', 'glide.enforce\_security\_scope.sn\_hr\_le','glide.enforce\_security\_scope.sn\_hr\_le\_ent', 'glide.enforce\_security\_scope.sn\_hr\_hc', 'glide.enforce\_security\_scope.sn\_hr\_gen\_ai', 'glide.enforce\_security\_scope.sn\_hr\_er', 'glide.enforce\_security\_scope.sn\_hr\_ef', 'glide.enforce\_security\_scope.sn\_hr\_core', 'glide.enforce\_security\_scope.sn\_hr\_awa', 'glide.enforce\_security\_scope.sn\_hr\_agent\_ws', 'glide.enforce\_security\_scope.sn\_hc\_professional', 'glide.enforce\_security\_scope.sn\_gsm\_soc\_bnfts', 'glide.enforce\_security\_scope.sn\_gsm\_lic\_prmt\_ex', 'glide.enforce\_security\_scope.sn\_gsm\_lic\_prmt', 'glide.enforce\_security\_scope.sn\_gsm\_info\_req', 'glide.enforce\_security\_scope.sn\_gsm', 'glide.enforce\_security\_scope.sn\_em', 'glide.enforce\_security\_scope.sn\_egd\_goals', 'glide.enforce\_security\_scope.sn\_egd\_core', 'glide.enforce\_security\_scope.sn\_egd\_act', 'glide.enforce\_security\_scope.sn\_doc', 'glide.enforce\_security\_scope.sn\_talent\_aia', 'glide.enforce\_security\_scope.sn\_hr\_na\_galileo', 'glide.enforce\_security\_scope.sn\_svc\_appl\_pgm\_mg', 'glide.enforce\_security\_scope.sn\_hr\_ai\_agents', 'glide.enforce\_security\_scope.sn\_hr\_mii\_base' \]; var pm = new GlidePluginManager\(\); for \(var i = 0; i &lt; properties.length; i++\) \{ var property = properties\[i\]; var application = property.split\('.'\)\[2\]; var propertyValue = gs.getProperty\(property, 'false'\); if \(pm.isActive\(application\) &amp;&amp; propertyValue.toLowerCase\(\) != 'true'\) \{ gs.print\(property\); \} \}

    -   \(New\)

For each application installed with the glide.enforce\_security\_scope property in the System Properties \[sys\_properties\] table, \(for example, glide.enforce\_security\_scope.sn\_hr\_core\), ensure the property value is set to true. These properties can only be modified by the scoped administrator for the specific application. If a sys\_properties record does not exist for the given application and respective property, it must be created. Use this script can to find which properties need to be updated or created on the instance:

var properties = \[ 'glide.enforce\_security\_scope.sn\_uni\_task','glide.enforce\_security\_scope.sn\_uni\_req', 'glide.enforce\_security\_scope.sn\_svc\_appl\_info', 'glide.enforce\_security\_scope.sn\_professional', 'glide.enforce\_security\_scope.sn\_opp\_market', 'glide.enforce\_security\_scope.sn\_lg\_ops', 'glide.enforce\_security\_scope.sn\_lg\_matter', 'glide.enforce\_security\_scope.sn\_lg\_contracts', 'glide.enforce\_security\_scope.sn\_jny', 'glide.enforce\_security\_scope.sn\_ja', 'glide.enforce\_security\_scope.sn\_imt\_vaccine', 'glide.enforce\_security\_scope.sn\_imt\_tracing', 'glide.enforce\_security\_scope.sn\_imt\_health\_test', 'glide.enforce\_security\_scope.sn\_hr\_ws', 'glide.enforce\_security\_scope.sn\_hr\_va', 'glide.enforce\_security\_scope.sn\_hr\_sp', 'glide.enforce\_security\_scope.sn\_hr\_pj', 'glide.enforce\_security\_scope.sn\_hr\_pad', 'glide.enforce\_security\_scope.sn\_hr\_mii\_base', 'glide.enforce\_security\_scope.sn\_hr\_le', 'glide.enforce\_security\_scope.sn\_hr\_le\_ent', 'glide.enforce\_security\_scope.sn\_hr\_hc', 'glide.enforce\_security\_scope.sn\_hr\_gen\_ai', 'glide.enforce\_security\_scope.sn\_hr\_er', 'glide.enforce\_security\_scope.sn\_hr\_ef', 'glide.enforce\_security\_scope.sn\_hr\_core', 'glide.enforce\_security\_scope.sn\_hr\_awa', 'glide.enforce\_security\_scope.sn\_hr\_agent\_ws', 'glide.enforce\_security\_scope.sn\_hc\_professional', 'glide.enforce\_security\_scope.sn\_gsm\_soc\_bnfts', 'glide.enforce\_security\_scope.sn\_gsm\_lic\_prmt\_ex', 'glide.enforce\_security\_scope.sn\_gsm\_lic\_prmt', 'glide.enforce\_security\_scope.sn\_gsm\_info\_req', 'glide.enforce\_security\_scope.sn\_gsm', 'glide.enforce\_security\_scope.sn\_em', 'glide.enforce\_security\_scope.sn\_egd\_goals', 'glide.enforce\_security\_scope.sn\_egd\_core', 'glide.enforce\_security\_scope.sn\_egd\_act', 'glide.enforce\_security\_scope.sn\_doc', 'glide.enforce\_security\_scope.sn\_talent\_aia', 'glide.enforce\_security\_scope.sn\_hr\_na\_galileo', 'glide.enforce\_security\_scope.sn\_svc\_appl\_pgm\_mg', 'glide.enforce\_security\_scope.sn\_hr\_ai\_agents', 'glide.enforce\_security\_scope.sn\_egd\_lh', 'glide.enforce\_security\_scope.sn\_ecn', 'glide.enforce\_security\_scope.sn\_ni\_core', 'glide.enforce\_security\_scope.sn\_hr\_voice\_aia', \];

var pm = new GlidePluginManager\(\); for \(var i = 0; i &lt; properties.length; i++\) \{ var property = properties\[i\]; var application = property.split\('.'\)\[2\]; var propertyValue = gs.getProperty\(property, 'false'\); if \(pm.isActive\(application\) &amp;&amp; propertyValue.toLowerCase\(\) != 'true'\) \{ gs.print\(property\); \} \}


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict access to background script](../reference/sc-restrict-access-to-background-script.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Use the glide.script\_processor.admin system property to set a required role to access the Scripts - Background module. If this property isn't set to the recommended value of background\_script\_admin or another high privileged role, users with lower privileged roles are able to run background scripts on your instance.

-   Remediation
    -   \(Old\)

Ensure the property "glide.script\_processor.admin" is set to the "admin". This is the default value on instances.

    -   \(New\)

Ensure the property glide.script\_processor.admin is set to background\_script\_admin. This is also the default value.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Background scripts allow a complete bypass of the ACL system allowing full access to tables.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Users without the role specified in the property are unable to access the Scripts - Background module, as intended.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

String containing a user role

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

background\_script\_admin

-   Fallback Value
    -   \(Old\)

admin

    -   \(New\)

background\_script\_admin


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Verify certificate revocation](../reference/sc-verify-certificate-revocation.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If the property "com.glide.communications.httpclient.verify\_revoked\_certificate" is not configured to the recommended value of true, certificate revocation checks will be skipped during the TLS handshake.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This omission undermines a critical security control, potentially allowing an attacker to use a revoked certificate without detection. As a result, it compromises the integrity of the Public Key Infrastructure \(PKI\) and the trust model that underpins secure web communications.


</td></tr><tr><td>

[Reduce the Scope of the IP Allow List for an Instance](../reference/sc-ip-addresses-access-allowlist.md)

</td><td>

-   Short Description
    -   \(Old\)

Define Allowed ServiceNow Internal IP Addresses

    -   \(New\)

Reduce the Scope of the IP Allow List for an Instance

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Use the glide.ip.authenticate.strict property to reduce the scope of the IP allow list of an instance and restrict the IP addresses that ServiceNow personnel can use to make inbound/outbound connections to an instance. The exact IP ranges removed from the IP allow list by this property may be adjusted over time as the

ServiceNow internal network changes. When set to true, glide.ip.authenticate.strict always guarantees an IP allow list that is equal to or more restrictive than the default. When glide.ip.authenticate.strict is set to true: A strict list of ServiceNow IP ranges replaces the default IP allow lists for inbound and outbound requests. This IP allow list, which starts with a more restrictive predefined set of allowed IP ranges, is replaced by the property glide.ip.authenticate.allow.secured.self\_hosted\_list if the instance is self-hosted. When glide.ip.authenticate.strict is set to false: The default IP allow list is used which contains a wider set of ServiceNow IP ranges. The default IP allow list is replaced by the contents of glide.ip.authenticate.allow.self\_hosted\_list if the instance is self-hosted. Note: Regardless of the value of glide.ip.authenticate.strict or if the instance is self-hosted, the allow list includes IP addresses in the glide.custom.ip.authenticate.allow and glide.custom.ip.outbound.authenticate.allow system properties, if defined. All IP list properties share the same format, which is a comma separated range of IP addresses in IPv4 or IPv6 format. IP ranges are specified using a hyphen \(10.0.10.14-10.0.10.19\), using CIDR notation \(10.0.10.0/24\), or consist of a single IP address \(10.0.10.5\). At runtime, you can make additions to the IP allow list by adding entries to the IP Address Access Controls \[ip\_access\] table. This table can also be used to explicitly deny IP ranges access to an instance.

-   Remediation
    -   \(Old\)

Ensure the property "glide.ip.authenticate.allow.secured" contains only trusted values and that the property "glide.ip.authenticate.strict" is set to "true".

    -   \(New\)

Ensure that the property glide.ip.authenticate.strict is set to true. If the property does not exist in the System Properties \[sys\_properties\] table, the default value is false.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Broader access increases the risk of unauthorized or unnecessary access to the instance by non-essential internal users, such as support or sales staff, and reduces control over privileged access. Enforcing strict IP authentication limits connectivity to essential infrastructure, strengthening security and reducing exposure to insider threats or misconfigurations.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This should have no functional impact. It may restrict nonessential ServiceNow personal from accessing an instance. However, these are individuals that do not generally require access to such instances. If access is required, you can grant it on a case by case basis using the IP Address Access Controls \[ip\_access\] table.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

boolean

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

false


</td></tr><tr><td>

[Enforce secure referrer policy](../reference/sc-enforce-secure-referrer-policy.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Use the com.glide.security.referrerpolicy system property to control what information is included in the referrer HTTP header across the Now Platform. The data included in the referrer header, according to the policy of this property, is the origin, path, and query strings of the full referrer URL. These values are the standardized Referrer-Policy values supported by the HTTP protocol with the addition of the

value "default." Depending on the policy set by this property, the referrer header may include sensitive information about or from the entity making the request.

-   Remediation
    -   \(Old\)

Ensure Glide Property 'com.glide.security.referrerpolicy' is set to 'default'.

    -   \(New\)

Ensure that the com.glide.security.referrerpolicy system property is set to one of the following: "default", "same-origin", "origin-when-cross-origin", or "strict-originwhen-cross-origin"

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the com.glide.security.referrerpolicy system property is set to no-referrer-when-downgrade or unsafe-url, the referrer header of a request to a site different to the origin includes the full URL for the referring page making the request. The full referrer URL shared with external sites may include sensitive information from or about your instance. This can lead to data leakage and privacy violations. When the property is set to no-referrer, origin, or strict-origin, the referrer header is either not included, or includes only the origin portion of the referrer URL when requests are sent to the origin. This change may impede efforts to trace attack paths in the logs when a security incident occurs, as the exact origin of a request can't be determined easily. Proper configuration of this property is essential to help prevent unauthorized disclosure of internal identifiers or confidential parameters while allowing for security incident investigations.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When the com.glide.security.referrerpolicy system property is set to no-referrer, origin, or strict-origin, the referrer header is either not included, or includes only the origin portion of the referrer URL when requests are sent to the origin. This change can break functionality that requires this data. Some sites like YouTube require embedded link requests to include at least the origin in the referrer header \(for example, the "origin-when-cross-origin" policy\). The appropriate value of this property is dependent on the instance owner and use case. Those we recommend are described here. These policies are secure and do not break base system functionality. More information of these and the other standardized policies can be found at https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Referrer-Policy. default: Functionally equal to setting the value to same-origin same-origin: Sends the origin, path, and query string for same-origin requests. Doesn't send the referrer header for cross-origin requests. origin-when-cross-origin: When performing a same-origin request, sends the origin, path, and query string. Sends only the origin for cross-origin requests and requests to less secure destinations \(from HTTPS to HTTP\). strict-origin-when-cross-origin: Sends the origin, path, and query string when performing a same-origin request. For cross-origin requests, sends the origin only when the protocol security level stays same \(from HTTPS to HTTPS\). Doesn't send the referrer header to less secure destinations \(from HTTPS to HTTP\).

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

string

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

default


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict allowed domains for cross-origin iframe communication](../reference/sc-enable-url-allowlist-for-cross-origin-iframe-communication.md)

</td><td>

-   Short Description
    -   \(Old\)

Enable URL Allowlist for Cross-Origin iframe Communication

    -   \(New\)

Restrict allowed domains for cross-origin iframe communication

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Use the glide.ui.concourse.onmessage\_enforce\_same\_origin property to prevent cross-origin communication from untrusted domains. If not set to the recommended value of true then validation is not performed for cross-origin messaging. If set to true then domains listed in the glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist system property can propagate messages in the UI. Use

glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist to control which domains are allowed.

-   Remediation
    -   \(Old\)

Ensure the property "glide.ui.concourse.onmessage\_enforce\_same\_origin" is set to "true".

    -   \(New\)

Ensure that the glide.ui.concourse.onmessage\_enforce\_same\_origin property exists in the System Properties \[sys\_properties\] table and is set to true.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If a web page's event handlers don't perform proper origin validation, then another web page or script from any origin can communicate with it. These pages or scripts can also initiate any functionality performed by the event handler. This property allows potentially untrusted external domains to send messages to the ServiceNow instance, increasing the risk of cross-origin attacks like data theft or UI manipulation.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If you don't add intended domains to the inclusion list in the glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist system property, cross-origin messages from that domain aren't allowed.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Boolean

-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

true

-   Fallback Value
    -   \(Old\)

true

    -   \(New\)

false


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Require Minimum and Maximum Password Length](../reference/sc-set-minimal-password-length.md)

</td><td>

-   Short Description
    -   \(Old\)

Set Minimal Password Length

    -   \(New\)

Require Minimum and Maximum Password Length

-   Description
    -   \(Old\)

If password policies are not enabled and enforcing a minimum password length of at least 12 characters, then a user can create a password with fewer than 12 characters.

    -   \(New\)

Password policies define the requirements for passwords your users create on your instance. The password length must fall within the range accepted by the NIST 800-63B document.

-   Remediation
    -   \(Old\)

For every Password Credential Store in use on the instance, ensure that a Password Policy is being enforced, and that the Password Policy mandates a minimum password length of at least 12 characters. For every utilized Password Credential Store \(the pwd\_cred\_store table\), ensure that "Enable password policy" is checked on the record. Next, navigate to the Password Policy \( password\_policy \) record referenced in the Password Credential Store record "Password policy" field. Ensure that the "Minimum Password Length" field is set to at least 12. Further instructions on configuring a password policy can be in the documentation: https://www.servicenow.com/docs/csh?topicname=enable-passwordpolicies.html&amp;version=latest.

    -   \(New\)

1. Ensure that a password policy is being enforced for each password credential store in use on your instance: a. For each password credential store record in the Password Reset Credential Stores \[pwd\_cred\_store\] table, ensure that Enable password policy field is activated. 2. Ensure that the password policy mandates a minimum password length of at least 15 characters and maximum password length of at least 64 characters. a. Navigate to the Password Policy \[password\_policy\] record referenced in the record's Password policy field. Ensure that the Minimum Password Length field is set to at least 15 and Maximum Password Length field is set to at least 64. 3. Further instructions on configuring a password policy can be in the documentation: https://www.servicenow.com/docs/csh?topicname=enable-passwordpolicies.html&amp;version=latest.

-   Security Risk
    -   \(Old\)

Setting the property to less than a value of 12 could lead to compliance issues and increases the risk of an attacker successfully brute forcing passwords.

    -   \(New\)

Allowing passwords that are too short or not long enough could lead to compliance issues and increases the risk of an attacker successfully brute forcing passwords.

-   Functional Impact
    -   \(Old\)

From a technical perspective, the instance will not suffer any impact from a minimum password length of 12.

    -   \(New\)

Instances do not suffer any impact from a minimum password length of 15 or maximum password length of 64.

-   Data Type
    -   \(Old\)

Integer

    -   \(New\)

Boolean and Integer

-   Out of Box Value
    -   \(Old\)

8

    -   \(New\)

- The Minimum Password Length on Password Policy \[password\_policy\] records is 8 by default. The Maximum Password Length on Password Policy \[password\_policy\] records is 100 by default.

-   Fallback Value
    -   \(Old\)

8

    -   \(New\)

- The fallback value of Minimum Password Length on Password Policy \[password\_policy\] records is 8. The fallback value of Maximum Password Length on Password Policy \[password\_policy\] record is 100.


 Rule Script

 \(New\) Script updated to improve detection accuracy.

</td></tr><tr><td>

[Limit maximum number of attachments in email](../reference/sc-limit-maximum-number-of-attachments-in-email.md)

</td><td>

-   Short Description
    -   \(Old\)

Limit Maximum Number of Attachments in Email

    -   \(New\)

Limit Maximum Number of Attachments in Inbound Emails

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Use the glide.email.inbound.max\_attachment\_count system property to control the maximum number of attachments allowed per inbound email. Attachments from inbound emails are by default stored as attachments in the Email \[sys\_email\] table on your instance. If an attachment exceeds the maxumim allowed count, a record is created in the Email Attachments \[sys\_email\_attachment\] table containing the discarded file name and the reason it was discarded.

-   Remediation
    -   \(Old\)

Ensure the property "glide.email.inbound.max\_attachment\_count" is set to "30" or less.

    -   \(New\)

Set the value of this property to 30 or less to help avoid instance performance degradation.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

A large number of attachments in inbound emails can cause instance performance degradation.

-   Functional Impact
    -   \(Old\)

Total number of ACONFs changed: 185

    -   \(New\)

If an email contains more attachments than the allowed count, the attachments are discarded.


</td></tr></tbody>
</table>**Parent Topic:**[Updated hardening settings](hardening-settings-updated.md)

