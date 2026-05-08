---
title: SNAnalytics - Client
description: The SNAnalytics API provides methods to push custom analytics data \(events, pages, and user properties\) to the Usage Insights for Service Portal dashboard.Stores the specified event information in the analytics data store.Appends the specified string to the specified user string property in the analytics data store.Increments or decrements the specified user property value with the specified number value in the analytics data store.Removes the specified property for the current user from the analytics data store.Sets the specified properties with the specified values for the current user in the analytics data store.Sets the specified property with the specified value for the current user in the analytics data store.Saves the name and description of a page in the analytics data store.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# SNAnalytics- Client

The SNAnalytics API provides methods to push custom analytics data \(events, pages, and user properties\) to the Usage Insights for Service Portal dashboard.

Usage Insights for Service Portal provides dashboard views for monitoring the key performance indicators \(KPIs\) of web applications built on Service Portal. You can use these insights to optimize your portal. For example, Usage Insights tracks when a user orders a catalog item or views a knowledge article. You can use this data to infer which items or articles are the most popular among users.

To access this API, the Service Portal Analytics \(com.glide.service-portal.analytics\) plugin must be activated on the instance. In addition, within your application, you must import the snAnalytics Angular service, such as:

```
<client_script><![CDATA[function($rootScope, $scope, $window, $timeout, spUtil, $sce, spModal, $uibModal, $location, cabrillo, snAnalytics)
```

For additional information, see Usage Insights for Service Portal.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## SNAnalytics - addEvent\(Object payload\)

Stores the specified event information in the analytics data store.

Events are actions performed by a user, such as clicking a button or submitting a form. Call this method within your web-page widget whenever you want to capture a user action. These events then automatically appear on the associated user session timeline and User Experience Analytics dashboard.

The following is an example of a payload passed in an addEvent\(\) call:

```
var payload= {};
payload.name = "Manage Account";
payload.data = {};
payload.data["Function Name"] = c.data.function_name;
payload.data["User Type"] = c.data.user_type;
payload.data["Company"] = c.data.company_name;
snAnalytics.addEvent(payload);
```

The screen capture below shows the information that appears on the analytics dashboard for the event "Manage Account." The timeline at the top represents the number of times that the event occurred. The pie charts below the timeline reflect the properties that were captured in the addEvent\(\) call. ![Dashboard with events](../image/Dashboard_with_events.png)

If you want to capture when users access a web page, use the [SNAnalytics - startPage\(String name, String description\)](SNAnalyticsClientAPI.md#) method instead of this method.

<table id="table_u1m_5gr_z4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

payload

</td><td>

Object

</td><td>

Event to store in the analytics data store.Data type: Object

 ```
"payload": {
  "data": [Array],
  "name": String
}
```

</td></tr><tr><td>

payload.data

</td><td>

ArrayEach element can be a string \(case-sensitive\), boolean, number, or date.

</td><td>

Optional. Name-value pairs of custom event properties. These properties can be any values that you want to track and see on the analytics dashboard. They appear under the associated event timeline on the analytics dashboard. The **Page Id** property always appears first on the dashboard for all base system events, and all other properties are sorted alphabetically.If no properties are required for an event, only an event timeline appears on the analytics dashboard. Properties can be added at a later time.

 The following values are automatically converted by this method:

-   String value of "yes": Boolean value of "true"
-   String value of "no": Boolean value of "false

 Default value: Null

</td></tr><tr><td>

payload.name

</td><td>

String

</td><td>

Descriptive name of the event. Special characters are not allowed.Maximum length: The length of the event name and value cannot exceed 300 bytes.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to call the addEvent\(\) method during initialization of a widget.

```
function initialize() {
  c.options.glyph = c.options.glyph || 'search';
  c.options.title = c.options.title || c.data.searchMsg;
  c.options.color = c.options.color || "default";
  c.searchTerm = c.data.q;
  c.searchQuery = "";
  c.pageID = $scope.page && $scope.page.id;
  c.showSuggestions =  c.data.searchTypeBehavior === "suggestions" && c.data.isSuggestionsEnabled === "true";
  c.suggestionsLimit = c.options.limit || "";
  c.latitude = null;
  c.longitude = null;
  c.isLocationTrackerDisabled = c.data.isLocationTrackerDisabled === "true";
  c.isTypeAheadEnabled = c.data.isTypeAheadEnabled === "true";

  c.sendAnalytics = function(type){
    var payload= {};
    payload.name = "Initiate Search";
    payload.data = {};
    payload.data["Keyword"] = (type == 'User Entered' ? c.searchTerm : c.searchQuery);
    payload.data["Type"] = type;
    snAnalytics.addEvent(payload);
  };
}
```

## SNAnalytics - appendToUserProperty\(String name, String value\)

Appends the specified string to the specified user string property in the analytics data store.

<table id="table_apg_5fv_dpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String or String\[\]

</td><td>

Name of the property to append the specified string to. Special characters are not allowed.**Note:** The associated property must be a string or string\[\].

 Maximum length: The length of the property name and property value cannot exceed 300 bytes.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Value to append to the string property.The following values are automatically converted by this method:

-   String value of "yes": Boolean value of "true"
-   String value of "no": Boolean value of "false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to add `television` to the `tags` property.

```
snAnalytics.setUserProperties({
  level: 7,
  lastPurchase: new Date(),
  lastPurchaseId: '41563cd2-1666-4855-8c0d-b9ca778aed23',
  isPremium: true,
  tags: ['chair', 'table'],
});

// Append television to the tags property (now 'tags' will have 'chair', 'table', and 'television')
snAnalytics.appendToUserProperty('tags', 'television');
```

## SNAnalytics - incUserProperty\(String name, Number value\)

Increments or decrements the specified user property value with the specified number value in the analytics data store.

<table id="table_pt1_syp_dpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name of the property to increment. Value is case-sensitive.**Note:** The associated property must be a number.

</td></tr><tr><td>

value

</td><td>

Number

</td><td>

Amount to increment the property by. If you enter a negative number, the value is decremented.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to increment the property `Grace days` by 5.

```
snAnalytics.incUserProperty('Grace days', 5)
```

## SNAnalytics - removeUserProperty\(String name\)

Removes the specified property for the current user from the analytics data store.

In addition, the property no longer appears on the analytics dashboard.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the property to remove. Value is case-sensitive.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to remove the IsAdmin property.

```
snAnalytics.removeUserProperty('IsAdmin');
```

## SNAnalytics - setUserProperties\(Object properties\)

Sets the specified properties with the specified values for the current user in the analytics data store.

These properties are saved in the analytics data store and appear on the user session details page as illustrated below. If a property already exists in the analytics data store, the current value is overwritten with the new value.

![Session page with properties](../image/User_session_properties.png)

<table id="table_iz1_41q_dpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

properties

</td><td>

ObjectEach element in this object can be a string, boolean, number, date, string\[\], or null.

</td><td>

Object that contains the name-value pairs of the user properties to set, such as:```
{
  level: 7,
  lastPurchase: new Date(),
  lastPurchaseId: '41563cd2-1666-4855-8c0d-b9ca778aed23',
  isPremium: true,
  tags: ['chair', 'table'],
}
```

 The following values are automatically converted by this method:

-   String value of "yes": Boolean value of "true"
-   String value of "no": Boolean value of "false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set multiple properties for the current user.

```
snAnalytics.setUserProperties({
  level: 7,
  lastPurchase: new Date(),
  lastPurchaseId: '41563cd2-1666-4855-8c0d-b9ca778aed23',
  isPremium: true,
  tags: ['chair', 'table'],
});
```

## SNAnalytics - setUserProperty\(String name, UserProperty value\)

Sets the specified property with the specified value for the current user in the analytics data store.

These properties are saved in the analytics data store and appear on the user session details page as illustrated below. If a property already exists in the analytics data store, the current value is overwritten with the new value.

![Session page with properties](../image/User_session_properties.png)

<table id="table_uj2_rfp_dpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name of the property to update. This name appears as the label for the property. For example, in the prior screenshot, Domain, Instance Name, Company, Role, and User Type are all name parameters. Special characters are not allowed.Maximum length: The length of the property name and property value cannot exceed 300 bytes.

</td></tr><tr><td>

value

</td><td>

UserPropertyThis value can be a string, boolean, number, date, string\[\], or null.

</td><td>

Value to set in the specified property.The following values are automatically converted by this method:

-   String value of "yes": Boolean value of "true"
-   String value of "no": Boolean value of "false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the property `Company`.

```
snAnalytics.setUserProperty('Company', "ABC Company")
```

## SNAnalytics - startPage\(String name, String description\)

Saves the name and description of a page in the analytics data store.

This information appears in the user session timeline and on the analytics dashboard. Call this method within your custom widgets to track the pages visited by a user. You can also use this method to track user navigation within an individual page. For more information, see Exploring Usage Insights.

**Note:** In general, portal pages are automatically tagged with this tracking capability. Use this method for custom scenarios, such as a single page custom widget in a wizard scenario.

![Page properties in timeline](../image/Page_properties_in_timeline.png)

<table id="table_lmt_pl3_dpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Descriptive name of the page or page section. Special characters are not allowed.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

Optional. Description of the page to appear in the timeline and analytics dashboard. Default: **name** parameter value

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to call the startPage\(\) method.

```
snAnalytics.startPage('login_view', 'Login');
```

