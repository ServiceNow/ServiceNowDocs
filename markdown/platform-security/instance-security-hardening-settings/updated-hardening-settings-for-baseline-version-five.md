---
title: Updated hardening settings for baseline version 5.0
description: Some hardening settings have been updated with the release of Security Center baseline version 5.0.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 18
breadcrumb: [Updated hardening settings, Baseline versions, Hardening settings, Platform Security]
---

# Updated hardening settings for baseline version 5.0

Some hardening settings have been updated with the release of Security Center baseline version 5.0.

Baseline version 5 includes several updates to short descriptions for style and consistency across records. In addition, many property related scripts were updated to improve the accuracy of default values in cases where the property has been removed from the sys\_property table.

<table id="table_g2z_bbt_bzb"><thead><tr><th>

Documentation

</th><th>

Updates

</th></tr></thead><tbody><tr><td>

[Require authorization for SOAP requests \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-soap-request-authorization.md)

</td><td>

-   New remediation: Ensure the Glide Property **glide.basicauth.required.soap** exists and is set to the value true. Alternatively, configure the instance for WS Security by setting the property glide.soap.require\_ws\_security to true and following the product documentation to configure WS Security Profiles. If the property does not appear in the sys\_properties table, add a new record.
-   Old remediation: Ensure the property **glide.basicauth.required.soap** is set to the value true. Alternatively, configure the instance for WS Security by setting the property **glide.soap.require\_ws\_security** to true and following the product documentation to configure WS Security Profiles.

</td></tr><tr><td>

[Enforce OCSP check on network error \[New in Security Center 1.3 and updated in 2.0\]](../reference/sc-enforce-ocsp-check-on-network-error.md)

</td><td>

-   New remediation: Ensure the property **com.glide.communications.httpclient.ocsp\_allow\_network\_error** exists and is set to false. If the property does not appear in the sys\_properties table, add a new record.
-   Old Remediation: Ensure the property **com.glide.communications.httpclient.ocsp\_allow\_network\_error** is set to false.

</td></tr><tr><td>

[Disable external content url \[Updated in Security Center 2.0\]](../reference/sc-disable-external-content-url.md)

</td><td>

-   New remediation: Ensure the Glide Property **glide.ui.url.external.content** exists and is set to the value false. If the property does not appear in the sys\_properties table, add a new record.
-   Old Remediation: Ensure the property **glide.ui.url.external.content** is set to false.
-   New CVSS Score: 7.2
-   Old CVSS Score: 8.1
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict XML external entities \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-xml-entity-validation-url-allowlist.md)

</td><td>

-   New remediation: Ensure the Glide Property **glide.xml.entity.whitelist** exists and is set to "[http://java.sun.com/j2ee/dtds/](http://java.sun.com/j2ee/dtds/)" and the Glide Property **glide.xml.entity.whitelist.enabled** exists and is set to the value true. If the properties do not appear in the sys\_properties table, add new records.
-   Old Remediation: Ensure the property **glide.xml.entity.whitelist** is set to "[http://java.sun.com/j2ee/dtds/](http://java.sun.com/j2ee/dtds/)" and the property **glide.xml.entity.whitelist.enabled** is set to true.

</td></tr><tr><td>

[Disable unauthenticated published reports \[Updated in Security Center 2.0\]](../reference/sc-disable-unauthenticated-published-reports.md)

</td><td>

-   New remediation: Ensure the Glide Property **glide.report.published\_reports.enabled** exists and is set to the value false. If the property does not appear in the sys\_properties table, add a new record.
-   Old Remediation: Ensure the property **glide.report.published\_reports.enabled** is set to false.

</td></tr><tr><td>

[Enable password reset policy checks \[Updated in Security Center 2.0\]](../reference/sc-enable-password-reset-policy-checks.md)

</td><td>

-   New remediation: Ensure the Glide Property **glide.enable.password\_policy** exists and is set to the value true. If the property does not appear in the sys\_properties table, add a new record.
-   Old Remediation: Ensure the property **glide.enable.password\_policy** is set to true.

</td></tr><tr><td>

[Minimize Entity Expansion Threshold for GlideXMLUtil Scriptable \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-setting-entity-expansion-threshold.md)

</td><td>

-   New remediation: Ensure the property **glide.xmlutil.max\_entity\_expansion** is set to 3000 or less. If the instance is on Washington or later, the default implied value is 3000 if the sys\_properties record does not exist. If the instance is not on Washington or later, the recommendaiton is for the instance admin to create a sys\_properties record with name **glide.xmlutil.max\_entity\_expansion** and the value 3000.
-   Old Remediation: Ensure the property **glide.xmlutil.max\_entity\_expansion** is set to 3000 or less.

</td></tr><tr><td>

[Disable outbound SSLv2/SSLv3 connections \[Updated in Security Center 1.3\]](../reference/sc-disabling-sslv2-sslv3.md)

</td><td>

-   New remediation: Ensure the Glide Property **glide.outbound.sslv3.disabled** exists and is set to the value true. If the property does not appear in the sys\_properties table, add a new record.
-   Old Remediation: Ensure the property **glide.outbound.sslv3.disabled** is set to true.

 **Important:** The value for the **glide.outbound.sslv3.disabled** property is a safe override and cannot be altered once changed.

</td></tr><tr><td>

[Disable GlideRecord Scope Fencing Legacy Behavior \[New in Security Center 1.3 and updated in 1.5 and 2.0\]](../reference/sc-enable-gliderecord-scope-fencing-legacy-behavior.md)

</td><td>

-   New short description: Disable GlideRecord Scope Fencing Legacy Behavior
-   Old short description: Enable GlideRecord Scope Fencing Legacy Behavior

</td></tr><tr><td>

[Restrict uploaded MIME types \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-upload-mime-type-restriction.md)

</td><td>

-   New remediation: Ensure the property **glide.security.file.mime\_type.validation** exists and is set to true. If the property does not appear in the sys\_properties table, add a new record.
-   Old remediation: Ensure the property **glide.security.file.mime\_type.validation** is set to true.

</td></tr><tr><td>

[Enable Jelly JS interpolation protection for nested expressions \[Updated in Security Center 2.0\]](../reference/sc-enable-jelly-js-interpolation-protection-for-nested-expressions.md)

</td><td>

-   New remediation: Ensure the Glide Property **glide.ui.jelly.js\_interpolation.protect\_nested\_expressions** exists and is set to the value true. If the property does not appear in the sys\_properties table, add a new record.
-   Old remediation: Ensure the property **glide.ui.jelly.js\_interpolation.protect\_nested\_expressions** is set to true.

</td></tr><tr><td>

[Enable SSL in LDAP authentication \[Updated in Security Center 1.5 and 2.0\]](../reference/sc-enable-ssl-in-ldap-authentication.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable UserCookie version 3.1 \[Updated in Security Center 2.0\]](../reference/sc-enable-usercookie-version-3-1.md)

</td><td>

-   New description: UserCookie v3 is generated only when property**glide.ui.secure.cookies.use\_kmf is disabled**. UserCookie v3 is not secure due to storing secret key for HMAC in source code and identical for all customers. That can support malicious actors to use this one secret key for attempts to hijacking user sessions. By setting the property **glide.ui.secure.cookies.use\_kmf** to true UserCookie v3.1 will be used and secret key will be stored in security storage such as KMF.
-   Old description: UserCookie v3 is generated only when property **glide.ui.secure.cookies.use\_kmf** is disabled. UserCookie v3 is not secure due to storing secret key for HMAC in source code and identical for all customers. That can support malicious actors to use this one secret key for attempts to hijacking user sessions.
-   New remediation: Ensure the property **glide.ui.secure.cookies.use\_kmf** exists and is set to true. If the property does not appear in the sys\_properties table, add a new record.
-   Old remediation: Ensure the property **glide.ui.secure.cookies.use\_kmf** is set to true. Which means UserCookie v3.1 will be used and secret key will be stored in security storage such as KMF.

</td></tr><tr><td>

[Set OTP lifetime for password reset to 1 hour \[Updated in Security Center 2.0\]](../reference/sc-set-otp-lifetime-for-password-reset-to-12-hours-or-less.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Log user impersonation \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-log-user-impersonation.md)

</td><td>

-   New remediation: Ensure the property **glide.sys.log\_impersonation** exists and is set to true. If the property does not appear in the sys\_properties table, add a new record.
-   Old remediation: Ensure the property **glide.sys.log\_impersonation** is set to true.

</td></tr><tr><td>

[Required jms connection factories \[New in Security Center 1.3 and updated in 1.5 and 2.0\]](../reference/sc-required-jms-connection-factories-plugin-applicability-mid-server.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Ensure dashboards creation/deletion requires access check \[New in Security Center 1.3 and updated in 2.0\]](../reference/sc-ensure-dashboards-creation-deletion-requires-access-check.md)

</td><td>

-   New remediation: Ensure the Glide Property **glide.processors.check\_access\_before\_process** exists and is set to the value true. If the property does not appear in the sys\_properties table, add a new record.
-   Old remediation: Ensure the value of **glide.processors.check\_access\_before\_process** is always true.

</td></tr><tr><td>

[Proactively invalidate inactive sessions \[New in Security Center 1.3 and updated in 1.5 and 2.0\]](../reference/sc-proactively-invalidate-inactive-sessions.md)

</td><td>

-   New remediation: Ensure the Glide Property **glide.active.session.timeout.invalidate.session** exists and is set to the value true. If the property does not appear in the sys\_properties table, add a new record.
-   Old remediation: Set the Glide Property **glide.active.session.timeout.invalidate.session** to true.

</td></tr><tr><td>

[Enforce Security Scope for Agent Workspace for HR Case Management \[New in Security Center 1.5 and updated in 2.0\]](../reference/sc-enforce-security-scope-for-agent-workspace-hr-case.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enforce security scope license and permit playbook \[New in Security Center 1.5 and updated in 2.0\]](../reference/sc-enforce-security-scope-license-and-permit-playbook.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict downloadable MIME types \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-downloadable-mime-type-denylist.md)

</td><td>

-   New description: If the property **glide.ui.attachment.force\_download\_all\_mime\_types** is set to true, then the **glide.ui.attachment.download\_mime\_types** property will be overridden so that all MIME types will be downloaded rather than rendered by the browser. For example, downloading text/html forces an HTML file to be downloaded to the client as a file rather than viewed inline in the browser, preventing a XSS attack. XSS can lead to easily attained privilege escalation to higher roles such as admin where more lateral movement can be taken.
-   Old description: If the property **glide.ui.attachment.force\_download\_all\_mime\_types** is not set to true, then the **glide.ui.attachment.download\_mime\_types** property will be overridden so that all MIME types will be downloaded rather than rendered by the browser. For example, downloading text/html forces an HTML file to be downloaded to the client as a file rather than viewed inline in the browser, preventing a XSS attack. The ability to have XSS can lead to easily attained privilege escalation to higher roles such as admin where more lateral movement can be taken.
-   New remediation: Ensure the property **glide.ui.attachment.force\_download\_all\_mime\_types** is set to true. If the property does not exist in the sys\_properties table, the default value is false.
-   Old remediation: Ensure the property **glide.ui.attachment.force\_download\_all\_mime\_types** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Define restricted downloadable MIME types \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-downloadable-mime-types.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Disallow infected file download \[Updated in Security Center 1.5 and 2.0\]](../reference/sc-disallow-infected-files-download.md)

</td><td>

-   New description: When the property **com.glide.snap.infected\_download\_allowed** is set to true, users can still download non-scanned attachments in the case that the antivirus service is down or unreachable. This means it is possible that a user downloads a malicious file and risks infecting the user's desktop \(in the case there is no other endpoint protection on the device\).
-   Old description: If **com.glide.snap.infected\_download\_allowed** is not set to the recommended value of False, then it is possible to download a malicious file that has not been scanned leading to a risk of infecting the user's desktop.
-   New remediation: Ensure the property **com.glide.snap.infected\_download\_allowed** is set to false.
-   Old remediation: Ensure the property **com.glide.snap.infected\_download\_allowed** is set to False.

</td></tr><tr><td>

[Restrict access to GlideSystemUserSession scriptable API \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-access-glidesystemusersession-scriptable-api.md)

</td><td>

-   New description: gs.addErrorMessageNoSanitizationMessaging\(\) and gs.addInfoMessageNoSanitization\(\) are used within the scripting environment for logging and notifications. Both of these are available in the sandbox if this property is not set to the recommended value of false. The sandbox is a low privileged scripting environment available to unauthenticated and no role users. Both of these methods can be used to display unsanitized input to a user. Displaying unsanitized input to the user is dangerous, as unsanitized input may contain dangerous code that runs in the user's browser. This can be utilized for traditional reflected XSS attacks. Reflected XSS attacks can be used in multiple scenarios, including session hijacking.
-   Old description: Messaging within the glide scripting sandbox is used for logging purposes. Calling this unsanitized error function exposes the platform to reflected XSS attacks. XSS attacks can allow for easy privilege escalation by stealing someone's session cookies. If **glide.sandbox.usersession.allow\_unsanitized\_messages** is not set to the recommended value of false, then the unsanitized error messaging functions addErrorMessageNoSanitization and addInfoMessageNoSanitization are available to script.

</td></tr><tr><td>

[Enable work order management query rules for service organizations \[New in Security Center 1.5 and updated in 2.0\]](../reference/sc-enable-work-order-management-query-rules.md)

</td><td>

-   New description: When set to true, rules/filters from sn\_query\_rule table will be used to determine read access to Field Service Management-related tables \(Work Order and Work Order Task\) to the logged in user through query business rules and read ACLs. When false, the records won't be filtered based on query rules. Query business rules add additional security validations. Specifically, this property will filter records for agents, qualifiers, and dispatchers based on their assigned territory or territory membership. It is best practice to follow the principle of least privilege when reading records. When this property is not set to true, there may be increased risk of data exposure from Field Service Management tables.
-   Old description: When set to true, rules/filters from sn\_query\_rule table will be used to determine read access to Field Service Management-related tables \(Work Order and Work Order Task\) to the logged in user through query business rules and read ACLs. When false, the records won't be filtered based on query rules. Query business rules add additional security validations. Specifically, this property will filter records for agents, qualifiers, and dispatchers based on their assigned territory or territory membership. It is best practice to follow the principle of least privilege when reading records.

</td></tr><tr><td>

[Restrict email domains for external user registration \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-external-user-registration-email-domain-allowlist.md)

</td><td>

-   New description: The **sn\_ext\_usr\_reg.allowed\_email\_domains** property defines which email addresses are allowed to self-register to a ServiceNow instance. The format should be a comma separated list of acceptable email domains such as domain1.com,domain2.com where emails such as example@domain2.com will be accepted. If **sn\_ext\_usr\_reg.allowed\_email\_domains** is not set with a list of acceptable domains, then users with any email address are allowed to register accounts on the instances. If not defined, malicious actors could perform registration using emails addresses from unwanted domains to gain authenticated access to the instance.
-   Old description: The **sn\_ext\_usr\_reg.allowed\_email\_domains** property defines which email addresses are allowed to self-register to a ServiceNow instance. If **sn\_ext\_usr\_reg.allowed\_email\_domains** is not set with a list of acceptable domains, then users with any email address are allowed to register accounts on the instances. If not defined, malicious actors could perform registration using emails addresses from unwanted domains to gain authenticated access to the instance.

</td></tr><tr><td>

[Apply domain separation on dot walked fields \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-apply-domain-separation.md)

</td><td>

-   New description: This property controls whether join queries are given domain separated conditions or not, in order to ensure they apply domain separation functionality for dot walked fields. If **glide.sys.domain.include\_domain\_condition\_on\_join** is not set to the recommended value of true on an instance using domain separation, then sensitive information could be disclosed that is not to be shared with a specific domain. There may be moderate functional impact to the instance if components are reliant on the unsafe cross domain queries. Instances should be tested in subproduction environments before enabling.
-   Old description: This property controls whether join queries are given domain separated conditions or not, in order to ensure they apply domain separation functionality for dot walked fields. If **glide.sys.domain.include\_domain\_condition\_on\_join** is not set to the recommended value of true on an instance using domain separation, then sensitive information could be disclosed that is not to be shared with a specific domain.

</td></tr><tr><td>

[Enforce URL allowlist check \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-enforce-url-allowlist-check.md)

</td><td>

-   New remediation: Ensure the property **glide.security.url.whitelist.strict\_check** is set to true or the property **glide.security.url.whitelist** is set to a value.
-   Old remediation: Ensure the property **glide.security.url.whitelist.strict\_check** is set to "true" and the property **glide.security.url.whitelist** is set to a value.

</td></tr><tr><td>

[Set guest user for soap requests \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-set-guest-user-for-soap-requests.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict access to background script \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-restrict-access-to-background-script.md)

</td><td>

-   New description: This property holds the required role to access Script Background module. If **glide.script\_processor.admin** is not set to the recommended and default value of admin, then users having a lower privileged role will be able to run background scripts on the instance. This will lead to a complete bypass of the ACL system allowing full access to tables.
-   Old description: This property holds the required role to access Script Background module. If **glide.script\_processor.admin** is not set to the recommended value of admin, security\_admin, or maint, then users having a lower privileged role will be able to run background scripts on the instance. This will lead to a complete bypass of the ACL system allowing full access to tables.
-   New remediation: Ensure the property **glide.script\_processor.admin** is set to the admin. This is the default value on instances.
-   Old remediation: Ensure the property **glide.script\_processor.admin** is set to the admin, security\_admin, or maint role.

</td></tr><tr><td>

[Verify certificate chain and hostname \[New in Security Center 1.3 and updated in 2.0\]](../reference/sc-verify-certificate-chain-and-hostname.md)

</td><td>

-   New description: When the Glide Property **com.glide.communications.httpclient.verify\_hostname** is not set to the secure value of true, the hostname and certificate chain presented by remote hosts during a TLS connection initiated from the ServiceNow instance are not validated. This could compromise the security of the TLS connection and allow person-in-the-middle attacks, where communications between two parties are intercepted. This may lead to sensitive data disclosure.
-   Old description: If **com.glide.communications.httpclient.verify\_hostname** is not set to true this could allow person-in-the-middle attacks where communications between two parties are intercepted. Setting this property to an insecure value disables the certificate verification process which evaluates all certifications in the certificate chain through checking revocation status. Set this property to true to prevent the http client from connecting to a potentially harmful hostname.

</td></tr><tr><td>

[Control Lockout Time for Invalid Password Reset Attempts \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-reset-password-request-max-attempts-window.md)

</td><td>

-   New short description: **Control Lockout Time for Invalid Password Reset Attempts**
-   Old short description: **Minimize Reset Password Request Max Attempts Window Duration**
-   New description: The **password\_reset.request.max\_attempt\_window** property defines the number of minutes a user must wait to reset or change their password after exceeding the maximum number of unsuccessful attempts that is set with the **password\_reset.request.max\_attempt property**. A small number of minutes for the **password\_reset.request.max\_attempt\_window** property increases the risk of successfully brute forcing a password as a greater number of password reset attempts can be made. The default of 1440 minutes is recommended.
-   Old description: If **password\_reset.request.max\_attempt\_window** is not set to the recommended value of 1440 or less, then it could be possible to perform account bruteforce as the account will not be locked after a maximum number of wrong authentication attempts.
-   New remediation: Ensure the property **password\_reset.request.max\_attempt\_window** is set to 1440 or greater.
-   Old remediation: Ensure the property **password\_reset.request.max\_attempt\_window** is set to 1440 or less.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Disable GlideRecord Scope Fencing Legacy Behavior \[New in Security Center 1.3 and updated in 1.5 and 2.0\]](../reference/sc-enable-gliderecord-scope-fencing-legacy-behavior.md)

</td><td>

-   New short description: **Disable GlideRecord Scope Fencing Legacy Behavior**
-   Old short description: **Enable GlideRecord Scope Fencing Legacy Behavior**
-   New remediation: Set the Glide Property **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** to false. When not present in the sys\_properties table, the default value is true.
-   Old remediation: Set the Glide Property **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** to false.

</td></tr><tr><td>

[Limit Invalid Password Reset Attempts \[Updated in Security Center 1.3 and updated in 2.0\]](../reference/sc-reset-password-request-max-attempts.md)

</td><td>

-   New short description: **Limit Invalid Password Reset Attempts**
-   Old short description: **Minimize Reset Password Request Max Attempt Allowance**

</td></tr></tbody>
</table>**Parent Topic:**[Updated hardening settings](hardening-settings-updated.md)

