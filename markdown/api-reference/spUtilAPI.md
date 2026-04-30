---
title: spUtil - Client
description: The spUtil API provides utility methods to perform common functions in a Service Portal widget client script.Displays a notification error message.Displays a notification info message.Displays a trivial notification message.Create a unique identifier.Embeds a widget model in a widget client script.Retrieves all headers to use for API calls.Returns the complete host domain.Executes the callback with User Preference response by passing the preference name.Returns the current service portal URL information.Formats a string that contains variables.Checks if the current client is a mobile device.Parses the comma-separated attributes within a specified string.Watches for updates to a table or filter and returns the value from the callback function.Calls the server and replaces the current options and data with the server response.Scrolls to the element with the specified selector, over a specified period of time.Updates the header breadcrumbs.Sets a user preference.Updates the search page.Updates the data object on the server within a given scope.
locale: en-US
release: xanadu
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# spUtil- Client

The spUtil API provides utility methods to perform common functions in a Service Portal widget client script.

These functions include:

-   Display a notification error message. [spUtil - addErrorMessage\(String message\)](spUtilAPI.md#)
-   Display a notification info message. [spUtil - addInfoMessage\(String message\)](spUtilAPI.md#)
-   Display a trivial notification message. [spUtil - addTrivialMessage\(String message\)](spUtilAPI.md#)
-   Create a unique identifier. [spUtil - createUid\(\)](spUtilAPI.md#)
-   Format a string with variables. [spUtil - format\(String template, Object data\)](spUtilAPI.md#)
-   Embed a widget model in a widget client script. [spUtil - get\(String widgetId Object data\)](spUtilAPI.md#)
-   Retrieve all headers to use for API calls. [spUtil - getHeaders\(\)](spUtilAPI.md#)
-   Return the complete host domain. [spUtil - getHost\(\)](spUtilAPI.md#)
-   Execute the callback with User Preference response by passing the preference name. [spUtil - getPreference\(String preference, Function callback\)](spUtilAPI.md#)
-   Return the current service portal URL information. [spUtil - getURL\(\)](spUtilAPI.md#)
-   Check if the current client is a mobile device. [spUtil - isMobile\(\)](spUtilAPI.md#)
-   Parse the comma-separated attributes within a specified string. [spUtil - parseAttributes\(String attributes\)](spUtilAPI.md#)
-   Watch for updates to a table or filter and returns the value from the callback function. [spUtil - recordWatch\(Object $scope, String table, String filter, Function callback\)](spUtilAPI.md#)
-   Call the server and replaces the current **options** and **data** with the server response. [spUtil - refresh\(Object $scope\)](spUtilAPI.md#)
-   Scroll to the element with the specified selector, over a specified period of time. [spUtil - scrollTo\(String selector, Number time\)](spUtilAPI.md#)
-   Update the header breadcrumbs. [spUtil - setBreadCrumb\(Object $scope, Array breadcrumbs\)](spUtilAPI.md#)
-   Set a user preference. [spUtil - setPreference\(String pref, String value\)](spUtilAPI.md#)
-   Update the search page. [spUtil - setSearchPage\(String searchPage\)](spUtilAPI.md#)
-   Update the data object on the server within a given scope. [spUtil - update\(Object $scope\)](spUtilAPI.md#)

For additional information on widgets, see [Service Portal widgets](https://www.servicenow.com/docs/access?context=service-portal-widgets&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## spUtil - addErrorMessage\(String message\)

Displays a notification error message.

|Name|Type|Description|
|----|----|-----------|
|message|String|Error message to display.|

|Type|Description|
|----|-----------|
|void| |

```
spUtil.addErrorMessage("There has been an error processing your request")
```

## spUtil - addInfoMessage\(String message\)

Displays a notification info message.

|Name|Type|Description|
|----|----|-----------|
|message|String|Message to display.|

|Type|Description|
|----|-----------|
|void| |

```
spUtil.addInfoMessage("Your order has been placed")
```

## spUtil - addTrivialMessage\(String message\)

Displays a trivial notification message.

Trivial messages disappear after a short period of time.

|Name|Type|Description|
|----|----|-----------|
|message|String|Message to display.|

|Type|Description|
|----|-----------|
|void| |

```
spUtil.addTrivialMessage("Thanks for your order")
```

## spUtil - createUid\(\)

Create a unique identifier.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|A unique 32 character ID.|

## spUtil - get\(String widgetId Object data\)

Embeds a widget model in a widget client script.

The callback function returns the full widget model. For additional information on widgets, see [Service Portal widgets](https://www.servicenow.com/docs/access?context=service-portal-widgets&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|widgetId|String|Widget ID or sys\_id of the widget to embed.|
|data|Object|Optional. Name/value pairs of parameters to pass to the widget model.|

|Type|Description|
|----|-----------|
|Object|Model of the embedded widget.|

Without data passed.

```
spUtil.get("widget-cool-clock").then(function(response) {
  c.coolClock = response;
});
```

With data passed.

```
spUtil.get('pps-list-modal', {title: c.data.editAllocations, 
  table: 'resource_allocation', 
  queryString: 'GROUPBYuser^resource_plan=' + c.data.sysId, 
  view: 'resource_portal_allocations' }).then(function(response) {
    var formModal = response;
    c.allocationListModal = response;
  });  	

```

## spUtil - getHeaders\(\)

Retrieves all headers to use for API calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|All headers to use for API calls.|

## spUtil - getHost\(\)

Returns the complete host domain.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The complete host domain, for example `hi.servicenow.com`|

## spUtil - getPreference\(String preference, Function callback\)

Executes the callback with User Preference response by passing the preference name.

|Name|Type|Description|
|----|----|-----------|
|preference|String|Name of the preference.|
|callback|Function|Define the callback function.|

|Type|Description|
|----|-----------|
|void| |

## spUtil - getURL\(\)

Returns the current service portal URL information.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current service portal URL.|

## spUtil - format\(String template, Object data\)

Formats a string that contains variables.

Use this method as an alternative to string concatenation.

|Name|Type|Description|
|----|----|-----------|
|template|String|String template that contains values for variable substitution.|
|data|Object|Object containing the values for the variables defined in the template string.|

|Type|Description|
|----|-----------|
|String|String containing the variable values instead of the variable nomenclature.|

```
spUtil.format('An error ocurred: {error} when loading {widget}', {error: '404', widget: 'sp-widget'})
```

Output:

```
'An error occurred: 404 when loading sp-widget'
```

## spUtil - isMobile\(\)

Checks if the current client is a mobile device.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_hz2_pcd_v2b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current client is a mobile device.Valid values:

-   true: Current client is a mobile device.
-   false: Current client is not a mobile device.

</td></tr></tbody>
</table>## spUtil - parseAttributes\(String attributes\)

Parses the comma-separated attributes within a specified string.

|Name|Type|Description|
|----|----|-----------|
|attributes|String|String containing comma separated attributes, such as the Attributes field of a dictionary record.|

|Type|Description|
|----|-----------|
|Array|Array of objects containing the parsed attributes.|

```
function getRefQualElements() {
  var refQualElements = [];
  if (field && field.attributes && field.attributes.indexOf('ref_qual_elements') > -1) {
    var attributes = spUtil.parseAttributes(field.attributes);
    refQualElements = attributes['ref_qual_elements'].split(';');
  }
  return refQualElements;
}
```

## spUtil - recordWatch\(Object $scope, String table, String filter, Function callback\)

Watches for updates to a table or filter and returns the value from the callback function.

Allows a widget developer to respond to table updates in real-time. For instance, by using recordWatch\(\), the Simple List widget can listen for changes to its data table. If records are added, removed, or updated, the widget updates automatically.

**Note:** When passing the `$scope` argument into the recordWatch\(\) function, inject `$scope` into the parameters of your client script function.

|Name|Type|Description|
|----|----|-----------|
|$scope|Object|Scope of the data object updated by the callback function.|
|table|String|Watched table.|
|filter|String|Filter for fields to watch.|
|callback|Function|Optional. Parameter to define the callback function.|

|Type|Description|
|----|-----------|
|Promise|Return value of the callback function.|

```
//A simple recordWatch function.
spUtil.recordWatch($scope, "live_profile", "sys_id=" + liveProfileId);

//In a widget client script
function(spUtil, $scope) {
  /* widget controller */
  var c =this;

  // Registers a listener on the incident table with the filter active=true, 
  // meaning that whenever something changes on that table with that filter, 
  // the callback function is executed.    
  // The callback function takes a single parameter 'response', which contains 
  // the property 'data'. The 'data' property contains information about the changed record. 
  spUtil.recordWatch($scope, "incident", "active=true", function(response) {
        
    // Returns the data inserted or updated on the table 
    console.log(response.data);   
    
    });
}
```

## spUtil - refresh\(Object $scope\)

Calls the server and replaces the current **options** and **data** with the server response.

Calling `spUtil.refresh()` is similar to calling `server.refresh()`. However, when you call `spUtil.refresh()`, you can define the $scope object.

|Name|Type|Description|
|----|----|-----------|
|$scope|Object|Scope defined for the update.|

|Type|Description|
|----|-----------|
|Object|Updated options and data objects.|

## spUtil - scrollTo\(String selector, Number time\)

Scrolls to the element with the specified selector, over a specified period of time.

<table id="table_drd_wzp_v2b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

selector

</td><td>

String

</td><td>

Selector to scroll to.

</td></tr><tr><td>

time

</td><td>

Number

</td><td>

Time taken to scroll to the specified selector.Unit: Milliseconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## spUtil - setBreadCrumb\(Object $scope, Array breadcrumbs\)

Updates the header breadcrumbs.

|Name|Type|Description|
|----|----|-----------|
|$scope|Object|Scope defined for the table.|
|breadcrumbs|Array|Conditions used to create the breadcrumb filter.|

|Type|Description|
|----|-----------|
|void| |

## spUtil - setPreference\(String pref, String value\)

Sets a user preference.

|Name|Type|Description|
|----|----|-----------|
|pref|String|Preference name|
|value|String|Preference value|

|Type|Description|
|----|-----------|
|void| |

## spUtil - setSearchPage\(String searchPage\)

Updates the search page.

|Name|Type|Description|
|----|----|-----------|
|searchPage|String|Name of the search page.|

|Type|Description|
|----|-----------|
|void| |

## spUtil - update\(Object $scope\)

Updates the data object on the server within a given scope.

This method is similar to `server.update()`, but includes a $scope parameter that defines the scope to pass over.

|Name|Type|Description|
|----|----|-----------|
|$scope|Object|Scope defined for the update.|

|Type|Description|
|----|-----------|
|Object|Updated data object.|

The following example includes a P1 widget that watches for changes to the state field and uses a filter to watch all active P1s and let the callback function determine whether to refresh the data. The **data.changes** property contains an array of any updated fields. If the state of any fields have changed, the data is updated in the widget.

```
var q = "priority=1^active=true^EQ";
spUtil.recordWatch($scope, "incident", q, function(event, data) {
   if (data.changes.includes("state")) { // only update if state was updated.
      spUtil.update($scope);
   }
});
```

