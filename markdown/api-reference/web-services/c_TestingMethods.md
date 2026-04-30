---
title: Testing REST message HTTP methods
description: Test an HTTP method for an outbound REST message to ensure that the request is valid and the response returns as expected.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Define a REST message HTTP method, Create a REST message, Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Testing REST message HTTP methods

Test an HTTP method for an outbound REST message to ensure that the request is valid and the response returns as expected.

## Before you begin

Role required: web\_service\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message**.

2.  Select the REST message with an HTTP method to test.

3.  In the HTTP Methods related list, select the HTTP method to test.

4.  Under Related Links, select **Test**.

    If the HTTP method includes variables, the **Test value** for each variable in the **Variable Substitutions** related list is used when testing the method.

    Each test run displays the response status, such as 200 for a successful GET request, the full endpoint URL, any parameters passed in the request, and the response body.

    **Note:** Fields on the Test Runs form are for information only; changes to these fields do not apply to the REST message or HTTP method. Do not modify these values when testing different REST message configurations. Instead, update the REST message or HTTP method, then run a new test.


## Result

Completed test runs for an HTTP method appear in the **Test Runs** related list. If there was an error during the request, the **Error Code** and **Error Message** fields appear.

**Parent Topic:**[Define a REST message HTTP method](../task/t_DefineAnHTTPMethod.md)

