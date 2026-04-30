---
title: Enforce application specific ACLs only for application data
description: Avoid unauthorized or undesired access to application data by enforcing application-specific access control lists \(ACLs\) only for application data.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-06-12"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce application specific ACLs only for application data

Avoid unauthorized or undesired access to application data by enforcing application-specific access control lists \(ACLs\) only for application data.

Control the behavior of application data residing in primary tables outside the application. When these properties have a value of **true**, only the application-specific ACLs are evaluated for access to the application data residing in these tables. Not all applications are designed to work in this configuration or use a System Property \[sys\_properties\] record for this purpose.

These system properties use the **glide.enforce\_security\_scope.&lt;scope&gt;** naming format. For example, use the **glide.enforce\_security\_scope.sn\_hr\_sp** property for the Employee Center Core \(sn\_hr\_sp\) scope. The following application scopes contain this property:

<table id="table_whg_pfg_32c"><tbody><tr><td>

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

</td><td>

-   sn\_hc\_professional
-   sn\_hr\_agent\_ws
-   sn\_hr\_awa
-   sn\_hr\_core
-   sn\_hr\_ef
-   sn\_hr\_er
-   sn\_hr\_gen\_ai
-   sn\_hr\_hc
-   sn\_hr\_le
-   sn\_hr\_le\_ent

</td><td>

-   sn\_hr\_mii\_base
-   sn\_hr\_pad
-   sn\_hr\_pj
-   sn\_hr\_sp
-   sn\_hr\_va
-   sn\_hr\_ws
-   sn\_imt\_health\_test
-   sn\_imt\_tracing
-   sn\_imt\_vaccine
-   sn\_ja

</td><td>

-   sn\_jny
-   sn\_lg\_contracts
-   sn\_lg\_matter
-   sn\_lg\_ops
-   sn\_opp\_market
-   sn\_professional
-   sn\_svc\_appl\_info
-   sn\_uni\_req
-   sn\_uni\_task

</td></tr></tbody>
</table>For each application installed with the **glide.enforce\_security\_scope** property in the System Properties \[sys\_properties\] table, \(for example, **glide.enforce\_security\_scope.sn\_hr\_core**\), ensure the property value is set to **true**.

**Note:** These properties can only be modified by the scoped administrator for the specific application. If a sys\_properties record does not exist for the given application and respective property, it must be created.

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

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.enforce\_security\_scope.&lt;scope&gt;**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.1
-   CVSS score: Medium
-   Security risk details: When these properties don’t have a value of **true**, the ACLs on the primary table are still evaluated for access, potentially allowing unauthorized or undesired access to application data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

