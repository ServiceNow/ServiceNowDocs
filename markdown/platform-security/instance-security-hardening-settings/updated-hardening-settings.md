---
title: Updated hardening settings for baseline version 2.0
description: Some hardening settings have been updated with the release of Security Center baseline version 2.0.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 43
breadcrumb: [Updated hardening settings, Baseline versions, Hardening settings, Platform Security]
---

# Updated hardening settings for baseline version 2.0

Some hardening settings have been updated with the release of Security Center baseline version 2.0.

<table id="table_g2z_bbt_bzb"><thead><tr><th>

Documentation

</th><th>

Updates

</th></tr></thead><tbody><tr><td>

[Minimize concurrent interactive session quantity \[Updated in Security Center 1.3\]](../reference/sc-glide-authenticate-max-concurrent-interactive-sessions.md)

</td><td>

-   New short description: Minimize Concurrent Interactive Session Quantity
-   Old short description: Glide Authenticate Max Concurrent Interactive Sessions

</td></tr><tr><td>

[Enforce certificate trust \[Updated in Security Center 1.3 and removed in 2.0\]](../reference/sc-certificate-trust.md)

</td><td>

-   New short description: Enforce Certificate Trust
-   Old short description: Certificate Trust

</td></tr><tr><td>

[Maximize reset password SMS complexity \[Updated in Security Center 1.3\]](../reference/sc-reset-password-sms-complexity.md)

</td><td>

-   New short description: Maximize Reset Password SMS Complexity
-   Old short description: Reset Password SMS Complexity

</td></tr><tr><td>

[Enable High Security Plugin \[Updated in Security Center 1.3\]](../reference/sc-high-security-plugin.md)

</td><td>

-   New short description: Enable High Security Plugin
-   Old short description: High Security Plugin

</td></tr><tr><td>

[Enforce strict security of session cookies \[Updated in Security Center 1.3\]](../reference/sc-secure-session-cookies.md)

</td><td>

-   New short description: Enforce Strict Security of Session Cookies
-   Old short description: Secure Session Cookies

</td></tr><tr><td>

[Do not use demo certificates for active saml configurations \[Updated in Security Center 1.5\]](../reference/sc-do-not-use-demo-certificates-active-saml-configurations-plugin.md)

</td><td>

-   New short description: Do Not Use Demo Certificates for Active SAML Configurations \(Plugin Applicability: Multiple Provider Single Sign-On\)
-   Old short description: Do Not Use Demo Certificates for Active SAML Configurations

</td></tr><tr><td>

[Disable Entity Expansion within the XMLDocument2 Streaming Parser \[Updated in Security Center 1.5\]](../reference/sc-disable-entity-expansion.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict allowed Java packages \[Updated in Security Center 1.3\]](../reference/sc-java-packages-allowlist.md)

</td><td>

-   New short description: Restrict Allowed Java Packages
-   Old short description: Java Packages Allowlist

</td></tr><tr><td>

[Require obfuscation of mobile app UI \[Updated in Security Center 1.3\]](../reference/sc-mobile-app-ui-obfuscation.md)

</td><td>

-   New short description: Require Obfuscation of Mobile App UI
-   Old short description: Mobile App UI Obfuscation

</td></tr><tr><td>

[Disable public access to favorites \[Updated in Security Center 1.3 and 2.0\]](../../security/reference/public-access-favorites.md)

</td><td>

-   New short description: Disable Public Access to Favorites
-   Old short description: Public Access to Favorites

</td></tr><tr><td>

[Escape JavaScript \[Updated in Security Center 1.3\]](../reference/sc-escape-javascript.md)

</td><td>

-   New description: The glide property **glide.html.escape\_script** helps sanitize HTML fields. If **glide.html.escape\_script**is not set to the recommended value of true, then inputs will not be sanitized for HTML fields \(output encoding\) from a backend Java context by removing embedded JavaScript. Javascript in HTML fields can lead to stored and reflected XSS. The ability to have XSS can lead to easily attained privilege escalation to higher roles such as admin where more lateral movement can be taken.
-   Old description: The glide property **glide.html.escape\_script** helps sanitize html fields. If **glide.html.escape\_script** is not set to the recommended value of true, then inputs will not be sanitized for HTML fields \(output encoding\) from a backend Java context by removing embedded JavaScript. Javascript in HTML fields can lead to stored and reflected XSS. The ability to have XSS can lead to easily attained privilege escalation to higher roles such as admin where more lateral movement can be taken.

</td></tr><tr><td>

[Set Xframe options to prevent embedding third-party websites \[Updated in Security Center 1.3\]](../reference/sc-xframe-options.md)

</td><td>

-   New short description: Set Xframe Options to Prevent Embedding Third-Party Websites
-   Old short description: Xframe Options
-   New description: If **com.glide.cs.embed.xframe\_options** is not set to the recommended value of DENY or SAMEORIGIN, then content of the web application could be embedded in a third-party site using an ALLOW-FROM uri. Allowing untrusted third-party sites could enable attacks such as clickjacking.
-   Old description: If **com.glide.cs.embed.xframe\_options** is not set to the recommended value of DENY or SAMEORIGIN, then content of a the web application could be embedded in a third-party site using an ALLOW-FROM uri. Allowing untrusted third-party sites could enable attacks such as clickjacking.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Escape HTML in list views \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-escape-html.md)

</td><td>

-   New short description: Escape HTML in List Views
-   Old short description: Escape HTML

</td></tr><tr><td>

[Require obfuscation of classic mobile app UI \[Updated in Security Center 1.3\]](../reference/sc-classic-mobile-app-ui-obfuscation.md)

</td><td>

-   New short description: Require Obfuscation of Classic Mobile App UI
-   Old short description: Classic Mobile App UI Obfuscation

</td></tr><tr><td>

[Deny by default with empty ACLs \[Updated in Security Center 1.3\]](../reference/sc-security-manager-default-deny.md)

</td><td>

-   New short description: Deny by Default with Empty ACLs
-   Old short description: Security Manager Default Deny
-   New description: If **glide.sm.default\_mode** is not set to the recommended value of deny, then the instance's legacy security manager allows access to a resource when there are no ACLs defined for that resource; or only wildcards table-level ACLs. By setting this to allow anything that does not have explicit ACLs set is susceptible to manipulation.
-   Old description: If **glide.sm.default\_mode** is not set to the recommended value of deny, then it allows access by the legacy security manager to a resource when there are no ACLs defined for that resource; or only wildcards table-level ACLs. By setting this to allow anything that does not have explicit ACLs set is susceptible to manipulation.

</td></tr><tr><td>

[Maximize reset password request retry window duration \[Updated in Security Center 1.3\]](../reference/sc-reset-password-request-retry-window.md)

</td><td>

-   New short description: Maximize Reset Password Request Retry Window Duration
-   Old short description: Reset Password Request Retry Window

</td></tr><tr><td>

[Require Authorization for XSD Requests \[Updated in Security Center 1.3\]](../reference/sc-xsd-request-authorization.md)

</td><td>

-   New short description: Require Authorization for XSD Requests
-   Old short description: XSD Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.xsd** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.xsd** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Escape jelly script \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-escape-jelly.md)

</td><td>

-   New short description: Escape Jelly Script
-   Old short description: Escape Jelly

</td></tr><tr><td>

[Double check inbound transactions \[Updated in Security Center 1.3\]](../reference/sc-double-check-inbound-transactions.md)

</td><td>

-   New remediation: Ensure the property **glide.security.strict.updates** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.security.strict.updates** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict downloadable files types in static content \[Updated in Security Center 1.3\]](../reference/sc-files-types-download-restrictions-from-static-content.md)

</td><td>

-   New short description: Restrict Downloadable Files Types in Static Content
-   Old short description: Files Types Download Restrictions from Static Content

</td></tr><tr><td>

[Require authorization for pdf requests \[Updated in Security Center 1.3\]](../reference/sc-require-authorization-for-pdf-requests.md)

</td><td>

-   New short description: Require Authorization for PDF Requests
-   Old short description: PDF Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.pdf** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.pdf** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict uploaded MIME types \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-upload-mime-type-restriction.md)

</td><td>

-   New short description: Restrict Uploaded MIME Types
-   Old short description: Upload MIME Type Restriction
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Disable legacy JQuery behavior \[Updated in Securty Center 1.3\]](../reference/sc-legacy-jquery-behavior.md)

</td><td>

-   New short description: Disable Legacy JQuery Behavior
-   Old short description: Legacy JQuery Behavior

</td></tr><tr><td>

[Maximize reset password request unlock window duration \[Updated in Security Center 1.3\]](../reference/sc-reset-password-request-unlock-window.md)

</td><td>

-   New short description: Maximize Reset Password Request Unlock Window Duration
-   Old short description: Reset Password Request Unlock Window

</td></tr><tr><td>

[Disable MultiSSO Debugging \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-disable-multisso-debugging.md)

</td><td>

-   New short description: Disable MultiSSO Debugging \(Plugin Applicability: Multiple Provider Single Sign-On\)
-   Old short description: Disable MultiSSO Debugging
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enforce production instance behavior \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-production-instance-behavior.md)

</td><td>

-   New short description: Enforce Production Instance Behavior
-   Old short description: Production Instance Behavior

</td></tr><tr><td>

[Limit Invalid Password Reset Attempts \[Updated in Security Center 1.3 and updated in 2.0\]](../reference/sc-reset-password-request-max-attempts.md)

</td><td>

-   New short description: Minimize Reset Password Request Max Attempt Allowance
-   Old short description: Reset Password Request Max Attempts

</td></tr><tr><td>

[Require authorization for csv requests \[Updated in Security Center 1.3\]](../reference/sc-require-authorization-for-csv-requests.md)

</td><td>

-   New short description: Require Authorization for CSV Requests
-   Old short description: CSV Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.csv** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.csv** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Minimize reset password request success window duration \[Updated in Securty Center 1.3\]](../reference/sc-reset-password-request-success-window.md)

</td><td>

-   New short description: Minimize Reset Password Request Success Window Duration
-   Old short description: Reset Password Request Success Window

</td></tr><tr><td>

[Enforce SOAP request strict security \[Updated in Security Center 1.3\]](../reference/sc-soap-request-strict-security.md)

</td><td>

-   New short description: Enforce SOAP Request Strict Security
-   Old short description: SOAP Request Strict Security

</td></tr><tr><td>

[Require authorization for SOAP requests \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-soap-request-authorization.md)

</td><td>

-   New short description: Require Authorization for SOAP Requests
-   Old short description: SOAP Request Authorization
-   New description: The glide property **glide.basicauth.required.soap** controls whether authentication is required to make a SOAP request to an instance. If **glide.basicauth.required.soap** is not set to the recommended value of true, then authentication is disable for SOAP requests on the instance. It allows unauthenticated access to administrator or maint level operations; thereby negating security controls within the instance.
-   Old description: The glide property **glide.basicauth.required.soap** controls whether authentication is required i order to make a SOAP request to an instance. If glide.basicauth.required.soap is not set to the recommended value of true, then authentication is disable for SOAP requests on the instance. It allows unauthenticated access to administrator or maint level operations; thereby negating all security controls within the instance.
-   New remediation: Ensure the property **glide.basicauth.required.soap** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.soap** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Require XMLdoc2 entity validation with allowlistDisable entity expansion \[Updated in Security Center 1.3\]](../reference/sc-xmldoc2-entity-validation-with-entity-expansion.md)

</td><td>

-   New short description: Require XMLdoc2 entity validation with allowlistDisable Entity Expansion
-   Old short description: XMLdoc2 entity validation with allowlistDisable Entity Expansion

</td></tr><tr><td>

[Apply domain separation on dot walked fields \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-apply-domain-separation.md)

</td><td>

-   New short description: Apply Domain Separation on Dot Walked Fields \(Plugin Applicability: Domain Separation
-   Old short description: Apply Domain Separation
-   New description: This property controls whether join queries are given domain separated conditions or not, in order to ensure they apply domain separation functionality for dot walked fields. If **glide.sys.domain.include\_domain\_condition\_on\_join** is not set to the recommended value of true on an instance using domain separation, then sensitive information could be disclosed that is not to be shared with a specific domain.
-   Old description: This property controls whether join queries are given domain separated conditions or not, in order to ensure they apply domain separation functionality for dot walked fields. If **glide.sys.domain.include\_domain\_condition\_on\_join** is not set to the recommended value of true, then sensitive information could be disclosed that is not to be shared with a specific domain.
-   New remediation: Ensure the property **glide.sys.domain.include\_domain\_condition\_on\_join** is set to true when the Domain Separation plugin is active.
-   Old remediation: Ensure the property **glide.sys.domain.include\_domain\_condition\_on\_join** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict JSONP requests to trusted URLs \[Updated in Security Center 1.3\]](../reference/sc-jsonp-request-inclusion-list.md)

</td><td>

-   New short description: Restrict JSONP Requests to Trusted URLs
-   Old short description: JSONP Request Inclusion List
-   New description: This property specifies trusted URLs for the angularJS $http service to allow/reject JSONP requests. Property is necessary because this is a potentially breaking change for customers, so they need a way to add their trusted URLs. If **angular.jsonp.inclusion\_list.enabled** is not set to the recommended value of "true", then JSONP requests are allowed to any URL.
-   Old description: This property specifies trusted URLs for the angularJS $http service to allow/reject JSONP requests. Property is necessary because this is a potentially breaking change for customers, so they need a way to add their trusted URLs. If **angular.jsonp.inclusion\_list.enabled**\) is not set to the recommended value of true, then jsonp requests are allowed to any url.

</td></tr><tr><td>

[Minimize reset password max SMS per day \[Updated in Security Center 1.3\]](../reference/sc-reset-password-max-sms-per-day.md)

</td><td>

-   New short description: Minimize Reset Password Max SMS Per Day
-   Old short description: Reset Password Max SMS Per Day

</td></tr><tr><td>

[Maximize reset password verification delay duration \[Updated in Security Center 1.3\]](../reference/sc-reset-password-verification-delay.md)

</td><td>

-   New short description: Maximize Reset Password Verification Delay Duration
-   Old short description: Reset Password Verification Delay
-   New description: If **password\_reset.verification.delay** is not set to the recommended value of 1000 or more, then it will lead the login more susceptable to brute force attacks. This number of milliseconds delay limits the ability of a malicious actor to attempt to guess users identification or verification details, by using automation tools \("bots"\).
-   Old description: If **password\_reset.verification.delay** is not set to the recommended value of 1000 or more, then it will lead the login more susceptable to brute force attacks. This number of milliseconds delay limits the ability of a hacker to attempt to guess users identification or verification details, by using automation tools \("bots"\).

</td></tr><tr><td>

[Require authorization for data broker rest API \[Updated in Security Center 1.3\]](../reference/sc-data-broker-rest-api-authorization.md)

</td><td>

-   New short description: Require Authorization for Data Broker Rest API
-   Old short description: Data Broker Rest API Authorization
-   New description: If **glide.basicauth.required.databrokerrestapiprocessor** is not set to the recommended value of true, then basic authorization is not required for all inbound Data Broker Rest API requests. This could lead to unauthenticated information disclosure from the instance.
-   Old description: Starting in Utah release, if **glide.basicauth.required.databrokerrestapiprocessor** is not set to the recommended value of "true", then basic authorization is not required for all inbound Data Broker Rest API requests. This could lead to unauthenticated information disclosure from the instance.
-   New remediation: Ensure the property **glide.basicauth.required.databrokerrestapiprocessor** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.databrokerrestapiprocessor** is set to true on instances running Utah release and later.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Require authorization for JSONv2 request \[Updated in Security Center 1.3\]](../reference/sc-jsonv2-request-authorization.md)

</td><td>

-   New short description: Require Authorization for JSONv2 Request
-   Old short description: JSONv2 Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.jsonv2** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.jsonv2** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Disable JavaScript tags in embedded HTML \[Updated in Security Center 1.3\]](../reference/sc-allow-javascript-tags-in-embedded-html.md)

</td><td>

-   New short description: Disable JavaScript Tags in Embedded HTML
-   Old short description: Allow Javascript tags in Embedded HTML
-   New remediation: Ensure the property **glide.ui.security.codetag.allow\_script** exists in the sys\_properties table and is set to false.
-   Old remediation: Ensure the property **glide.ui.security.codetag.allow\_script** is set to false.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable security jump start plugin \(ACL Rules\) \[Updated in Security Center 1.3\]](../reference/sc-security-jump-start-plugin-acl-rules.md)

</td><td>

-   New short description: Enable Security Jump Start Plugin \(ACL Rules\)
-   Old short description: Security Jump Start Plugin \(ACL Rules\)

</td></tr><tr><td>

[Set guest user for soap requests \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-set-guest-user-for-soap-requests.md)

</td><td>

-   New short description: Set Guest User for SOAP Requests
-   Old short description: Guest User for SOAP Requests

</td></tr><tr><td>

[Enable script sandbox \[Updated in Security Center 1.3\]](../reference/sc-client-generated-scripts-sandbox.md)

</td><td>

-   New short description: Enforce Client Generated Scripts Sandbox
-   Old short description: Client Generated Scripts Sandbox

</td></tr><tr><td>

[Restrict XML external entities \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-xml-entity-validation-url-allowlist.md)

</td><td>

-   New short description: Restrict XML External Entities
-   Old short description: XML Entity Validation URL Allowlist

</td></tr><tr><td>

[Enable ACLs to Control Live Profile Details \[Updated in Security Center 1.3\]](../reference/sc-enable-acls-to-control-live-profile-details.md)

</td><td>

-   New short description: Enable ACLs to Control Live Profile Details
-   Old short description: Enable ACLs to control Live Profile Details

</td></tr><tr><td>

[Restrict access to custom journal entries \[Updated in Security Center 1.3 and removed in 2.0\]](../reference/sc-secure-custom-journal-entries.md)

</td><td>

-   New short description: Restrict Access to Custom Journal Entries
-   Old short description: Secure Custom Journal Entries
-   New description: If **glide.live\_feed.custom\_journal.acl\_check\_enabled** is not set to the recommended value of true, then all users to be able to see all journal entries within the life feed feature. Setting property to true will respect ACL's on custom journal fields which is a good to have feature.
-   Old description: If **glide.live\_feed.custom\_journal.acl\_check\_enabled** is not set to the recommended value of true, then all users to be able to see all journal entries. Setting property to true will respect ACL's on custom journal fields which is a good to have feature.

</td></tr><tr><td>

[Set OTP lifetime for password reset to 1 hour \[Updated in Security Center 2.0\]](../reference/sc-set-otp-lifetime-for-password-reset-to-12-hours-or-less.md)

</td><td>

-   New description: This property **glide.pwd\_reset.onetime.token.validity** allows the link in the password reset email to expire after the number of hours specified in that **glide.pwd\_reset.onetime.token.validity property**. Validity time of password reset token should be keeped as short as possible in according of normal user experience. Have long validity time for password reset token can help malicious actors to perform account takeover.
-   Old description: This property **glide.pwd\_reset.onetime.token.validity** allows the link in the password reset email to expire after the number of hours specified in that **glide.pwd\_reset.onetime.token.validity** property. Validity time of password reset token should be keeped as short as possible in according of normal user experience. Have long validity time for password reset token can help hackers to perform account takeover.

</td></tr><tr><td>

[Restrict delegated developers read access \[Updated in Security Center 1.3\]](../reference/sc-delegated-developers-read-access-allowlist.md)

</td><td>

-   New short description: Restrict Delegated Developers Read Access
-   Old short description: Delegated Developers Read Access Allowlist

</td></tr><tr><td>

[Define allowed ServiceNow internal IP addresses \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-ip-addresses-access-allowlist.md)

</td><td>

-   New short description: Define Allowed ServiceNow Internal IP Addresses
-   Old short description: IP Addresses Access Allowlist

</td></tr><tr><td>

[Validate SOAP content type \[Updated in Security Center 1.3\]](../reference/sc-soap-content-type-checking.md)

</td><td>

-   New short description: Validate SOAP Content Type
-   Old short description: SOAP Content Type Checking
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Require authorization for excel requests \[Updated in Security Center 1.3\]](../reference/sc-excel-request-authorization.md)

</td><td>

-   New short description: Require Authorization for Excel Requests
-   Old short description: Excel Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.excel** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.excel** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Require authorization for API requests \[Updated in Security Center 1.3\]](../reference/sc-api-request-authorization.md)

</td><td>

-   New short description: Require Authorization for API Requests
-   Old short description: API Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.api** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.api** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Minimize Entity Expansion Threshold for GlideXMLUtil Scriptable \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-setting-entity-expansion-threshold.md)

</td><td>

-   New short description: Minimize Entity Expansion Threshold
-   Old short description: Setting Entity Expansion Threshold

</td></tr><tr><td>

[Notify users during password reset/change process \[Removed in Security Center 1.5\]](../reference/sc-password-reset-change-notification-process.md)

</td><td>

-   New short description: Notify Users During Password Reset/Change Process
-   Old short description: Password Reset/Change Notification Process
-   New remediation: Ensure Password Reset process notifies users upon password change or reset.
-   Old remediation: Ensure Password reset process notifies users upon password change or reset.

</td></tr><tr><td>

[Disable legacy AngularJS behavior \[Removed in Security Center 2.2\]](../reference/sc-legacy-angularjs-behavior.md)

</td><td>

-   New short description: Disable Legacy AngularJS Behavior
-   Old short description: Legacy AngularJS Behavior

</td></tr><tr><td>

[Maximize failed login unlock timeout duration \[Updated in Security Center 1.3\]](../reference/sc-managing-unlock-timeout-after-failed-logins.md)

</td><td>

-   New short description: Maximize Failed Login Unlock Timeout Duration
-   Old short description: Managing Unlock Timeout after Failed Logins

</td></tr><tr><td>

[Enable HTTP Only Cookie Flag \[Updated in Security Center 1.3\]](../reference/sc-http-only-cookie-flag.md)

</td><td>

-   New short description: Enable HTTP Only Cookie Flag
-   Old short description: HTTP Only Cookie Flag
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable scoped admin application ACLs \[Updated in Security Center 1.3\]](../reference/sc-administer-scoped-admin-application-acls.md)

</td><td>

-   New short description: Enable Scoped Admin Application ACLs
-   Old short description: Administer Scoped Admin Application ACLs
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable UserCookie version 3.1 \[Updated in Security Center 2.0\]](../reference/sc-enable-usercookie-version-3-1.md)

</td><td>

-   New description: UserCookie v3 is generated only when property **glide.ui.secure.cookies.use\_kmf** is disabled. UserCookie v3 is not secure due to storing secret key for HMAC in source code and identical for all customers. That can support malicious actors to use this one secret key for attempts to hijacking user sessions.
-   Old description: UserCookie v3 is generated only when property glide.ui.secure.cookies.use\_kmf is disabled. UserCookie v3 is not secure due to storing secret key for HMAC in source code and identical for all customers. That can support hackers to use this one secret key for attempts to hijacking user sessions.

</td></tr><tr><td>

[Require authorization for XML requests \[Updated in Security Center 1.3\]](../reference/sc-xml-request-authorization.md)

</td><td>

-   New short description: Require Authorization for XML Requests
-   Old short description: XML Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.xml** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.xml** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Minimize external user registration link expiration duration \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-external-user-registration-link-expiration.md)

</td><td>

-   New short description: Minimize External User Registration Link Expiration Duration
-   Old short description: External User Registration Link Expiration

</td></tr><tr><td>



</td><td>

-   New short description: Convert Inbound Email Images to Attachments
-   Old short description: Convert Inbound Email HTML

</td></tr><tr><td>

[Minimize SMTP Recipient Quantity \[Updated in Security Center 1.3\]](../reference/sc-max-smtp-recipients.md)

</td><td>

-   New short description: Minimize SMTP Recipient Quantity
-   Old short description: Max SMTP Recipients

</td></tr><tr><td>

[Enable updated version of MultiSSO plugin \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-updated-version-of-multi-sso-plugin-is-enabled.md)

</td><td>

-   New short description: Enable Updated Version of Multi SSO Plugin \(Plugin Applicability: Multiple Provider Single Sign-On\)
-   Old short description: Updated Version of Multi SSO Plugin is Enabled
-   New CVSS Score: 7.1
-   Old CVSS Score: 5

</td></tr><tr><td>

[Disable raw database query execution \[Updated in Security Center 1.3 and removed in 2.0\]](../reference/sc-operation-level-access-control-requirements.md)

</td><td>

-   New short description: Disable Raw Database Query Execution
-   Old short description: Operation Level Access Control Requirements
-   New description: This property allows a user to perform raw SQL queries on the database which can give access to tables and data outside of GlideRecord restrictions. If **glide.db.allow\_unsafe\_dbi\_execute\_sql** is not set to the recommended value of false, then this allows calling dbi.executeStatement\(\) from a Glide Scriptable.
-   Old description: This property allows a user to perform raw SQL queries on the database which can give access to tables and data out of GlideRecord restrictions. If **glide.db.allow\_unsafe\_dbi\_execute\_sql** is not set to the recommended value of false, then this allows calling dbi.executeStatement\(\) from a Glide Scriptable.

</td></tr><tr><td>

[Escape XML markup \[Updated in Security Center 1.3\]](../reference/sc-escape-xml.md)

</td><td>

-   New short description: Escape XML Markup
-   Old short description: Escape XML
-   New remediation: Ensure the property **glide.ui.escape\_text** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.ui.escape\_text** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Require authorization for RSS requests \[Updated in Security Center 1.3\]](../reference/sc-rss-request-authorization.md)

</td><td>

-   New short description: Require Authorization for RSS Requests
-   Old short description: RSS Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.rss** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.rss** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Maximum allowed attachment size \[Updated in Security Center 1.3\]](../reference/sc-max-allowed-attachment-size.md)

</td><td>

-   New short description: Minimize Allowed Attachment Size
-   Old short description: Max Allowed Attachment Size

</td></tr><tr><td>

[Enforce relative links \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-enforce-relative-links.md)

</td><td>

-   New description: The **glide.cms.catalog\_uri\_relative** property enforces relative links from the URI parameter on /ess/catalog.do. If **glide.cms.catalog\_uri\_relative** is not set to the recommended value of true, then the URL will not be sanitized with the enforceRelativeURL\(url\) function. Absolute URLs can pose a security risk when used as a part of parameter or a field value, thus redirecting the source page to an adversary-controlled website.
-   Old description: Use the **glide.cms.catalog\_uri\_relative** property to enforce relative links from the URI parameter on /ess/catalog.do. If **glide.cms.catalog\_uri\_relative** is not set to the recommended value of true, then it may not sanitize URL with the enforceRelativeURL\(url\) function.

</td></tr><tr><td>

[Enable SMS code notification for enrollment and verification \[Updated in Security Center 1.3\]](../reference/sc-sms-code-notification-for-enrollment-and-verification.md)

</td><td>

-   New short description: Enable SMS Code Notification for Enrollment and Verification
-   Old short description: SMS Code Notification for Enrollment and Verification

</td></tr><tr><td>

[Cache-Control HTTP Header Value \[Updated in Security Center 1.3 and removed in 1.5\]](../reference/sc-cache-control-http-header-value.md)

</td><td>

-   New short description: Cache-Control HTTP Header Value
-   Old short description: Cache-Control HTTP header value
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Deny internal access to explicit external roles \[Updated in Security Center 1.3 and 1.5\]](../../security/reference/sc-enable-explicit-roles-internal-denylist.md)

</td><td>

-   New short description: Deny Internal Access to Explicit External Roles
-   Old short description: Enable Explicit Roles Internal Denylist
-   New technical configuration name: glide.security.explicit\_roles.enable\_internal\_user\_blacklist,glide.security.explicit\_roles.internal\_user\_blacklist
-   Old technical configuration name: glide.security.explicit\_roles.enable\_internal\_user\_blacklist
-   New description: This prevents external users from being assigned the snc\_internal role. If **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** is not set to the recommended value of true, and the **glide.security.explicit\_roles.internal\_user\_blacklist** property is not set to a list of untrusted user classes, then the specified roles can be assigned the snc\_internal role instead of the snc\_external role. If the list is empty, then all users will be assigned the snc\_internal role by default. The property should contain at least the default roles csm\_consumer\_user,customer\_contact. Misconfiguration of these properties increases the risk that an external user account gains access to internal information.
-   Old description: This property prevents external users from being assigned the snc\_internal role. If **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** is set to the recommended value of true, then it enables **glide.security.explicit\_roles.internal\_user\_blacklist property** which allows to assign snc\_external role. If the value is set to false, it disables **glide.security.explicit\_roles.internal\_user\_blacklist** property.
-   New remediation: Ensure the property **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** is set to true and that the property **glide.security.explicit\_roles.internal\_user\_blacklist** includes the dangerous items csm\_consumer\_user, customer\_contact.
-   Old remediation: Ensure the property **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Minimize one-time out of band verifier lifetime duration \[Updated in Security Center 1.3\]](../reference/sc-short-one-time-out-of-band-verifier-lifetime.md)

</td><td>

-   New short description: Minimize One-Time Out of Band Verifier Lifetime Duration
-   Old short description: Short One-Time Out of Band Verifier Lifetime

</td></tr><tr><td>

[Require authorization for script requests \[Updated in Security Center 1.3\]](../reference/sc-script-request-authorization.md)

</td><td>

-   New short description: Require Authorization for Script Requests
-   Old short description: Script Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.scriptedprocessor** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.scriptedprocessor** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Limit concurrent interactive sessions \[Updated in Security Center 1.3\]](../reference/sc-glide-authenticate-limit-concurrent-interactive-sessions.md)

</td><td>

-   New short description: Limit Concurrent Interactive Sessions
-   Old short description: Glide Authenticate Limit Concurrent Interactive Sessions
-   New description: This property is meant to be used with the Limit Concurrent Sessions \(**com.glide.limit.concurrent.sessions**\) plugin. When the plugin is active and the property is set to false, a user can have any number of concurrent interactive sessions on an instance. A greater number of open sessions means there is a great possibility for session hijacking to occur.
-   Old description: This propert is meant to be used with the Limit Concurrent Sessions \(**com.glide.limit.concurrent.sessions**\) plugin. When the plugin is active and the property is set to false, a user can have any number of concurrent interactive sessions on an instance. A greater number of open sessions means there is a great possibility for session hijacking to occur.

</td></tr><tr><td>

[Prevent Users From Accepting Warning To Bypass CSRF Validation \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-csrf-strict-validation.md)

</td><td>

-   New short description: Enforce CSRF Token Strict Validation
-   Old short description: CSRF Strict Validation
-   New description: This property enables CSRF token strict validation which prevents the reuse of CSRF tokens. If **glide.security.csrf.strict.validation.mode** is not set to the recommended value of true, then CSRF tokens could be reused which opens a door to CSRF attacks.
-   Old description: This property enables CSRF token strict validation which prevents the reuse of CSRF tokens. If **glide.security.csrf.strict.validation.mode** is not set to the recommended value of true, then CSRF token could be reused which opens a door tot CSRF attacks.

</td></tr><tr><td>

[Minimize session activity timeout duration \[Updated in Security Center 1.3\]](../reference/sc-session-activity-timeout.md)

</td><td>

-   New short description: Minimize Session Activity Timeout Duration
-   Old short description: Session Activity Timeout

</td></tr><tr><td>

[Enable HTML Sanitizer \[Updated in Security Center 1.3\]](../reference/sc-html-sanitizer.md)

</td><td>

-   New short description: Enable HTML Sanitizer
-   Old short description: HTML Sanitizer

</td></tr><tr><td>

[Restrict access to background script \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-restrict-access-to-background-script.md)

</td><td>

-   New description: This property holds the required role to access Script Background module. If **glide.script\_processor.admin** is not set to the recommended value of admin, security\_admin, or maint, then users having a lower privileged role will be able to run background scripts on the instance. This will lead to a complete bypass of the ACL system allowing full access to tables.
-   Old description: This property holds the required role to access Script Background module. If **glide.script\_processor.admin** is not set to the recommended value of Admin, then any user having a low privileged role will be able to run background scripts on the instance. This will lead to a complete bypass of the ACL system allowing full access to tables
-   New remediation: Ensure the property **glide.script\_processor.admin** is set to the admin, security\_admin, or maint role.
-   Old remediation: Ensure the property **glide.script\_processor.admin** is set to Admin.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Disable embedded HTML code \[Updated in Security Center 1.3\]](../reference/sc-allow-embedded-html-code.md)

</td><td>

-   New short description: Disable Embedded HTML Code
-   Old short description: Embedded HTML Code

</td></tr><tr><td>

[Minimize absolute session timeout duration \[Updated in Security Center 1.3\]](../reference/sc-absolute-session-timeout.md)

</td><td>

-   New short description: Minimize Absolute Session Timeout Duration
-   Old short description: Absolute Session Timeout

</td></tr><tr><td>

[Require authentication by default for client-callable script includes \[Updated in Security Center 1.3\]](../reference/sc-privacy-on-client-callable-script-includes.md)

</td><td>

-   New short description: Require Authentication by Default for Client-Callable Script Includes
-   Old short description: Privacy on Client-Callable Script Includes

</td></tr><tr><td>

[Restrict access to GlideSystemUserSession scriptable API \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-access-glidesystemusersession-scriptable-api.md)

</td><td>

-   New short description: Restrict Access to GlideSystemUserSession Scriptable API
-   Old short description: Access to GlideSystemUserSession scriptable API

</td></tr><tr><td>

[Enforce HTML Sanitization \[Updated in Security Center 1.3\]](../reference/sc-check-unsanitized-html.md)

</td><td>

-   New short description: Enforce HTML Sanitization
-   Old short description: Check Unsanitized HTML
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Minimize absolute session timeout duration \[Updated in Security Center 1.3\]](../reference/sc-absolute-session-timeout.md)

</td><td>

-   New short description: Minimize Absolute Session Timeout Duration
-   Old short description: Absolute Session Timeout

</td></tr><tr><td>

[Activate role based multi-factor authentication \[Updated in Security Center 1.3\]](../reference/sc-role-based-multi-factor-authentication.md)

</td><td>

-   New short description: Activate Role Based Multi-Factor Authentication
-   Old short description: Role Based Multi-Factor Authentication

</td></tr><tr><td>

[Minimize SAML notBefore or notOnOrAfter constraint duration \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-saml-notbefore-or-notonorafter-constraint.md)

</td><td>

-   New short description: Minimize SAML "notBefore" or "notOnOrAfter" Constraint Duration \(Plugin Applicability: Multiple Provider Single Sign-On\)
-   Old short description: SAML "notBefore" or "notOnOrAfter" Constraint
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict email domains for external user registration \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-external-user-registration-email-domain-allowlist.md)

</td><td>

-   New short description: Restrict Email Domains for External User Registration \(Plugin Applicability: External User Registration\)
-   Old short description: External User Registraiton Email Domain Allowlist
-   New remediation: Ensure the property **sn\_ext\_usr\_reg.allowed\_email\_domains** is not set to an empty value.
-   Old remediation: Ensure the property **sn\_ext\_usr\_reg.allowed\_email\_domains** is not set to an empty value.

</td></tr><tr><td>

[Maximize reset password SMS pause window duration \[Updated in Security Center 1.3\]](../reference/sc-reset-password-sms-pause-window.md)

</td><td>

-   New short description: Maximize Reset Password SMS Pause Window Duration
-   Old short description: Reset Password SMS Pause Window
-   New remediation: Ensure the property **password\_reset.sms.pause\_window** is set to 2 or greater.
-   Old remediation: Ensure the property **password\_reset.sms.pause\_window** is set to 2.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Disable outbound SSLv2/SSLv3 connections \[Updated in Security Center 1.3\]](../reference/sc-disabling-sslv2-sslv3.md)

</td><td>

-   New short description: Disable Outbound SSLv2/SSLv3 Connections
-   Old short description: Disabling SSLv2/SSLv3

</td></tr><tr><td>

[Require authorization for unload requests \[Updated in Security Center 1.3\]](../reference/sc-require-authorization-for-unload-requests.md)

</td><td>

-   New short description: Require Authorization for Unload Requests
-   Old short description: Unload Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.unl** exists in the sys\_properties\_table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.unl** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable email spam scoring and filtering \[Updated in Security Center 1.3\]](../reference/sc-email-spam-scoring-and-filtering.md)

</td><td>

-   New short description: Enable Email Spam Scoring and Filtering
-   Old short description: Email Spam Scoring and Filtering

</td></tr><tr><td>

[Unset LDAP Initial distinguished name \[Updated in Security Center 1.3 and removed in 2.0\]](../reference/sc-ldap-initial-distinguished-name.md)

</td><td>

-   New short description: Unset LDAP Initial Distinguished Name
-   Old short description: LDAP Initial Distinguished Name

</td></tr><tr><td>

[Enable Anti-CSRF token \[New in Security Center 1.3, updated in 1.5, and removed in 2.0\]](../reference/sc-anti-csrf-token.md)

</td><td>

-   New short description: Enable Anti-CSRF Token
-   Old short description: Anti-CSRF Token

</td></tr><tr><td>

[Require AJAXGlideRecord ACL checking \[Updated in Security Center 1.3\]](../reference/sc-enabling-ajaxgliderecord-acl-checking.md)

</td><td>

-   New short description: Require AJAXGlideRecord ACL Checking
-   Old short description: Enabling AJAXGlideRecord ACL Checking

</td></tr><tr><td>

[Log user impersonation \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-log-user-impersonation.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Disallow infected file download \[Updated in Security Center 1.5 and 2.0\]](../reference/sc-disallow-infected-files-download.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable Captcha for External User Registration \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-enable-captcha-external-user-registration.md)

</td><td>

-   New short description: Enable Captcha for External User Registration \(Plugin Applicability: External User Registration\)
-   Old short description: Enable Captcha for External User Registration

</td></tr><tr><td>

[Disable SQL Error Messages \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-disabling-sql-error-messages.md)

</td><td>

-   New short description: Disable SQL Error Messages
-   Old short description: Disabling SQL error messages

</td></tr><tr><td>

[Minimize reset password request expiration duration \[Updated in Security Center 1.3\]](../reference/sc-reset-password-request-expiration.md)

</td><td>

-   New short description: Minimize Reset Password Request Expiration Duration
-   Old short description: Reset Password Request Expiration
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Control Lockout Time for Invalid Password Reset Attempts \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-reset-password-request-max-attempts-window.md)

</td><td>

-   New short description: Minimize Reset Password Request Max Attempts Window Duration
-   Old short description: Reset Password Request Max Attempts Window

</td></tr><tr><td>

[Restrict downloadable MIME types \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-downloadable-mime-type-denylist.md)

</td><td>

-   New short description: Restrict Downloadable MIME Types
-   Old short description: Downloadable Mime Type Denylist

</td></tr><tr><td>

[Escape Excel Formulas \[Updated in Security Center 1.3\]](../reference/sc-escape-excel-formula.md)

</td><td>

-   New short description: Escape Excel Formulas
-   Old short description: Escape Excel Formula

</td></tr><tr><td>

[Enable contextual security plugin \[Updated in Security Center 1.3\]](../reference/sc-contextual-security-plugin.md)

</td><td>

-   New short description: Enable Contextual Security Plugin
-   Old short description: Contextual Security Plugin

</td></tr><tr><td>

[Enable account recovery \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-account-recovery.md)

</td><td>

-   New short description: Enable Account Recovery \(Plugin Applicability: Multiple Provider Single Sign-On\)
-   Old short description: Account Recovery
-   New description: This property controls the account recovery feature which binds the ability to bypass single sign-on to specifically designated administrators. If**glide.sso.acr.enabled** is not set to the recommended value of true, then the local interactive log-ins \(username or password based\) will be remain enabled when single sign-on is enabled on the instance. Eliminating local interactive log-ins reduces the potential for unauthorized access to the instance.
-   Old description: This property controls the account recovery feature. If **glide.sso.acr.enabled** is not set to the recommended value of true, then Account recovery by userId will not be possible.
-   New CVSS Score: 6.5
-   Old CVSS Score: 9.1
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Require authorization for import requests \[Updated in Security Center 1.3\]](../reference/sc-import-request-authorization.md)

</td><td>

-   New short description: Require Authorization for Import Requests
-   Old short description: Import Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.importprocessor** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.importprocessor** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable SNC access control plugin \[Updated in Security Center 1.3\]](../reference/sc-snc-access-control-plugin.md)

</td><td>

-   New short description: Enable SNC Access Control Plugin
-   Old short description: SNC Access Control Plugin

</td></tr><tr><td>

[Limit concurrent sessions across all nodes \[Updated in Security Center 1.3\]](../reference/sc-limit-concurrent-sessions-across-all-nodes.md)

</td><td>

-   New short description: Limit Concurrent Sessions Across All Nodes
-   Old short description: Glide Authenticate Limit Concurrent Sessions Across All Nodes

</td></tr><tr><td>

[Require authorization for XML output requests \[Updated in Security Center 1.3\]](../reference/sc-xml-output-authorization.md)

</td><td>

-   New short description: Require Authorization for XML Output Requests
-   Old short description: XML Output Authorization
-   New remediation: Ensure the property **glide.basicauth.required.xmloutputprocessor** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.xmloutputprocessor** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Escape scripts in scratchpad \[Updated in Security Center 1.3\]](../reference/sc-escape-scratchpad.md)

</td><td>

-   New short description: Escape Scripts in Scratchpad
-   Old short description: Escape Scratchpad
-   New description: The scratchpad is an easy way to set information on the server that can be accessed in the browser. An admin can script anything to be on it, including arbitrary data from arbitrary records. If **glide.ui.escape\_scratchpad** is not set to the recommended value of true, then it is possible to execute malicious script like a cross-site scripting vulnerability.
-   Old description: The scratchpad is an easy way to set information on the server that can be accessed in the browser. An admin can script anything to be on it, including arbitrary data from arbitrary records.If **glide.ui.escape\_scratchpad** is not set to the recommended value of true, then it is possible to execute malicious script like a cross-site scripting vulnerability.

</td></tr><tr><td>

[Require authorization for WSDL request \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-wsdl-request-authorization.md)

</td><td>

-   New short description: Require Authorization for WSDL Request
-   Old short description: WSDL Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.wsdl** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.wsdl** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Require authorization for SCHEMA requests \[Updated in Security Center 1.3\]](../reference/sc-schema-request-authorization.md)

</td><td>

-   New short description: Require Authorization for SCHEMA Requests
-   Old short description: SCHEMA Request Authorization
-   New remediation: Ensure the property **glide.basicauth.required.schema** exists in the sys\_properties table and is set to true.
-   Old remediation: Ensure the property **glide.basicauth.required.schema** is set to true.
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict downloadable MIME types \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-downloadable-mime-type-denylist.md)

</td><td>

-   New short description: Restrict Downloadable MIME Types
-   Old short description: Downloadable Mime Types

</td></tr><tr><td>

[Disable logger for low privilege users in script sandbox \[Updated in Security Center 1.3\]](../reference/sc-glide-security-logger-no-loggining-for-sandbox.md)

</td><td>

-   New short description: Disable Logger for Low Privilege Users in Script Sandbox
-   Old short description: Glide Security Logger No Loggining for Sandbox
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Implement the x-frame-options: SAMEORIGIN security header \[Updated in Security Center 1.3\]](../reference/sc-x-frame-options-sameorigin.md)

</td><td>

-   New short description: Implement the X-Frame-Options: SAMEORIGIN Security Header
-   Old short description: X-Frame-Options: SAMEORIGIN
-   Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Restrict performance monitoring access \[Updated in Security Center 1.3\]](../reference/sc-performance-monitoring-acl.md)

</td><td>

-   New short description: Restrict Performance Monitoring Access
-   Old short description: Performance Monitoring ACL

</td></tr><tr><td>

[Turn off verbose SQL error messages for import processor \[Updated in Security Center 1.3\]](../reference/sc-turn-off-verbose-sql-error-messages-for-import-processor.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Minimize reset password SMS expiracy duration \[Updated in Security Center 1.3\]](../reference/sc-reset-password-sms-expiracy.md)

</td><td>

-   New short description: Minimize Reset Password SMS Expiracy Duration
-   Old short description: Reset Password SMS Expiracy

</td></tr><tr><td>

[Disable creating users from incoming emails \[Updated in Securty Center 1.3\]](../reference/sc-restrict-emails-by-domain.md)

</td><td>

-   New short description: Disable Creating Users from Incoming Emails
-   Old short description: Restrict Emails by Domain
-   New description: An administrator can set an email property to automatically create users from incoming emails. If set this property to the insecure value, the instance will automatically create users from incoming email. Each user created will have the same hardcoded default password which makes bypassing authentication through brute force easier.
-   Old description: An administrator can set an email property to automatically create users from incoming emails. If set this property to the insecure value, the instance will automatically create users from incoming email. Each user created will have the same hardcoded default password which makes bypassing authentication through brute force easier.
-   New remediation: Ensure the property **glide.pop3readerjob.create\_caller** is set to false.
-   Old remediation: Ensure the property **glide.pop3readerjob.create\_caller** is set to false

</td></tr></tbody>
</table>**Parent Topic:**[Updated hardening settings](hardening-settings-updated.md)

