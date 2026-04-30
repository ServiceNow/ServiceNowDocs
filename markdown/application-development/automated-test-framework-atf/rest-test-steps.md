---
title: REST test steps
description: Test custom inbound web services and backwards compatibility by making REST calls.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server test steps, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# REST test steps

Test custom inbound web services and backwards compatibility by making REST calls.

REST requests can only be sent to the current instance. You cannot send a request to another instance or third-party at a remote address.

The REST test configuration only supports the XML and JSON response formats. Binary formats are not supported.

You can create tests that include steps from each of the test step configuration categories. The REST test configuration category contains the Send REST Request - Inbound and assert test configurations. Assert steps must immediately follow a **Send REST Request - Inbound** step. You can have multiple REST assert steps following a **Send REST Request - Inbound** step, but the assert steps cannot be separated from the **Send REST Request - Inbound** step by steps from other test categories. For more information about the REST test steps, see [REST category](../reference/test-steps-rest-category.md#).

## Authentication

As part of the Automated Test Framework, there are two situations when you send REST requests:

-   When you use the REST API Explorer to create and test a request
-   When you run a test that contains a **Send REST Request - Inbound** step

When you use the REST API Explorer to create and test a request, and the request requires authentication, the REST API Explorer uses your credentials. When the ATF runs the test, the REST API Explorer uses the credentials of the user who scheduled the test. This means that a test might fail unintentionally because of the difference in privileges between the user who created the test and the user who runs the test.

To address the issue of user credentials, you can create a basic-authentication profile for a test user and then on the **Send REST Request - Inbound** form, specify that the profile be used when the test is run.

**Parent Topic:**[Server test steps](server-test-steps.md)

