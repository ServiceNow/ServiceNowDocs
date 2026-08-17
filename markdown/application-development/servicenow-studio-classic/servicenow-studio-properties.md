---
title: ServiceNow Studio properties
description: Configure system properties to control ServiceNow Studio application behavior and delegated development deployment. Access ServiceNow Studio system properties by navigating to All sys\_properties.list .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/servicenow-studio-properties.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: reference
last_updated: "2026-05-29"
reading_time_minutes: 4
breadcrumb: [Reference, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio properties

Configure system properties to control ServiceNow Studio application behavior and delegated development deployment. Access ServiceNow Studio system properties by navigating to **All** &gt; **sys\_properties.list**.

<table id="table_ayv_sf2_dbc"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_devstudio.servicenow\_studio\_banner.enable

</td><td>

Shows the banner for navigating to ServiceNow Studio from App Engine Studio or legacy Studio. Set to **false** to hide the banner.-   Type: true \| false
-   Default value: true
-   Location: System Properties \[sys\_properties\] table

</td></tr><tr><td>

sn\_sns.is\_app\_summarization\_disabled

</td><td>

This property is not included by default in the ServiceNow AI Platform. To disable Now Assist app summary generation in ServiceNow Studio, create a new property on the System Properties \[sys\_properties\] table named `sn_sns.is_app_summarization_disabled` and set the value to **true**.

</td></tr><tr><td>

sn\_udc.smaller\_app\_files\_count\_threshold

</td><td>

Determines the number of files an app can contain and still be treated as a small app in the file navigator. Small apps load all files at once in the file navigator; large apps load a subset of the files on open.-   Admin: Less than or equal to 2300 files
-   Delegated developer: Less than or equal to 1150 files

</td></tr></tbody>
</table><table id="table_pdk_ltt_bfc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.dd.manage\_update\_set\_enabled

</td><td>

Enables or disables display of the **Manage Update Set** permission. Delegated developers cannot see the update sets list unless this property is set to **true**.-   Type: true \| false
-   Default value: false
-   To enable the display of this permission, set this value to **true**.

</td></tr><tr><td>

com.snc.dd.publish\_to\_app\_repo\_enabled

</td><td>

Enables or disables display of the **Publish To App Repo** permission.-   Type: true \| false
-   Default value: true
-   To disable display of this permission, set this value to **false**.

</td></tr><tr><td>

com.snc.dd.publish\_to\_app\_store\_enabled

</td><td>

Enables or disables display of the **Publish To App Store** permission.-   Type: true \| false
-   Default value: true
-   To disable display of this permission, set this value to **false**.

</td></tr><tr><td>

com.snc.dd.publish\_to\_update\_set\_enabled

</td><td>

Enables or disables display of the **Publish To Update Set** permission.-   Type: true \| false
-   Default value: false, which disables display of this permission.
-   To enable the display of this permission, set this value to **true**.

</td></tr><tr><td>

com.snc.dd.upgrade\_app\_enabled

</td><td>

Enables or disables display of the **Upgrade App** permission.

 -   Type: true \| false
-   Default value: true
-   To disable display of this permission, set this value to **false**.

</td></tr></tbody>
</table><table><thead><tr><th>

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

Enables converting existing applications that weren't created with the ServiceNow IDE or ServiceNow SDK to support development in source code from the ServiceNow IDE.-   Type: true \| false
-   Default value: true
-   Location: Add the property to the System Property \[sys\_properties\] table
-   Learn more: [Convert an application with the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/convert-application-servicenow-ide.md)

</td></tr><tr><td>

sn\_glider.git.attachment.extension.binary

</td><td>

Defines a custom extension for attachment files with binary content types \(for example, `application/octet-stream`\) to override the default `gitdata` extension. The custom extension that you specify with this property must also be specified with the **glide.attachment.extensions** system property.**Note:** If you reuse an existing extension, confirm that the value you set passes MIME type validations for binary types.

-   Type: string
-   Default value: gitdata
-   Location: Add the property to the System Property \[sys\_properties\] table
-   Learn more: [ServiceNow IDE MID Server User \[sn\_glider.ide\_git\_user\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/servicenow-ide-roles.md)

</td></tr><tr><td>

sn\_glider.git.attachment.extension.text

</td><td>

Defines a custom extension for attachment files with text content types \(for example, `text/plain`\) to override the default `txt` extension. The custom extension that you specify with this property must also be specified with the **glide.attachment.extensions** system property.**Note:** If you reuse an existing extension, confirm that the value you set passes MIME type validations for text types.

-   Type: string
-   Default value: txt
-   Location: Add the property to the System Property \[sys\_properties\] table
-   Learn more: [ServiceNow IDE MID Server User \[sn\_glider.ide\_git\_user\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/servicenow-ide-roles.md)

</td></tr><tr><td>

sn\_glider.pinnedSdkVersion

</td><td>

Specifies the version of the ServiceNow SDK to use when creating or converting applications in the ServiceNow IDE.-   Type: string
-   Default value: The latest version of the ServiceNow SDK
-   Location: Add the property to the System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Studio reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-reference.md)

