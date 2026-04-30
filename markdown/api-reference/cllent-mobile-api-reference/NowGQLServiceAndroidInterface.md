---
title: NowGraphQLService interface - Android
description: The NowGraphQLService interface provides functions that allow you to make GraphQL requests to your ServiceNow through its GraphQL API.Passes the specified GraphQL query to the associated ServiceNow instance and returns the query results.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowGraphQLService interface- Android

The NowGraphQLService interface provides functions that allow you to make GraphQL requests to your ServiceNow through its GraphQL API.

**Note:** The GraphQL API works for guest users in the base ServiceNow system.

For more details on the ServiceNow GraphQL API, see [Query record data using the GraphQL API framework](../../../../../../integrate/graphql/concept/scripted-graph-ql.md).

|Name|Type|Description|
|----|----|-----------|
|configuration|[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationAndroidAPI.md)|Configuration to associate with the service.|

**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## NowGraphQLService - graphQLRequest\(String query\)

Passes the specified GraphQL query to the associated ServiceNow instance and returns the query results.

|Name|Type|Description|
|----|----|-----------|
|query|String|GraphQL query to pass.|

|Type|Description|
|----|-----------|
|[Call](../../Call/concept/CallAndroidInterface.md#)&lt;[Byte Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/)&gt;|Query response.|

```
fun makeGraphQLRequest(query: String) { 
  val call = graphQLService.graphQLRequest(query) 
  call.enqueue( 
    { response -> handleResponse(response) },
    { nowDataError -> handleError(nowDataError) } 
  )
} 
```

