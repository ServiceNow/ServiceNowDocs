---
title: Use the Post component
description: Perform a POST request to a server by providing the request using the Post component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [HTTP, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Post component

Perform a POST request to a server by providing the request using the Post component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Post component. For more information about these properties, see [Properties of the HTTP components](../reference/properties-http-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **HTTP**.

2.  Drag the Post component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Post component to the corresponding ports of the other components as described in the following table:

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port Name

</th><th>

Port type

</th><th>

Data type

</th><th>

Purpose of connection

</th><th>

Mandatory

</th></tr></thead><tbody><tr><td>

URL

</td><td>

Data In

</td><td>

String

</td><td>

Takes the URL where the content will be posted from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Data

</td><td>

Data In

</td><td>

Object

</td><td>

Takes the data the component posts from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

ContentType

</td><td>

Data In

</td><td>

String

</td><td>

Takes the content type such as JSON or XML from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

RequestTimeout

</td><td>

Data In

</td><td>

Integer

</td><td>

Time value in seconds to timeout the request. If the post request does not work after the timeout value that you set, the request fails and a connection timeout exception is displayed. The default timeout value is 100 seconds.

</td><td>

Optional

</td></tr><tr><td>

Status

</td><td>

Data In

</td><td>

String

</td><td>

Takes status of the content from a previously executed component.

</td><td>

Yes

</td></tr><tr><td>

Response

</td><td>

Data Out

</td><td>

Object

</td><td>

Returns the status of the POST operation.

</td><td>

Yes.To preview the data, right-click the **Status** and **Response** fields and click **Preview Data**.

</td></tr><tr><td>

NA

</td><td>

Control In

</td><td>

 

</td><td>

Connects to the Control Out port of one or more components.

</td><td>

Yes

</td></tr><tr><td>

NA

</td><td>

Control Out

</td><td>

 

</td><td>

Connects to the Control In port of another component or the default end component.

</td><td>

Optional

</td></tr></tbody>
</table>5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[HTTP](../concept/http.md)

