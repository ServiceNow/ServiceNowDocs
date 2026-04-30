---
title: GlideURI - Global
description: The GlideURI API provides methods to handle URI parameters in a global application.Deletes one or more parameters from the URI that match the beginning of the provided string.Removes a specified parameter from the query portion of the URI.Returns the value of the specified parameter.Returns the file name portion of the URI.Returns a map \(key value pairs\) containing each parameter in the query and its associated value.Sets the specified parameter to the specified value.Adds the sysparm\_view parameter to the query with the named view.Reconstructs the URI string and performs the proper URL encoding by converting non-valid characters to their URL code. For example, converting &amp; to '%26'.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideURI- Global

The GlideURI API provides methods to handle URI parameters in a global application.

**Note:** Do not use the GlideURI API in scripts that are executed during export or in background jobs.

For more information on using URIs:

-   [Navigate by URL](https://www.servicenow.com/docs/access?context=navigate-using-url&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)
-   [Navigation stack](https://www.servicenow.com/docs/access?context=c_NavigationStack&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

See also [Action - getGlideURI\(\)](../../Action/concept/ActionAPIBoth.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideURI - deleteMatchingParameter\(String match\)

Deletes one or more parameters from the URI that match the beginning of the provided string.

|Name|Type|Description|
|----|----|-----------|
|match|String|Partial name of one or more parameters to remove from the query portion of a URI.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to delete URI parameters that partially match the name provided.

```
// create the GlideURI object
var uri = action.getGlideURI();

uri.deleteMatchingParameter('sysparm_list_');
uri.deleteMatchingParameter('sysparm_record_');
```

### Scoped equivalent

This method is not available in scoped applications.

## GlideURI - deleteParameter\(String name\)

Removes a specified parameter from the query portion of the URI.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the parameter to remove from the query portion of a URI.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to delete a URI parameter.

```
// create the GlideURI object
var uri = action.getGlideURI(); 

uri.deleteParameter('sysparm_referring_url');
```

### Scoped equivalent

This method is not available in scoped applications.

## GlideURI - get\(String name\)

Returns the value of the specified parameter.

|Name|Type|Description|
|----|----|-----------|
|name|String|The parameter name.|

|Type|Description|
|----|-----------|
|String|The value for the specified parameter.|

```
// create the GlideURI object
var uri = action.getGlideURI();
uri.set('sysparm_query', 'priority=2^active=true' );
var fileString = uri.get('sysparm_query');
gs.info(fileString);
```

Output:

```
priority=2^active=true
```

### Scoped equivalent

To use the get\(\) method in a scoped application, use the corresponding scoped method: [GlideURI - get\(String name\)](../../GlideURIScoped/concept/c_GlideURIScopedAPI.md#) .

## GlideURI - getFileFromPath\(\)

Returns the file name portion of the URI.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The file name portion of the URI.|

```
var gURI = action.getGlideURI();
        
var fileString = gURI.getFileFromPath();
gs.info(fileString);
```

### Scoped equivalent

To use the getFileFromPath\(\) method in a scoped application, use the corresponding scoped method: [GlideURI - getFileFromPath\(\)](../../GlideURIScoped/concept/c_GlideURIScopedAPI.md#) .

## GlideURI - getMap\(\)

Returns a map \(key value pairs\) containing each parameter in the query and its associated value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object| |

The following example shows how to get `sysparm_query` parameters. See also [Action - getGlideURI\(\)](../../Action/concept/ActionAPIBoth.md#) .

```
gs.action.getGlideURI().getMap().get('sysparm_query');
```

### Scoped equivalent

This method is not available in scoped applications.

## GlideURI - set\(String name, String value\)

Sets the specified parameter to the specified value.

|Name|Type|Description|
|----|----|-----------|
|name|String|The parameter name.|
|value|String|The value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set value of a sysparm\_query field. See also [Action - getGlideURI\(\)](../../Action/concept/ActionAPIBoth.md#) .

```
var gURI = action.getGlideURI();
gURI.set('sysparm_query', 'priority=2^active=true' );
var fileString = gURI.get('sysparm_query');
gs.info(fileString);
```

Output:

```
priority=2^active=true
```

### Scoped equivalent

To use the set\(\) method in a scoped application, use the corresponding scoped method: [GlideURI - set\(String name, String value\)](../../GlideURIScoped/concept/c_GlideURIScopedAPI.md#) .

## GlideURI - setView\(String view\)

Adds the **sysparm\_view** parameter to the query with the named view.

A view defines the elements that appear when a user opens a form or a list. The **sysparm\_view** parameter specifies the view to be used for a list or a form. For more information on views, see [View management](https://www.servicenow.com/docs/access?context=view-management-overview&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

See also:

-   [Action - getGlideURI\(\)](../../Action/concept/ActionAPIBoth.md#)
-   [GlideModalV3 - switchView\(\)](../../GlideModalClientSideV3/concept/c_GlideModalV3API.md#)

|Name|Type|Description|
|----|----|-----------|
|view|String|Name of the **sysparm\_view** parameter to set in the URI query.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add the major incidents view to the URI query in the Incidents \[incident\] table. For example, `sysparm_view=Major%20Incidents`. See also [Action - getGlideURI\(\)](../../Action/concept/ActionAPIBoth.md#) .

```
// create the GlideURI object
var uri = action.getGlideURI(); 

// Adds the Major incidents to the query
uri.setView('Major Incidents');

// https://instance.service-now.com/incident.do?sys_id=0&sysparm_view=Major%20Incidents ...
```

### Scoped equivalent

This method is not available in scoped applications.

## GlideURI - toString\(String path\)

Reconstructs the URI string and performs the proper URL encoding by converting non-valid characters to their URL code. For example, converting &amp; to '%26'.

Parameters set with the set\(\) method are encoded with the URI as well.

|Name|Type|Description|
|----|----|-----------|
|path|String|The base portion of the system URL to which the URI is appended.|

|Type|Description|
|----|-----------|
|String|The URL.|

The following examples shows how to convert invalid characters to URL code in an instance URL. See also [Action - getGlideURI\(\)](../../Action/concept/ActionAPIBoth.md#) .

```
var gURI = action.getGlideURI();
fileString = gURI.toString('https://<your instance>.service-now.com/navpage.do');
```

### Scoped equivalent

To use the toString\(\) method in a scoped application, use the corresponding scoped method: [GlideURI - toString\(String path\)](../../GlideURIScoped/concept/c_GlideURIScopedAPI.md#) .

