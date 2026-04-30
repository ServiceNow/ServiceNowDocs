---
title: ServiceNow IDE properties
description: Manage how the ServiceNow IDE functions on an instance using the following system properties.
locale: en-US
release: xanadu
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# ServiceNow IDE properties

Manage how the ServiceNow IDE functions on an instance using the following system properties.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter. To add properties to the table, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

<table id="table_acm_jnt_tdc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_glider.default\_to\_bundled\_sdk

</td><td>

Specifies whether to use the bundled version or the latest version of the ServiceNow SDK when creating or converting applications in the ServiceNow IDE. If true, the version of the ServiceNow SDK that's bundled with a version of the ServiceNow IDE is used. If false, the latest version of the ServiceNow SDK is used.-   Type: true \| false
-   Default value: false
-   Location: Add the property to the System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_glider.enable\_ide

</td><td>

Enables access to the ServiceNow IDE. If false, access to the ServiceNow IDE is turned off across the instance.-   Type: true \| false
-   Default value: true
-   Location: Add the property to the System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_glider.fluent\_convert\_enabled

</td><td>

Enables converting existing scoped applications that weren't created with the ServiceNow IDE or ServiceNow SDK to support development in source code from the ServiceNow IDE.-   Type: true \| false
-   Default value: true
-   Location: Add the property to the System Property \[sys\_properties\] table
-   Learn more: [Convert an application with the ServiceNow IDE](../task/convert-application-servicenow-ide.md)

</td></tr><tr><td>

sn\_glider.git.attachment.extension.binary

</td><td>

Defines a custom extension for attachment files with binary content types \(for example, `application/octet-stream`\) to override the default `gitdata` extension. The custom extension that you specify with this property must also be specified with the **glide.attachment.extensions** system property.**Note:** If you reuse an existing extension, confirm that the value you set passes MIME type validations for binary types.

-   Type: string
-   Default value: gitdata
-   Location: Add the property to the System Property \[sys\_properties\] table
-   Learn more: [ServiceNow IDE MID Server User \[sn\_glider.ide\_git\_user\]](servicenow-ide-roles.md#)

</td></tr><tr><td>

sn\_glider.git.attachment.extension.text

</td><td>

Defines a custom extension for attachment files with text content types \(for example, `text/plain`\) to override the default `txt` extension. The custom extension that you specify with this property must also be specified with the **glide.attachment.extensions** system property.**Note:** If you reuse an existing extension, confirm that the value you set passes MIME type validations for text types.

-   Type: string
-   Default value: txt
-   Location: Add the property to the System Property \[sys\_properties\] table
-   Learn more: [ServiceNow IDE MID Server User \[sn\_glider.ide\_git\_user\]](servicenow-ide-roles.md#)

</td></tr><tr><td>

sn\_glider.pinnedSdkVersion

</td><td>

Specifies the version of the ServiceNow SDK to use when creating or converting applications in the ServiceNow IDE.-   Type: string
-   Default value: The latest version of the ServiceNow SDK
-   Location: Add the property to the System Property \[sys\_properties\] table

</td></tr></tbody>
</table>