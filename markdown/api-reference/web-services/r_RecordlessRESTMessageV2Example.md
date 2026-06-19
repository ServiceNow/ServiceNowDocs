---
title: Recordless RESTMessageV2 example
description: You can use the RESTMessageV2\(\) constructor with no parameters to define a REST message entirely in the script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/r\_RecordlessRESTMessageV2Example.html
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scripting, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# Recordless RESTMessageV2 example

You can use the RESTMessageV2\(\) constructor with no parameters to define a REST message entirely in the script.

When using this constructor you must provide an endpoint and HTTP method. In this example, the script creates an empty REST message and sets the values needed to insert an incident record.

```
var restMessage = new sn_ws.RESTMessageV2();
restMessage.setBasicAuth("admin", "admin");
restMessage.setHttpMethod("post");
restMessage.setEndpoint("http://<instance>.service-now.com/api/now/table/incident");
restMessage.setRequestBody("{\"short_description\" : \"Test incident\"}");
var response = restMessage.execute();
```

**Parent Topic:**[Scripting outbound REST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_ScriptingOutboundREST.md)

