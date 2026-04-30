---
title: Provide input values for your API connector
description: Provide input parameters to make a valid API call, test the connection, and receive a sample response.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-12-05"
reading_time_minutes: 2
breadcrumb: [Creating your own API connector, Use the workspace, Security Posture Control, Security Operations]
---

# Provide input values for your API connector

Provide input parameters to make a valid API call, test the connection, and receive a sample response.

## Before you begin

For all templates, you can select the information icon \(![lower case letter i for more information](../../../reuse/icons/product-icons/circle-info-outline-24.svg)\) to learn more about each parameter. You can use the API samples provided with each template. After you define your input parameters, you must test your connection.

Roles required:

-   sn\_sec\_spc\_core.developer
-   sn\_spc\_cxf.admin - required for advanced scripting

## Procedure

1.  Fill in the fields.

    **Note:** If you change any input parameters after testing the connection, you must test the connection again before you can continue on to [Map API response to SPC attributes](spc-sgc-stepper-5.md).

<table id="table_j1c_st4_sfc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Object list path

</td><td>

Path to the list of assets in the response payload.

</td><td>

An example: `$.list`

</td></tr><tr><td>

API endpoint relative path

</td><td>

This is the path to the API without the host URL.

</td><td>

An example: `/r2`

</td></tr><tr><td>

API query parameters

</td><td>

Key-value pairs that are appended to the API URL for filtering. Values can be strings, scripts, or references to fields in the credential table.

</td><td>

An example:

 Name \[name of query parameter\]

 Value type \[Static values\]

 Value \[a string\]

</td></tr><tr><td>

Pagination parameters

</td><td>

Dynamic parameters used to retrieve subsequent pages of API data. Specify the parameter name, its location in the request \(Query, Header, or Body\), the path to extract its next value from the API response, and an optional default value.

</td><td>

An example of pagination type Offset:

 Offset

 Parameter name \[start\]

 Location in API request \[Query parameters\]

 Default value \[0\]

 Limit

 Parameter name \[count\]

 Location in API request \[Query parameters\]

 Default value \[5\]

</td></tr><tr><td>

\(Optional\) Add parameter

</td><td>

Add custom parameters

</td><td>

Select **Add parameter** to define your own parameters.For example, you might want to determine if there are additional pages of data that are included in the API response.

Parameter name \[hasMore\]

Path in API response \[$.hasMore\]

Location in API request \[Header parameters\]

Default value \[1\]

</td></tr></tbody>
</table>2.  When you’re satisfied with your API input, select **Get sample response**.

    After a few moments, a message is displayed if the connection was successful.

    If you entered your parameters manually for this step, the data imported from the connection test that is rendered in the sample response is authentic and you can use it in the next step to help you map parameters.

3.  Select **Save and continue** to save your edits.

    You must save your changes before you can continue.


