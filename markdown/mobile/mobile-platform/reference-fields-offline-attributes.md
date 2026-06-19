---
title: Reference field attributes for input form screens in offline mode
description: Configure the fields that you want to use and the data you want to display in offline mode by using various input attributes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/reference-fields-offline-attributes.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 3
breadcrumb: [Input forms in offline, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Reference field attributes for input form screens in offline mode

Configure the fields that you want to use and the data you want to display in offline mode by using various input attributes.

**Note:** You must create an input form screen before you create variables and attributes. For information about creating an input form screen, see [Configure an input form screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/parameter-screen-config.md).

## Reference inputs

Use reference inputs for inputs that reference a field on a table. These inputs work like reference fields in the forms on your instance. You can configure your reference input with conditions, reference qualifiers, and a search option to help your users find what they need quickly.

You can use these attributes with reference inputs.

**Note:** All attributes are case-sensitive.

|Attribute|Description|
|---------|-----------|
|SourceTable|The source table for your reference qualifier.|
|SourceFieldName|The field name of the referenced field in the source table.|
|TargetTable|The table you want to target for your reference qualifier.|

The following additional attributes are optional:

<table id="table_anh_jbw_b4b"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OfflineMobileViewId

</td><td>

Define the mobile card used to display reference field data in offline mode. The **OfflineMobileViewId** attribute takes precedence over the **MobileViewId** attribute.

</td></tr><tr><td>

EnableSearch

</td><td>

Option to determine whether the search bar displays. The value must be **true** or **false**.

</td></tr><tr><td>

OfflineConditions

</td><td>

Encoded query condition used to query the reference data. The **OfflineConditions** attribute takes precedence over the **Conditions** attribute.**Note:** This attribute can also be used when the **Conditions** attribute has a condition that can't be supported in offline.

</td></tr><tr><td>

SearchType

</td><td>

Defines the query used for search. The value can be `starts_with` or `contains`. If this attribute is not configured, the instance uses `starts_with` by default on the display label column.

</td></tr><tr><td>

OfflineFetchScript

</td><td>

Use to specify a list of Sys IDs for reference records. Using this attribute, you can define what records to cache while in offline mode.

 Reference fields can return many thousands of records, but only 1,000 records are supported to cache for offline mode. Use this attribute to define the specific records \(1,000 or less\) that you want to cache for use while offline.

 If this attribute is not used, then the first 1,000 records returned are cached. An example script is shown in the next section.

</td></tr><tr><td>

OfflineMaxNumRecords

</td><td>

Defines the number of records that you can cache in offline mode. The maximum number is 1000.You can set a different value for each reference input.

</td></tr></tbody>
</table>## OfflineFetchScript implementation example

This example shows how the system dynamically retrieves users who share the logged-in user's location for the **Assigned To**field in the input form.

1.  Create a Script Include to return active users in the same location as the logged-in user, plus the user themself.

    ```
    var MobileOfflineUserFetch = Class.create(); 
    MobileOfflineUserFetch.prototype = { 
        initialize: function() {}, 
     
        getUsersByMyLocation: function() { 
            var ids = []; 
            var myId = gs.getUserID(); 
            var myLoc = gs.getUser().getLocation(); 
     
            ids.push(myId); // include myself 
     
            if (!myLoc) 
                return ids.join(','); 
     
            var gr = new GlideRecord('sys_user'); 
            gr.addActiveQuery(); 
            gr.addQuery('location', myLoc); 
            gr.setLimit(1000); // Reference field limitation 
            gr.query(); 
     
            while (gr.next()) { 
                ids.push(gr.getUniqueValue()); 
            } 
            return ids.join(','); 
        }, 
     
        type: 'MobileOfflineUserFetch' 
    }; 
    ```

2.  Add the OfflineFetchScript input attribute to the **Assigned To** input field and set the value to the following:

    ```
    javascript: new MobileOfflineUserFetch().getUsersByMyLocation()
    ```


**Parent Topic:**[Input forms in offline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-input-form.md)

