---
title: Prevent impersonating user from viewing application data
description: Use system properties to prevent an impersonating user from viewing application data.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Prevent impersonating user from viewing application data

Use system properties to prevent an impersonating user from viewing application data.

Prevent admin level from accessing the application specific data belonging to that user when impersonating an account. This permission can be set at the application level by creating a system property specific to the application.

These system properties use the **&lt;scope&gt;.impersonateCheck** naming format \(for example **sn\_hr\_core.impersonateCheck**\). Create a system property with a value of **true** to prevent users from accessing the application-specific data belonging to another user when impersonating an account.

**Note:** Not all applications are designed to work in this configuration or have a System Properties \[sys\_properties\] record for this purpose. The following scopes are configured to work with this property.

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
-   sn\_ecn

For each application with the **&lt;scope&gt;.impersonateCheck** property in the System Properties \[sys\_properties\] table, ensure the property value is set to **true**.

**Note:** These properties can only be modified by the scoped administrator for the specific application.

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
	'sn_talent_aia.impersonateCheck',
        'sn_ecn.impersonateCheck'
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

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**&lt;scope&gt;.impersonateCheck**

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

false

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.8
-   CVSS score: Low
-   A value of **false** for these properties allows an admin level user to impersonate another user and access application data with the impersonated user's access. This may be undesirable or allow for unauthorized data access in specific application contexts.

</td></tr><tr><td>

Functional impact

</td><td>

Admin level users are not be able to impersonate another user and view that user's data in a specific application context.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see Add a system property.

**Parent Topic:**[Access control](sc-access-control.md)

