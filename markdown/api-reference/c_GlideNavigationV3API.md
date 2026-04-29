---
title: GlideNavigation - Client
description: The GlideNavigation API provides methods to control and refresh the navigator and main frame.Redirects to a new URL.Opens the specified URL in a popup window.Redirects to a record. The record displays in the navigator frame.Refreshes content in the navigator frame.Reloads the current frame.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideNavigation- Client

The GlideNavigation API provides methods to control and refresh the navigator and main frame.

These methods are accessed using the `g_navigation` global object.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideNavigation - open\(String url, String target\)

Redirects to a new URL.

<table id="table_wnq_lmb_mv" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

url

</td><td>

String

</td><td>

The URL to load. It can be any URL supported by the browser.

</td></tr><tr><td>

target

</td><td>

String

</td><td>

Optional. The frame in which to load the content specified by the URL. Default: Current frame

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to open the list of active incidents within an instance and display the content in the current frame.

```
g_navigation.open('incident_list.do?sysparm_query=active=true');

```

## GlideNavigation - openPopup\(String url, String name, String features, Boolean noStack\)

Opens the specified URL in a popup window.

The **features** parameter is part of the DOM specification and is passed through. For more information on the available feature list, refer to the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/API/Window/open).

<table id="table_p4g_c4b_mv" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

url

</td><td>

String

</td><td>

URL to open.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Window name.

</td></tr><tr><td>

features

</td><td>

String

</td><td>

Comma separated list of features for the popup window.

</td></tr><tr><td>

noStack

</td><td>

Boolean

</td><td>

Flag that indicates whether to append `sysparm_stack=no` to the URL. This parameter helps prevent unexpected behavior when using the form back button.Valid values:

-   true: Append `sysparm_stack=no` to the URL.
-   false: Do not append `sysparm_stack=no` to the URL.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Window|Instance of the new window.|

This example shows how to open the list of active incidents within a popup window called "Active Incidents", and enable the resizable, scrollbars, and status features on the window.

```
g_navigation.openPopup('incident_list.do?sysparm_query=active=true', 'Active Incidents', 'resizable,scrollbars,status', true);

```

## GlideNavigation - openRecord\(String tableName, String sys\_id\)

Redirects to a record. The record displays in the navigator frame.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table containing the record to display.|
|sys\_id|String|Sys\_id of the record to display.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to open a specified incident record in the navigator frame.

```
g_navigation.openRecord('incident', '4e49c0e81bf198101363ff37dc4bcb8a');

```

## GlideNavigation - refreshNavigator\(\)

Refreshes content in the navigator frame.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how to refresh the content in the navigator frame.

```
g_navigation.refreshNavigator();

```

## GlideNavigation - reloadWindow\(\)

Reloads the current frame.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how to refresh the content in the current frame.

```
g_navigation.reloadWindow();

```

