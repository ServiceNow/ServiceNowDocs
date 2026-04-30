---
title: Updated hardening settings for baseline version 6.0
description: Some hardening settings have been updated with the release of Security Center baseline version 6.0.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 23
breadcrumb: [Updated hardening settings, Baseline versions, Hardening settings, Platform Security]
---

# Updated hardening settings for baseline version 6.0

Some hardening settings have been updated with the release of Security Center baseline version 6.0.

<table id="table_oz1_qwv_bfc"><thead><tr><th>

Documentation

</th><th>

Updates

</th></tr></thead><tbody><tr><td>

[Prevent Unauthenticated Access to Virtual Agent Embedded Web Client](../reference/sc-publicly-exposed-virtual-agent-embedded-web-client.md)

</td><td>

-   New Short Description: Prevent Unauthenticated Access to Virtual Agent Embedded Web Client
-   Old Short Description:Publicly Exposed Virtual Agent Embedded Web Client sn\_va\_web\_client\_app\_embed

</td></tr><tr><td>

[Prevent Empty ACL Creation \[New in Security Center 2.0\]](../reference/sc-prevent-empty-acl-creation.md)

</td><td>

Rule: Script: Script has been updated to improve detection accuracy.

</td></tr><tr><td>

[Enable ACLs for Encoded Query in Simple List Widget \[New in Security Center 2.0\]](../reference/sc-enable-acls-for-encoded-query-in-simple-list-widget.md)

</td><td>

-   CVSS Score \(New\): 4.3
-   CVSS Score \(Old\): 5.3

</td></tr><tr><td>

[Sanitize All Translated HTML Fields \[New in Security Center 2.0\]](../reference/sc-sanitize-all-translated-html-fields.md)

</td><td>

-   CVSS Score \(New\): 4.6
-   CVSS Score \(Old\): 8.8

</td></tr><tr><td>

[Enable HTML Sanitizer \[Updated in Security Center 1.3\]](../reference/sc-html-sanitizer.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Implement the x-frame-options: SAMEORIGIN security header \[Updated in Security Center 1.3\]](../reference/sc-x-frame-options-sameorigin.md)

</td><td>

-   CVSS Score \(New\): 5.9
-   CVSS Score \(Old\): 7.1

</td></tr><tr><td>

[Restrict access to GlideSystemUserSession scriptable API \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-access-glidesystemusersession-scriptable-api.md)

</td><td>

-   Remediation \(New\): Ensure the property**glide.sandbox.usersession.allow\_unsanitized\_messages** is set to **false**. If a System Property \[sys\_properties\] record does not exist for this property, create one.
-   Remediation \(Old\): Ensure the property **glide.sandbox.usersession.allow\_unsanitized\_messages** is set to **false**.

</td></tr><tr><td>

[Disallow target cloning \[New in Security Center 1.3\]](../reference/sc-disallow-target-cloning.md)

</td><td>

-   Description \(New\): If **glide.db.clone.allow\_clone\_target** is not set to the recommended value of **false**, then the instance can be used as a clone target, or a record that specifies the instance URL and credentials used for cloning. A system clone is when everything in a database is copied from one instance to another. This is a security risk because the instance database can be overwritten in the cloning process, leading to data loss and lack of data integrity. As a remediation, ensure that **glide.db.clone.allow\_clone\_target** is set to **false**. Not setting this property to the recommended value of false enables the instance to be used as a clone target. This is a security risk because the instance database can be overwritten in the cloning process.
-   Description \(Old\): If **glide.db.clone.allow\_clone\_target** is not set to the recommended value of **false**, then the Instance can be used as a clone target. This risks the instance database being overwritten by cloning process, leading to integrity and availability loss.

</td></tr><tr><td>

[Restrict oauth parameters to POST body \[New in Security Center 1.3\]](../reference/sc-restrict-oauth-parameters-to-post-body.md)

</td><td>

-   CVSS Score \(New\): 4.2
-   CVSS Score \(Old\): 7.4

</td></tr><tr><td>

[Enforce URL allowlist check \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-enforce-url-allowlist-check.md)

</td><td>

-   Description \(New\): If **glide.security.url.whitelist.strict\_check** is not set to the recommended value of **true** then all external URLs are allowed for redirection when **glide.security.url.whitelist** is empty. If **glide.security.url.whitelist** is not empty, then only external URLs in the whitelist are allowed. Thus either setting **glide.security.url.whitelist.strict\_check** to true OR ensuring **glide.security.url.whitelist** is set to a non-empty value with the allowed external URLs leaves the instance in a secure state. If all external URLs are allowed for redirection, this could allow an attacker to redirect a user to a malicious website.
-   Description \(Old\): If **glide.security.url.whitelist.strict\_check** is not set to the recommended value of **true**, and if **glide.security.url.whitelist** is not set to an organization's approved URL, then all external URLs are allowed for redirection. This could allow an attacker to redirect a user to a malicious website.
-   CVSS Score \(New\): 6.3
-   CVSS Score \(Old\): 8.3

</td></tr><tr><td>

[Require XMLdoc2 entity validation with allowlistDisable entity expansion \[Updated in Security Center 1.3\]](../reference/sc-xmldoc2-entity-validation-with-entity-expansion.md)

</td><td>

-   If the **glide.stax.whitelist\_enabled** system property does not exist in the System Properties \[sys\_properties\] table, or it is not set to the recommended value of **true**, then all external entities are allowed when the **glide.stax.allow\_entity\_resolution** system property is set to the value of **true**. If customizations do not require entity expansion, use the **glide.stax.allow\_entity\_resolution** system property to disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.

    -   If you set **glide.stax.allow\_entity\_resolution** to **true**, all external entities attempt to resolve or expand subject entities, subject to the setting of the **glide.stax.whitelist\_enabled** property.
    -   If you set **glide.stax.allow\_entity\_resolution** to **false**, all entity resolution and expansion is blocked. To learn more about this property, see [Disable Entity Expansion within the XMLDocument2 Streaming Parser \[Updated in Security Center 1.5\]](../reference/sc-disable-entity-expansion.md).
When **glide.stax.whitelist\_enabled** is set to **true**, define a listing of comma-delimited FQDN in the **glide.xml.entity.whitelist** property, which are the only URLs that can be reached using the XML entity processing property. To learn more, see [Restrict XML external entities \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-xml-entity-validation-url-allowlist.md). Attackers can use this vulnerability to expand data exponentially in an External Entities Expansion \(XXE\) attack, quickly consuming all system resources.

-   Description \(Old\): If **glide.stax.whitelist\_enabled** is not set to the recommended value of **true**, then all external entities are allowed. This could lead to External Entities Expansion \(XXE\) attacks.
-   Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Restrict XML external entities \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-xml-entity-validation-url-allowlist.md)

</td><td>

-   Protect against XXE attacks by using an allow list to prevent attackers from including arbitrary HTTP requests that the server may execute. This could lead to additional attacks using the server's trust relationship with other entities.

Add `http://java.sun.com/j2ee/dtds/` to the value of the **glide.xml.entity.whitelist** system property, then set the **glide.xml.entity.whitelist.enabled** system property to **true**.

Values other than `http://java.sun.com/j2ee/dtds/` can be included in the in the **glide.xml.entity.whitelist** property, but are unnecessary for the out of the box platform state. Review any additional values to determine if they are safe.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

-   Description \(Old\): If "glide.xml.entity.whitelist" is not set to the recommended value of "[http://java.sun.com/j2ee/dtds/](http://java.sun.com/j2ee/dtds/)" and "glide.xml.entity.whitelist.enabled" is not set to "true", then a malicious external entity can be allowed which could cause an XXE attack. An attacker can use the DTD to include arbitrary HTTP requests that the server may execute. This could lead to additional attacks using the server's trust relationship with other entities.
-   Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Restrict email domains for external user registration \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-external-user-registration-email-domain-allowlist.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Validate file mime type in AttachmentCreator soap web service \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-validate-file-mime-type-in-attachmentcreator.md)

</td><td>

-   Ensure that MIME-types are validated for attachments to prevent dangerous files from being uploaded on your instance using wrong file extensions.

Set the **glide.attachment.enforce\_security\_validation** system property to **true**. When set to **true**, files are uploaded with the correct file type extension.

-   Description \(Old\): If "glide.attachment.enforce\_security\_validation" is not set to the recommended value of "true", then there will be no validation for attachment mime-type and dangerous files could be uploaded on the system using wrong file extensions. When this property is set to 'true', files are uploaded with the correct file type extension.

It is a security best practice to validate file uploads at least with MIME type validation.

-   CVSS Score \(New\): 6.7
-   CVSS Score \(Old\): 7.5

</td></tr><tr><td>

[Define allowed ServiceNow internal IP addresses \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-ip-addresses-access-allowlist.md)

</td><td>

-   Description \(New\) Prevent unnecessary exposure of instance access to wider group of people using the **glide.ip.authenticate.strict** and **glide.ip.authenticate.allow.secured** system properties.

When the **glide.ip.authenticate.strict** system property is set to **true**, internal ServiceNow personnel and systems can only make inbound connections to your instance from essential IP ranges. This limits ServiceNow's visibility to essential internal infrastructure on your instance, and prevents access by broader ServiceNow personnel such as support and sales staff via corporate networks. The **glide.ip.authenticate.allow.secured** system property grants internal ServiceNow inbound connections, including regular authenticated access and unauthenticated diagnostic pages.

If not set to **true**, then a broader ServiceNow internal IP range defined in the **glide.ip.authenticate.allow** property is used to grant these internal ServiceNow inbound connections.

Ensure the **glide.ip.authenticate.allow.secured** system property contains only trusted values and that the property **glide.ip.authenticate.strict** is set to **true**.

-   Description \(Old\): If "glide.ip.authenticate.strict" is set to "true", then internal ServiceNow personelle and systems can only make inbound connections to the instance from essential IP ranges. This limit's ServiceNow's visibility into the instance to essential internal infrastructure, and prevents access by broader ServiceNow personelle such as support and sales staff via corporate networks.

When set to "true", the "glide.ip.authenticate.allow" property is used to grant internal ServiceNow inbound connections. If not set to "true", then a broader ServiceNow internal IP range as defined in "glide.ip.authenticate.allow" is used to grant internal ServiceNow inbound connections.


</td></tr><tr><td>

[Disable Entity Expansion within the XMLDocument2 Streaming Parser \[Updated in Security Center 1.5\]](../reference/sc-disable-entity-expansion.md)

</td><td>

-   Description \(New\):

Disable entity expansion on your instance to secure your instance from attacks such as ability to read system files, and Denial of Service. Use the system property to disallow XML entities to be expanded during parsing by the streaming parser \(XMLDocument2\).

Set the **glide.stax.allow\_entity\_resolution** system property to **false** to disable entity expansion on your instance. If this property does not appear in the System Properties \[sys\_properties\] table, the default value is **true**. Create the property record and set the value to **false** to change it's value.

-   Description \(Old\): If "glide.stax.allow\_entity\_resolution" is not set to the recommended value of "False", then this property allow XML entities to be expanded during parsing by the streaming parser \(XMLDocument2\). XML entity expansion can lead to attacks such as ability to read system files, and Denial of Service.
-   Remediation \(New\): Ensure the property **glide.stax.allow\_entity\_resolution** exists in the sys\_properties table and is set to **false**. If the property does not appear in the sys\_properties list the default value is **true**.
-   Remediation \(Old\): Ensure the property "glide.stax.allow\_entity\_resolution" is set to "false".

</td></tr><tr><td>

[Deny by default with empty ACLs \[Updated in Security Center 1.3\]](../reference/sc-security-manager-default-deny.md)

</td><td>

-   Description \(New\):

Prevent your instance's legacy security manager from allowing access to resources when there are no ACLs defined for that resource, or if there are only wildcard table-level ACLs \(for example, `incident.*`\). When allowed access by default, anything that does not have explicit ACLs set is susceptible to manipulation.

Set the **glide.sm.default\_mode** system property value to **deny** to disallow access when there are no define ACL rules, or there are only wildcard table-level ACLs.

-   Description \(Old\): If "glide.sm.default\_mode" is not set to the recommended value of "deny", then the instance's legacy security manager allows access to a resource when there are no ACLs defined for that resource; or only wildcards table-level ACLs. By setting this to "allow" anything that does not have explicit ACLs set is susceptible to manipulation.
-   CVSS Score \(New\): 6.3
-   CVSS Score \(Old\): 8.8
-   Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Restrict unauthenticated access to attachments](../reference/sc-restrict-unauthenticated-access-attachments.md)

</td><td>

-   Description \(New\):

Secure the images on your instance to prevent sensitive information leak. Images on your instance are accessible via urls that end in `.iix`.

Set the **glide.image\_provider.security\_enabled** system property to **true** to prevent access to your images via these URLs.

**Note:**

This property is not honored for images from the attachment table if the origin table is one of:

    -   Stationeries \[sysevent\_email\_style\]
    -   Welcome Page Sections \[sys\_home\]
    -   System Properties \[sys\_properties\]
Restriction should be applied for unauthenticated users as some attachments might contain sensitive information.

-   Description \(Old\): If "glide.image\_provider.security\_enabled" is not set to the recommended value of "True", then all images are accessible via urls that end in ".iix". This would allow unauthenticated access to images leading to sensitive information leak.

</td></tr><tr><td>

[Disable embedded HTML code \[Updated in Security Center 1.3\]](../reference/sc-allow-embedded-html-code.md)

</td><td>

-   Description \(New\):

Disable support for displaying HTML code embedded using the `[code]` tag. This tag allows rendered HTML to display in journal fields and may lead to cross-site scripting \(XSS\) attacks. These attacks can enable foreign scripts to execute on a user session in the logged in browser's context. Attackers can use these scripts to steal session information and sensitive data. The HTML language was not designed to separate script from formatting, so allowing user-controlled HTML in any system has inherent risk.

Setting the **glide.ui.security.codetag.allow\_script** to **false** is compliant, and significantly reduces this risk, however some small risk remains. It disables only the script portion of a `code` tag, and relies on sanitizing all known conventions of script in the HTML.

Set the **glide.ui.security.allow\_codetag** system property to **false** to completely prohibit journal fields and forms from displaying rendered HTML.

The ServiceNow AI Platform mitigates many injection and cross-site attacks by implementing escaping and encoding techniques. As a result, users can't write/submit HTML formatted inputs for journal fields. But journal fields can render text enclosed within code tags as HTML.

    -   However, there is an associated security risk. If set to `true`, malicious users can write harmful HTML JS code that may be executed on a different client browser after rendering of journal fields.
    -   Set this property to `false` so that administrators can prevent journal fields from rendering HTML code by disabling support for the `[code]` tag.
-   Description \(Old\): Disables support for embedding HTML code created using the \[code\] tag. If "glide.ui.security.allow\_codetag" is not set to the value of "false", then rendered HTML in journal fields and forms will not be displayed. Setting "glide.ui.security.allow\_codetag" to "true" with display embedded HTML code with may lead to cross-site scripting \(XSS\) attacks.

</td></tr><tr><td>

[Enable password reset policy checks \[Updated in Security Center 2.0\]](../reference/sc-enable-password-reset-policy-checks.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Enable email spam scoring and filtering \[Updated in Security Center 1.3\]](../reference/sc-email-spam-scoring-and-filtering.md)

</td><td>

-   Technical Configuration Name \(New\): com.glide.email\_filter,glide.email.read.active
-   Technical Configuration Name \(Old\): com.glide.email\_filter
-   Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Escape Excel Formulas \[Updated in Security Center 1.3\]](../reference/sc-escape-excel-formula.md)

</td><td>

-   Description \(New\):

Prevent potentially malicious formulas in programs such as Excel from being executed after exporting and opening the file by escaping formulas in these files. Excel injection occurs when websites embed untrusted entries inside Excel files. When you use a spreadsheet application such as Microsoft Excel, or LibreOffice Call, to open a file, any cells starting with +, -, =, or @ are interpreted as a formula unless properly escaped. Malicious formulas pose a risk even when the spreadsheet doesn't contain any sensitive information, as they can be used to compromise the viewer's computer through code execution.

Set the **glide.export.escape\_formulas** system property to **true** to escape these formulas from executing.

-   Description \(Old\): Setting the property "glide.export.escape\_formulas" to the recommended value of "true" prevents potentially malicious formulas in programs such as Excel from being executed after exporting and opening the file. Cell values for CSV, Xls, and XLSX can be interpreted as formulas by spreadsheet applications unless properly escaped which can lead to malicious code execution.
-   CVSS Score \(New\): 6.4
-   CVSS Score \(Old\): 6.5

</td></tr><tr><td>

[Restrict JSONP Requests to Trusted URLs \[Updated in Security Center 1.3\]](../reference/sc-restrict-jsonp-requests-to-trusted-urls.md)

</td><td>

-   Description \(New\):

Increase security on your instance by ensuring that only trusted URLs for the AngularJS $http service can allow/reject JSONP requests. JSONP requests are allowed to any URL if these properties are not configured and enabled.

Use the value of the **angular.jsonp.inclusion\_list.urls** system property to define a list of URLs that are trusted and allow for this purpose. Set the value of the **angular.jsonp.inclusion\_list.enabled** system property to **true** to limit allowed JSONP to only the URLs listed in **angular.jsonp.inclusion\_list.urls**.

-   Description \(Old\): This property specifies trusted URLs for the angularJS $http service to allow/reject JSONP requests. Property is necessary because this is a potentially breaking change for customers, so they need a way to add their trusted URLs. If "angular.jsonp.inclusion\_list.enabled" is not set to the recommended value of "true", then JSONP requests are allowed to any URL.

</td></tr><tr><td>

[Enable SNC access control plugin \[Updated in Security Center 1.3\]](../reference/sc-snc-access-control-plugin.md)

</td><td>

-   Description \(New\):

Prevent ServiceNow Customer Service and Support personnel from accessing the instances without your express permission by enabling the SNC Access Control \(com.snc.snc\_access\_control\) plugin. Although all access to your instance is audited, you may prefer to control this access. This access method is fully auditable and tracked.

**Note:** Other authorized ServiceNow Operations personnel, in their capacity to support and manage the product, are required to perform administrative actions on the underlying infrastructure. Enabling this plugin may affect support service levels and the Availability SLA. Availability SLA is then measured from the time that Support staff personnel are granted access to your instance.

Enable the SNC Access Control \(com.snc.snc\_access\_control\) plugin to restrict access to your instance without your express permission. For more details on this feature, see [ServiceNow access control](../../security/concept/c_SNCAccessControl.md). For activation information, see [Activate ServiceNow access control](../../security/task/t_ActivateSNCAccessControl.md)

-   Description \(Old\): The SNC Access Control \(com.snc.snc\_access\_control\) plugin prevents Customer Service and Support personnel from accessing the instances without your express permission. However, other authorized ServiceNow Operations personnel, in their capacity to support and manage the product, are required to perform administrative actions on the underlying infrastructure. This infrastructure includes servers and databases, among other infrastructure components that make up the SaaS solution. This access method is fully auditable and tracked.This plugin enables you to restrict access to your instance without your express permission, so it may affect support service levels and the Availability SLA. Availability SLA is then measured from the time that Support staff personnel are granted access to your instance.
-   Remediation \(New\): Ensure the plugin "com.snc.snc\_access\_control" is activated. Read the documentation on activating at [https://www.servicenow.com/docs/csh?topicname=t\_ActivateSNCAccessControl.html&amp;version=latest.](https://www.servicenow.com/docs/csh?topicname=t_ActivateSNCAccessControl.html&version=latest.)
-   Remediation \(Old\): Ensure the plugin "com.snc.snc\_access\_control" is activated.
-   CVSS Score \(New\): 3.3
-   CVSS Score \(Old\): 8.2

</td></tr><tr><td>

[Maximize failed login unlock timeout duration \[Updated in Security Center 1.3\]](../reference/sc-managing-unlock-timeout-after-failed-logins.md)

</td><td>

-   Technical Configuration Name \(New\): glide.user.unlock\_timeout\_in\_mins, sysevent\_script\_action
-   Technical Configuration Name \(Old\): glide.user.unlock\_timeout\_in\_mins
-   Description \(New\):

Help secure your instance against brute force attacks by defining a time period during which a user cannot attempt to log in after being locked out. The **glide.user.unlock\_timeout\_in\_mins** system property unlocks the user account after the time period that is specified in it's value. If no value is specified, your instance unlocks the user account after the default period of 15 minutes.

-   Description \(Old\): If "glide.user.unlock\_timeout\_in\_mins" is not set to the recommended value of "15", then it may be easier to brute force accounts in a faster timeframe. This property unlocks the user account after the time period that is specified for the glide.user.unlock\_timeout\_in\_mins property. If no value is specified, then the system unlocks the user account after the default period of 15 minutes.
-   Remediation \(New\):

Set the **glide.user.unlock\_timeout\_in\_mins** system property value to a minimum of **15**. If **glide.user.unlock\_timeout\_in\_mins** does not exist, the default lockout time is set to 15 minutes.

Ensure that the **SNC User Lockout Check with Auto Unlock** script action \(found on the Script Action \[sysevent\_script\_action\] table\) is present and active. The **SNC User Lockout Check with Auto Unlock** script action is installed with the High Security Settings \(com.glide.high\_security\) plugin.

-   Remediation \(Old\): Ensure the property "glide.user.unlock\_timeout\_in\_mins" is set to "15" or more.
-   Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Restrict access to specific IP ranges plugin \[Updated in Security Center 1.3\]](../reference/sc-restrict-access-to-specific-ip-ranges-plugin.md)

</td><td>

-   Technical Configuration Name \(New\): com.snc.ipauthenticator,ip\_access
-   Technical Configuration Name \(Old\): com.snc.ipauthenticator

</td></tr><tr><td>

[Restrict access to emails with empty target table](../reference/sc-restrict-access-to-emails-with-empty-target-table.md)

</td><td>

-   CVSS Score \(New\): 6.5
-   CVSS Score \(Old\): 5.4

</td></tr><tr><td>

[Restrict downloadable MIME types \[Updated in Security Center 1.3 and 2.0\]](../reference/sc-downloadable-mime-type-denylist.md)

</td><td>

-   CVSS Score \(New\): 6.4
-   CVSS Score \(Old\): 8

</td></tr><tr><td>

[Enable updated version of MultiSSO plugin \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-updated-version-of-multi-sso-plugin-is-enabled.md)

</td><td>

-   Technical Configuration Name \(New\): glide.authenticate.multissov2\_feature.enabled
-   Technical Configuration Name \(Old\): glide.authenticate.multisso.enabled,glide.authenticate.multissov2\_feature.enabled
-   Description \(New\):

If the Multi SSO plugin is enabled on an instance, reduce security vulnerabilities by confirming that the v2 version is enabled. The latest version enhances security and has more features, such as Assertion encryption support, and IDP-initiated Single Logout \(SLO\). If the latest version is not enabled, the new security features cannot be used and the instance is at risk of using an plugin which is deprecated.

Follow the steps in [KB0756504](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0756504) to upgrade to the latest version. This process includes checking for and migrating any customization-related changes, then upgrading the version. When complete, the **glide.authenticate.multissov2\_feature.enabled** system property is automatically set **true**.

-   Description \(Old\): If the Multi SSO plugin is enabled on an instance, the v2 version should be enabled. Versions prior to MultiSSOv2, including SAML 1.1 and SAML 2.0, do not follow best practice and use opensaml library versions with known CVEs. If the known CVEs were exploitable in outdated opensaml libraries, this could allow the attacker to forge messages and bypass authentication through XML Signature Wrapping attacks, impersonate entities or allow person-in-the-middle attackers to gain unauthorized access to the platform.
-   CVSS Score \(New\): 0
-   CVSS Score \(Old\): 7.1

</td></tr><tr><td>

[Prevent inactive users from logging in \[New in Security Center 1.5\]](../reference/sc-prevent-inactive-users-from-logging-in.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Enable MID audit log \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-enable-mid-audit-log-plugin-applicability-mid-server.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Ensure archive table ACLs are checked \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-ensure-archive-table-acls-are-checked.md)

</td><td>

Rule Script: Script has been updated to improve detection accuracy

</td></tr><tr><td>

[Define active session timeout exception roles \[New in Security Center 1.3\]](../reference/sc-define-active-session-timeout-exception-roles.md)

</td><td>

-   CVSS Score \(New\): 6.4
-   CVSS Score \(Old\): 7.1

</td></tr><tr><td>

[Limit HTTP response body size \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-limit-http-response-body-size.md)

</td><td>

-   Description \(New\):

Prevent `OutOfMemoryExceptions` that can result from a request response body being too large using the **glide.http.response.get\_body.limit.enabled** and **glide.http.response.get\_body.limit** system properties. These exceptions can cause denial of service \(DOS\) attacks as well as other issues that may aid attackers in compromising an instance. Not setting these properties to the recommended values could make your instance vulnerable to OutOfMemoryExceptions and denial of service attacks.

To protect your instance against these security vulnerabilities:

    -   Set the **glide.http.response.get\_body.limit.enabled** system property to **true**.
    -   Ensure that the **glide.http.response.get\_body.limit** system property set to no more than 524,288,000 megabytes \(500 MB\).
-   Description \(Old\): The properties glide.http.response.get\_body.limit.enabled and glide.http.response.get\_body.limit were introduced to enable new functionality that prevents Out of memory exceptions being thrown as a result of a requests response body being too big. Out of memory exceptions can cause denial of service attacks as well as other issues that may aid attackers in compromising an instance.
-   CVSS Score \(New\): 3.1
-   CVSS Score \(Old\): 6.4

</td></tr><tr><td>

[Limit UI active session life span \[New in Security Center 1.3\]](../reference/sc-limit-ui-active-session-life-span.md)

</td><td>

-   Description \(New\):

Reduce the scope of potential security incidents by decreasing the lifespan of active HTTP sessions. The **glide.ui.active.session.life\_span** system property enforces a maximum lifespan on active HTTP sessions irrespective of inactive timeout. Longer maximum lifespans can allow an attacker to use a stolen session a for longer time, increasing the scope of a security incident. The default value of **0** disables timeout of active sessions

Set the **glide.ui.active.session.life\_span** to a value between 1 and 720. This value represents the time in minutes that HTTP sessions can remain active.

-   Description \(Old\): This configuration will enforce max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes and the value of zero will disable timing out the active sessions. A larger maximum lifespan could allow an attacker to persist a stolen session for longer, increasing the scope of a security incident. This particular property is limited to UI session timeout.

</td></tr></tbody>
</table>**Parent Topic:**[Updated hardening settings](hardening-settings-updated.md)

