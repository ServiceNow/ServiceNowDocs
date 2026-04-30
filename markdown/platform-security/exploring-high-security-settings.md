---
title: Exploring High Security Settings
description: High Security Settings refer to several security options available in your instance.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [High Security Settings]
---

# Exploring High Security Settings

High Security Settings refer to several security options available in your instance.

The High Security Settings module is activated with the High Security Settings plugin, which is active by default on new instances. If High Security Settings are not active on your instance, see [Requesting High Security Settings activation](../task/t_ActivateHighSecuritySettings.md). To learn more about this plugin, see [Enable High Security Plugin \[Updated in Security Center 1.3\]](../../security-center/reference/sc-high-security-plugin.md) in Instance Security Hardening Settings. Properties for these types of high security settings are available:

-   Default property values: To harden security on your platform by centralizing all critical security settings to one location for management and auditing.
-   Default deny property: Provides a security manager property to control the default security behavior for table access.
-   Security Administrator role: Provides a role to prevent modification of key security settings and resources. The Security Administrator role is not inherited by the admin role and must be explicitly assigned.
-   Elevated privileges: Allows users with the security admin role to operate in the context of a normal user and elevate to higher security role when needed.
-   Property access controls: Allows security administrators to set the roles required to read and write properties.
-   System logs: Are read only.
-   Access control rules: Control what data users can access and how they can access it.

**Note:**

-   High Security Settings also automatically activates the Contextual Security plugin, if it is not already active. In addition, Platform Security Settings - High delivers settings and features in the context of increasing the security of your instance.
-   The Instance Security Hardening Settings content contains detailed descriptions, and compliance values, for the security-related system properties and plugins in the ServiceNow AI Platform.
-   To learn more about each of these properties, see [Hardening settings](../../security-center/reference/security-hardening-settings.md).

There are two ways to set or change High Security Settings properties.

-   Navigate to **System Security** &gt; **High Security Settings**.

    Options on the High Security Properties page are **Yes** or **No**.

-   Navigate to the **sys\_properties.list** and search for the property you want to set or change.

    Options in the System Properties table \[sys\_properties.list\] are **true** or **false**.


## Property access control

Two additional columns are created in the Properties \[sys\_properties\] table when High Security Settings are active:

-   **read\_roles**: A comma-separated list of role names that are allowed to read all fields of this property.
-   **write\_roles**: A comma-separated list of role names that are allowed to write/modify all fields of this property.

Properties listed in the Properties table have **read\_roles** of admin, and **write\_roles** of security\_admin. Users with the admin role can view and read the property values, but must elevate to the security\_admin role to modify them.

## Notifications

Activation of high security settings also activates security warning messages. The following is an example of a message that appears after an approval.

![Security Warning notification](../image/Highsecuritywarning.png "Security Warning notification")

## High Security Settings properties

<table id="table_q1z_23k_nsb"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Default Value

</th><th>

Instance Security Hardening Settings

</th></tr></thead><tbody><tr><td>

glide.ui.escape\_text

</td><td>

Escape XML values at the parser level for the user interface. Prevents reflected and stored cross-site scripting attacks. This property is not applicable in Service Portal.

 **Note:** This property is set to **true** by default in Vancouver and later releases, and can't be changed by administrators. For a use case where the property has to be changed, contact customer support.

</td><td>

Yes

</td><td>

[Escape XML markup \[Updated in Security Center 1.3\]](../../security-center/reference/sc-escape-xml.md)

</td></tr><tr><td>

glide.ui.escape\_all\_script

</td><td>

Forces all expressions within Jelly JavaScript `<script type="text/javascript">` tags to be escaped by default. Enforces escaping only if the type attribute in the `<script>` tag is empty, or if the value is `text/javascript`, `text/ecmascript`, `application/javascript`, `application/ecmascript`, or `application/x-javascript`.

</td><td>

Yes in new instances

</td><td>

[Escape jelly script \[Updated in Security Center 1.3 and 1.5\]](../../security-center/reference/sc-escape-jelly.md)

</td></tr><tr><td>

glide.ui.rotate\_sessions

</td><td>

Rotate HTTP session identifiers to reduce security vulnerabilities. See: [http://www.owasp.org/index.php/Session\_Management\#Rotate\_Session\_Identifiers](http://www.owasp.org/index.php/Session_Management#Rotate_Session_Identifiers).

</td><td>

Yes**Note:**

If you are using the SAML 2.0 plugin for Single Sign-on authentication, set this property to No. Otherwise, it interferes with the session information sharing that takes place between the instance and the Identity Provider.

</td><td>

[Rotate HTTP session identifiers](../../security-center/reference/sc-rotate-http-session-identifiers.md)

</td></tr><tr><td>

glide.ui.secure\_cookies

</td><td>

Enable secure session cookies: Enable additional cookie security. If **Yes**, strict session cookie validation is enforced.

</td><td>

Yes

</td><td>

[Enforce strict security of session cookies \[Updated in Security Center 1.3\]](../../security-center/reference/sc-secure-session-cookies.md)

</td></tr><tr><td>

glide.security.password\_reset.uri

</td><td>

For mobile Password Reset, URL that the user is taken to when the user clicks the **Forgot password?** button.

</td><td>

 

</td><td>

None

</td></tr><tr><td>

glide.security.strict.updates

</td><td>

Double-check security on inbound transactions during form submission \(rights are always checked on form generation\).

 **Note:** This property is set to **true** by default in Vancouver and later releases, and can't be changed by administrators. For a use case where the property has to be changed, contact customer support.

</td><td>

Yes

</td><td>

[Double check inbound transactions \[Updated in Security Center 1.3\]](../../security-center/reference/sc-double-check-inbound-transactions.md)

</td></tr><tr><td>

glide.security.strict.actions

</td><td>

Check conditions on UI actions before execution. Normally conditions are checked only during form rendering.

</td><td>

Yes

</td><td>

[Check UI action conditions before execution](../../security-center/reference/sc-check-ui-action-conditions-before-execution.md)

</td></tr><tr><td>

glide.security.use\_csrf\_token

</td><td>

Enable usage of a secure token to identify and validate incoming requests. This token is used to prevent cross-site request forgery attacks.

</td><td>

Yes

</td><td>

[Enable Anti-CSRF token \[New in Security Center 1.3, updated in 1.5, and removed in 2.0\]](../../security-center/reference/sc-anti-csrf-token.md)

</td></tr><tr><td>

glide.ui.escape\_html\_list\_field

</td><td>

Escape HTML for HTML fields in a list view.

</td><td>

Yes

</td><td>

[Escape HTML in list views \[Updated in Security Center 1.3 and 1.5\]](../../security-center/reference/sc-escape-html.md)

</td></tr><tr><td>

glide.html.escape\_script

</td><td>

Escape JavaScript tags in HTML fields.

</td><td>

Yes

</td><td>

[Escape JavaScript \[Updated in Security Center 1.3\]](../../security-center/reference/sc-escape-javascript.md)

</td></tr><tr><td>

glide.ui.forgetme

</td><td>

Remove the **Remember me** check box from the login page.

</td><td>

Yes

</td><td>

[Remove remember me](../../security-center/reference/sc-remove-remember-me.md)

</td></tr><tr><td>

glide.smtp.auth

</td><td>

Authenticate with the SMTP server by the user name and password properties.**Note:** This property is deprecated.

</td><td>

Yes

</td><td>



</td></tr><tr><td>

glide.script.use.sandbox

</td><td>

Run client-generated scripts \(AJAXEvaluate and query conditions\) inside a reduced-rights sandbox. If true, only those business rules with the **Client callable** option selected and script includes with the **Sandbox enabled** option selected are available and certain back-end API calls are disallowed. For more information, see [Configuring Script sandbox property](../reference/r_ScriptSandboxing.md).

</td><td>

Yes

</td><td>

[Enable script sandbox \[Updated in Security Center 1.3\]](../../security-center/reference/sc-client-generated-scripts-sandbox.md)

</td></tr><tr><td>

glide.soap.strict\_security

</td><td>

Enforce strict security on incoming SOAP requests. Requires incoming SOAP requests to go through the security manager for table and field access and checks SOAP users for the correct roles for using the web service.

</td><td>

Yes

</td><td>

[Enforce SOAP request strict security \[Updated in Security Center 1.3\]](../../security-center/reference/sc-soap-request-strict-security.md)

</td></tr><tr><td>

glide.basicauth.required.wsdl

</td><td>

Require authorization for incoming WSDL requests.

 **Note:** If you choose not to require authorization for incoming WSDL requests, you must modify the Access Control \(ACL\) rules to allow guest users to access the WSDL content.

</td><td>

Yes

</td><td>

[Require authorization for WSDL request \[Updated in Security Center 1.3 and 1.5\]](../../security-center/reference/sc-wsdl-request-authorization.md)

</td></tr><tr><td>

glide.basicauth.required.csv

</td><td>

Require basic authorization for incoming CSV requests

.

</td><td>

Yes

</td><td>

[Require authorization for csv requests \[Updated in Security Center 1.3\]](../../security-center/reference/sc-require-authorization-for-csv-requests.md)

</td></tr><tr><td>

glide.basicauth.required.excel

</td><td>

Require basic authorization for incoming Excel requests.

</td><td>

Yes

</td><td>

[Require authorization for excel requests \[Updated in Security Center 1.3\]](../../security-center/reference/sc-excel-request-authorization.md)

</td></tr><tr><td>

glide.basicauth.required.importprocessor

</td><td>

Require basic authorization for incoming import requests.

</td><td>

Yes

</td><td>

[Require authorization for import requests \[Updated in Security Center 1.3\]](../../security-center/reference/sc-import-request-authorization.md)

</td></tr><tr><td>

glide.basicauth.required.pdf

</td><td>

Require basic authorization for incoming PDF requests.

</td><td>

Yes

</td><td>

[Require authorization for pdf requests \[Updated in Security Center 1.3\]](../../security-center/reference/sc-require-authorization-for-pdf-requests.md)

</td></tr><tr><td>

glide.basicauth.required.rss

</td><td>

Require basic authorization for incoming RSS requests.

</td><td>

Yes

</td><td>

[Require authorization for RSS requests \[Updated in Security Center 1.3\]](../../security-center/reference/sc-rss-request-authorization.md)

</td></tr><tr><td>

glide.basicauth.required.scriptedprocessor

</td><td>

Require basic authorization for incoming script requests.

</td><td>

Yes

</td><td>

[Require authorization for script requests \[Updated in Security Center 1.3\]](../../security-center/reference/sc-script-request-authorization.md)

</td></tr><tr><td>

glide.basicauth.required.soap

</td><td>

Require basic authorization for incoming SOAP requests.

</td><td>

Yes

</td><td>

[Require authorization for SOAP requests \[Updated in Security Center 1.3, 1.5, and 2.0\]](../../security-center/reference/sc-soap-request-authorization.md)

</td></tr><tr><td>

glide.basicauth.required.unl

</td><td>

Require basic authorization for incoming unload requests.

</td><td>

Yes

</td><td>

[Require authorization for unload requests \[Updated in Security Center 1.3\]](../../security-center/reference/sc-require-authorization-for-unload-requests.md)

</td></tr><tr><td>

glide.basicauth.required.xml

</td><td>

Require basic authorization for incoming XML requests.

</td><td>

Yes

</td><td>

[Require authorization for XML requests \[Updated in Security Center 1.3\]](../../security-center/reference/sc-xml-request-authorization.md)

</td></tr><tr><td>

glide.basicauth.required.xsd

</td><td>

Require basic authorization for incoming XSD requests.

</td><td>

Yes

</td><td>

[Require Authorization for XSD Requests \[Updated in Security Center 1.3\]](../../security-center/reference/sc-xsd-request-authorization.md)

</td></tr><tr><td>

glide.cms.catalog\_uri\_relative

</td><td>

Enforce relative links from the URI parameter on /ess/catalog.do. If **Yes**, only relative URLs are permitted through the /ess/catalog.do page using the **uri** parameter. If **No**, all URLs are permitted, which may permit linking to external unauthorized content.

</td><td>

Yes

</td><td>

[Enforce relative links \[Updated in Security Center 1.3 and 1.5\]](../../security-center/reference/sc-enforce-relative-links.md)

</td></tr><tr><td>

glide.set\_x\_frame\_options

</td><td>

Enable this property to set the X-Frame-Options response header to SAMEORIGIN for all UI pages. The X-Frame-Options HTTP response header can be used to indicate whether a browser should be allowed to render a page in a &lt;frame&gt; or &lt;iframe&gt;. Sites can use this property to avoid clickjacking attacks by ensuring that their content is not embedded into other sites. [https://developer.mozilla.org/en/the\_x-frame-options\_response\_header](https://developer.mozilla.org/en/the_x-frame-options_response_header)

</td><td>

Yes

</td><td>

[Implement the x-frame-options: SAMEORIGIN security header \[Updated in Security Center 1.3\]](../../security-center/reference/sc-x-frame-options-sameorigin.md)

</td></tr><tr><td>

glide.ui.attachment.download\_mime\_types

</td><td>

A list of comma-separated attachment mime types that do not render inline in the browser. Prevents cross-site scripting attacks. For example, `text/html` forces HTML files to be downloaded to the client as attachments rather than viewed inline in the browser.

</td><td>

`text/html,image/svg,image/svg+xml`

</td><td>

[Restrict downloadable MIME types \[Updated in Security Center 1.3 and 2.0\]](../../security-center/reference/sc-downloadable-mime-type-denylist.md)

</td></tr><tr><td>

glide.security.groupby\_acl\_check

</td><td>

When this property is enabled, ACL checks for GroupBy operations are performed for the group names based on the actual data from the groups.

</td><td>

Yes

</td><td>

None

</td></tr><tr><td>

glide.security.diag\_txns\_acl

</td><td>

If **Yes**, only the admin user or user from allowed IP address can access `stats.do`, `threads.do`, and `replication.do`.

</td><td>

No

</td><td>

[Restrict performance monitoring access \[Updated in Security Center 1.3\]](../../security-center/reference/sc-performance-monitoring-acl.md)

</td></tr><tr><td>

glide.ui.security.codetag.allow\_script

</td><td>

Allow embedded HTML \(using \[code\] tags\) to contain JavaScript tags.

 **Note:** This property is set to **true** by default in Vancouver and later releases, and can't be changed by administrators. For a use case where the property has to be changed, contact customer support.

</td><td>

No

</td><td>

[Disable embedded HTML code \[Updated in Security Center 1.3\]](../../security-center/reference/sc-allow-embedded-html-code.md)

</td></tr><tr><td>

glide.script.allow.ajaxevaluate

</td><td>

Enable the AJAXEvaluate processor. The AJAXEvaluate API call allows the client to send and execute arbitrary scripts on the server.

</td><td>

No

</td><td>

[Disable AJAXEvaluate](../../security-center/reference/sc-disable-ajaxevaluate.md)

</td></tr></tbody>
</table>The following properties are defined in the sys\_properties table, but are not visible on the High Security Settings page.

<table id="table_jgq_1mk_nsb"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Default value

</th><th>

Instance Security Hardening Settings

</th></tr></thead><tbody><tr><td>

com.glide.communications.httpclient.verify\_hostname

</td><td>

Verify the hostname and certificate chain presented by remote SSL hosts. Protect against Man-In-The-Middle \(MITM\) attacks.

 For more detail, see [Set up Kubernetes spoke](https://www.servicenow.com/docs/access?context=set-up-kubernetes&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)

 **Note:** This property overrides the com.glide.communications.trustmanager\_trust\_all property.

</td><td>

true

</td><td>

None

</td></tr><tr><td>

glide.basicauth.required.schema

</td><td>

Require basic authentication for inbound table schema requests.

</td><td>

true

</td><td>

None

</td></tr><tr><td>

glide.security.csrf\_previous.allow

</td><td>

Allow usage of an expired secure token to identify and validate incoming requests. This token is used to prevent cross-site request forgery attacks.

</td><td>

false

</td><td>

None

</td></tr><tr><td>

glide.security.csrf\_previous.time\_limit

</td><td>

Time in seconds for a secure token to expire. Allows control over the length of time that the previous CSRF token is valid. When the user session expires, the secure token expires with it unless the **glide.security.csrf\_previous.allow** property is enabled and it is within the timeframe described by this property. This token is used to prevent cross-site request forgery attacks.

</td><td>

86400**Note:** Value in seconds. Equivalent to 1 day.

</td><td>

None

</td></tr><tr><td>

glide.security.csrf.strict.validation.mode

</td><td>

Enforces strict validation on CSRF tokens so that users cannot resubmit a request if the CSRF token does not match.

</td><td>

false

</td><td>

[Prevent Users From Accepting Warning To Bypass CSRF Validation \[Updated in Security Center 1.3 and 1.5\]](../../security-center/reference/sc-csrf-strict-validation.md)

</td></tr><tr><td>

com.glide.security.check\_unsanitized\_html

</td><td>

Enforces sanitization behavior of translated\_html fields on a global level for field assignments.

</td><td>

enforce

</td><td>

None

</td></tr></tbody>
</table>