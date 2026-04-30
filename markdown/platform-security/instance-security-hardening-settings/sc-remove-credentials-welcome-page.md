---
title: Remove credentials from Welcome page
description: Modify the default content on the Welcome page to remove the default credentials.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Remove credentials from Welcome page

Modify the default content on the Welcome page to remove the default credentials.

Two **How to Login** records are installed as part of the demo data for the CMS plugin.

**Note:** If you do not install the demo data for an instance, these records do not exist. In that case, the configuration is considered as Security Compliant as per the recommended security practices.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**How to login**

</td></tr><tr><td>

Configuration type

</td><td>

Table: sys\_home

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Purpose

</td><td>

To remove default credentials from Welcome page that were added with demo data.

</td></tr><tr><td>

Recommended value

</td><td>

False or null if no demo data was utilized.

</td></tr><tr><td>

Default value

</td><td>

None. This is a table configuration, not a Glide property. Therefore, there is no value for default value.

</td></tr><tr><td>

Configuration type

</td><td>

Boolean

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) Demo data is provided for the CMS plugin, which includes two default passwords included on the welcome page. If this is not removed, an unauthorized attacker could gain access to the instance.

</td></tr><tr><td>

References

</td><td>

[https://support.servicenow.com/kb\_view.do?sysparm\_article=KB0550107](https://support.servicenow.com/kb_view.do?sysparm_article=KB0550107)

 [Welcome pages](https://www.servicenow.com/docs/access?context=c_WelcomePageContent&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](sc-authentication.md)

