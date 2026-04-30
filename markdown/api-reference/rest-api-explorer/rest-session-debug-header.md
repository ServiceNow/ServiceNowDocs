---
title: Return session debug logs in a REST response
description: You can include session debug logs in a REST response body by passing the X-WantSessionDebugMessages header in the request.
locale: en-US
release: xanadu
product: REST API Explorer
classification: rest-api-explorer
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# Return session debug logs in a REST response

You can include session debug logs in a REST response body by passing the X-WantSessionDebugMessages header in the request.

To return session debug messages when session debugging is enabled for the current session, set the header X-WantSessionDebugMessages to **true** in the REST request.

**Note:** You must enable session debugging before sending this header.

## Request

This example demonstrates a Table API request made using REST API Explorer with **Session Debug SQL** enabled.

```
GET api/now/table/incident/9c573169c611228700193229fff72400
X-WantSessionDebugMessages:true
Content-Type: application/json;charset=UTF-8
Accept: application/json, text/plain,*/*
X-UserToken: <user token>
```

## Response body

```
{
  "result":{
    "description":"User can't access email on mail.company.com.",
    "number":"INC0000001"
  },
  "session":{
    "debug_logs":[
       {
         "type":"sql",
         "customerUpdate":false,
         "line":"17:17:27.777: Time: 0:00:00.000 for: glide_master_db[glide.5] ..... sys_user_session0.`id` = '3BEA7001EB230200C46AC2EEF106FE2A'</span>",
         "debugClassSet":""
       },
      {
        "type":"sql",
        "customerUpdate":false,
        "line":"17:17:27.779: Time: 0:00:00.002 for: glide_master_db[glide.6]  ... `sys_id` = '7fea7001eb230200c46ac2eef106fe2a'</span>",
        "debugClassSet":""
       }
    ]
  }
}
```

**Parent Topic:**[REST APIs](c_RESTAPI.md)

**Related topics**  


[Session debug](../../../script/debugging/concept/c_SessionDebug.md#)

