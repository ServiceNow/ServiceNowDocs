---
title: Properties installed with Public Sector Digital Services
description: Use the system properties that are added with the activation of the Public Sector Digital Services application to configure access control to application data.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-09-09"
reading_time_minutes: 1
breadcrumb: [Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Properties installed with Public Sector Digital Services

Use the system properties that are added with the activation of the Public Sector Digital Services application to configure access control to application data.

These properties are available for Public Sector Digital Services.

**Note:** All of these properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="table_tn2_2b2_rcc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.enforce\_security\_scope.sn\_gsm\_info\_req

</td><td>

Controls access to playbook data for the Information Request Playbook feature. If this property is set to false, then ACLs from all scopes are considered when granting access to playbook data in the scope master table. This would expose information request playbook data.

-   Type: Boolean
-   Default value: true
-   Location: System Property \[/sys\_properties\_list.do\] table

</td></tr><tr><td>

glide.enforce\_security\_scope.sn\_gsm

</td><td>

Controls how the application data from the Public Sector Digital Services application is accessed.If this property is set to false, access to the application data within the global tables of the Public Sector Digital Services app may be accessible based on the access control lists \(ACLs\) of those global tables.

If this property is set to true, access to data residing in global tables are only evaluated based off the ACLs shipped directly in the Public Sector Digital Services app. Setting this property to false may lead to information disclosure from over permissive ACLs.

-   Type: boolean
-   Default value: true
-   Location: System Property \[/sys\_properties\_list.do\] table

</td></tr><tr><td>

glide.enforce\_security\_scope.sn\_gsm\_lic\_prmt

</td><td>

Determines if only the access control lists \(ACLs\) within the License and Permit plugin will be used in determining access to the scope, or if ACLs from all scopes will be considered. If this property is set to true, the License and Permit Playbooks data is secured in scope master tables by considering only ACLs from sn\_gsm\_lic\_prmt scope for granting access.

If this property is set to false, the License and Permit Playbooks data is exposed in scope master tables by considering the ACLs from all scopes for granting access. For example, the IT Administrator can access License and Permit Playbooks data when this property is set to false.

-   Type: boolean
-   Default value: true
-   Location: System Property \[/sys\_properties\_list.do\] table

</td></tr></tbody>
</table>