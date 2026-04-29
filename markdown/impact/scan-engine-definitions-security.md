---
title: Scan Engine definitions: Security
description: Scan Engine security definitions measure implementation of protocols across a ServiceNow instance to prevent unauthorized access, data breaches, cyber attacks, and potential vulnerabilities.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 38
breadcrumb: [Scan Engine definitions, Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan Engine definitions: Security

Scan Engine security definitions measure implementation of protocols across a ServiceNow instance to prevent unauthorized access, data breaches, cyber attacks, and potential vulnerabilities.

## Australia definitions

The following security definitions have been added for the Australia 2026 release:

<table id="table_security"><thead><tr><th>

Number

</th><th>

Active

</th><th>

Level of Finding

</th><th>

Unique ServiceNow Product

</th><th>

Short Description

</th><th>

Business Impact

</th><th>

Steps to Resolve

</th><th>

Supporting Documentation

</th></tr></thead><tbody><tr><td>

sn\_SE10023

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Scripts should not use the eval\(\) function

</td><td>

Security breach.

</td><td>

Remove the **eval** function from the script.

</td><td>

[Documentation](https://developer.servicenow.com/dev.do%23!/guides/zurich/now-platform/tpb-guide/scripting_technical_best_practices)

</td></tr><tr><td>

sn\_SE10024

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Scripts should not use the eval\(\) function

</td><td>

Security breach.

</td><td>

Remove the **eval** function from the script.

</td><td>

[Documentation](https://developer.servicenow.com/dev.do%23!/guides/zurich/now-platform/tpb-guide/scripting_technical_best_practices)

</td></tr><tr><td>

sn\_SE10045

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

High Security Plugin should be enabled

</td><td>

Many security configurations will be unintentionally left open which in turn may open door for some of the critical vulnerabilities.

</td><td>

Activate the **High Security** plugin.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=high-security-plugin.html)

</td></tr><tr><td>

sn\_SE10046

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Contextual Security: Role Management V2 should be enabled

</td><td>

Removes duplicate records and helps visualize role inheritance.

</td><td>

Activate the Contextual Security: Role Management V2 plugin.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=Role-Mgmt-V2.html)

</td></tr><tr><td>

sn\_SE10074

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Scan Engine doesn't have access to read data from Applies To table

</td><td>

SE cannot identify any possible findings on these tables without read access.

</td><td>

Remove the Applies To Table record, grant read access on the table to the Scan Engine application, or modify the Table Applies To Table record by selecting Restricted Caller Access.

</td><td>

 

</td></tr><tr><td>

sn\_SE10083

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Scoped Certification: ACL required on client callable script includes

</td><td>

Users may gain access to data which they are not authorized to. Data inaccuracies could arise.

</td><td>

Create a new ACL with a type of Client Callable Script Include and set the name field to the Script Include name. Associate the appropriate roles to the ACL.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=acl-rule-types.html)

</td></tr><tr><td>

sn\_SE10085

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

The security manager default mode should be set to "deny".

</td><td>

Prevents users from unintentionally gaining access to data.

</td><td>

Set the value to "Deny".

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_DefaultDenyProperty.html)

</td></tr><tr><td>

sn\_SE10089

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Field set to Read Only through UI Policy without conditions

</td><td>

Unintended updates to the field could happen through list editing.

</td><td>

Check the read only flag on the **field\_\_\_**UICTRL\_0\_\_\_table\_name.**field\_name\_\_\_**UICTRL\_1\_\_\_t meet the criteria to edit the field.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ModifyADictionaryEntryFromAForm.html)

</td></tr><tr><td>

sn\_SE10090

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Field set to Mandatory through UI Policy without conditions

</td><td>

Required data could be empty that prevents the business process from continuing.

</td><td>

Check the mandatory flag on the field's dictionary record to make the field mandatory at all times.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateAUIPolicy.html)

</td></tr><tr><td>

sn\_SE10100

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

UI Pages should have an associated read ACL

</td><td>

Unauthorized users may have access to see data they wouldn't have access to through the backend.

</td><td>

Create a read ACL with an operation of read where the name of the ACL matches the name of the UI Page. Associate the appropriate roles to the read ACL of whom should have read access to the UI page.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=acl-rule-types.html)

</td></tr><tr><td>

sn\_SE10101

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Default admin account should be disabled

</td><td>

Unauthorized users may still gain access to the system, potentially leading to breaches of confidential data and data integrity issues. The resulting business impact could be significant and unrestricted.

</td><td>

Deactivate the admin account and remove any group and role association from the admin profile.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=change-default-credentials.html)

</td></tr><tr><td>

sn\_SE10146

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

HTML data input should be validated through the use of escaping

</td><td>

Injection attacks can occur causing security risks.

</td><td>

Either update the value of the **glide.ui.escape\_html\_list\_field** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=escape-html)

</td></tr><tr><td>

sn\_SE10147

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Jelly data input should be validated through the use of escaping

</td><td>

Injection attacks can occur causing security risks.

</td><td>

Either update the value of the **glide.ui.escape\_all\_script** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=escape-jelly.html)

</td></tr><tr><td>

sn\_SE10148

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

JavaScript data input should be validated through the use of escaping

</td><td>

Injection attacks can occur causing security risks.

</td><td>

Either update the value of the **glide.html.escape\_script** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=sc-escape-javascript.html)

</td></tr><tr><td>

sn\_SE10150

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Client-script queries should be validated

</td><td>

There is a potential for an attacker to perform unauthorized operations against the platform.

</td><td>

Either update the value of the **glide.script.use.sandbox** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_ScriptSandboxing.html)

</td></tr><tr><td>

sn\_SE10151

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Embedded HTML code should be disabled

</td><td>

Leveraged by attackers to steal session information and sensitive data.

</td><td>

Either update the value of the **glide.ui.security.allow\_codetag** system property to **false** OR insert this system property with a value of **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=allow-embedded-html-code.html)

</td></tr><tr><td>

sn\_SE10152

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

JavaScript tags in Embedded HTML should be disabled

</td><td>

Leveraged by attackers to steal session information and sensitive data.

</td><td>

Either update the value of the **glide.ui.security.codetag.allow\_script** system property to **false** OR insert this system property with a value of **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_HighSecuritySettings.html)

</td></tr><tr><td>

sn\_SE10153

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

AJAXEvaluate API should be disabled

</td><td>

AJAXEvaluate can allow arbitrary JavaScript to execute on the client browser by leveraging the server side objects

</td><td>

Either update the value of the **glide.script.allow.ajaxevaluate** system property to **false** OR insert this system property with a value of **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=enable-ajaxevaluate.html)

</td></tr><tr><td>

sn\_SE10154

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

HTMLSanitizer validation should be enabled

</td><td>

Client-side cross-site scripting attacks.

</td><td>

Either update the value of the **glide.html.sanitize\_all\_fields** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_HTMLSanitizer.html)

</td></tr><tr><td>

sn\_SE10155

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Strict security should be enabled for SOAP requests

</td><td>

Unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.soap.strict\_security** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=soap-request-strict-security.html)

</td></tr><tr><td>

sn\_SE10156

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Jelly interpolation should be enabled

</td><td>

JEXL injection can lead to both Cross Site Request Forgery and Code Execution

</td><td>

Either update the value of the **glide.ui.jelly.js\_interpolation.protect** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=jelly-js-interpolation.html)

</td></tr><tr><td>

sn\_SE10157

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Escaping Excel formulas should be enabled

</td><td>

Malicious formulae pose a risk even when the embedding spreadsheet doesn't contain any sensitive information, as they can be used to compromise the viewer's computer.

</td><td>

Either update the value of the **glide.export.escape\_formulas** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=escape-excel-formula.html)

</td></tr><tr><td>

sn\_SE10159

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Optional: Restrict Access to Specific IP Ranges

</td><td>

Unnecessary risk of exposure to the target instance on the internet

</td><td>

Activate the **IP Range Based Authentication** plugin if only certain IP addresses should have access to your instance.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=restrict-access-to-specific-ip-ranges.html)

</td></tr><tr><td>

sn\_SE10160

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Security Jump Start \(ACL rules\) plugin should be enabled

</td><td>

Access control should be enforced to lock down the unintended access to the instance. ACL jumpstart rules were written to provide a starting point on securing many system tables to make it easier for an organization to quickly get into production.

</td><td>

Activate the **Security Jump Start \(ACL Rules\)** plugin.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=security-jump-start-acl-rules.html)

</td></tr><tr><td>

sn\_SE10161

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Inbound transactions should be validated twice

</td><td>

Access request should always be checked when transactions happen between two zones.

</td><td>

Either update the value of the **glide.security.strict.updates** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=double-check-inbound-transactions.html)

</td></tr><tr><td>

sn\_SE10162

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

UI Action conditions should be validated before execution

</td><td>

Access request should always be checked when transactions happen between two zones.

</td><td>

Either update the value of the **glide.security.strict.actions** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=check-ui-action-conditions-before-execution.html)

</td></tr><tr><td>

sn\_SE10163

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Performance Monitoring ACL should be enabled

</td><td>

Sensitive data such as server details, threads and process that are being executed on the server should never be visible or accessible to the end user without appropriate privileges.

</td><td>

Either update the value of the **glide.security.diag\_txns\_acl** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=performance-monitoring-acl.html)

</td></tr><tr><td>

sn\_SE10165

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

AJAXGlideRecord ACL Checking should be enabled

</td><td>

Through client scripts, it is possible to query arbitrary data from the server through the GlideAjax API. Server-side resources can be accessed without proper authorization so validating the ACL helps the application validate the request based on the authorization configured.

</td><td>

Either update the value of the **glide.script.secure.ajaxgliderecord** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=enabling-ajaxgliderecord-acl-checking.html)

</td></tr><tr><td>

sn\_SE10166

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

SOAP Content Type Checking should be enabled

</td><td>

When accepting inbound SOAP requests, the appropriate validation has to be performed to ensure the relevant content type is being defined as a part of the request and thus restricting the invalid SOAP responses that can be viewed as a security risk.

</td><td>

Either update the value of the **glide.soap.require\_content\_type\_xml** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=soap-content-type-checking.html)

</td></tr><tr><td>

sn\_SE10167

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

SNC Access Control Plugin should be enabled

</td><td>

Unnecessary exposure of instance access to wider group of people.

</td><td>

Activate the **SNC Access Control** plugin by contacting &lt;ph keyref="var.company-no-reg-tm"/&gt; Customer Support.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=snc-access-control-plugin.html)

</td></tr><tr><td>

sn\_SE10168

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Optional: Strict IP restriction should be enabled.

</td><td>

Unnecessary exposure of instance access to wider group of people.

</td><td>

Either update the value of the **glide.ip.authenticate.strict** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=strict-ip-restriction.html)

</td></tr><tr><td>

sn\_SE10169

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Optional: Explicit Role Plugin should be enabled

</td><td>

External Users \(Non-employees\) will have access to many sensitive tables within ServiceNow which does not have any roles assigned to it and which are meant or designed to be accessible by internal users \(Employees\) only.

</td><td>

Activate the **Explicit Role** plugin by contacting &lt;ph keyref="var.company-no-reg-tm"/&gt; Customer Support.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=explicit-role-plugin.html)

</td></tr><tr><td>

sn\_SE10172

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

ACLs should be enabled for Live Profile Details

</td><td>

API requests should always honor table ACLs. Restriction needs to be applied to prevent unauthorized users accessing details of a Live Profile.

</td><td>

Either update the value of the **glide.live\_profile.details** system property to ACL OR insert this system property with a value of ACL.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=enable-acls-to-control-live-profile-details.html)

</td></tr><tr><td>

sn\_SE10173

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Client-Callable Script Includes should be private

</td><td>

Setting this property to "true" circumvents ACLs for client-side script includes and may result in unintended public functionality. This could have a potential security risk if the client script provides confidential information.

</td><td>

Either update the value of the **glide.script.ccsi.ispublic** system property to **false** OR insert this system property with a value of **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=sc-privacy-on-client-callable-script-includes.html)

</td></tr><tr><td>

sn\_SE10174

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

SMTP Authentication should be enabled

</td><td>

Authentication should always be performed before the transactions happen to/from to ServiceNow instance. SMTP authentication enables this requirement before sending the content to the external Mail server by authenticating to the target SMTP server.

</td><td>

Either update the value of the **glide.smtp.auth** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=smtp-authentication.html)

</td></tr><tr><td>

sn\_SE10175

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

WSDL Request Authorization should be enabled

</td><td>

Without appropriate authorization configured on the WSDL web services, an unauthorized user can get access to sensitive WSDL content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.wsdl** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=wsdl-request-authorization.html)

</td></tr><tr><td>

sn\_SE10176

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

CSV Request Authorization should be enabled

</td><td>

Without appropriate authorization configured on the incoming CSV requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.csv** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=csv-request-authorization.html)

</td></tr><tr><td>

sn\_SE10177

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Excel Request Authorization should be enabled

</td><td>

Without appropriate authorization configured on the incoming Excel requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.excel** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=excel-request-authorization.html)

</td></tr><tr><td>

sn\_SE10178

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Import Request Authorization should be enabled

</td><td>

Without appropriate authorization configured on the data source import requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.importprocessor** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=import-request-authorization.html)

</td></tr><tr><td>

sn\_SE10179

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

PDF Request Authorization should be enabled

</td><td>

Without appropriate authorization configured on the incoming PDF requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.pdf** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=pdf-request-authorization.html)

</td></tr><tr><td>

sn\_SE10180

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

RSS Request Authorization should be enabled

</td><td>

Without appropriate authorization configured on the incoming RSS requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.rss** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=rss-request-authorization.html)

</td></tr><tr><td>

sn\_SE10181

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Script Request Authorization should be enabled

</td><td>

High - Without appropriate authorization configured on the incoming Script requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.scriptedprocessor** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=script-request-authorization.html)

</td></tr><tr><td>

sn\_SE10182

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Basic Auth: SOAP Requests should be enabled

</td><td>

Without appropriate authorization configured on the data source SOAP requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.soap** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_SOAPWebService.html)

</td></tr><tr><td>

sn\_SE10183

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Basic Auth: JSONv2 Requests should be enabled

</td><td>

Without appropriate authorization configured on the data source JSON requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.jsonv2** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=access-control-instance-security-hardening.html)

</td></tr><tr><td>

sn\_SE10184

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Unload Request Authorization should be enabled

</td><td>

Without appropriate authorization configured on the data source unload requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.unl** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=unload-request-authorization.html)

</td></tr><tr><td>

sn\_SE10185

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

XML Request Authorization should be enabled

</td><td>

Without appropriate authorization configured on the incoming XML requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.xml** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=xml-request-authorization.html)

</td></tr><tr><td>

sn\_SE10186

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

XSD Request Authorization should be enabled

</td><td>

Without appropriate authorization configured on the incoming XSD requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td><td>

Either update the value of the **glide.basicauth.required.xsd** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=xsd-request-authorization.html)

</td></tr><tr><td>

sn\_SE10187

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Optional: SAML 2.0 Web Browser SSO Profile plugin should be enabled

</td><td>

Vulnerable to cross-site scripting attacks.

</td><td>

Activate the **Integration - Multiple Provider Single Sign-On Installer** plugin.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=sc-updated-version-of-multi-sso-plugin-is-enabled.html)

</td></tr><tr><td>

sn\_SE10188

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Remove Credentials From Welcome Page

</td><td>

Default credentials could be exposed.

</td><td>

The default content on the Welcome page should be changed to remove the default credentials.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=sc-remove-credentials-welcome-page.html)

</td></tr><tr><td>

sn\_SE10189

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Remember Me should be disabled

</td><td>

When the Remember me check box is selected at login, an additional cookie is stored on the user's computer to automatically re-establish the session for the logged-in user upon subsequent visits. This poses a security risk as it allows the user session to be active until they deliberately log out. The likelihood of an attack for such scenario would increase when end user has left the machine/browser unattended or if their browser is compromised from a different attack vector.

</td><td>

Either update the value of the **glide.ui.forgetme** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=remove-remember-me.html)

</td></tr><tr><td>

sn\_SE10190

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Password Field Autocomplete should be disabled

</td><td>

User authentication fields should be validated and should never let the client side caching to happen.

</td><td>

Either update the value of the **glide.login.autocomplete** system property to **false** OR insert this system property with a value of **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=password-field-autocomplete.html)

</td></tr><tr><td>

sn\_SE10191

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

ValidatePasswordStronger should be enabled

</td><td>

Weak password being enabled on the instance is a critical security risk due to ease of access and extremely high likelihood for an adversary to get access to the instance with the help of simple password guessing/brute-forcing techniques.

</td><td>

Activate the ValidatePasswordStronger installation exit.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=sc-enable-password-reset-policy-checks.html)

</td></tr><tr><td>

sn\_SE10192

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Disable Password-Less Authentication should be disabled

</td><td>

An attacker will be able to login to the instance with the default usernames, or by specific individual/group \(usually firstname.lastname\) without any password. This is viewed as a critical security risk, as it would enable a public user to violate confidentiality and integrity of the instance data.

</td><td>

Either update the value of the **glide.login.no\_blank\_password** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=disable-password-less-authentication.html)

</td></tr><tr><td>

sn\_SE10193

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Optional: Multi-Factor Authentication should be enabled

</td><td>

Increased risk of unauthorized access to sensitive data.

</td><td>

Either update the value of the **glide.authenticate.multifactor** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=multi-factor-authentication.html)

</td></tr><tr><td>

sn\_SE10194

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Download MIME Types should be populated

</td><td>

Client side scripting attack vectors come in different flavors and the attachments MIME type abuse is no exception. MIME types can be abused by attackers and render the unintended script content of the attachment on the victim's side and thus capture sensitive information. In the current context, the property should be populated with a list of comma-separated attachment mime types that should not render inline in the browser. Ex: text/html

</td><td>

Either update the value of the **glide.ui.attachment.download\_mime\_types** system property to trusted file types such as **text/csv,text/html,image/svg,image/svg+xml,application/xml, application/xhtml+xml** OR insert this system property with a value of the trusted file types.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=download-mime-types.html)

</td></tr><tr><td>

sn\_SE10195

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Force Download Attachments should be enabled

</td><td>

To reduce the client side scripting attacks, file attachments should be force downloaded as opposed to being rendered in the browser context.

</td><td>

Either update the value of the **glide.ui.attachment.force\_download\_all\_mime\_types** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=force-download-mime-types.html)

</td></tr><tr><td>

sn\_SE10197

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Downloadable File Types should be populated

</td><td>

File download restrictions should be applied to any untrusted user input sources.

</td><td>

Either update the value of the **glide.ui.strict\_customer\_uploaded\_content\_types** system property to the trusted file types OR insert this system property with a value of the trusted file types.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=specify-downloadable-file-types.html)

</td></tr><tr><td>

sn\_SE10198

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

File extensions should be restricted

</td><td>

As MIME type verification depends on this property, it is recommended to mitigate against the vulnerabilities related to malicious file upload.

</td><td>

Either update the value of the **glide.attachment.extensions** system property to the trusted file extensions OR insert this system property with a value of the trusted file extensions.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=restrict-file-extensions.html)

</td></tr><tr><td>

sn\_SE10199

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Upload MIME Type should be validated

</td><td>

To reduce vulnerabilities such as file inclusion and malicious file uploads, MIME type verification should be followed.

</td><td>

Either update the value of the **glide.security.file.mime\_type.validation** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=upload-mime-type-restriction.html)

</td></tr><tr><td>

sn\_SE10200

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Unauthenticated Access to Attachments should be restricted

</td><td>

Restriction needs to be applied for unauthenticated users as some attachment might contain sensitive information.

</td><td>

Either update the value of the **glide.image\_provider.security\_enabled** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=restrict-unauthenticated-access-to-attachments.html)

</td></tr><tr><td>

sn\_SE10201

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

HTTP Session Identifiers should be on rotation

</td><td>

SessionID is used to process and authenticate the instance user by maintaining the session state on the browser. Thus, SessionID is deemed sensitive data and should be secure by default. Session Rotation is a security control to enforce alteration of sessionID whenever the user navigates from un-authenticated page\(s\) to authenticate page\(s\).

</td><td>

Either update the value of the **glide.ui.rotate\_sessions** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=rotate-http-session-identifiers.html)

</td></tr><tr><td>

sn\_SE10202

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Secure Session Cookies should be enabled

</td><td>

Session cookies are sensitive data and should be properly formatted. It is always recommended to strictly validate the session cookie before serving the request.

</td><td>

Either update the value of the **glide.ui.secure\_cookies** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=secure-session-cookies.html)

</td></tr><tr><td>

sn\_SE10203

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Session Activity Timeout should be enabled

</td><td>

User sessions being active for indefinite amount of time is a security risk and should expire on a time-based configuration.

</td><td>

Either update the value of the **glide.ui.session\_timeout** system property to 60 OR insert this system property with a value of 60.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=session-activity-timeout.html)

</td></tr><tr><td>

sn\_SE10204

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Cookies HTTP Only should be enabled

</td><td>

Session Cookies on the application authenticate an end user and provide implicit access permissions on the application, and thus there is a need to secure them from being stolen or exported. HTTP Only flags would protect the session cookies from being stolen by JavaScript injections or Cross Site scripting vulnerabilities.

</td><td>

Either update the value of the **glide.cookies.http\_only** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=cookies-http-only.html)

</td></tr><tr><td>

sn\_SE10205

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Anti-CSRF Token should be enabled

</td><td>

Cross site Request Forgery is a significant security risk that violates the integrity of the instance data. An attacker can launch the CSRF attack on any instance user by abusing the application's trust on the instance user. With the help of social engineering attacks, a user can submit a malformed request on behalf of the attacker on the instance.

</td><td>

Either update the value of the **glide.security.use\_csrf\_token** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=anti-csrf-token.html)

</td></tr><tr><td>

sn\_SE10206

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Optional: CSRF Strict Validation should be enabled

</td><td>

Cross site Request Forgery is a significant security risk that violates the integrity of the instance data. An attacker can launch the CSRF attack on any instance user by abusing the application's trust on the instance user. With the help of social engineering attacks, a user can submit a malformed request on behalf of the attacker on the instance.

</td><td>

Either update the value of the **glide.security.csrf.strict.validation.mode** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=csrf-strict-validation.html)

</td></tr><tr><td>

sn\_SE10207

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Certificate Trust should be disabled

</td><td>

For confidentiality and integrity reasons, application should validate the certificate's CA before using the certificate for any transactional operations.

</td><td>

Either update the value of the **com.glide.communications.trustmanager\_trust\_all** system property to **false** OR insert this system property with a value of **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=certificate-trust.html)

</td></tr><tr><td>

sn\_SE10208

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

SSLv2/SSLv3 should be disabled

</td><td>

Due to a number of Client side attacks such as BEAST, SSL heart-bleed etc., legacy versions of SSL were proven to be insecure when utilized for HTTP secure shell implementation.

</td><td>

Either update the value of the **glide.outbound.sslv3.disabled** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=disabling-sslv2-sslv3.html)

</td></tr><tr><td>

sn\_SE10209

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Relative Links should be enforced

</td><td>

Absolute URLs can pose a security risk when being used as a part of parameter or a field value, and thus redirecting the source page to an adversary controlled website.

</td><td>

Either update the value of the **glide.cms.catalog\_uri\_relative** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=enforce-relative-links.html)

</td></tr><tr><td>

sn\_SE10210

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

X-Frame-Options: SAMEORIGIN should be enabled

</td><td>

"Same Origin policy" allows to restrict a domain from retrieving a script or a resource from another domains. All modern browsers support this functionality. The policy validates the connection based on protocol, port and host. CORS \(Cross Origin Request\) is a slight modification to "Same Origin Policy" that allows access to resources/scripts from another domain when explicitly stated as a part of header value. In the current case, X-Frame-Options header controls whether or not ServiceNow application can be rendered on the 3rd party website, and thus to reduce sensitive exposure the property value when set to "SAMEORIGIN" doesn't allow the rendering to happen.

</td><td>

Either update the value of the **glide.set\_x\_frame\_options** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=x-frame-options-sameorigin.html)

</td></tr><tr><td>

sn\_SE10211

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Managing Failed Login Attempts should be configured

</td><td>

A logging and auditing strategy should be applied so that suspicious activity can be identified and acted upon in a timely manner.

</td><td>

Activate the SNC User related Script Actions.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=sc-managing-failed-login-attempts.html)

</td></tr><tr><td>

sn\_SE10212

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

SQL error message rendering should be disabled

</td><td>

No sensitive SQL information should be allowed to display as a part of error message on a webpage that could help an attacker.

</td><td>

Either update the value of the **glide.db.loguser** system property to **false** OR delete this system property.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=disabling-sql-error-messages.html)

</td></tr><tr><td>

sn\_SE10213

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Mobile UI Obfuscation should be enabled

</td><td>

A compromised \(jailbroken\) device would allow an attacker to have full access to the file system and thus will be able to access those files/snapshots with sensitive information embedded in them .

</td><td>

Either update the value of the **glide.ui.m.blur\_ui\_when\_backgrounded** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=mobile-ui-obfuscation.html)

</td></tr><tr><td>

sn\_SE10214

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

URL Allow list For Logout Redirects

</td><td>

Client side open redirection can enable attacker to redirect victims/users to attacker controlled website and is viewed as a security risk.

</td><td>

Either update the value of the **glide.security.url.whitelist** system property to include whitelisted URLs OR insert this system property with a value of the whitelisted URLs.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=url-whitelist-for-logout-redirects.html)

</td></tr><tr><td>

sn\_SE10215

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Optional: Entity Validation should be disabled

</td><td>

An attacker can leverage this to expand data exponentially, quickly consuming all system resources.

</td><td>

Either update the value of the **glide.stax.allow\_entity\_resolution** system property to **false** OR insert this system property with a value of **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=disable-entity-expansion.html)

</td></tr><tr><td>

sn\_SE10216

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Email Domain restrictions should be configured

</td><td>

If the property is not enabled, an attacker might using email spoofing/spamming campaign to send number of emails that might end up creating more number of unnecessary guest users.

</td><td>

Either update the value of the **glide.user.trusted\_domain** system property to include trusted domains OR insert this system property with a value of the trusted domains.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=restrict-emails-by-domain.html)

</td></tr><tr><td>

sn\_SE10237

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Unaffiliated credentials should be removed

</td><td>

Unused credentials could be used to spoof accounts in hacking attempts

</td><td>

Either apply the credential, or delete the unused record.

</td><td>

[Documentation](https://community.servicenow.com/community?id=community_blog&sys_id=4efc26a5dbd0dbc01dcaf3231f96191a)

</td></tr><tr><td>

sn\_SE10248

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Cross Scope Privileges in requested status should be reviewed

</td><td>

Possibility for bugs in the application resulting in inaccurate data and/or poor user experience.

</td><td>

Review the Cross Scope Privilege record to determine whether to allow or deny the operation requested.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_CrossScopePrivilegeRecord.html)

</td></tr><tr><td>

sn\_SE10266

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Default password should not be set to "password"

</td><td>

Unnecessary security risk of an attacker gaining access to the system.

</td><td>

Update the value of the **glide.user.default\_password** property to have a more complex password include lower case letters, upper case letters, a number, and a special character.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_InboundMailConfiguration.html)

</td></tr><tr><td>

sn\_SE10277

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Enforce Strict User Image Upload

</td><td>

When this property is set to false, ACLs are not enforced on image uploads to the Photo field and open the possibility of an unauthorized user uploading an image to another user's profile.

</td><td>

Set the "**glide.security.strict.user\_image\_upload**" system property to **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=sc-enforce-strict-user-image-upload.html)

</td></tr><tr><td>

sn\_SE10278

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Restrict Access to Emails with Empty Target Table

</td><td>

Users may have access to view unintended emails.

</td><td>

Set the "**glide.email.email\_with\_no\_target\_visible\_to\_all**" system property to **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=restrict-access-to-emails-with-empty-target-table.html)

</td></tr><tr><td>

sn\_SE10279

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Entity Expansion Threshold should be set to 3000.

</td><td>

An attacker can leverage this to expand data exponentially, quickly consuming all system resources.

</td><td>

The **glide.xmlutil.max\_entity\_expansion** **system\_property** should have a minimum value of 3000.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=setting-entity-expansion-threshold.html)

</td></tr><tr><td>

sn\_SE10280

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Email Spam Scoring and Filtering plugin should be enabled

</td><td>

Email filters enable administrators to specify when to move email to particular mailboxes or to ignore it using a condition builder or a condition script. The is particularly useful while receiving malicious email from known/unknown sender.

</td><td>

Activate the Email Spam Scoring and Filtering \(**com.\_\_\_PARM\_0\_\_\_**\) plugin.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=email-spam-scoring-and-filtering)

</td></tr><tr><td>

sn\_SE10281

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

XML External Entity Processing - Whitelist should be configured

</td><td>

An attacker can use the DTD may include arbitrary HTTP requests that the server may execute.

</td><td>

Set the value to the list of URLs that can be accessed by XML Entity processing. This is used to allow access to a list of comma-delimited FQDN, if needed. These will be the only URLs that can be reached via XML Entity processing. Note : An Entity SYSTEM ID must start with either "http:" or "https:" or it will automatically be blocked. When the allow list is enabled the PUBLIC form of an external entity definition is required.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=xml-external-entity-processing-whitelist.html)

</td></tr><tr><td>

sn\_SE10282

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Entity expansion should be disabled

</td><td>

An attacker can leverage this to expand data exponentially, quickly consuming all system resources resulting in a Billion Laugh attack.

</td><td>

Ensure the property "**glide.xml.entity.whitelist**" is set to "http://java.sun.com/j2ee/dtds/" and the property "**glide.xml.entity.whitelist.enabled**" is set to "**true**".

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=disable-entity-expansion.html)

</td></tr><tr><td>

sn\_SE10284

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Openframe origin validation should be enabled

</td><td>

Without proper origin validation, any webpage or script can control the event handler.

</td><td>

Set the value to **true** to enable origin checking. Once this property is set to **true**, any allow-listed domains will need to be added to the **glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist** system property.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=enable-url-whitelist-for-cross-origin-iframe-communication.html)

</td></tr><tr><td>

sn\_SE10285

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Set a maximum cap for user sessions to expire

</td><td>

User sessions being active for indefinite amount of time is a security risk and should expire on a time-based configuration.

</td><td>

Set the **glide.ui.user\_cookie.max\_life\_span\_in\_days** system property to 30.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=absolute-session-timeout.html)

</td></tr><tr><td>

sn\_SE10287

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

The default Cache-Control value should be set to Private

</td><td>

Instances with CDN/proxies may cache static content and render without authentication.

</td><td>

Set the **glide.http.cache\_control** system property to private.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=cache-control-http-header-value.html)

</td></tr><tr><td>

sn\_SE10295

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Reports should typically not be made public

</td><td>

Unauthenticated users may see classified data.

</td><td>

Share reports through Roles, Users, and/or Groups rather than have them be accessible by any user. To make a report available only to logged-in users, set its Sharing setting to Everyone, but do not publish it. List reports are excluded from this definition as they always apply table-level security \(ACLs\).

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_PublishAReport.html)

</td></tr><tr><td>

sn\_SE10314

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Domain Separated: Users with cross-domain visibility

</td><td>

Users can be exposed to the data of another domain.

</td><td>

Instead of using "visibility domains" it is best to use "contains domains" for more robust control.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_DomainVisibility.html)

</td></tr><tr><td>

sn\_SE10432

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Portal pages should typically not be made public

</td><td>

Unauthenticated users may see classified data.

</td><td>

Set the Public field to **false** and ensure access is limited to the required audience only.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=portal-security.html)

</td></tr><tr><td>

sn\_SE10433

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Review public UI Pages

</td><td>

Unauthenticated users may see classified data.

</td><td>

Set the Active field to **false** and ensure access is limited to the required audience only.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_MakeAPagePublic.html)

</td></tr><tr><td>

sn\_SE10434

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

HR Lifecycle Event: Altering the "Assignable by" field

</td><td>

Changes to the "Assignable by" field on these HR Roles can pose a security risk as it could allow inexperienced or malicious users to access classified HR data.

</td><td>

Ensure that these HR Roles are only "Assignable by" the **sn\_hr\_le**.admin or **sn\_hr\_le**.**activity\_set\_manager** role. Reverting these records to baseline will resolve these Findings.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_ManageRoles.html)

</td></tr><tr><td>

sn\_SE10435

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

HR Core: Altering the "Assignable by" field

</td><td>

Changes to the "Assignable by" field can pose a security risk as it could allow inexperienced or malicious users to access classified HR data.

</td><td>

Ensure that the "Assignable by" field on these records is set as provided when this plugin was activated. Reverting these records to baseline would resolve these Findings.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_ManageRoles.html)

</td></tr><tr><td>

sn\_SE10436

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Planned Start and End Dates for Change records should be protected through ACLs

</td><td>

Users can update the Planned Start and End Date fields from the list view if there are not ACLs protecting these fields. Changed dates may cause confusion among different users.

</td><td>

Create an ACL rather than a UI Policy to secure the Planned Start and End Date fields.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateAnACLRule.html)

</td></tr><tr><td>

sn\_SE10437

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Mobile devices should restrict copy/paste

</td><td>

A compromised \(jailbroken\) device would allow an attacker to have full access to the clipboard and thus will be able to access the sensitive information embedded within the clipboard.

</td><td>

Set the property "**glide.sg.clear\_pasteboard\_when\_backgrounded**" to **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-copy-paste.html)

</td></tr><tr><td>

sn\_SE10438

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Default value of the user lockout duration should be 1440 minutes

</td><td>

Setting this property to a shorter value may allow hackers to resume their attacks after just a short time.

</td><td>

Set the value of the property "**password\_reset**.request.**max\_attempt\_window**" to 1440 \(in minutes\).

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=password-reset-global-properties.html)

</td></tr><tr><td>

sn\_SE10439

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Optional: Automatic User Creation should be enabled

</td><td>

Users outside of your organization can create incident records.

</td><td>

Set the property "**glide.pop3readerjob.create\_caller**" to **false**. When **false**, the instance will run inbound actions from users who do not match an existing user by impersonating the guest user. Review your existing user records to reconcile any that contain identical email addresses. If you activate the plugin prior to reconciling email addresses, your instance cannot distinguish between users with identical email addresses and randomly selects one of the users with the matching email address.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_EnablingAutomaticUserCreation.html)

</td></tr><tr><td>

sn\_SE10440

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Google re-CAPTCHA on the self-registration page should be enabled

</td><td>

Increased spam through the self-registration page.

</td><td>

Set the property "**sn\_ext\_usr\_reg**.captchaEnabled" to **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=communities-properties.html)

</td></tr><tr><td>

sn\_SE10441

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Antivirus Protection Scanning should be enabled

</td><td>

Increased threat of virus infections from file attachments.

</td><td>

Set the property "**com.\_\_\_PARM\_0\_\_\_**" to **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-antivirus-protection.html)

</td></tr><tr><td>

sn\_SE10442

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

System property "glide.pop3.process\_locked\_out" should not be enabled

</td><td>

Allows locked-out or untrusted users to reset their password and send emails to the instance

</td><td>

Set the property "**glide.pop3.process\_locked\_out**" to **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_AllowLockedUsersInbdEmailAct.html)

</td></tr><tr><td>

sn\_SE10443

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Increased number of unsuccessful password reset attempts

</td><td>

Setting this property to a greater value may allow hackers multiple attempts to log in.

</td><td>

Set the value of the property "**password\_reset**.request.**max\_attempt**" to 3 password attempts.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=sc-reset-password-request-max-attempts.html)

</td></tr><tr><td>

sn\_SE10444

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Integration accounts assigned the Admin role

</td><td>

Integration accounts with administrative access serve as potential security threats.

</td><td>

Ensure that Integration account users are not assigned the admin role. Alternative approaches would be to grant access to the actual tables and records needed. Import Admin is also sufficient to process Import Sets. Care should be taken to not implement scheduled jobs using the admin role.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_MarkSvcAcctsAsInternalIntegUsers.html)

</td></tr><tr><td>

sn\_SE10446

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

PA breakdown visibility to roles

</td><td>

Users may view data that is not relevant to them.

</td><td>

Unselect "Visible by all roles" and select the specific roles that are required to access the breakdown.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreatingABreakdownForIndicators.html)

</td></tr><tr><td>

sn\_SE10447

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Remove the Campaign Admin role from IT System Administrator role

</td><td>

IT System Administrators could view sensitive HR data.

</td><td>

As an Admin user, navigate to the **sys\_user\_role\_contains** table, then select the "admin" role record. From the "Contains Roles" related list, remove **sn\_ca**.**campaign\_admin**. Ensure that you have at least two users with that role already.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_HRRemoveAdminRole.html)

</td></tr><tr><td>

sn\_SE10448

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Remove the Content Delivery Admin role from IT System Administrator role

</td><td>

IT System Administrators could view sensitive HR data.

</td><td>

As an Admin user, navigate to the **sys\_user\_role\_contains** table, then select the "admin" role record. From the "Contains Roles" related list, remove **sn\_cd**.**content\_admin**. Ensure that you have at least two users with that role already.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_HRRemoveAdminRole.html)

</td></tr><tr><td>

sn\_SE10449

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Remove the Employee Document Management Admin role from IT System Administrator role

</td><td>

IT System Administrators could view sensitive HR data.

</td><td>

As an Admin user, navigate to the **sys\_user\_role\_contains** table, then select the "admin" role record. From the "Contains Roles" related list, remove **sn\_hr\_ef**.admin. Ensure that you have at least two users with that role already.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_HRRemoveAdminRole.html)

</td></tr><tr><td>

sn\_SE10450

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

App PINs for the mobile app should be enabled

</td><td>

Any user could access the mobile application when PINs aren't required.

</td><td>

Set the property "**glide.sg.require\_mobile\_application\_pin**" to **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=require-app-pin.html)

</td></tr><tr><td>

sn\_SE10452

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Service Portal resources should define roles to restrict access

</td><td>

A breach of data could take place if access control using Roles is not correctly configured on Service Portal Pages and Widgets.

</td><td>

For Service Portal resources that are not public, there should be a list of roles configured to restrict access. Only pages and widgets that do not require access control should be public or have no roles defined.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-page-security.html)

</td></tr><tr><td>

sn\_SE10455

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Record Producers should have defined roles to restrict access

</td><td>

Record Producers are viewable by all users, no matter their roles.

</td><td>

Either set the system property "**glide.sc.use\_user\_criteria**" to **true** or navigate to the Accessibility tab within a Record Producer and ensure roles are defined.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_DefRecProdInSCat.html)

</td></tr><tr><td>

sn\_SE10457

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

The maximum number of recipients listed on a single email notification should be limited to 100

</td><td>

Duplicated email notifications will be created to address those who exceed the 100 recipient limit.

</td><td>

Set the property "**glide.email.smtp.max\_recipients**" to a value less than or equal to 100.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=sc-max-smtp-recipients.html)

</td></tr><tr><td>

sn\_SE10460

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Users with Alumni in their HR profile still marked as active

</td><td>

Users who have left the company may still have access to the instance.

</td><td>

Deactivate the user account of the users with the "**sn\_hr\_core**.**hrsm\_alumni**" role assigned.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_HRProfileRecords.html)

</td></tr><tr><td>

sn\_SE10461

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Web service access only users should not have elevated access

</td><td>

May serve as a potential point of compromise if elevated access is provided to such users.

</td><td>

Remove elevated access roles from the web service access only user.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_NonInteractiveSessions.html)

</td></tr><tr><td>

sn\_SE10462

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Access controls on Tables

</td><td>

Without access controls, any user would be able to access tables they should not have access to.

</td><td>

Elevate to the Security Admin role, then navigate to System Security &gt; Access Control and create a new ACL.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=acl-rule-types.html)

</td></tr><tr><td>

sn\_SE10463

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Remove the HR core admin and LE Admin roles from the Admin role

</td><td>

Only users with the HR Administrator \[sn\_hr\_core.admin\] and LE Administrator \[sn\_hr\_le.admin\] have access to the HR data with sensitive information.

</td><td>

After system configuration, remove the HR Administrator role from the Admin role to prevent admins from viewing sensitive HR information. This will ensure that only the HR Administrator \[**sn\_hr\_core**.admin\] has access to the sensitive information.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_HRRemoveAdminRole.html)

</td></tr><tr><td>

sn\_SE10466

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Unintentional Cross Scope privileges

</td><td>

Peventing unauthorized access to scope application

</td><td>

Investigate each Cross Scope privilege and identify whether this is really needed as part of the application. If not, remove the privilege and regression test to ensure that behavior is as expected.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_CrossScopePrivilegeRecord.html)

</td></tr><tr><td>

sn\_SE10468

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

External users should not have access to the sys\_audit table.

</td><td>

External users can access system audit table and view potentially confidential data.

</td><td>

System tables usually are not needed to be accessed by all internal and external users and can be restricted to the groups needed.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=access-control-rules.html)

</td></tr><tr><td>

sn\_SE10469

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Do not deactivate or delete the "Assign HR Roles" business rule

</td><td>

The BR will prevent security issues by automatically granting or removing access to HR portal based on employment type and start/end date.

</td><td>

Set the business rule "Assign HR Roles" to Active.

</td><td>

/api/now/v1/context\_doc\_url/CSHelp:client-role-assignment-rules

</td></tr><tr><td>

sn\_SE10470

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Grant the HR Administrator with Delegated Developer for HR Scope Application

</td><td>

To prevent unintended access to HR sensitive information of IT System Adminstrator by assigning delegated developer to HR Core scope.

</td><td>

Assign a Delegated Developer role to the HR Core Scope.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_HRAdminRoles.html)

</td></tr><tr><td>

sn\_SE10471

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

HR Tables not excluded from cloning on Production

</td><td>

HR data with sensitive information could be cloned down into sub-production instances.

</td><td>

Create exclusions for HR tables in your production instance.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ExcludeATableFromCloning.html)

</td></tr><tr><td>

sn\_SE10472

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Not using the appropriate user account for Vulnerability integrations

</td><td>

Using an inappropriate user account may lead to security vulnerabilities.

</td><td>

Use the VR System account as the RunAs user for scheduled script executions and scheduled data imports.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_MarkSvcAcctsAsInternalIntegUsers.html)

</td></tr><tr><td>

sn\_SE10473

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Number of users with high privilege roles

</td><td>

Having more than 10 users with high-privilege roles increases the chance of a security leak.

</td><td>

Make sure that all high-privilege roles do not have more than 10 users assigned.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_ElevatedPrivilege.html)

</td></tr><tr><td>

sn\_SE10474

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Report shared with a role that does not exist

</td><td>

Reports shared with a role that does not exist might lead to unforeseen behavior.

</td><td>

Remove the invalid role by editing the report, then share the report with valid roles.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ShareASetting.html)

</td></tr><tr><td>

sn\_SE10475

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Use the dedicated integration user to run actions in place of the default

</td><td>

Authentication is required for all SOAP requests including internal integration when WS-Security is enabled. Communication requests may be blocked when a MID Server or ODBC Driver user account user is not set as an internal integration user.

</td><td>

Check the **internal\_integration\_user** field for the MID Server or ODBC Driver user account.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_MarkSvcAcctsAsInternalIntegUsers.html)

</td></tr><tr><td>

sn\_SE10476

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

System Audit table access for all external users

</td><td>

Users may have unnecessary access to system tables.

</td><td>

System tables usually are not needed to be accessed by all internal and external users and can be restricted to the groups needed.

</td><td>

[Documentation](https://docs.servicenow.com/csh?topicname=access-control-rules.html)

</td></tr><tr><td>

sn\_SE10478

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Remove the Security Incident Admin Role from the Admin role

</td><td>

Only users with the Security Incident Admin role should have access to Security Incident data with sensitive information.

</td><td>

After system configuration, remove the Security Incident Administrator role from the Admin role to prevent admins from viewing sensitive Security Incident information. This will ensure that only the Security Incident Administrator \[**sn\_si**.admin\] has access to the sensitive information.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ConfigureSIM.html)

</td></tr><tr><td>

sn\_SE10479

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Use RCA to secure HR Core

</td><td>

Server-side queries may be run against HR data or tables to access sensitive information.

</td><td>

It is recommended to utilize the Restricted Caller Access \(ID: **com.\_\_\_PARM\_0\_\_\_**\) plugin when using the Human Resources Core Application \(ID:**com.sn\_hr\_core**\).

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=hr-security.html)

</td></tr><tr><td>

sn\_SE10480

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Baseline CISO Role has write access

</td><td>

Senior leadership users who not require write access to Security Incident records would be able to edit such records.

</td><td>

Discuss whether or not senior leadership users actually require the ability to edit / write to Security Incident records. Consider de-coupling the "**sn\_si**.basic" role from "**sn\_si**.ciso" if senior leadership does not require write / edit permissions on Security Incident records.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=installed-with-sir.html)

</td></tr><tr><td>

sn\_SE10483

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Security Incident assignment groups are missing a type attribute

</td><td>

The users in these groups would not be able to have any security incidents assigned to them.

</td><td>

Groups that currently have role "**sn\_si**.analyst" assigned to them should have the Type attribute defined as "Security Incident".

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=setup-assistant-reference.html)

</td></tr><tr><td>

sn\_SE10491

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

API calls to Security Incident Response should use accounts with the "sn\_si.integration\_user" role

</td><td>

Using an inappropriate user account may lead to security vulnerabilities.

</td><td>

Consider adding the "**sn\_si**.**integration\_user**" role to each user account accessing the Security Incident \[**sn\_si\_incident**\] table via API.

</td><td>

/api/now/v1/context\_doc\_url/CSHelp:components-installed-sir

</td></tr><tr><td>

sn\_SE10492

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Enable Report ACL

</td><td>

If Report View ACLs are left disabled, users may have access to report data that they should not.

</td><td>

Report View ACLs provide control over who can view reports protected by the Report View ACL.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=report-view-acl-dashboard.html)

</td></tr><tr><td>

sn\_SE10493

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Multiple encryption keys in existence

</td><td>

Older keys might be removed, and the record information will be encrypted with no possibility to decrypt.

</td><td>

Rotate and encrypt new keys to ensure that no old records exist with old keys.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_EncryptionKeyRotation.html)

</td></tr><tr><td>

sn\_SE10494

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Knowledge Base and articles are public

</td><td>

All users would have access to knowledge bases and articles

</td><td>

Make sure to define user criteria for Knowledge Base and articles.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=select-user-criteria-for-knowledge-block.html)

</td></tr><tr><td>

sn\_SE10522

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Scripted REST resource without enabled security

</td><td>

Making your APIs public is not suggested because doing so allows the public access to update data in the instance.

</td><td>

To require authorization, select the **Requires Authentication** checkbox and then select the **Requires ACL authorization** check box. Finally select an ACL record\(s\). Leave the **ACL** field blank to enforce the **Default ACLs** from the parent API. Access is granted if at least one matching ACL record is found.

</td><td>

[Documentation](https://docs.servicenow.com/csh?topicname=t_WbSvcRqACL.html)

</td></tr><tr><td>

sn\_SE10523

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Enable IP Range Based Authentication

</td><td>

Unauthorized users may be able to access your instance.

</td><td>

-   Activate the IP Range Based Authentication **com.snc.ipauthenticator** plugin, if it is not already activated.
-   Use IP Address Access Control to setup Deny or Allow record entries with the appropriate IP Address ranges.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=restrict-access-to-specific-ip-ranges.html)

</td></tr><tr><td>

sn\_SE10534

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Tracked Configuration Files may be exposing passwords, API tokens, and secret keys

</td><td>

Users with the itil role may have unathenticated access to passwords, API tokens, and secret keys.

</td><td>

Review the tracked config files by navigating to the **cmdb\_ci\_config\_file\_tracked** table and confirming that secure information is present. Either control access to this table through ACL's or reimplement your applications to make use of password vault applications so that no secure credential information is stored in clear text.

</td><td>

[Documentation](https://snprotips.com/blog/2023/3-ways-to-check-your-servicenow-instance-for-dangerous-code-in-less-than-5-minutes)

</td></tr><tr><td>

sn\_SE10541

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

ACL defined without role, script, and condition

</td><td>

Your data could potentially be exposed as the default behavior when role , security attrubute , script, and conditions are empty is to allow unauthenticated access.

</td><td>

Review the ACL and add the appropriate roles, security attributes, conditions, or scripting. If the ACL should remain as is, at a minimum, add the following to the ACL script to ensure only authenticated users may access the data: answer = **gs.getSession\(\)**.**isLoggedIn**;.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1553688)

</td></tr><tr><td>

sn\_SE10585

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Potential Misconfiguration of Knowledge Base User Criteria

</td><td>

Users may receive unintended and unauthenticated access to your KB articles.

</td><td>

Create the system property **glide.knowman.block\_access\_with\_no\_user\_criteria** and set the value to **true**.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123580)

</td></tr><tr><td>

sn\_SE10594

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Block access to non-public Knowledge Bases for unauthenticated users

</td><td>

Potential loss of confidential or PII information

</td><td>

Either update the value of the **glide.knowman.block\_access\_with\_no\_user\_criteria** system property to **true** OR insert this system property with a value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=sc-restrict-knowledge-bases-access.html)

</td></tr><tr><td>

sn\_SE10639

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Any users encapsulated within a KB's 'Can Contribute' list have the ability to read all of the KB's

</td><td>

Users may receive unintended and unauthenticated access to your KB articles.

</td><td>

Create the system property **glide.knowman.apply\_article\_read\_criteria** and set the value to **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=user-access-knowledge.html)

</td></tr><tr><td>

sn\_SE10640

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Defines a list of roles that can view KB articles that are in a 'Draft State'

</td><td>

Users may receive unintended and unauthenticated access to your KB articles.

</td><td>

Create the system property **glide.knowman.section.view\_roles.draft** and set the value to **admin, knowledge\_admin**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_KnowledgeProperties.html)

</td></tr><tr><td>

sn\_SE10641

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

All users within the defined roles have the ability to view articles that exist in a custom state.

</td><td>

Users may receive unintended and unauthenticated access to your KB articles.

</td><td>

Create the system property **glide.knowman.section.view\_roles.stagesAndRoles** and set the value to **admin, knowledge\_admin**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_KnowledgeProperties.html)

</td></tr><tr><td>

sn\_SE10642

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Show unpublished articles

</td><td>

Users may view KB articles that are not yet published.

</td><td>

Create the system property **glide.knowman.show\_unpublished** and set the value to **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_KnowledgeProperties.html)

</td></tr><tr><td>

sn\_SE10643

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

The ACL checks user authentication and references a system property to allow or deny access based on

</td><td>

Allowing unauthenticated access could expose the organization to data breaches, regulatory non-compliance, and security risks.

</td><td>

Ensure the **glide.security.allow\_unauth\_roleless\_acl** system property is set to **false** to prevent unauthenticated access.

</td><td>

[Documentation](https://appomni.com/ao-labs/a-technical-analysis-and-lessons-from-the-recent-service-now-misconfiguration-risks/)

</td></tr><tr><td>

sn\_SE10644

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Defines a list of roles that can view KB articles that are in a 'Review' state

</td><td>

Users may receive unintended and unauthenticated access to your KB articles.

</td><td>

Create the system property **glide.knowman.section.view\_roles.review** and set the value to **admin,knowledge\_admin,knowledge,itil**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_KnowledgeProperties.html)

</td></tr><tr><td>

sn\_SE10645

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Inactive OOB Business Rule\(s\) to Prevent Unauthenticated Access By Default

</td><td>

Users may receive unintended and unauthenticated access to your KB articles.

</td><td>

Search for business rule **Restrict guest user to knowledge base** with SysId **6c8ec5147711111016f35c207b5a9969** and set active field to **true**.

</td><td>

[Documentation](https://appomni.com/ao-labs/servicenow-knowledge-bases-data-exposures-uncovered/)

</td></tr></tbody>
</table>