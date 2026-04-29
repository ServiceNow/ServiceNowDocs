---
title: Updated hardening settings for baseline version 7.0
description: Some hardening settings have been updated with the release of Security Center baseline version 7.0.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 31
breadcrumb: [Updated hardening settings, Baseline versions, Hardening settings, Platform Security]
---

# Updated hardening settings for baseline version 7.0

Some hardening settings have been updated with the release of Security Center baseline version 7.0.

<table id="table_um1_qnp_xgc"><thead><tr><th>

Documentation

</th><th>

Updates

</th></tr></thead><tbody><tr><td>

[Enable relay state in SAML requests to prevent replay attacks](../reference/sc-enable-relay-state-in-saml-requests-to-prevent-replay-attacks.md)

</td><td>

-   Description:
    -   \(Old\) When "glide.authenticate.sso.saml2.enable\_relay\_state\_with\_id" is set to "true", the relay state parameter will contain the sys id of a record in the table multisso\_request\_parameter which the relay state url to redirect to. This relay state protects against SAML Replay attacks which could be possible in some ServiceNow instance versions if the property glide.authenticate.sso.saml2.enable\_relay\_state\_with\_id is set to false. Replay attacks allow a well-positioned attacker who has gained access to the SAML request to resubmit a valid request in orger to gain unauthorized access to the platform.
    -   \(New\) Protect against SAML replay attacks using the glide.authenticate.sso.saml2.enable\_relay\_state\_with\_id system property. When this property is set to true, the relay state parameter contains the sys\_id of a record in the MultiSSO Request Parameters \[multisso\_request\_parameter\] table, which the relay state URL redirects to.

Set the system property glide.authenticate.sso.saml2.enable\_relay\_state\_with\_id to true. This helps prevent attackers who have gained access to a SAML request from accessing your instance by resubmitting a valid request.

The relay state enabled by this system property helps protect your instance against replay attacks. Enabling the property helps prevent attackers who have gained access to a SAML request from accessing your instance by resubmitting a valid request.

-   Remediation:
    -   \(Old\) Set the property glide.authenticate.sso.saml2.enable\_relay\_state\_with\_id to true.
    -   \(New\) Set the property glide.authenticate.sso.saml2.enable\_relay\_state\_with\_id to true. If the property does not exist in the System Properties \[sys\_properties\] table, the default value is false.
-   security risk:
    -   \(Old\) This relay state protects against SAML Replay attacks which could be possible in some ServiceNow instance versions if the property glide.authenticate.sso.saml2.enable\_relay\_state\_with\_id is set to false. Replay attacks allow a well-positioned attacker who has gained access to the SAML request to resubmit a valid request in orger to gain unauthorized access to the platform.
    -   \(New\) The relay state enabled by this system property helps protect your instance against replay attacks. Enabling the property helps prevent attackers who have gained access to a SAML request from accessing your instance by resubmitting a valid request.
-   Functional Impact:
    -   \(Old\) When this property is set to true, relay state in the SAML request will contain sys id of the record in the table multisso\_request\_parameter which contains relay state url to redirect to.
    -   \(New\) When this property is set to true, the relay state in a SAML request contains the sys\_id of a record in the MultiSSO Request Parameters \[multisso\_request\_parameter\] table, which contains relay state URL to redirect to.

</td></tr><tr><td>

[Disable local login for users with Single Sign-On \(SSO\) enabled](../reference/sc-disable-local-login-for-users-with-single-sign-on-sso-enabled.md)

</td><td>

-   Technical Configuration Name
    -   \(Old\) &lt;blank&gt;
    -   \(New\) glide.sso.acr.enabled,glide.authenticate.multisso.enabled
-   Description
    -   \(Old\)

ServiceNow instance owners are responsible for provisioning user accounts for their instance and ensuring that users can access the instance in expected ways. When a user, that is not locked out, has a valid password hash on the "sys\_user.user\_password" field, that user can perform local database authentication for both interactive and non-interactive access types. If a user is also configured to use SSO authentication, local database authentication can still occur without additional controls in place. That is, SSO users with valid local credentials may access the instance, or parts of the instance, with those local credentials.

When SSO authentication is enabled for a user, it is best practice to prevent that user from logging in locally. This reduces the chance that the valid local login credentials are stolen and used to login by a malicious user.

    -   \(New\)

Users configured to use SSO authentication may be able to access the instance, or parts of the instance, with local credentials stored in the user\_password field of their User \[sys\_user\] record. This access applies to both interactive and non-interactive access for users who aren't locked out. Help prevent SSO-configured users from using local credentials to reduce the chance that valid local login credentials are stolen and used by malicious users.

Review Now Support Knowledge Base article KB1649420 for instructions on identifying and addressing accounts with local login still enabled on an instance with SSO enabled.

-   CVSS score
    -   \(Old\) 5.9
    -   \(New\) 4.2

</td></tr><tr><td>

[Disable legacy JQuery UI usage](../reference/sc-disable-legacy-jquery-ui-usage.md)

</td><td>

Fallback Value

 -   \(Old\) true
-   \(New\) false

</td></tr><tr><td>

[Enforce application specific ACLs only for application data](../reference/sc-enforce-application-specific-acls-only-for-application-data.md)

</td><td>

-   Description
    -   \(Old\)

Properties in the format 'glide.enforce\_security\_scope.' property, such as 'glide.enforce\_security\_scope.sn\_hr\_core', control the behavior of application data residing in primary tables outside the application, such as 'sys\_attachment' or 'sys\_email'. When properties in the format have a value of 'true', only the application specific ACLs are evaluated for access to the application data residing in these tables. When the properties do not have a value of 'true', the ACLs on the primary table will still be evaluated for access, potentially allowing unauthorized or undesired access to application data. Not all applications are designed to work in this configuration or ship a 'sys\_properties' record for this purpose.

The following application scopes contain this property:

        -   sn\_uni\_task
        -   sn\_uni\_req
        -   sn\_svc\_appl\_info
        -   sn\_professional
        -   sn\_opp\_market
        -   sn\_lg\_ops
        -   sn\_lg\_matter
        -   sn\_lg\_contracts
        -   sn\_jny
        -   sn\_ja
        -   sn\_imt\_vaccine
        -   sn\_imt\_tracing
        -   sn\_imt\_health\_test
        -   sn\_hr\_ws
        -   sn\_hr\_va
        -   sn\_hr\_sp
        -   sn\_hr\_pj
        -   sn\_hr\_pad
        -   sn\_hr\_mii\_base
        -   sn\_hr\_le
        -   sn\_hr\_hc
        -   sn\_hr\_gen\_ai
        -   sn\_hr\_er
        -   sn\_hr\_ef
        -   sn\_hr\_core
        -   sn\_hr\_awa
        -   sn\_hr\_agent\_ws
        -   sn\_hc\_professional
        -   sn\_gsm\_soc\_bnfts
        -   sn\_gsm\_lic\_prmt\_ex
        -   sn\_gsm\_lic\_prmt
        -   sn\_gsm\_info\_req
        -   sn\_gsm
        -   sn\_em
        -   sn\_egd\_goals
        -   sn\_egd\_core
        -   sn\_egd\_act
        -   sn\_doc
    -   \(New\)

Control the behavior of application data residing in primary tables outside the application. When these properties have a primary value of true, only the application-specific ACLs are evaluated for access to the application data residing in these tables. Not all applications are designed to work in this configuration or use a System Property \[sys\_properties\] record for this purpose.

These system properties use the glide.enforce\_security\_scope. naming format. For example, use the glide.enforce\_security\_scope.sn\_hr\_sp property for the Employee Center Core \(sn\_hr\_sp\) scope. The following application scopes contain this property:

        -   sn\_doc
        -   sn\_egd\_act
        -   sn\_egd\_core
        -   sn\_egd\_goals
        -   sn\_em
        -   sn\_gsm
        -   sn\_gsm\_info\_req
        -   sn\_gsm\_lic\_prmt
        -   sn\_gsm\_lic\_prmt\_ex
        -   sn\_gsm\_soc\_bnfts
        -   sn\_hc\_professional
        -   sn\_hr\_agent\_ws
        -   sn\_hr\_ai\_agents
        -   sn\_hr\_awa
        -   sn\_hr\_core
        -   sn\_hr\_ef
        -   sn\_hr\_er
        -   sn\_hr\_gen\_ai
        -   sn\_hr\_hc
        -   sn\_hr\_le
        -   sn\_hr\_le\_ent
        -   sn\_hr\_mii\_base
        -   sn\_hr\_na\_galileo
        -   sn\_hr\_pad
        -   sn\_hr\_pj
        -   sn\_hr\_sp
        -   sn\_hr\_va
        -   sn\_hr\_ws
        -   sn\_imt\_health\_test
        -   sn\_imt\_tracing
        -   sn\_imt\_vaccine
        -   sn\_ja
        -   sn\_jny
        -   sn\_lg\_contracts
        -   sn\_lg\_matter
        -   sn\_lg\_ops
        -   sn\_opp\_market
        -   sn\_professional
        -   sn\_svc\_appl\_info
        -   sn\_svc\_appl\_pgm\_mg
        -   sn\_talent\_aia
        -   sn\_uni\_req
        -   sn\_uni\_task
When the properties do not have a value of 'true', the ACLs on the primary table will still be evaluated for access, potentially allowing unauthorized or undesired access to application data.

-   Remediation
    -   \(Old\)

For any applications installed with the 'glide.enforce\_security\_scope.' property, such as 'glide.enforce\_security\_scope.sn\_hr\_core', in the 'sys\_properties' table, ensure the property value is set to 'true'. These properties can only be modified by the scoped administrator for the specific application.

    -   \(New\)

For each application installed with the glide.enforce\_security\_scope property in the System Properties \[sys\_properties\] table, \(for example, glide.enforce\_security\_scope.sn\_hr\_core\), ensure the property value is set to true.

These properties can only be modified by the scoped administrator for the specific application. If a sys\_properties record does not exist for the given application and respective property, it must be created.

Use this script can to find which properties need to be updated or created on the instance:

        ```
var properties = [
    'glide.enforce_security_scope.sn_uni_task',
    'glide.enforce_security_scope.sn_uni_req',
    'glide.enforce_security_scope.sn_svc_appl_info',
    'glide.enforce_security_scope.sn_professional',
    'glide.enforce_security_scope.sn_opp_market',
    'glide.enforce_security_scope.sn_lg_ops',
    'glide.enforce_security_scope.sn_lg_matter',
    'glide.enforce_security_scope.sn_lg_contracts',
    'glide.enforce_security_scope.sn_jny',
    'glide.enforce_security_scope.sn_ja',
    'glide.enforce_security_scope.sn_imt_vaccine',
    'glide.enforce_security_scope.sn_imt_tracing',
    'glide.enforce_security_scope.sn_imt_health_test',
    'glide.enforce_security_scope.sn_hr_ws',
    'glide.enforce_security_scope.sn_hr_va',
    'glide.enforce_security_scope.sn_hr_sp',
    'glide.enforce_security_scope.sn_hr_pj',
    'glide.enforce_security_scope.sn_hr_pad',
    'glide.enforce_security_scope.sn_hr_mii_base',
    'glide.enforce_security_scope.sn_hr_le',
    'glide.enforce_security_scope.sn_hr_le_ent',
    'glide.enforce_security_scope.sn_hr_hc',
    'glide.enforce_security_scope.sn_hr_gen_ai',
    'glide.enforce_security_scope.sn_hr_er',
    'glide.enforce_security_scope.sn_hr_ef',
    'glide.enforce_security_scope.sn_hr_core',
    'glide.enforce_security_scope.sn_hr_awa',
    'glide.enforce_security_scope.sn_hr_agent_ws',
    'glide.enforce_security_scope.sn_hc_professional',
    'glide.enforce_security_scope.sn_gsm_soc_bnfts',
    'glide.enforce_security_scope.sn_gsm_lic_prmt_ex',
    'glide.enforce_security_scope.sn_gsm_lic_prmt',
    'glide.enforce_security_scope.sn_gsm_info_req',
    'glide.enforce_security_scope.sn_gsm',
    'glide.enforce_security_scope.sn_em',
    'glide.enforce_security_scope.sn_egd_goals',
    'glide.enforce_security_scope.sn_egd_core',
    'glide.enforce_security_scope.sn_egd_act',
    'glide.enforce_security_scope.sn_doc',
    'glide.enforce_security_scope.sn_talent_aia',
    'glide.enforce_security_scope.sn_hr_na_galileo',
    'glide.enforce_security_scope.sn_svc_appl_pgm_mg',
    'glide.enforce_security_scope.sn_hr_ai_agents',
    'glide.enforce_security_scope.sn_hr_mii_base'
];

var pm = new GlidePluginManager();

for (var i = 0; i < properties.length; i++) {
    var property = properties[i];
    var application = property.split('.')[2];
    var propertyValue = gs.getProperty(property, 'false');

    if (pm.isActive(application) && propertyValue.toLowerCase() != 'true') {
        gs.print(property);
    }
}

        ```

-   CVSS score
    -   \(Old\) 5.5
    -   \(New\) 4.1

</td></tr><tr><td>

[Prevent impersonating user from viewing application data](../reference/sc-prevent-impersonating-user-from-viewing-application-data.md)

</td><td>

-   Description
    -   \(Old\)

Properties in the format '.impersonateCheck', such as 'sn\_hr\_core.impersonateCheck', control how an impersonating user can access specific application data belonging to another user. When properties in this form are set to 'true', an admin level user impersonating another user will not be able to access the application specific data belonging to that user. Not all applications are designed to work in this configuration or ship a 'sys\_properties' record for this purpose.

A value of "false" for these properties allows an admin level user to impersonate another user and access application data with the impersonated user's access. This may be undesirable or allow for unauthorized data access in specific application contexts.

The following scopes contain this property:

        -   sn\_opp\_market
        -   sn\_jny
        -   sn\_imt\_vaccine
        -   sn\_imt\_health\_test
        -   sn\_hr\_core
        -   sn\_egd\_goals
        -   sn\_egd\_core
        -   sn\_egd\_act
    -   \(New\)

Use system properties to prevent an impersonating user from viewing application data.

Prevent admin level from accessing the application specific data belonging to that user when impersonating an account. This permission can be set at the application level by creating a system property specific to the application.

These system properties use the .impersonateCheck naming format \(for example sn\_hr\_core.impersonateCheck\). Create a system property with a value of true to prevent users from accessing the application-specific data belonging to another user when impersonating an account.

NOTE: Not all applications are designed to work in this configuration or have a System Properties \[sys\_properties\] record for this purpose. The following scopes are configured to work with this property.

        -   sn\_opp\_market
        -   sn\_jny
        -   sn\_imt\_vaccine
        -   sn\_imt\_health\_test
        -   sn\_hr\_core
        -   sn\_egd\_goals
        -   sn\_egd\_core
        -   sn\_egd\_act
        -   sn\_em
        -   sn\_talent\_aia
-   Remediation
    -   \(Old\)

For any application with the '.impersonateCheck' property, such as 'sn\_hr\_core.impersonateCheck', in the 'sys\_properties' table, ensure the property value is set to 'true'. These properties can only be modified by the scoped administrator for the specific application.

    -   \(New\)

For each application with the .impersonateCheck property in the System Properties \[sys\_properties\] table, ensure the property value is set to true.

These properties can only be modified by the scoped administrator for the specific application.

Use this script to find which properties need to be updated or created on the instance:

        ```
var properties = [
    'sn_opp_market.impersonateCheck',
    'sn_jny.impersonateCheck',
    'sn_imt_vaccine.impersonateCheck',
    'sn_imt_health_test.impersonateCheck',
    'sn_hr_core.impersonateCheck',
    'sn_egd_goals.impersonateCheck',
    'sn_egd_core.impersonateCheck',
    'sn_egd_act.impersonateCheck',
'sn_em.impersonateCheck',
'sn_talent_aia.impersonateCheck'
];

var pm = new GlidePluginManager();

for (var i = 0; i < properties.length; i++) {
    var property = properties[i];
    var application = property.split('.')[0];
    var propertyValue = gs.getProperty(property, 'false');

    if (pm.isActive(application) && propertyValue.toLowerCase() != 'true') {
        gs.print(property);
    }
}

        ```

-   CVSS score
    -   \(Old\) 4.4
    -   \(New\) 3.8

</td></tr><tr><td>

[Escape JavaScript \[Updated in Security Center 1.3\]](../reference/sc-escape-javascript.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

The property "glide.html.escape\_script" helps sanitize HTML fields. If "glide.html.escape\_script" is not set to the recommended value of "true", then inputs will not be sanitized for HTML fields \(output encoding\) from a backend Java context by removing embedded JavaScript. Javascript in HTML fields can lead to stored and reflected XSS.

-   security risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\) The ability to have XSS can lead to easily attained privilege escalation to higher roles such as admin.

</td></tr><tr><td>

[Enable HTML Sanitizer \[Updated in Security Center 1.3\]](../reference/sc-html-sanitizer.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property controls sanitization behavior of HTML fields on a global level from a backend Java context. If "glide.html.sanitize\_all\_fields" is not set to the recommended value of "true", then, the ServiceNow instance is open to XSS in HTML fields.

-   security risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\) The ability to have XSS can lead to easily attained privilege escalation to higher roles such as admin.

</td></tr><tr><td>

[Escape jelly script \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-escape-jelly.md)

</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property escapes all the JS and HTML strings included in &lt;j:jelly&gt; ... &lt;/j:jelly&gt; before they are written to the output stream, preventing several XSS issues from occurring. If "glide.ui.escape\_all\_script" is not set to the recommended value of "true", then escaping of scripts injected into Jelly is disabled.

-   security risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Without this mitigation, the platform becomes widely open to a variety of script injection attacks. An attacker could execute arbitrary Rhino scripts on the instance.


</td></tr><tr><td>



</td><td>

-   Description
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This property enables the "script sandbox" feature. The script sandbox is mainly utilized when executing client-generated scripts \(such as query conditions and GlideAjax expressions\). If "glide.script.use.sandbox" is not set to the recommended value of "true", then the script sandbox feature will be disabled.

-   security risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Without the script sandbox, unauthorized/unauthenticated users can execute arbitrary privileged script on a ServiceNow instance. This would lead to complete security impact across all areas, including, but not limited to potentially malicious access to all data on the ServiceNow instance.


</td></tr><tr><td>

[Disallow target cloning \[New in Security Center 1.3\]](../reference/sc-disallow-target-cloning.md)

</td><td>

-   Description
    -   \(Old\)

If glide.db.clone.allow\_clone\_target is not set to the recommended value of false, then the instance can be used as a clone target, or a record that specifies the instance URL and credentials used for cloning. A system clone is when everything in a database is copied from one instance to another. This is a security risk because the instance database can be overwritten in the cloning process, leading to data loss and lack of data integrity. As a remediation, ensure that glide.db.clone.allow\_clone\_target is set to false.

    -   \(New\)

Protect your instance from being used as a clone target by setting the glide.db.clone.allow\_clone\_target system property to false. A system clone copies everything in a database from a source instance to the target instance. This is a security risk because the instance database on the target instance is overwritten in the cloning process, leading to data loss and lack of data integrity.

-   Remediation
    -   \(Old\)

Ensure the property "glide.db.clone.allow\_clone\_target" is set to "false".

    -   \(New\)

Set the glide.db.clone.allow\_clone\_target system property to false on production instances to disallow your instance from being selected as a clone target.

-   CVSS score
    -   \(Old\) 5.9
    -   \(New\) 4.4
-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Boolean
-   Out of box value
    -   \(Old\) &lt;blank&gt;
    -   \(New\) true

</td></tr><tr><td>

[Deny internal access to explicit external roles \[Updated in Security Center 1.3 and 1.5\]](../../security/reference/sc-enable-explicit-roles-internal-denylist.md)

</td><td>

-   Description
    -   \(New\)

Use system properties to determine whether external users can be assigned the snc\_internal role.

Use the glide.security.explicit\_roles.enable\_internal\_user\_blacklist system property to prevent external users from being assigned the snc\_internal role. When this property is set to true, it enforces the parameters of the maint-protected glide.security.explicit\_roles.internal\_user\_blacklist property. This property assigns the snc\_external role to a list of untrusted user classes. If glide.security.explicit\_roles.enable\_internal\_user\_blacklist is set to false, the glide.security.explicit\_roles.internal\_user\_blacklist property is ignored.

    -   \(Old\) This property prevents external users from being assigned the snc\_internal role. When "glide.security.explicit\_roles.enable\_internal\_user\_blacklist" is set to the recommended value of "true", then it enforces the parameters of the maint-protected "glide.security.explicit\_roles.internal\_user\_blacklist" property which assigns the 'snc\_external' role to a list of untrusted user classes. If the value is set to false, the "glide.security.explicit\_roles.internal\_user\_blacklist" property is ignored. Misconfiguration of this property increases the risk that an external user account gains access to internal information.
-   Plugin applicability
    -   \(New\)

Explicit Roles Plugin, Customer Service Base Extension Entities

    -   \(Old\) Explicit Roles Plugin
-   security risk
    -   \(New\)

Misconfiguration of this property increases the risk that an external user account gains access to internal information.

    -   \(Old\) &lt;blank&gt;
-   Data type
    -   \(New\) Boolean
    -   \(Old\) &lt;blank&gt;
-   Out of box value
    -   \(New\) true
    -   \(Old\) &lt;blank&gt;
-   Fallback value
    -   \(New\) false
    -   \(Old\) true

</td></tr><tr><td>

[Restrict oauth parameters to POST body \[New in Security Center 1.3\]](../reference/sc-restrict-oauth-parameters-to-post-body.md)

</td><td>

-   Description
    -   \(Old\)

This property controls the inbound OAuth authentication's acceptance of access tokens. Access tokens are sensitive and should only be accepted when located within a POST request body.

    -   \(New\)

Use the glide.oauth.allow.parameters.in.post.body.only property to control the inbound OAuth authentication's acceptance of access tokens. Access tokens are sensitive and should only be accepted when located within a POST request body.

-   Remediation
    -   \(Old\)

Ensure the property "glide.oauth.allow.parameters.in.post.body.only" is set to "true".

    -   \(New\)

Ensure the property "glide.oauth.allow.parameters.in.post.body.only" is set to "true". If the property does not exist in the "sys\_properties" table, the default is "false".

-   Plugin applicability
    -   \(Old\) &lt;blank&gt;
    -   \(New\) OAuth 2.0
-   security risk
    -   \(Old\)

If "glide.oauth.allow.parameters.in.post.body.only" is not set to the recommended value of "true", then access tokens could be present in the GET request parameter which could linger in client and infrastructure logs and potentially lead to account takeover if those logs are leaked.

    -   \(New\)

If glide.oauth.allow.parameters.in.post.body.only isn't set to the recommended value of true, access tokens could be present in the GET request parameter. These access tokens could linger in client and infrastructure logs and potentially lead to account takeover if those logs are leaked.

-   Dependencies and prerequisites
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Plugin OAuth 2.0
-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Boolean
-   Out of box value
    -   \(Old\) &lt;blank&gt;
    -   \(New\) true

</td></tr><tr><td>

[Enforce GroupBy ACLs](../reference/sc-enforce-groupby-acls.md)

</td><td>

-   Description
    -   \(Old\)

If "glide.security.groupby\_acl\_check" is not set to the recommended value of "True", then make sure that a table has "groupby\_acl\_check" attribute set in order to honor groupby ACLs. In other case there will be no ACLs check on groupby columns of a table. This could lead to information disclosure.

    -   \(New\)

Use the glide.security.groupby\_acl\_check system property to configure your instance to conduct ACL checks on groupby columns. If this property is set to the recommended value of true, then ACLs on groupby columns are honored by default. A table's groupby\_acl\_check attribute takes precedent over the glide.security.groupby\_acl\_check property. If the property is set to false, then ensure that any table which should have ACL checks on groupby columns has the groupby\_acl\_check attribute set to true.

-   security risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

If "glide.security.groupby\_acl\_check" is set to false and there is no "groupby\_acl\_check" attribute on the individual table, then ACLs on groupby columns will not be honored which could lead to information leakage.

-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

ACLs on groupby columns will be enforced by default for tables.

-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Boolean
-   Out of box value
    -   \(Old\) &lt;blank&gt;
    -   \(New\) true

</td></tr><tr><td>

[Require XMLdoc2 entity validation with allowlist](../reference/sc-xmldoc2-entity-validation-with-entity-expansion.md)

</td><td>

-   Description
    -   \(Old\)

If the Glide Property "glide.stax.whitelist\_enabled" does not exist in the sys\_properties table or is not set to the recommended value of "true", then all external entities are allowed when the Glide Property "glide.stax.allow\_entity\_resolution" is set to the value of "true". If customizations do not require entity expansion, use the "glide.stax.allow\_entity\_resolution" property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.

        -   If you set "glide.stax.allow\_entity\_resolution" to true, all external entities attempt to resolve or expand subject entities, subject to the setting of the "glide.stax.whitelist\_enabled" property.
        -   If you set "glide.stax.allow\_entity\_resolution" to false, all entity resolution and expansion is blocked. To learn more about this property, see https://www.servicenow.com/docs/csh?topicname=sc-disable-entity-expansion.html&amp;version=latest.
When "glide.stax.whitelist\_enabled" is set to true, define a listing of comma-delimited FQDN in the "glide.xml.entity.whitelist" property, which is the only URLs that can be reached using XML Entity processing property. To learn more, see https://www.servicenow.com/docs/csh?topicname=sc-xml-entity-validation-url-allowlist.html&amp;version=latest.

    -   \(New\)

If the Glide Property "glide.stax.whitelist\_enabled" does not exist in the sys\_properties table or is not set to the recommended value of "true", then all external entities are allowed when the Glide Property "glide.stax.allow\_entity\_resolution" is set to the value of "true".

If customizations do not require entity expansion, use the "glide.stax.allow\_entity\_resolution" property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.

        -   If you set "glide.stax.allow\_entity\_resolution" to true, all external entities attempt to resolve or expand subject entities, subject to the setting of the "glide.stax.whitelist\_enabled" property.
        -   If you set "glide.stax.allow\_entity\_resolution" to false, all entity resolution and expansion is blocked. To learn more about this property, see https://www.servicenow.com/docs/csh?topicname=sc-disable-entity-expansion.html&amp;version=latest.
When "glide.stax.whitelist\_enabled" is set to true, define a listing of comma-delimited FQDN in the "glide.xml.entity.whitelist" property, which is the only URLs that can be reached using XML Entity processing property. To learn more, see https://www.servicenow.com/docs/csh?topicname=sc-xml-entity-validation-url-allowlist.html&amp;version=latest.

-   Remediation
    -   \(Old\)

Ensure the property "glide.stax.whitelist\_enabled" is set to "true".

    -   \(New\)

Ensure the property "glide.stax.whitelist\_enabled" is set to "true" when the Glide Property "glide.stax.allow\_entity\_resolution" is set to the value of "true".


</td></tr><tr><td>

[Define restricted downloadable MIME types \[Updated in Security Center 1.3, 1.5, and 2.0\]](../reference/sc-downloadable-mime-types.md)

</td><td>

-   Description
    -   \(Old\)

If "glide.ui.attachment.download\_mime\_types" does include dangerous items such as "text/html,image/svg,image/svg+xml,application/xml", then dangerous files could be rendered inline in the browser which could lead to Cross Sitte Scripting attacks \(XSS\). This property is the list of comma separated attachment mime types which will not render inline in the browser. For example, including text/html will force HTML files to be downloaded to the client as attachments rather than viewed inline in the browser. Maintaining this list properly will prevent cross site scripting attacks.

    -   \(New\)

If glide.ui.attachment.download\_mime\_types does include dangerous MIME types such as text/html, image/svg ,image/svg+xml,application/xml, then dangerous files could be rendered inline in the browser, which could lead to Cross Site Scripting attacks \(XSS\). This property is the list of comma-separated attachment mime types, which won't render inline in the browser. For example, including text/html forces HTML files to be downloaded to the client as attachments rather than viewed inline in the browser. Maintaining this list properly prevents cross-site scripting attacks.

If the glide.ui.attachment.download\_mime\_types system property doesn't include dangerous MIME types such as "text/html, image/svg,image/svg+xml,application/xml", then dangerous files could be rendered inline in the browser. This can lead to Cross Site Scripting \(XSS\) attacks. This check is only relevant when glide.ui.attachment.force\_download\_all\_mime\_types is set to false.

This property is a list of comma-separated attachment MIME types, which don't render inline in the browser. For example, including text/html forces HTML files to be downloaded to the client as attachments rather than viewed inline in the browser.

-   Remediation
    -   \(Old\)

If glide.ui.attachment.force\_download\_all\_mime\_types is set to false, verify that the glide.ui.attachment.download\_mime\_types system property includes the dangerous MIME types "text/html,image/svg,image/svg+xml,application/xml".

    -   \(New\)

Ensure the property "glide.ui.attachment.download\_mime\_types" includes the dangerous items "text/html,image/svg,image/svg+xml,application/xml".

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Maintaining this list properly can prevent cross site scripting attacks.

-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

Attachments with the MIME type listed in this property cannot be viewed inline in the browser.

-   Dependencies and prerequisites
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

This check is only relevant when glide.ui.attachment.force\_download\_all\_mime\_types is set to false or does not exist in the System Properties \[sys\_properties\] table.

-   Data Type
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Comma separated list of MIME types
-   Out of box value
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

text/html,image/svg,image/svg+xml,application/xml


</td></tr><tr><td>

[Escape HTML in list views \[Updated in Security Center 1.3 and 1.5\]](../reference/sc-escape-html.md)

</td><td>

-   Description
    -   \(Old\)

This property helps sanitize list view displaying of HTML fields. If "glide.ui.escape\_html\_list\_field" is not set to the recommended value of "true", then a malicious user can inject HTML code within the form field to execute unwanted scripts on different client/user sessions. This could potentially be leveraged by attackers to steal session information and sensitive data.

    -   \(New\)

Set glide.ui.escape\_html\_list\_field to true to prevent HTML from being rendered in HTML fields in list view. Leaving HTML sanitization inactive platform wide \(via system property\) or by field \(via a schema attribute\), may lead to XSS style attacks. XSS attacks may allow a low privileged user to hijack the session of a high privileged user or interfere in standard web application behaviors, including redirects or defacement.

-   CVSS score
    -   \(Old\) 8.8
    -   \(New\) 3.1
-   Security risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

When HTML sanitization is disabled platform wide \(via Glide Properties\) or per field \(schema attribute\), this may lead to XSS style attacks if low privileged users have access to write to an HTML field. XSS attacks may allow a low privileged user to hijack the session of a high privileged user or interfere in standard web application behaviors \(redirects or defacement\).

-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\)

By default, HTML can be rendered \(and is sanitized\) in form view. This same behavior may be desired in list view, in which case setting this property to "false" may be the preferred experience. There will be minimal security impact as long as HTML sanitizaiton is not disabled platform wide or on the field.

-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Boolean
-   Out of box value
    -   \(Old\) &lt;blank&gt;
    -   \(New\) true

</td></tr><tr><td>

[Minimize reset password max SMS per day](../reference/sc-reset-password-max-sms-per-day.md)

</td><td>

-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Integer
-   Out of box value
    -   \(Old\) &lt;blank&gt;
    -   \(New\) 10
-   Fallback value
    -   \(Old\) 10
    -   \(New\) 5

</td></tr><tr><td>

[Disallow infected file download](../reference/sc-disallow-infected-files-download.md)

</td><td>

Out of box value

 -   \(Old\) &lt;blank&gt;
-   \(New\) true

</td></tr><tr><td>

[Restrict unauthenticated access to attachments](../reference/sc-restrict-unauthenticated-access-attachments.md)

</td><td>

Description

 -   \(Old\)

Description \(Old\): If "glide.image\_provider.security\_enabled" is not set to the recommended value of "True", then all images are accessible via urls that end in ".iix". This would allow unauthenticated access to images leading to sensitive information leak. This property is not honored for the images from attachment table where origin table is \[sysevent\_email\_style, sys\_home, sys\_properties\]. Restriction should be applied for unauthenticated users as some attachments might contain sensitive information.

-   \(New\)

Secure the images on your instance to prevent sensitive information leak. Images on your instance are accessible via urls that end in `.iix`.

Set the **glide.image\_provider.security\_enabled** system property to **true** to prevent access to your images via these URLs.

**Note:**

This property is not honored for images from the attachment table if the origin table is one of:

    -   Stationeries \[sysevent\_email\_style\]
    -   Welcome Page Sections \[sys\_home\]
    -   System Properties \[sys\_properties\]
Restriction should be applied for unauthenticated users as some attachments might contain sensitive information.


</td></tr><tr><td>

[Activate role based multi-factor authentication](../reference/sc-role-based-multi-factor-authentication.md)

</td><td>

CVSS Score

 -   \(Old\) 8.8
-   \(New\) 3.1

</td></tr><tr><td>

[Maximize failed login unlock timeout duration \[Updated in Security Center 1.3\]](../reference/sc-managing-unlock-timeout-after-failed-logins.md)

</td><td>

-   Description
    -   \(Old\)

If "glide.user.unlock\_timeout\_in\_mins" is not set to the recommended value of "15", then it may be easier to brute force accounts in a faster timeframe. This property unlocks the user account after the time period that is specified for the glide.user.unlock\_timeout\_in\_mins property. If no value is specified, then the system unlocks the user account after the default period of 15 minutes.

If the property is not configured to a secure value and the lockout duration is not enabled, then it may be easier to brute force account logins in a faster timeframe. This may allow a malicious user to eventually obtain unauthorized access to the instance. Impact on the instance will be limited to the privileged of the affected user login brute-forced.

    -   \(New\)

If "glide.user.unlock\_timeout\_in\_mins" is not set to at least the minimum value of "15", then it may be easier to brute force accounts in a faster timeframe. This property unlocks the user account after the time period that is specified for the glide.user.unlock\_timeout\_in\_mins property. If no value is specified, then the system unlocks the user account after the default period of 15 minutes.

If the property is not configured to a secure value and the lockout duration is not enabled, then it may be easier to brute force account logins in a faster timeframe. This may allow a malicious user to eventually obtain unauthorized access to the instance. Impact on the instance will be limited to the privileged of the affected user login brute-forced.

-   Remediation
    -   Set the glide.user.unlock\_timeout\_in\_mins system property value to a minimum of 15. If glide.user.unlock\_timeout\_in\_mins does not exist, the default lockout time is set to 15 minutes.

Ensure that the SNC User Lockout Check with Auto Unlock script action \(found on the Script Action \[sysevent\_script\_action\] table\) is present and active. The SNC User Lockout Check with Auto Unlock script action is installed with the High Security Settings \(com.glide.high\_security\) plugin.

Ensure the property "glide.user.unlock\_timeout\_in\_mins" is set to "15" or more and that the Script Action \(sysevent\_script\_action\) "SNC User Lockout Check with Auto Unlock" is present and active. If the Glide Property "glide.user.unlock\_timeout\_in\_mins" does not exist, it will default to a secure value of "15".

The "SNC User Lockout Check with Auto Unlock" is installed with the High Security Plugin.

    -   \(New\) 10

</td></tr><tr><td>

[Maximize failed login unlock timeout duration \[Updated in Security Center 1.3\]](../reference/sc-managing-unlock-timeout-after-failed-logins.md)

</td><td>

Remediation

 -   \(Old\)

Ensure at least one of the script actions: "SNC User Lockout Check" or "SNC User Lockout Check with Auto Unlock" are enabled to manage failed login attempts. Additionally, ensure the property "glide.user.max\_unlock\_attempts" is set to "5" or less.

-   \(New\)

Ensure at least one of the script actions: "SNC User Lockout Check" or "SNC User Lockout Check with Auto Unlock" are enabled to manage failed login attempts. These script actions are stored in the "sysevent\_script\_action" table.

Additionally, ensure the property "glide.user.max\_unlock\_attempts" is set to "5" or less.


</td></tr><tr><td>

[Set OTP lifetime for password reset to 1 hour \[Updated in Security Center 2.0\]](../reference/sc-set-otp-lifetime-for-password-reset-to-12-hours-or-less.md)

</td><td>

-   Short Description
    -   \(Old\) Set OTP Lifetime for Password Reset to 12 Hours or Less
    -   \(New\) Set OTP lifetime for password reset to 1 hour
-   Description
    -   \(Old\)

This property "glide.pwd\_reset.onetime.token.validity" allows the link in the password reset email to expire after the number of hours specified in that "glide.pwd\_reset.onetime.token.validity" property. Validity time of password reset token should be keeped as short as possible in according of normal user experience. Have long validity time for password reset token can help malicious actors to perform account takeover.

    -   \(New\)

Control the time duration of the link in the password reset email.

The property glide.pwd\_reset.onetime.token.validity makes the link in the password reset email expire after the number of hours specified in the property. The validity time of a password reset token should be kept as short as possible while not disrupting normal user experience. A longer validity time for password reset token gives malicious actors a wider window to perform account takeover if the email with the reset token is leaked or otherwise compromised.

-   Remediation
    -   \(Old\) Set the property value to 12 hours or a shorter validity time.
    -   \(New\) Set the property value to 1 \(in hours\)
-   CVSS
    -   \(Old\) 5.6
    -   \(New\) 4.6
-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\) A longer validity time for password reset token gives malicious actors a wider window to perform account takeover if the email with the reset token is leaked or compromised.
-   Functional Impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\) A user must reset their password within the number of hours specified in this property. Otherwise they will need to request a new link.
-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Integer representing number of hours
-   Out of box value
    -   \(Old\) &lt;blank&gt;
    -   \(New\) 1
-   Fallback value
    -   \(Old\) 12
    -   \(New\) 1

</td></tr><tr><td>

[Minimize Concurrent Interactive Sessions with Limit Concurrent Sessions Plugin](../reference/sc-glide-authenticate-limit-concurrent-interactive-sessions.md)

</td><td>

-   Short Description
    -   \(Old\) Limit Concurrent Interactive Sessions
    -   \(New\) Limit Concurrent Interactive Sessions When Limit Concurrent Sessions Plugin Is Installed
-   Plugin Applicability
    -   \(Old\) &lt;blank&gt;
    -   \(New\) com.glide.limit.concurrent.sessions

</td></tr><tr><td>

[Limit maximum number of attachments in email](../reference/sc-limit-maximum-number-of-attachments-in-email.md)

</td><td>

-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Integer
-   Out of box value
    -   \(Old\) &lt;blank&gt;
    -   \(New\) 30
-   Fallback value
    -   \(Old\) 30
    -   \(New\) 50

</td></tr><tr><td>

[Enable protected tables plugin](../reference/sc-enable-protected-tables-plugin.md)

</td><td>

-   Description
    -   \(Old\)

When the Glide Property 'com.glide.security.protected\_table.enabled' is set to 'true', The Protected Tables plugin will be utilized to prevent higher privilege users on an instance from tampering with log tables. The following logging tables will have special protections when this property is set to 'true':

        -   syslog \(config not modifiable\)
        -   syslog\_transaction
        -   sys\_outbound\_http\_log
        -   sysevent
        -   sys\_audit
        -   sys\_push\_notification
        -   protected\_table\_configuration \(config not modifiable\)
    -   \(New\)

When the Glide Property 'com.glide.security.protected\_table.enabled' is set to 'true', The Protected Tables plugin will be utilized to prevent higher privilege users on an instance from tampering with log tables. The following logging tables will have special protections when this property is set to 'true':

        -   syslog \(config not modifiable\)
        -   syslog\_transaction
        -   sys\_outbound\_http\_log
        -   sysevent
        -   sys\_audit
        -   sys\_push\_notification
        -   protected\_table\_configuration \(config not modifiable\)
        -   syslog\_app\_scope
The integrity of logs is important for determining malicious activity on an instance by a customer admin.

-   Remediation
    -   \(Old\) Set the Glide Property 'com.glide.security.protected\_table.enabled' to 'true'.
    -   \(New\) Set the Glide Property 'com.glide.security.protected\_table.enabled' to 'true'. This requires a user with the "security\_admin" role.
-   CVSS Score
    -   \(Old\) 4.5
    -   \(New\) 4

</td></tr><tr><td>

[Ensure dashboards creation/deletion requires access check \[New in Security Center 1.3 and updated in 2.0\]](../reference/sc-ensure-dashboards-creation-deletion-requires-access-check.md)

</td><td>

-   Description
    -   \(Old\)

The property 'glide.processors.check\_access\_before\_process' enables ACL enforcement for creating or deleting dashboards so long as a user is logged in. Disabling this property \(i.e., setting it to false\) effectively allows for an ACL bypass on dashboards which allows all authenticated low privileged users to arbitrarily delete and add dashboards. This property should always be set to true.

    -   \(New\)

The property 'glide.processors.check\_access\_before\_process' enables ACL enforcement for creating or deleting dashboards. When the property is set to "true", access control checks are performed on the dashboards. When this property is set to "false", authenticated users can arbitrarily delete and add dashboards.

-   Remediation
    -   \(Old\)

Ensure the Glide Property 'glide.processors.check\_access\_before\_process' exists and is set to the value 'true'. If the property does not appear in the sys\_properties table, add a new record.

    -   \(New\)

Set the glide.processors.check\_access\_before\_process system property to true. If the property does not appear in the System Properties \[sys\_properties\] table, the fallback value is true.

-   Security Risk
    -   \(Old\) &lt;blank&gt;
    -   \(New\) When this property is set to "false", authenticated users can arbitrarily delete and add dashboards.
-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Users may not have access to delete dashboards as before. To mitigate this functional impact, users can be granted standard access to dashboards.
-   Fallback Value
    -   \(Old\) false
    -   \(New\) true

</td></tr><tr><td>

[Define active session timeout exception roles](../reference/sc-define-active-session-timeout-exception-roles.md)

</td><td>

-   Description
    -   \(Old\)Active session timeouts are a feature to ensure that a hijacked session cannot be used indefinitely without providing authentication information. This property controls the roles that are exempted from an active session timeout limit. It is best practice to only consider an active session timeout limit exception for internal integration account roles. If a role is given an exception to the session timeout, and that role is given to a user who is the victim of a session hijacking attack, an attacker can continue to authenticate to that session indefinitely. This may increase the affected scope of a security incident by allowing an attacker more time to make use of a hijacked account.
    -   \(New\)

Use the glide.active.session.timeout.exception.roles system property to exempt roles from an active session timeout limit. The active session timeout feature helps ensure that a hijacked session can't be used indefinitely without providing authentication information. It is best practice to only consider an active session timeout limit exception for internal integration account roles.

Consider an active session timeout limit exception only for internal integration account roles. If a user is a victim of a session hijacking attempt, and has a role with an exception, attackers using that session can continue to authenticate to that session indefinitely. This may increase the impact of a security incident by enabling an attacker more time to make use of a hijacked account.

-   Remediation
    -   \(Old\)

Ensure Glide Property 'glide.active.session.timeout.exception.roles' is set to value 'edge\_encryption,mid\_server'.

    -   \(New\)

Configure the glide.active.session.timeout.exception.roles property to roles which should be exempt from active session timeouts. This property value is a comma separated list of roles. The default value is edge\_encryption,mid\_server,maint.

-   Security Risk
    -   \(Old\) Only consider an active session timeout limit exception for internal integration account roles. If a role is given an exception to the session timeout, and that role is given to a user who is the victim of a session hijacking attack, then an attacker can continue to authenticate to that session indefinitely. This may increase the impact of a security incident by enabling an attacker more time to make use of a hijacked account.
    -   \(New\) Consider an active session timeout limit exception only for internal integration account roles. If a user is a victim of a session hijacking attempt, and has a role with an exception, attackers using that session can continue to authenticate to that session indefinitely. This may increase the impact of a security incident by enabling an attacker more time to make use of a hijacked account.
-   Functional impact
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Roles added to this list will be exempt from active session timeout limit.
-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Comma-separated list of roles
-   Out of Box Value
    -   \(Old\) &lt;blank&gt;
    -   \(New\) edge\_encryption,mid\_server,maint
-   Fallback Value
    -   \(Old\) edge\_encryption,mid\_server
    -   \(New\) edge\_encryption,mid\_server,maint

</td></tr><tr><td>

[Limit HTTP response body size \[New in Security Center 1.3 and updated in 1.5\]](../reference/sc-limit-http-response-body-size.md)

</td><td>

-   Data type
    -   \(Old\) &lt;blank&gt;
    -   \(New\) Boolean, Integer
-   Out of box value
    -   \(Old\) &lt;blank&gt;
    -   \(New\) true,524288000

</td></tr></tbody>
</table>**Parent Topic:**[Updated hardening settings](hardening-settings-updated.md)

