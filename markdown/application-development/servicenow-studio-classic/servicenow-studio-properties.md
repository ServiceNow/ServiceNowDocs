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
reading_time_minutes: 2
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
</table>**Parent Topic:**[ServiceNow Studio reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-reference.md)

