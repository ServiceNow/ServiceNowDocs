---
title: Validation, sanitization, and encoding
description: Validation, sanitization, and encoding addresses input validation to prevent against vulnerabilities like Cross-Site Scripting \(XSS\), SQL injection and other attacks.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Hardening settings, Platform Security]
---

# Validation, sanitization, and encoding

Validation, sanitization, and encoding addresses input validation to prevent against vulnerabilities like Cross-Site Scripting \(XSS\), SQL injection and other attacks.

This control ensures input validation and output encoding are in place and correctly configured, such as encoding or escaping output data. This category also includes checks for items such as deserialization of objects, sandboxing where needed, and positive validation through allow lists.

-   **[Restrict access to GlideSystemUserSession scriptable API \[Updated in Security Center 1.3 and 2.0\]](sc-access-glidesystemusersession-scriptable-api.md)**  
The client callable GlideSystemUserSessionSandbox scriptable API exposes GlideSystemUserSession's addErrorMessageNoSanitization and addInfoMessageNoSanitization methods to the JavaScript sandbox. This allows all users to call this method via script.
-   **[Disable JavaScript tags in embedded HTML \[Updated in Security Center 1.3\]](sc-allow-javascript-tags-in-embedded-html.md)**  
Use the **glide.ui.security.codetag.allow\_script** property to disable support for embedding HTML JavaScript code created using of the \[code\] tag.
-   **[Enable the hardened java security manager \[New in Security Center 1.3\]](sc-enable-the-hardened-java-security-manager.md)**  
The **glide.security.manager** property contains the Java classname of the current Java security manager.
-   **[Enforce HTML Sanitization \[Updated in Security Center 1.3\]](sc-check-unsanitized-html.md)**  
Use the **com.glide.security.check\_unsanitized\_html** property to enforce sanitization behavior of translated\_html fields on a global level for field assignments.
-   **[Enable script sandbox \[Updated in Security Center 1.3\]](sc-client-generated-scripts-sandbox.md)**  
Use the **glide.script.use.sandbox** property to enable script sandboxing.
-   **[Disable AJAXEvaluate](sc-disable-ajaxevaluate.md)**  
Use the **glide.script.allow.ajaxevaluate** to protect the system API from vulnerabilities of Client script execution through AJAX calls.
-   **[Disable Entity Expansion within the XMLDocument2 Streaming Parser \[Updated in Security Center 1.5\]](sc-disable-entity-expansion.md)**  
If customizations do not require entity expansion, use the **glide.stax.allow\_entity\_resolution** property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.
-   **[Disable external content url \[Updated in Security Center 2.0\]](sc-disable-external-content-url.md)**  
Manage how external link metadata is used in your instance with Connect Chat.
-   **[Restrict downloadable MIME types \[Updated in Security Center 1.3 and 2.0\]](sc-downloadable-mime-type-denylist.md)**  
The **glide.ui.attachment.download\_mime\_types** property will force the specified list of dangerous file types to be downloaded to the client and not viewed inline in the browser.
-   **[Disable embedded HTML code \[Updated in Security Center 1.3\]](sc-allow-embedded-html-code.md)**  
Use the **glide.ui.security.allow\_codetag** property to disable support for embedding HTML code created using the \[code\] tag.
-   **[Enable HTML Sanitizer within Virtual Agent \[Updated in Security Center 1.3 and 1.5\]](sc-enable-html-sanitizer.md)**  
Use the **com.glide.cs.html.sanitizer.enabled** property to enable HTMLSanitizerService.
-   **[Enable Jelly JS Interpolation Protection](sc-enable-jelly-js-interpolation-protection.md)**  
Use the **glide.ui.jelly.js\_interpolation.protect** property to ensure that any JavaScript about to be executed on a Jelly page is protected from injection with the help of Jelly interpolation.
-   **[Enable Jelly JS interpolation protection for nested expressions \[Updated in Security Center 2.0\]](sc-enable-jelly-js-interpolation-protection-for-nested-expressions.md)**  
Manage the interpolation protection on your instance.
-   **[Enforce relative links \[Updated in Security Center 1.3 and 1.5\]](sc-enforce-relative-links.md)**  
Use the **glide.cms.catalog\_uri\_relative** property to enforce relative links from the URI parameter on `/ess/catalog.do`.
-   **[Enforce URL allowlist check \[Updated in Security Center 1.3, 1.5, and 2.0\]](sc-enforce-url-allowlist-check.md)**  
Use the **glide.security.url.whitelist** system property to add extra layer of validation to ensure whether any external URL introduced should be a part of inclusion listed URLs.
-   **[Escape Excel Formulas \[Updated in Security Center 1.3\]](sc-escape-excel-formula.md)**  
Use the **glide.export.escape\_formulas** property to prevent Excel Injection, also, known as formula injection.
-   **[Escape HTML in list views \[Updated in Security Center 1.3 and 1.5\]](sc-escape-html.md)**  
Use the **glide.ui.escape\_html\_list\_field** property to force HTML escapes for HTML fields in a list view.
-   **[Escape JavaScript \[Updated in Security Center 1.3\]](sc-escape-javascript.md)**  
Use the **glide.html.escape\_script** property to force escape from JavaScript \(`<script></script>`\) tags in HTML fields during list views.
-   **[Escape jelly script \[Updated in Security Center 1.3 and 1.5\]](sc-escape-jelly.md)**  
Use the **glide.ui.escape\_all\_script** property to force escape of all scripts injected into Jelly.
-   **[Escape scripts in scratchpad \[Updated in Security Center 1.3\]](sc-escape-scratchpad.md)**  
Learn how scratchpad factors into the security posture of your instance and how to manage it so that malicious scripts can't be executed on it.
-   **[Escape XML markup \[Updated in Security Center 1.3\]](sc-escape-xml.md)**  
Use the **glide.ui.escape\_text** property to force escape of XML values at the parser level before transmitting them to the client's browser.
-   **[Escape xml response](sc-escape-xml-response.md)**  
Manage how XML escapes are handled on your instance.
-   **[Enable HTML Sanitizer \[Updated in Security Center 1.3\]](sc-html-sanitizer.md)**  
Use the **glide.html.sanitize\_all\_fields** property to enable the HTMLSanitizer script include, which sanitizes HTML input based on exclusion listed and inclusion listed attributes configured in a script.
-   **[Restrict allowed Java packages \[Updated in Security Center 1.3\]](sc-java-packages-allowlist.md)**  
Configuring these properties protect from dangerous APIs being exposed to the scripting engine.
-   **[Unset LDAP Initial distinguished name \[Updated in Security Center 1.3 and removed in 2.0\]](sc-ldap-initial-distinguished-name.md)**  
Use this property to manage the distinguished name of a LDAP Server record.
-   **[Enforce strict security of session cookies \[Updated in Security Center 1.3\]](sc-secure-session-cookies.md)**  
Use the **glide.ui.secure\_cookies** property to require properly formatted cookies
-   **[Minimize Entity Expansion Threshold for GlideXMLUtil Scriptable \[Updated in Security Center 1.3, 1.5, and 2.0\]](sc-setting-entity-expansion-threshold.md)**  
Use the **glide.xmlutil.max\_entity\_expansion** property to change the maximum entity expansion limit to a smaller number.
-   **[Prevent Empty ACL Creation \[New in Security Center 2.0\]](sc-prevent-empty-acl-creation.md)**  
Set the **glide.security.empty\_acl.popup\_window.enabled** property to the secure value of true to block attempts to create, update, or save an invalid ACL. This setting will also provide a client-side model to configure a role or security attribute for the ACL.
-   **[Define restricted downloadable MIME types \[Updated in Security Center 1.3, 1.5, and 2.0\]](sc-downloadable-mime-types.md)**  
Use the **glide.ui.attachment.force\_download\_all\_mime\_types** property to download MIME types and not to render inline in the browser.
-   **[Restrict uploaded MIME types \[Updated in Security Center 1.3 and 2.0\]](sc-upload-mime-type-restriction.md)**  
Use the **glide.security.file.mime\_type.validation** property to activate MIME type checking for uploads. You can enable \(set the property to **true**\) or disable \(set it to **false**\) MIME type validation for file attachments.
-   **[Restrict XML external entities \[Updated in Security Center 1.3 and 2.0\]](sc-xml-entity-validation-url-allowlist.md)**  
Configure system properties to ensure that your instance only processes XML from trusted sources to help prevent XML external entity \(XXE\) attacks.
-   **[Require XMLdoc2 entity validation with allowlistDisable entity expansion \[Updated in Security Center 1.3\]](sc-xmldoc2-entity-validation-with-entity-expansion.md)**  
If customizations do not require entity expansion, use the **glide.xmlutil.max\_entity\_expansion** property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.
-   **[Sanitize All Translated HTML Fields \[New in Security Center 2.0\]](sc-sanitize-all-translated-html-fields.md)**  
Learn how to configure the **glide.translated\_html.sanitize\_all\_fields** property to the secure value to ensure that all **translated\_html** elements are sanitized with an HTML sanitizer.
-   **[Sanitize HTML in the Description Fields of the Impact Workspace Module](sanitize-html-in-the-description-fields-of-the-impact-workspace-module.md)**  
Sanitize the HTML in the description fields by removing HTML tags that are sources of HTML injection attacks with the **sn\_impact\_common.blacklist\_tags\_HTML\_injection** property.
-   **[Set safe content security policy for svg files \[New in Security Center 1.3\]](sc-set-safe-content-security-policy-for-svg-files.md)**  
The **com.glide.csp.self\_script\_src\_svg** property adds the **script-src none** directive to the HTTP Content-Security-Policy header when Scalable Vector Graphics \(SVGs\) are accessed through the Translation Memory Index \(IIX\) file extension.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

