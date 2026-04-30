---
title: Controlling maximum request size
description: You can specify the maximum file size allowed in a scripted REST API request payload.
locale: en-US
release: xanadu
product: REST API Explorer
classification: rest-api-explorer
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Controlling maximum request size

You can specify the maximum file size allowed in a scripted REST API request payload.

The file size limit applies when accessing any of the following variables or functions from a RESTAPIRequestBody object.

-   data
-   dataString
-   nextEntry\(\)
-   hasNext\(\)

Accessing these variables or functions with a request payload that exceeds the maximum size causes the service to respond with error code 400.

The file size limit does not apply when accessing the dataStream variable.

## Maximum request size properties

Several properties control the maximum allowed request size. Add these properties to the System Properties \[sys\_properties\] table to specify a maximum request size.

<table id="table_rwj_2m2_ht"><thead><tr><th>

Property

</th><th>

Default value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.rest.scripted.max\_inbound\_content\_length\_mb

</td><td>

10

</td><td>

The maximum size, in megabytes, for a scripted REST request body that is not gzipped.

</td></tr><tr><td>

glide.rest.scripted.max\_inbound\_gzip\_content\_length\_mb

</td><td>

1

</td><td>

The maximum size, in megabytes, for a scripted REST request body that is gzipped.

</td></tr><tr><td>

glide.rest.max\_content\_length

</td><td>

10

</td><td>

The maximum size, in megabytes, for a scripted REST request body, whether or not it is gzipped.

 Maximum: 25

 As a result, even if **glide.rest.scripted.max\_inbound\_content\_length\_mb** or **glide.rest.scripted.max\_inbound\_gzip\_content\_length\_mb** are set, the request body is limited to the value of **glide.rest.max\_content\_length**.

</td></tr></tbody>
</table>**Parent Topic:**[Create a scripted REST API](../task/t_CreateAScriptedRESTService.md)

