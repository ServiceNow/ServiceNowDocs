---
title: ServiceNow Studio properties
description: System properties control system behavior. The properties in this section are specific to the ServiceNow Studio application and delegated development deployment. You can access system properties for ServiceNow Studio by navigating to All sys\_properties.list .
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Studio reference, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio properties

System properties control system behavior. The properties in this section are specific to the ServiceNow Studio application and delegated development deployment. You can access system properties for ServiceNow Studio by navigating to **All** &gt; **sys\_properties.list**.

<table id="table_ayv_sf2_dbc"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.dd.manage\_update\_set\_enabled

</td><td>

Enables or disables display of the **Manage Update Set** permission.-   Type: true \| false
-   Default value: false
-   To enable the display of this permission, set this value to **true**. Delegated developers cannot see the update sets list unless granted permissions via the system property shown.

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

</td></tr><tr><td>

sn\_devstudio.servicenow\_studio\_banner.enable

</td><td>

Shows the banner for navigating to ServiceNow Studio from App Engine Studio or legacy Studio. Change this property to false to hide the banner.-   Type: true \| false
-   Default value: true
-   Location: System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Studio reference](../concept/servicenow-studio-reference.md)

