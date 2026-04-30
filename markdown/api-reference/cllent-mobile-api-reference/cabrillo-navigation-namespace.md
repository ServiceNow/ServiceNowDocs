---
title: cabrillo.navigation - Client
description: Cabrillo JS functions for forward and backward navigation.Enables backward navigation.Enables forward navigation.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# cabrillo.navigation - Client

Cabrillo JS functions for forward and backward navigation.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## cabrillo.navigation - goBack\(\)

Enables backward navigation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if Cabrillo JS will navigate backward; otherwise false.|

```
cabrillo.navigation.goBack();
```

## cabrillo.navigation - goto\( String url, Cabrillo.NavigationRequest request\)

Enables forward navigation.

Use the request parameter not the url parameter for list or record navigation.

|Name|Type|Description|
|----|----|-----------|
|url|String|An URL to navigate to. This should be used for custom URL navigation. Optional.|
|request|Cabrillo.NavigationRequest|Describes the list or record to navigate to. Optional.|

|Type|Description|
|----|-----------|
|Boolean|Returns true if Cabrillo JS will navigate; otherwise returns false.|

Navigate to a URL.

```
cabrillo.navigation["goto"]('/$sp.do?id=my_custom_page');
```

Navigate to a list. The request parameter is preferred over the url parameter for list navigation.

```
// A Cabrillo.NavigationRequest dictionary that specifies a list of active incidents.
var request = {
    table: 'incident',
    query: 'active=true',
};
cabrillo.navigation["goto"](null, request);
```

Navigate to a record. The request parameter is preferred over the url parameter for record navigation.

```
// A Cabrillo.NavigationRequest dictionary that specifies an incident record.
var request = {
    table: 'incident',
    sysId: 'a9e30c7dc61122760116894de7bcc7bd'
};
cabrillo.navigation["goto"](null, request);
```

Navigate to a new record.

```
// A Cabrillo.NavigationRequest dictionary that specifies a new incident record.
// The new record will be seeded with the encoded query.
var request = {
    table: 'incident',
    sysId: '-1',
    query: 'short_description=This is a new incident.'
};
cabrillo.navigation["goto"](null, request);
```

