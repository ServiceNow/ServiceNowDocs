---
title: Debug in-bound REST queries
description: You can debug in-bound REST queries by reviewing the session debug log.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# Debug in-bound REST queries

You can debug in-bound REST queries by reviewing the session debug log.

When the **glide.rest.debug** property is **true**, all in-bound REST processing is logged in the session debug log.

REST logging includes processing durations, headers, and the request body. Prolonged use of this property can affect performance, so it is best to use it while debugging REST processing, and then set the property back to **false**.

**Note:** You may not see the resulting log statements if you are not on the application node that processed your REST request. In this case, please contact Technical Support.

You can include session debug logs in a REST response body by passing the X-WantSessionDebugMessages header in the request. For more information, see [Returning session debug logs in a REST response](rest-session-debug-header.md). To view debug logs, see [Display debugging logs](../../../script/debugging/concept/c_SessionDebug.md#).

## Sample log output

```
 2014-03-19 11:10:37 (633) http-12 New transaction 083A6031D7231100261253B2B252035C #28 /api/now/table/incident
 2014-03-19 11:10:37 (653) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Started initializing REST Request 
 2014-03-19 11:10:37 (653) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Method:POST 
 2014-03-19 11:10:37 (656) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Header: host:localhost:8080
 2014-03-19 11:10:37 (656) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Header: user-agent:Mozilla/5.0 (Macintosh; Intel Mac OS X 10.7; rv:12.0) Gecko/20100101 Firefox/12.0
 2014-03-19 11:10:37 (656) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Header: accept:application/json
 2014-03-19 11:10:37 (656) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Header: accept-encoding:gzip, deflate
 2014-03-19 11:10:37 (656) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Header: connection:keep-alive
 2014-03-19 11:10:37 (657) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Header: content-type:application/json; charset=UTF-8
 2014-03-19 11:10:37 (657) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Header: content-length:31
 2014-03-19 11:10:37 (657) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Header: cookie:glide_user_route=glide.20e7f4cd6bdc0d444810117aacc0eeae; JSESSIONID=F07CE6ACF8AF237CB239AF43B7F360BF; glide_user="U0N2Mjo0MDNhNjAzMWQ3MjMxMTAwMjYxMjUzYjJiMjUyMDM2OTo2ODE2Zjc5Y2MwYTgwMTY0MDFjNWEzM2JlMDRiZTQ0MQ=="; glide_user_session="U0N2Mjo0MDNhNjAzMWQ3MjMxMTAwMjYxMjUzYjJiMjUyMDM2OTo2ODE2Zjc5Y2MwYTgwMTY0MDFjNWEzM2JlMDRiZTQ0MQ=="
 2014-03-19 11:10:37 (657) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Header: pragma:no-cache
 2014-03-19 11:10:37 (657) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Request Header: cache-control:no-cache
 2014-03-19 11:10:38 (357) REST API-thread-1 SYSTEM [REST API] RouteRegistry : Loaded Routes to Cache
 2014-03-19 11:10:38 (357) REST API-thread-1 SYSTEM DEBUG: [REST API] RouteRegistry : Route loading time 0:00:00.105
 2014-03-19 11:10:38 (357) REST API-thread-1 SYSTEM DEBUG: [REST API] URIHandler : Resolving URI: /now/table/incident
 2014-03-19 11:10:38 (391) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : URI Resolving Duration 387570:10:38.391
 2014-03-19 11:10:38 (424) REST API-thread-1 SYSTEM DEBUG: [REST API] RESTAPIProcessor : Finished initializing REST Request
 2014-03-19 11:10:38 (540) REST API-thread-1 083A6031D7231100261253B2B252035C #28 /api/now/table/incident Parameters -------------------------
 api=api
 2014-03-19 11:10:38 (541) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] RESTAPIProcessor : Processing REST Request /api/now/table/incident
 2014-03-19 11:10:38 (541) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] RESTAPIProcessor : Pre-Service processing duration 0:00:00.000
 2014-03-19 11:10:38 (548) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] ServiceHandler : Invoking Service TableAPIService
 2014-03-19 11:10:38 (552) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] TableAPIService : Inserting record
 2014-03-19 11:10:38 (560) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] RequestDeserializer : Incoming Request Body:{"short_description":"test me"}
 2014-03-19 11:10:39 (508) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] TableAPIService : Glide Record Insert Duration 0:00:00.956
 2014-03-19 11:10:39 (508) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] TableAPIService : Querying for inserted record
 2014-03-19 11:10:39 (513) REST API-thread-1 083A6031D7231100261253B2B252035C #### Compiler Stats ####
 2014-03-19 11:10:39 (514) REST API-thread-1 083A6031D7231100261253B2B252035C Compiles: 600, time: 1,130ms
 2014-03-19 11:10:39 (514) REST API-thread-1 083A6031D7231100261253B2B252035C Cache name: "syscache_expression", max: 8,192, size: 599, seeks: 34,182, hits: 32,980, misses: 1,202, flushed: 0
 2014-03-19 11:10:39 (514) REST API-thread-1 083A6031D7231100261253B2B252035C Total classes: 1,402, bytecode length: 3,263,462
 2014-03-19 11:10:39 (514) REST API-thread-1 083A6031D7231100261253B2B252035C Total loaders created: 601, unloaded: 0, existing: 601
 2014-03-19 11:10:39 (652) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] TableAPIService : Creating service result for insert request
 2014-03-19 11:10:39 (655) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] ServiceHandler : End of Service InvocationTableAPIService
 2014-03-19 11:10:39 (655) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] ServiceHandler : Service Invocation Duration 0:00:01.107
 2014-03-19 11:10:39 (660) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] ServiceHandler : Serializing Response
 2014-03-19 11:10:39 (706) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] ServiceHandler : End of Response Serialization
 2014-03-19 11:10:39 (706) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] ServiceHandler : Response Serialization Duration 0:00:00.046
 2014-03-19 11:10:39 (706) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] RESTAPIProcessor : Service handling duration 0:00:01.165
 2014-03-19 11:10:39 (706) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] RESTAPIProcessor : End of Request Processing
 2014-03-19 11:10:39 (706) REST API-thread-1 083A6031D7231100261253B2B252035C DEBUG: [REST API] RESTAPIProcessor : REST Request Processing time 0:00:01.165
 2014-03-19 11:10:39 (707) REST API-thread-1 083A6031D7231100261253B2B252035C #28 /api/now/table/incident -- total transaction time: 0:00:02.074, total wait time: 0:00:00.001, session wait: 0:00:00.000, semaphore wait: 0:00:00.001, source: 127.0.0.1
```

**Parent Topic:**[REST APIs](c_RESTAPI.md)

