---
title: Updated hardening settings for baseline version 4.0
description: Some hardening settings have been updated with the release of Security Center baseline version 4.0.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 26
breadcrumb: [Updated hardening settings, Baseline versions, Hardening settings, Platform Security]
---

# Updated hardening settings for baseline version 4.0

Some hardening settings have been updated with the release of Security Center baseline version 4.0.

Baseline version 4.0 includes several updates to short descriptions for style and consistency between records. In addition, many property related scripts were also updated to improve accuracy of the default value for cases where the property has been removed from the sys\_property table.

<table id="table_g2z_bbt_bzb"><thead><tr><th>

Documentation

</th><th>

Updates

</th></tr></thead><tbody><tr><td>

[Require authorization for SOAP requests \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-soap-request-authorization.md)

</td><td>

-   New technical configuration name: **glide.basicauth.required.soap, glide.soap.require\_ws\_security**
-   Old technical configuration name: **glide.basicauth.required.soap**
-   New description: The glide property **glide.basicauth.required.soap** controls whether basic authentication is required to make a SOAP request to an instance. If **glide.basicauth.required.soap** is not set to the recommended value of true, then unauthenticated users performing SOAP operations will be mapped to the soap.guest user. This may enable an unauthenticated user to perform operations on the instance as if a logged in user to the instance. There may be additional impact if the user define within **com.glide.soap.guest\_user** is assigned additional roles.
-   Old description: The glide property **glide.basicauth.required.soap** controls whether authentication is required to make a SOAP request to an instance. If **glide.basicauth.required.soap** is not set to the recommended value of true, then authentication is disable for SOAP requests on the instance. It allows unauthenticated access to administrator or maint level operations; thereby negating security controls within the instance.
-   New remediation: Ensure the property **glide.basicauth.required.soap** is set to the value true. Alternatively, configure the instance for WS Security by setting the property **glide.soap.require\_ws\_security** to true and following the product documentation to configure WS Security Profiles.
-   Old remediation: Ensure the property **glide.basicauth.required.soap** exists in the sys\_properties table and is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Escape jelly script \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-escape-jelly.md)

</td><td>

-   New description: This property escapes all the JS and HTML strings included in before they are written to the output stream, preventing several XSS issues from occurring. If **glide.ui.escape\_all\_script** is not set to the recommended value of true, then escaping of scripts injected into Jelly is disabled. Without this mitigation, the platform becomes widely open to a variety of script injection attacks. An attacker could execute arbitrary Rhino scripts on the instance.
-   Old description: The following property escapes all the JS and HTML strings included in &lt;j:jelly&gt; ... &lt;/j:jelly&gt; before they are written to the output stream, preventing several XSS issues from occurring. If **glide.ui.escape\_all\_script** is not set to the recommended value of "true", then escaping of scripts injected into Jelly is disabled. Without this mitigation, the platform becomes widely open to a variety of script injection attacks. An attacker could execute arbitrary Rhino scripts on the instance.

</td></tr><tr><td>

[Prevent Users From Accepting Warning To Bypass CSRF Validation \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-csrf-strict-validation.md)

</td><td>

-   New short description: Prevent Users From Accepting Warning To Bypass CSRF Validation
-   Old short description: Enforce CSRF Token Strict Validation
-   New description: This property prevents users from being able to accept a warning which allows a potentially malicious request to be sent to the instance. This warning appears when a POST request fails due to having a mis-matched anti-CSRF token belonging to one of the victim's other active sessions. If **glide.security.csrf.strict.validation.mode** is not set to the recommended value of true, then an attacker can formulate a CSRF attack utilizing a leaked anti-CSRF token from a different active session belonging to the victim.A POST request to an instance contains an anti-CSRF token within sysparm\_ck or X-UserToken which matches the user's current session. If the anti-CSRF token is instead tied to one of the user's other active sessions, the POST request will return a 302 redirection to security\_interceptor.do with a Continue button available to the user when this property is set to false. Clicking this button will re-submit the request to the instance, except it will now having a valid anti-CSRF token. When this property is set to true, the 302 redirection to the security\_interceptor.do page will not display a Continue button and the user will not be allowed to resubmit the request.A successful CSRF attack will allow an attacker to effectively perform any operation that the victim is able to perform.
-   Old description: This property enables CSRF token strict validation which prevents the reuse of CSRF tokens. If **glide.security.csrf.strict.validation.mode** is not set to the recommended value of true, then CSRF tokens could be reused which opens a door to CSRF attacks.
-   New CVSS Score: 3.7
-   Old CVSS Score: 3.1

</td></tr><tr><td>

[Require Authentication on Event Management HTTP Processor \[New in Security Center 1.3, Updated in 1.5, and removed in 2.0\]](../reference/sc-require-authentication-on-event-management-http-processor.md)

</td><td>

-   New short description: Require Authentication on Event Management HTTP Processor
-   Old short description: Require Authentication on Event Management HTTP Processor

</td></tr><tr><td>

[Enable Anti-CSRF token \[New in Security Center 1.3, updated in 1.5, and removed in 2.0\]](../reference/sc-anti-csrf-token.md)

</td><td>

-   New description: Cross-Site Request Forgery \(CSRF\) is an attack that forces authenticated users to submit a request to a Web application against which they are currently authenticated. CSRF attacks exploit the trust a Web application has in an authenticated user. This property enables usage of a secure token to identify and validate incoming requests. This token is used to prevent cross site request forgery attacks. If **glide.security.use\_csrf\_token** is not set to the recommended value of true, then CSRF is possible.
-   Old description: Cross-Site Request Forgery \(CSRF\) is an attack that forces authenticated users to submit a request to a Web application against which they are currently authenticated. CSRF attacks exploit the trust a Web application has in an authenticated user. This property enables usage of a secure token to identify and validate incoming requests. This token is used to prevent cross site request forgery attacks. If**glide.security.use\_csrf\_token** is not set to the recommended value of true, then CSRF is possible.

</td></tr><tr><td>

[Enable HTML Sanitizer within Virtual Agent \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-enable-html-sanitizer.md)

</td><td>

-   New short description: Enable HTML Sanitizer within Virtual Agent
-   Old short description: Enable HTML Sanitizer
-   New description: This property controls the whether the HtmlSanitizerService is enabled. If **com.glide.cs.html.sanitizer.enabled** is not set to true, then a Stored Cross-Site Scripting \(XSS\) attack is possible in the VA web client.
-   Old description: This property controls the whether the HTMLSanitezerService is enabled. If **com.glide.cs.html.sanitizer.enabled** is not set to true, then a Stored Cross-Site Scripting \(XSS\) attack is possible in the VA web client.

</td></tr><tr><td>

[Deny internal access to explicit external roles \[Updated in Security Center 1.3 and 1.5\]](../../security/reference/sc-enable-explicit-roles-internal-denylist.md)

</td><td>

-   New technical configuration name: **glide.security.explicit\_roles.enable\_internal\_user\_blacklist**
-   Old technical configuration name: **glide.security.explicit\_roles.enable\_internal\_user\_blacklist,glide.security.explicit\_roles.internal\_user\_blacklist**
-   New description: This property prevents external users from being assigned the snc\_internal role. When **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** is set to the recommended value of true, then it enforces the parameters of the maint-protected **glide.security.explicit\_roles.internal\_user\_blacklist property** which assigns the snc\_external role to a list of untrusted user classes. If the value is set to false, the **glide.security.explicit\_roles.internal\_user\_blacklist** property is ignored. Misconfiguration of this propery increases the risk that an external user account gains access to internal information.
-   Old description: This prevents external users from being assigned the snc\_internal role. If **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** is not set to the recommended value of true, and the **glide.security.explicit\_roles.internal\_user\_blacklist** property is not set to a list of untrusted user classes, then the specified roles can be assigned the snc\_internal role instead of the snc\_external role. If the list is empty, then all users will be assigned the snc\_internal role by default. The property should contain at least the default roles csm\_consumer\_user, customer\_contact.

Misconfiguration of these properties increases the risk that an external user account gains access to internal information.

-   New remediation: Ensure the property **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** is set to true.
-   Old Remediation: Ensure the property **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** is set to true and that the property **glide.security.explicit\_roles.internal\_user\_blacklist** includes the dangerous items csm\_consumer\_user, customer\_contact.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Require authorization for WSDL request \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-wsdl-request-authorization.md)

</td><td>

-   New description: If **glide.basicauth.required.wsdl** is not set to the recommended value of true, then this will disable Basic Authentication for WSDL requests. WSDL is a protocol that is used to describe web services such as instance table schemas, and is not a mechanism for sharing the data within tables. Setting this property to true allows for disclosure of table schemas to unauthenticated users.
-   Old description: If **glide.basicauth.required.wsdl** is not set to the recommended value of true, then this will disable Basic Authentication for WSDL requests. This could lead to information disclosure to unauthenticated users.
-   New CVSS Score: 5.3
-   Old CVSS Score: 4.3

</td></tr><tr><td>

[Enforce URL allowlist check \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-enforce-url-allowlist-check.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Define restricted downloadable MIME types \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-downloadable-mime-types.md)

</td><td>

-   New short description: Define Restricted Downloadable MIME Types
-   Old short description: Restrict Downloadable MIME Types
-   New description: If **glide.ui.attachment.download\_mime\_types** does include dangerous items such as text/html,image/svg,image/svg+xml,application/xml, then dangerous files could be rendered inline in the browser which could lead to Cross Sitte Scripting attacks \(XSS\). This property is the list of comma separated attachment mime types which will not render inline in the browser. For example, including text/html will force HTML files to be downloaded to the client as attachments rather than viewed inline in the browser. Maintaining this list properly will prevent cross site scripting attacks.
-   Old description: If **glide.ui.attachment.download\_mime\_types** does include dangerous items such as text/html,image/svg,image/svg+xml,application/xml, then dangerous files could be rendered inline in the browser which could lead to Cross Sitte Scripting attacks \(XSS\). This property is the list of comma separated attachment mime types which will not render inline in the browser. For example, including text/html will force html files to be downloaded to the client as attachments rather than viewed inline in the browser. Maintaining this list properly will prevent cross site scripting attacks.

</td></tr><tr><td>

[Escape HTML in list views \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-escape-html.md)

</td><td>

-   New description: This property helps sanitize list view displaying of HTML fields. If **glide.ui.escape\_html\_list\_field** is not set to the recommended value of true, then a malicious user can inject HTML code within the form field to execute unwanted scripts on different client/user sessions. This could potentially be leveraged by attackers to steal session information and sensitive data.
-   Old description: The following property helps sanitize list view displaying of HTML fields. If **glide.ui.escape\_html\_list\_field** is not set to the recommended value of true, then a malicious user can inject HTML code within the form field to execute unwanted scripts on different client/user sessions. This could potentially be leveraged by attackers to steal session information and sensitive data.

</td></tr><tr><td>

[Restrict email domains for external user registration \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-external-user-registration-email-domain-allowlist.md)

</td><td>

-   New short description: Restrict Email Domains for External User Registration
-   Old short description: Restrict Email Domains for External User Registration \(Plugin Applicability: External User Registration\)
-   New Description: The **sn\_ext\_usr\_reg.allowed\_email\_domains** property defines which email addresses are allowed to self-register to a ServiceNow instance. If **sn\_ext\_usr\_reg.allowed\_email\_domains** is not set with a list of acceptable domains, then users with any email address are allowed to register accounts on the instances. If not defined, malicious actors could perform registration using emails addresses from unwanted domains to gain authenticated access to the instance.
-   Old Description: If **sn\_ext\_usr\_reg.allowed\_email\_domains** is not set with a whitelist of acceptable domains, then malicious actors could perform registration using emails addresses from unwanted domains.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable Captcha for External User Registration \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-enable-captcha-external-user-registration.md)

</td><td>

-   New short description: Enable Captcha for External User Registration
-   Old short description: Enable Captcha for External User Registration \(Plugin Applicability: External User Registration\)
-   Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Minimize external user registration link expiration duration \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-external-user-registration-link-expiration.md)

</td><td>

-   New short description: Minimize External User Registration Link Expiration Duration
-   Old short description: Minimize External User Registration Link Expiration Duration \(Plugin Applicability: External User Registration\)
-   Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Disallow infected file download \[Updated in Security Center 1.5 and 2.0\]](../reference/sc-disallow-infected-files-download.md)

</td><td>

-   New short description: Disallow Infected File Download
-   Old short description: Disallow Infected Files Download
-   New remediation: Ensure the property **com.glide.snap.infected\_download\_allowed** is set to False.
-   Old Remediation: Ensure the property **com.glide.snap.infected\_download\_allowed** is set to True.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Validate file mime type in AttachmentCreator soap web service \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-validate-file-mime-type-in-attachmentcreator.md)

</td><td>

-   New description: If **glide.attachment.enforce\_security\_validation** is not set to the recommended value of true, then there will be no validation for attachment mime-type and dangerous files could be uploaded on the system using wrong file extensions. When this property is set to true, files are uploaded with the correct file type extension. It is a security best practice to validate file uploads at least with MIME type validation.
-   Old description: If **glide.attachment.enforce\_security\_validation** is not set to the recommended value of True, then there will be no validation for attachment mime-type and dangerous files could be uploaded on the system using wrong file extensions. When this property is set to true, files are uploaded with the correct file type extension. It is a security best practice to validate file uploads at least with MIME type validation.
-   New remediation: Ensure the property **glide.attachment.enforce\_security\_validation** is set to true.
-   Old Remediation: Ensure the property **glide.attachment.enforce\_security\_validation** is set to True.

</td></tr><tr><td>

[Disable MultiSSO Debugging \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-disable-multisso-debugging.md)

</td><td>

-   New short description: Disable MultiSSO Debugging
-   Old short description: Disable MultiSSO Debugging \(Plugin Applicability: Multiple Provider Single Sign-On\)

</td></tr><tr><td>

[Define allowed ServiceNow internal IP addresses \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-ip-addresses-access-allowlist.md)

</td><td>

-   New technical configuration name: **glide.ip.authenticate.strict**
-   Old technical configuration name: **glide.ip.authenticate.strict,glide.ip.authenticate.allow.secured**
-   New description: If **glide.ip.authenticate.strict** is set to true, then internal ServiceNow personelle and systems can only make inbound connections to the instance from essential IP ranges. This limit's ServiceNow's visibility into the instance to essential internal infrastructure, and prevents access by broader ServiceNow personelle such as support and sales staff via corporate networks. When set to "true", the **glide.ip.authenticate.allow** property is used to grant internal ServiceNow inbound connections. If not set to true, then a broader ServiceNow internal IP range as defined in **glide.ip.authenticate.allow** is used to grant internal ServiceNow inbound connections.
-   Old description: If **glide.ip.authenticate.strict** is set to true, then only IP ranges specified in **glide.ip.authenticate.allow.secured** can make inbound connections to the instance. This property contains a list of only essential ServiceNow internal IP ranges \(Secure VPN, DC\). If **glide.ip.authenticate.allow.secured** is not set to the recommended value or permutation of "10.0.0.0/8, 37.98.232.0/21, 103.23.64.0/22, 149.96.0.0/17, 149.96.0.0/16, 199.91.136.0/21, 148.139.0.0/16, 127.0.0.1" or the newer value list "10.0.0.0/8, 37.98.232.0/21, 103.23.64.0/22, 149.96.0.0/17, 149.96.0.0/16, 199.91.136.0/21, 148.139.0.0/16, 127.0.0.1, 0:0:0:0:0:0:0:1, ::1" which adds IPv6 localhost to Utah, then it may allow untrusted sources outside of SN DataCenter and secure VPN to access sensitive monitoring endpoints on instances.
-   New remediation: Ensure the property **glide.ip.authenticate.allow.secured** contains only trusted values and that the property **glide.ip.authenticate.strict** is set to true.
-   Old remediation: Ensure the property **glide.ip.authenticate.allow.secured** contains only values in "10.0.0.0/8, 37.98.232.0/21, 103.23.64.0/22, 149.96.0.0/17, 149.96.0.0/16, 199.91.136.0/21, 148.139.0.0/16, 127.0.0.1, 0:0:0:0:0:0:0:1, ::1" and that the property **glide.ip.authenticate.strict** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Disable Entity Expansion within the XMLDocument2 Streaming Parser \[Updated in Security Center 1.5\]](../reference/sc-disable-entity-expansion.md)

</td><td>

-   New short description: Disable Entity Expansion within the XMLDocument2 Streaming Parser
-   Old short description: Disable Entity Expansion
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Apply domain separation on dot walked fields \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-apply-domain-separation.md)

</td><td>

-   New short description: Apply Domain Separation on Dot Walked Fields
-   Old short description: Apply Domain Separation on Dot Walked Fields \(Plugin Applicability: Domain Separation\)
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict permissions for CMDB model \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-restrict-permissions-cmdb-model.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Require clearing pasteboard when backgrounding mobile application \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-require-clearing-pasteboard-when-backgrounding-mobile-application.md)

</td><td>

-   New description: The **glide.sg.clear\_pasteboard\_when\_backgrounded** property controls if text copied from ServiceNow mobile app is kept in the clipboard and pasteboard after the app is in background mode. If it is not set to the recommended value of true, then sensitive information may be disclosed to the Android or iOS clipboard where it can be exposed to other applications on the device.
-   Old description: The property **glide.sg.clear\_pasteboard\_when\_backgrounded** controls if text copied from ServiceNow mobile app is kept in the clipboard/pasteboard after the app is no longer in focus. If it is not set to the recommended value of true, then sensitive information may be disclosed to the Android or iOS clipboard where it can be exposed to other applications on the device.

</td></tr><tr><td>

[Enable account recovery \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-account-recovery.md)

</td><td>

-   New short description: Enable Account Recovery
-   Old short description: Enable Account Recovery \(Plugin Applicability: Multiple Provider Single Sign-On\)

</td></tr><tr><td>

[Disable SQL Error Messages \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-disabling-sql-error-messages.md)

</td><td>

-   New description: If **glide.db.loguser** is not set to the recommended value of false, then sensitive server-side error messages could be displayed to end-users. Error messages can include stack traces and information about the structure of the database that could provide an attacker the knowledge needed to perform successful SQL Injection should the preconditions exist. As defense in depth, these error messages should not be displayed to the end user.
-   Old description: If **glide.db.loguser** is not set to the recommended value of false, then sensitive server-side error messages could be displayed to end-users.

</td></tr><tr><td>

[Enforce relative links \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-enforce-relative-links.md)

</td><td>

-   New description: The **glide.cms.catalog\_uri\_relative** property enforces relative links from the URI parameter on /ess/catalog.do. If **glide.cms.catalog\_uri\_relative** is not set to the recommended value of true, then the URL will not be sanitized with the enforceRelativeURL\(url\) function. Absolute URLs can pose a security risk when used as a part of parameter or a field value, thus redirecting the source page to an adversary-controlled website. This property impacts the legacy Content Management System \(CMS\) which has been replaced with Service Portal.
-   Old description: The **glide.cms.catalog\_uri\_relative** property enforces relative links from the URI parameter on /ess/catalog.do. If **glide.cms.catalog\_uri\_relative** is not set to the recommended value of true, then the URL will not be sanitized with the enforceRelativeURL\(url\) function. Absolute URLs can pose a security risk when used as a part of parameter or a field value, thus redirecting the source page to an adversary-controlled website.

</td></tr><tr><td>

[Minimize Entity Expansion Threshold for GlideXMLUtil Scriptable \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-setting-entity-expansion-threshold.md)

</td><td>

-   New short description: Minimize Entity Expansion Threshold for GlideXMLUtil Scriptable
-   Old short description: Minimize Entity Expansion Threshold
-   New description: This property controls the maximum amount of entity expansion within an XML Parser. If **glide.xmlutil.max\_entity\_expansion** is not set to the recommended value of 3000 or less, then the GlideXMLUtil parsing scriptable may be vulnerable to denial of service attacks.
-   Old description: This property controls the maximum amount of entity expansion within an XML Parser. If **glide.xmlutil.max\_entity\_expansion** is not set to the recommended value of 3000 or less, then XML parser may be vulnerable to denial of service attacks.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Disable GlideRecord Scope Fencing Legacy Behavior \[New in Security Center 1.3 and updated in 1.5 and 2.0\]](../reference/sc-enable-gliderecord-scope-fencing-legacy-behavior.md)

</td><td>

-   New description: GlideRecord provided cross scope create/update access to tables that were not configured with that level of access. In order to prevent customers from having applications broken when this scoped access behavior was patched, the property **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** was created. When true, cross scope access falls back onto legacy behavior \(insecure\). This property disables scope fencing, allowing scoped apps to access global script interfaces. It is best security practice to have scope fencing restrictions in place. Scoping ensures applications can only access resources with explicit access or within their scope, following the principle of least privilege. Disabiling this feature could lead to confidentiality, availability, and integrity impacts.
-   Old description: Legacy behavior provided create/update access to tables that did not allow so. In order to prevent legacy customers from having applications broken when this scoped access behavior was patched, the property **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** was created. When true, cross scope access falls back onto legacy behavior \(insecure\). This property disables scope fencing, allowing scoped apps to access global script interfaces. It is best security practice to have scope fencing restrictions in place. Scoping ensures applications can only access resources with explicit access or within their scope, following the principle of least privilege. Disabiling this feature could lead to confidentiality, availability, and integrity impacts.

</td></tr><tr><td>

[Enable updated version of MultiSSO plugin \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-updated-version-of-multi-sso-plugin-is-enabled.md)

</td><td>

-   New short description: Enable Updated Version of Multi SSO Plugin
-   Old short description: Enable Updated Version of Multi SSO Plugin \(Plugin Applicability: Multiple Provider Single Sign-On\)

</td></tr><tr><td>

[Enable SSL in LDAP authentication \[Updated in Security Center 1.5 and 2.0\]](../reference/sc-enable-ssl-in-ldap-authentication.md)

</td><td>

Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enforce password reset on api requests \[Updated in Security Center 1.5\]](../reference/sc-enforce-password-reset-on-api-requests.md)

</td><td>

Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Do not apply password policy at login \[Updated in Security Center 1.5 and removed in 2.0\]](../reference/sc-do-not-apply-password-policy-at-login.md)

</td><td>

-   New description: By setting the property**glide.apply.password\_policy.on\_login** to False there will be no password complexity enforcement at login time. Setting the property to True will enforce password complexity and lead to organization policy compliance issues.

As per ASVS 4.03 v2.1.9 recommendations :

Verify that there are no password composition rules limiting the type of characters permitted. There should be no requirement for upper or lower case or numbers or special characters. \(C6\)

Instead of password complexity enforcement, ASVS recommendations are to enforce a minimum length of 12 characters for password length.

Ref: [OWASP ASVS v4.0 Authentication](https://github.com/OWASP/ASVS/blob/master/4.0/en/0x11-V2-Authentication.md)

-   Old description:

By setting the property **glide.apply.password\_policy.on\_login** to False there will be no password complexity enforcement at login time. Setting the property to True will enforce password complexity and lead to organisation policy compliance issues.

As per ASVS 4.03 v2.1.9 recommendations :

Verify that there are no password composition rules limiting the type of characters permitted. There should be no requirement for upper or lower case or numbers or special characters. \(C6\)

Instead of password complexity enforcement, ASVS recommendations are to enforce a minimum length of 12 characters for password length.

Ref: [OWASP ASVS v4.0 Authentication](https://github.com/OWASP/ASVS/blob/master/4.0/en/0x11-V2-Authentication.md)


</td></tr><tr><td>

[Do not use demo certificates for active saml configurations \[Updated in Security Center 1.5\]](../reference/sc-do-not-use-demo-certificates-active-saml-configurations-plugin.md)

</td><td>

-   New short description: Do Not Use Demo Certificates for Active SAML Configurations
-   Old short description: Do Not Use Demo Certificates for Active SAML Configurations \(Plugin Applicability: Multiple Provider Single Sign-On\)

</td></tr><tr><td>

[Minimize SAML notBefore or notOnOrAfter constraint duration \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-saml-notbefore-or-notonorafter-constraint.md)

</td><td>

-   New short description: Minimize SAML "notBefore" or "notOnOrAfter" Constraint Duration
-   Old short description: Minimize SAML "notBefore" or "notOnOrAfter" Constraint Duration \(Plugin Applicability: Multiple Provider Single Sign-On\)

</td></tr><tr><td>

[Block Expired Anti-CSRF Tokens \[Updated in Security Center 1.5\]](../reference/sc-block-expired-csrf-tokens.md)

</td><td>

-   New short description: Block Expired Anti-CSRF Tokens
-   Old short description: Block Expired CSRF Tokens

</td></tr><tr><td>

[Require captcha for guest walk-up experience in customer service application \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-require-captcha-for-guest-walk-up-experience-in-customer-service-application.md)

</td><td>

-   New short description: Require Captcha for Guest Walk-up Experience in Customer Service Application
-   Old short description: Require Captcha for Guest Walk-up Experience in Customer Service Application \(Plugin Applicability: Guest Walk-up Experience for Customer Service\)

</td></tr><tr><td>

[Check impersonation on ACL evaluation in HR App \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-check-impersonation-on-acl-evaluation-in-hr-app-plugin-applicability-human-resources-scoped-app.md)

</td><td>

-   New short description: Check Impersonation on ACL Evaluation in HR App
-   Old short description: Check Impersonation on ACL Evaluation in HR App \(Plugin Applicability: Human Resources Scoped App\)

</td></tr><tr><td>

[Restrict HR case updates from personal emails \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-restrict-hr-case-updates-from-personal-emails-plugin-applicability-human-resources-scoped-app.md)

</td><td>

-   New short description: Restrict HR Case Updates from Personal Emails
-   Old short description: Restrict HR Case Updates from Personal Emails \(Plugin Applicability: Human Resources Scoped App\)
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable MID audit log \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-enable-mid-audit-log-plugin-applicability-mid-server.md)

</td><td>

-   New short description: Enable MID Audit Log
-   Old short description: Enable MID Audit Log \(Plugin Applicability: MID Server\)

</td></tr><tr><td>



</td><td>

-   New short description: Enforce Credential Alias Usage
-   Old short description: Enforce Credential Alias Usage \(Plugin Applicability: MID Server\)

</td></tr><tr><td>

[Required jms connection factories \[New in Security Center 1.3 and updated in 1.5 and 2.0\]](../reference/sc-required-jms-connection-factories-plugin-applicability-mid-server.md)

</td><td>

-   New short description: Required JMS Connection Factories
-   Old short description: Required JMS Connection Factories \(Plugin Applicability: MID Server\)
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Limit attachment size in training and prediction flows \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-limit-attachment-size-in-training-and-prediction-flows-plugin-applicability-platform-document-intelligence.md)

</td><td>

-   New short description: Limit Attachment Size in Training and Prediction Flows
-   Old short description: Limit Attachment Size in Training and Prediction Flows \(Plugin Applicability: Platform Document Intelligence\)

</td></tr><tr><td>

[Ensure archive table ACLs are checked \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-ensure-archive-table-acls-are-checked.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Log session audit events \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-log-session-audit-events.md)

</td><td>

-   New description: When the Glide Property **glide.authenticate.session\_access.log\_audit\_event** is set to true, session audit events will be created in the sys\_session\_access\_audit table. It is best practice to log information about who accessed a session to assist in malicious actor investigations. Information logged will include user, session ID \(non-sensitive\), IP address, roles, and policies.
-   Old description: When the Glide Property **glide.authenticate.session\_access.log\_audit\_event** is set to true, session audit events will be created in the sys\_session\_access\_audit table. It is best practice to log general information about session access to assist in malicious actor investigations. Information logged will include user, session ID \(non-sensitive\), IP address, roles, and policies.

</td></tr><tr><td>

[Enforce scoped ACL access for information request playbooks \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-enforce-scoped-acl-access-for-information-request-playbooks.md)

</td><td>

-   New short description: Enforce Scoped ACL Access for Information Request Playbooks
-   Old short description: Enforce Scoped ACL Access for Information Request Playbooks
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Proactively invalidate inactive sessions \[New in Security Center 1.3 and updated in 1.5 and 2.0\]](../reference/sc-proactively-invalidate-inactive-sessions.md)

</td><td>

-   New description: The Glide Property **glide.active.session.timeout.invalidate.session** controls if a timed out session is proactively invalidated before the Tomcat container invalidates the session. When this property is not set to true, there can be a small interval of time where a timed out session is not invalidated \(60+ seconds, depending on queue size\). If a session is hijacked, an attacker may be able to utilize a session during this small period of time.
-   Old description: The Glide Property **glide.active.session.timeout.invalidate.session** controls if a timeout session is proactively invalidated before the Tomcat container. When this property is not set to true, there can be a small interval of time where a timed out session is not invalidated \(60+ seconds, depending on queue size\). If a session is hijacked, an attacker may be able to utilize a session during this small period of time.

</td></tr><tr><td>

[Limit HTTP response body size \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-limit-http-response-body-size.md)

</td><td>

-   New short description: Limit HTTP Response Body Size
-   Old short description: Ensure HTTP Responses Do Not Trigger a OutofMemory Exception Due to Response Body Size

</td></tr></tbody>
</table>**Parent Topic:**[Updated hardening settings](hardening-settings-updated.md)

