---
title: REST category
description: Verify the functionality of REST calls.This test step begins with the REST API Explorer. Use the REST API Explorer to create and specify the HTTP method, path, query parameters, request headers, and body of a REST request, and then send the REST request to the current instance.Create a test step to send a REST request to the current instance. Specify the HTTP method, path, query parameters, request headers, and body of a REST request.Assert that the HTTP response status code has the specified relationship to the specified value. You specify a numeric value of the status code and the relationship.Assert that the HTTP response status code name has the specified relationship to the specified value. You specify a value of the status code name, and the relationship.Assert that the HTTP response time has the specified relationship to the specified value. You specify a value of the response time and the relationship.Assert the HTTP response header exists, or the header has the specified relationship to the specified value.Assert that the response payload is in valid JSON format.Assert that the response payload is well-formed XML.Assert the XML response payload element exists, or has the specified relationship to the specified value.Assert the JSON response payload element exists, or has the specified relationship to the specified value.Assert the HTTP response payload has the specified relationship to the specified value. You specify the value and the relationship.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Automated Test Framework \(ATF\) test step categories, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# REST category

Verify the functionality of REST calls.

## Send REST Request - Inbound - REST API Explorer

This test step begins with the REST API Explorer. Use the REST API Explorer to create and specify the HTTP method, path, query parameters, request headers, and body of a REST request, and then send the REST request to the current instance.

When you have tested the request, the **Create Automated Test Step** button appears. Click **Create Automated Test Step** to create the test step. This button does not appear until after the request has been sent. You cannot create a test step when the request payload is larger than the maximum request payload size property.

This test step creates the same test record as the **Send REST Request - Inbound** test step. After the test step is created, you cannot go back and use the REST API Explorer to update the test. All changes must be made on the **Send REST Request - Inbound** test step form.

No HTTP response validation is performed as part of this step. The step fails if the response payload size is too big, the request parameters are invalid, or the request could not be sent. Use the assert steps to validate the response.

You cannot use this step to send a request to another instance or third party/remote address.

These inputs are for the REST API Explorer. The fields you see depend upon the API selected. For more information on using REST APIs on your instance, see REST APIs.

<table id="table_bdv_bn1_xy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Namespace

</td><td id="namespace">

Namespace for the request. Select from the list.

</td></tr><tr><td>

API Name

</td><td id="api-name">

API to be used. Select from the list.

</td></tr><tr><td>

API Version

</td><td id="api-version">

API version to be used. Select the version available on your instance from the list.

</td></tr><tr><td>

Path parameters

</td><td id="api-path-parameters">

The part of the path after the API name. Path parameters are generally name-value pairs where the allowable values are in a list.

</td></tr><tr><td>

Query parameters

</td><td id="api-query-parameters">

Name-value pairs of query parameters added to the URI after the path. The REST API Explorer encodes the URI, so it is not necessary to encode query parameters and values.

</td></tr><tr><td>

Request headers

</td><td id="api-request-headers">

Name-value pairs contained in the request header. The authentication header is set to **Send as me** to use the current user's credentials. To use the test step in production, you may need to change the **Authentication Type** field in the **Send REST - Inbound** test step. Do not encode the name or value.

</td></tr><tr><td>

Request Body

</td><td id="api-request-body">

The request content. Some requests do not have a body.

</td></tr></tbody>
</table>## Send REST Request - Inbound

Create a test step to send a REST request to the current instance. Specify the HTTP method, path, query parameters, request headers, and body of a REST request.

No HTTP response validation is performed as part of this step. The step fails if the response payload size is too big, the request parameters are invalid, or the request could not be sent. Use the assert steps to validate the response.

You cannot use this step to send a request to another instance or third party/remote address.

For more information on using REST APIs, see the REST APIs.

<table id="table_gny_jkd_yy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Authentication Type

</td><td>

The type of authentication to use. For public APIs, select **None**.

 To configure basic or mutual authentication, users need the atf\_ws\_designer role. For more information, see [Automated Test Framework roles](atf-roles.md).

</td></tr><tr><td>

Basic authentication

</td><td id="basic-authentication">

The basic authentication profile to use when doing the test. You must create or select a basic authentication profile to assign to test steps to avoid authentication issues when running the test. For more information, see [Create a basic auth profile using the Automated Test Framework](../task/atf-create-basic-auth-profile.md).

</td></tr><tr><td>

Mutual authentication

</td><td>

An X.509 certificate for mutual authentication. You must create or select a client certificate to assign to test steps to avoid authentication issues when running the test. For more information, see Set up Certificate-based authentication.

</td></tr><tr><td>

Method

</td><td id="atf-method-send">

The HTTP method to be used:-   **GET**
-   **POST**
-   **PUT**
-   **DELETE**
-   **PATCH**

</td></tr><tr><td>

Path

</td><td id="atf-path-send">

The path to be used. This field accepts only the portion of the URI after the instance name. If you use `https://<instance name>`, you get an error.

</td></tr><tr><td>

Query Parameters

</td><td id="atf-query-parameters-send">

Query parameter names and values. Do not encode the parameter names or values.

</td></tr><tr><td>

Headers

</td><td id="atf-headers-send">

Header names and values. Do not encode the header names or values.

</td></tr><tr><td>

Body

</td><td id="atf-body-send">

The body of the request.

</td></tr></tbody>
</table>## Assert Status Code

Assert that the HTTP response status code has the specified relationship to the specified value. You specify a numeric value of the status code and the relationship.

Assert steps must immediately follow a **Send REST Request - Inbound** step. You can have multiple REST assert steps following a **Send REST Request - Inbound** step, but the assert steps cannot be separated from the **Send REST Request - Inbound** step by steps from other test categories.

<table id="table_bgl_2b2_yy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Operation

</td><td id="atf-operation">

Comparison to be performed between values:-   **is**
-   **is not**
-   **less than**
-   **greater than**
-   **less than or is**
-   **greater than or is**

</td></tr><tr><td>

Status code

</td><td id="atf-status-code">

Status code to be tested against the response code.

</td></tr></tbody>
</table>## Assert Status Code Name

Assert that the HTTP response status code name has the specified relationship to the specified value. You specify a value of the status code name, and the relationship.

Assert steps must immediately follow a **Send REST Request - Inbound** step. You can have multiple REST assert steps following a **Send REST Request - Inbound** step, but the assert steps cannot be separated from the **Send REST Request - Inbound** step by steps from other test categories.

<table id="atf-assert-status-code-name-table"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Operation

</td><td id="atf-operation-status-code-name">

Comparison to be performed between values:-   **contains**
-   **does not contain**
-   **is**
-   **is not**

</td></tr><tr><td>

Status code name

</td><td id="atf-status-code-name">

Status code name to be tested.

</td></tr></tbody>
</table>## Assert Response Time

Assert that the HTTP response time has the specified relationship to the specified value. You specify a value of the response time and the relationship.

Assert steps must immediately follow a **Send REST Request - Inbound** step. You can have multiple REST assert steps following a **Send REST Request - Inbound** step, but the assert steps cannot be separated from the **Send REST Request - Inbound** step by steps from other test categories.

<table id="atf-assert-response-time-table"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Operation

</td><td id="atf-operation-response-time">

Comparison to be performed between **Response time** entered and actual response time:-   **less than**
-   **greater than**

</td></tr><tr><td>

Response time \(ms\)

</td><td id="atf-response-time">

Time in milliseconds to be compared to the actual response time.

</td></tr></tbody>
</table>## Assert Response Header

Assert the HTTP response header exists, or the header has the specified relationship to the specified value.

Assert steps must immediately follow a **Send REST Request - Inbound** step. You can have multiple REST assert steps following a **Send REST Request - Inbound** step, but the assert steps cannot be separated from the **Send REST Request - Inbound** step by steps from other test categories.

<table id="atf-assert-response-header-table"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Header

</td><td id="atf-header">

Header name.

</td></tr><tr><td>

Operation

</td><td id="atf-operation-assert-header">

Comparison to be performed between values:-   **contains**
-   **does not contain**
-   **is**
-   **is not**
-   **is not empty**

</td></tr><tr><td>

Value

</td><td id="atf-value">

Element value to be used in the test. Not shown if the **Operation** is **is not empty**.

</td></tr></tbody>
</table>## Assert Response JSON Payload is Valid

Assert that the response payload is in valid JSON format.

Assert steps must immediately follow a **Send REST Request - Inbound** step. You can have multiple REST assert steps following a **Send REST Request - Inbound** step, but the assert steps cannot be separated from the **Send REST Request - Inbound** step by steps from other test categories.

<table id="table_mcf_sxq_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr></tbody>
</table>## Assert Response XML Payload is Well-Formed

Assert that the response payload is well-formed XML.

Assert steps must immediately follow a **Send REST Request - Inbound** step. You can have multiple REST assert steps following a **Send REST Request - Inbound** step, but the assert steps cannot be separated from the **Send REST Request - Inbound** step by steps from other test categories.

<table id="table_kg2_hyq_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr></tbody>
</table>## Assert XML Payload Element

Assert the XML response payload element exists, or has the specified relationship to the specified value.

Assert steps must immediately follow a **Send REST Request - Inbound** step. You can have multiple REST assert steps following a **Send REST Request - Inbound** step, but the assert steps cannot be separated from the **Send REST Request - Inbound** step by steps from other test categories.

<table id="assert-xml-response-payload-element-table"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Element path

</td><td id="atf-element-path">

XML path to the element to be evaluated. For example, `/result/short_description` for```
{
  "result": {
    "number": "INC0020001",
    "short_description": "test"
  }
}
```

</td></tr><tr><td>

Operation

</td><td id="atf-operation-assert-header">

Comparison to be performed between values:-   **contains**
-   **does not contain**
-   **is**
-   **is not**
-   **is not empty**

</td></tr><tr><td>

Value

</td><td id="atf-value">

Element value to be used in the test. Not shown if the **Operation** is **is not empty**.

</td></tr></tbody>
</table>## Assert JSON Response Payload Element

Assert the JSON response payload element exists, or has the specified relationship to the specified value.

Assert steps must immediately follow a **Send REST Request - Inbound** step. You can have multiple REST assert steps following a **Send REST Request - Inbound** step, but the assert steps cannot be separated from the **Send REST Request - Inbound** step by steps from other test categories.

<table id="assert-json-response-payload-element-table"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Element path

</td><td id="atf-json-element-path">

SNC path to the element to be evaluated. For example, `/result/short_description` for```
{
  "result": {
    "number": "INC0020001",
    "short_description": "test"
  }
}
```

 See Importing JSON files for more information.

</td></tr><tr><td>

Operation

</td><td id="atf-operation-assert-header">

Comparison to be performed between values:-   **contains**
-   **does not contain**
-   **is**
-   **is not**
-   **is not empty**

</td></tr><tr><td>

Value

</td><td id="atf-value">

Element value to be used in the test. Not shown if the **Operation** is **is not empty**.

</td></tr></tbody>
</table>## Assert Response Payload

Assert the HTTP response payload has the specified relationship to the specified value. You specify the value and the relationship.

Assert steps must immediately follow a **Send REST Request - Inbound** step. You can have multiple REST assert steps following a **Send REST Request - Inbound** step, but the assert steps cannot be separated from the **Send REST Request - Inbound** step by steps from other test categories.

**Note:** The entire payload is used to look for a match. A large payload can affect performance.

<table id="assert-response-payload-table"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Operation

</td><td id="atf-operation-assert-header">

Comparison to be performed between values:-   **contains**
-   **does not contain**
-   **is**
-   **is not**
-   **is not empty**

</td></tr><tr><td>

Response body

</td><td id="atf-response-body">

The value of the response body to be used in the test.Must contain the name and value to be compared as it appears in the response payload. Must not contain any curly braces.

 Not shown if the **Operation** is **is not empty**.

</td></tr></tbody>
</table>To check the short description in the response payload

```
{"result":{"number":"INC0010040","short_description":"Test ATF Incident"}}
```

the **Response body** should contain

```
"short_description":"Test ATF Incident"
```

These formats are incorrect and the step fails.

-   `{"short_description":"Test ATF Incident"}`
-   `"{"short_description":"Test ATF Incident"}"`
-   `short_description: Test ATF Incident`
-   `short_description:"Test ATF Incident"`

