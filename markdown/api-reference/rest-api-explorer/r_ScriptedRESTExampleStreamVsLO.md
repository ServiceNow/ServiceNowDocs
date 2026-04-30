---
title: Scripted REST API example - streaming vs object serialization
description: These examples demonstrate how to send a JSON response using streaming and using default object serialization.
locale: en-US
release: xanadu
product: REST API Explorer
classification: rest-api-explorer
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Scripted REST API examples, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Scripted REST API example - streaming vs object serialization

These examples demonstrate how to send a JSON response using streaming and using default object serialization.

## Streaming vs object serialization

When sending a response, you can send a response as a stream or serialize an object. There are advantages and disadvantages to either approach. Pick a technique based on the needs of your integration.

Generally, if the response object is simple, can be represented as XML or JSON, and is a consistent size, use object serialization. If using a format other than XML or JSON or if the size of the response varies, use streaming.

## Streaming the response

Using a streaming responses provides advantages in response time, instance performance, and content flexibility, but adds additional complexity to the script. When using streaming, you are responsible for formatting the response, setting the response status, and setting the Content-Type header. When streaming a response, the requesting user receives a response quickly because the entire response does not need to be created before starting streaming.

This example demonstrates a Scripted REST Resource script that returns an array of incident records using streaming.

```
/**
 *  Sample Scripted REST Resource that returns custom JSON objects with properties from Incident GlideRecords
 *  This sample uses ServiceNow JavaScript API to query incident records
 *  and then iterates over those records to build and stream a custom JSON object that 
 *  includes some values from the incidents
 */
(function runOperation(/*RESTServiceRequest*/ request, /*RESTServiceResult*/ response) {
    var writer = response.getStreamWriter(),
        hdrs = {},
        table = 'incident',
        record_limit = 100,
        gr = new GlideRecord(table);


    hdrs['Content-Type'] = 'application/json';
    response.setStatus(200);
    response.setHeaders(hdrs);

    gr.setLimit(record_limit);
    gr.query();

    //  start building response object
    writer.writeString("{\"results\":[");


    //  iterate over incident records and build JSON representations to be streamed out.
    while (gr.next()) {
        var incidentObj = {};

        incidentObj.number = gr.number + '';
        incidentObj.short_description = gr.short_description + '';
        writer.writeString(global.JSON.stringify(incidentObj));

        if (gr.hasNext()) {
            writer.writeString(",");
        }
    }

    //  close the response object
    writer.writeString("]}");
})(request, response);

```

A request to this resource returns the following response.

```

//  sample response
/*
 HTTP/1.1 200 OK
 Content-Type: application/json
 Server: ServiceNow

  // sample response number of records returned has been truncated for this example

 {
 "results": [
 {
 "number": "INC0011301",
 "short_description": "lorem ipsum short description 0 my new incident"
 },
 {
 "number": "INC0011302",
 "short_description": "lorem ipsum short description 1 my new incident"
 },
 {
 "number": "INC0011303",
 "short_description": "lorem ipsum short description 2 my new incident"
 },
 {
 "number": "INC0011304",
 "short_description": "lorem ipsum short description 3 my new incident"
 },
 {
 "number": "INC0011309",
 "short_description": "lorem ipsum short description 8 my new incident"
 },
 {
 "number": "INC0011310",
 "short_description": "lorem ipsum short description 9 my new incident"
 },
 {
 "number": "INC0011311",
 "short_description": "lorem ipsum short description 0 my new incident"
 },
 {
 "number": "INC0011312",
 "short_description": "lorem ipsum short description 1 my new incident"
 },
 {
 "number": "INC0011313",
 "short_description": "lorem ipsum short description 2 my new incident"
 },
 {
 "number": "INC0011314",
 "short_description": "lorem ipsum short description 3 my new incident"
 },
 {
 "number": "INC0011315",
 "short_description": "lorem ipsum short description 4 my new incident"
 },
 {
 "number": "INC0011326",
 "short_description": "lorem ipsum short description 15 my new incident"
 }
 ]
 }
 */

```

## Streaming pagination

To paginate large tables so that you only send a limited number of records per query, use the [Scoped GlideRecord - chooseWindow\(Number firstRow, Number lastRow, Boolean forceCount\)](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#) method. The Community article [Paginated Glide Record + Expanded GR Method Support](https://www.servicenow.com/community/developer-articles/paginated-glide-record-expanded-gr-method-support/ta-p/2300446) exemplifies how to use chooseWindow\(\) to achieve pagination, which you can adapt to your own particular use case.

## Building an object

Using object serialization allows you to take advantage of ServiceNow provided serialization and content negotiation. When serializing an object instead of streaming, the entire object must be created and serialized before the client receives a response. This may delay the response, or require a large amount of system resources if the response object is very large. Object serialization is available only for XML or JSON responses. Responses using a different format must use streaming.

This example returns the same Incident data as the streaming example, but collects all of the response data in an array before sending the response.

```
/**
 *  Sample Scripted REST Resource returns an array of custom JSON objects that include 2 incident properties.
 *  This sample uses ServiceNow JavaScript API to query incident records and then iterates
 *  over those records building a custom JSON object that includes 2 values from the incident records.
 *  note that because we are returning a simple JSON object we can rely on built in serialization
 *  to set the content-type header as well as response status. The 'result_arr' object will not be returned
 *  until it has been completely built and stored
 */
(function runOperation(/*RESTServiceRequest*/ request, /*RESTServiceResult*/ response) {
    var table = 'incident',
        record_limit = 100,
        result_arr = [],
        gr = new GlideRecord(table);


    gr.setLimit(record_limit);
    gr.query();


    //  iterate over incident records and build JSON representations to be streamed out.
    while (gr.next()) {
        var incidentObj = {};

        incidentObj.number = gr.number + '';
        incidentObj.short_description = gr.short_description + '';

        result_arr.push(incidentObj);
    }

    return result_arr;
})(request, response);

```

A request to this resource returns the following response.

```

/*
 HTTP/1.1 200 OK
 Content-Type: application/json;charset=UTF-8
 Server: ServiceNow

 // sample response number of records returned has been truncated for this example

 {
 "result": [{
 "short_description": "lorem ipsum short description 0 my new incident",
 "number": "INC0011301"
 }, {
 "short_description": "lorem ipsum short description 1 my new incident",
 "number": "INC0011302"
 }, {
 "short_description": "lorem ipsum short description 2 my new incident",
 "number": "INC0011303"
 }, {
 "short_description": "lorem ipsum short description 3 my new incident",
 "number": "INC0011304"
 }, {
 "short_description": "lorem ipsum short description 4 my new incident",
 "number": "INC0011305"
 }, {
 "short_description": "lorem ipsum short description 5 my new incident",
 "number": "INC0011306"
 }, {
 "short_description": "lorem ipsum short description 6 my new incident",
 "number": "INC0011307"
 }, {
 "short_description": "lorem ipsum short description 7 my new incident",
 "number": "INC0011308"
 }, {
 "short_description": "lorem ipsum short description 8 my new incident",
 "number": "INC0011309"
 }, {
 "short_description": "lorem ipsum short description 9 my new incident",
 "number": "INC0011310"
 }]
 }
 */

```

**Parent Topic:**[Scripted REST API examples](../concept/c_ScriptedRESTAPIExamples.md)

