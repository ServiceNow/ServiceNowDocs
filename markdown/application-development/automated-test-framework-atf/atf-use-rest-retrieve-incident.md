---
title: Automated Test Framework use case: retrieve an incident using REST-Inbound
description: The Get Newly Created Resource via REST API Test test is provided with the Automated Test Framework, and uses the REST - Inbound and assert steps.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Automated Test Framework use case examples, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Automated Test Framework use case: retrieve an incident using REST-Inbound

The **Get Newly Created Resource via REST API Test** test is provided with the Automated Test Framework, and uses the REST - Inbound and assert steps.

## Before you begin

Review the REST APIs and the [Send REST Request- Inbound- REST API Explorer](../reference/test-steps-rest-category.md#) configuration step information before creating this test.

Role required: atf\_ws\_designer

## About this task

This test creates an incident record, uses a REST- Inbound step to retrieve the record, and then uses assert steps to determine whether the request was successful.

You can use the Send REST Request- Inbound REST API Explorer step to build and test the request, or you can manually create the request using the Send REST Request- Inbound step. In either case, you must specify the basic authentication information on the Send REST Request- Inbound step form.

When creating your test, start with your REST API and determine what behavior you want to validate. You can then determine what test data to create. You can use other test step configuration categories to create, update, or delete records, and then use a Send REST Inbound step to retrieve, update, or delete the test data. Conversely, you can use the Send REST Inbound step to create records, and then use other test step configuration categories to validate that the records were created correctly.

This task steps you through creating the **Get Newly Created Resource via REST API Test** test.

## Procedure

1.  Create a test.

    1.  Navigate to **Automated Test Framework** &gt; **Tests**, click **New**.

        The **Test** new record form is shown.

    2.  Enter a test name and a description, and click **Submit**.

    3.  Click the test created in the previous step.

        The **Test** form is shown.

2.  Create test data.

    1.  Click the **Add Test Step** button.

        The **Add Test Step** form is shown.

    2.  Click a test configuration category, and then click a test configuration.

        To replicate the **Get Newly Created Resource via REST API Test** test, click **Server** &gt; **Record Insert**, and then **Next**.

        The test configuration form you selected is shown.

    3.  Fill in the information needed for the test configuration you selected.

        To replicate the **Get Newly Created Resource via REST API Test** test, on the **Record Insert** form, specify the incident table, and add a value for the **Short description** field, and click **Submit**.

3.  Create the REST request.

    1.  Click the **Add Test Step** button.

        The **Add Test Step** form is shown.

    2.  Click a test configuration category, and then click a test configuration.

        To replicate the **Get Newly Created Resource via REST API Test** test, click **REST** &gt; **Send REST Request - Inbound REST API Explorer**, and then **Next**.

        The **REST API Explorer** is shown.

    3.  Fill in the information needed for the REST request, and click **Send**.

        To replicate the **Get Newly Created Resource via REST API Test** test, fill in the fields.

        |Name|Value|
        |----|-----|
        |Namespace|now|
        |API Name|Table API|
        |API Version|latest|
        |tableName|incident|

        When you do not specify the **Basic authentication**, the REST API Explorer uses your credentials.

        The **Create Automated Test Step** is shown after you click **Send**.

    4.  When ready, click **Create Automated Test Step**.

        The Send REST Request - Inbound test step is created.

    5.  Click the Send REST Request - Inbound step, and in the **Basic authentication** field, specify a basic auth configuration.

        If no configurations are available, you can create a basic auth configuration by clicking **New** on the **Basic Auth Configurations** form.

    6.  To replicate the **Get Newly Created Resource via REST API Test** test, in the **Path** field, click the contextual search button, and then click **Record Insert** &gt; **Record**.

    7.  Click **Update**.

4.  Create assert steps to verify the REST response.

    1.  Click the **Add Test Step** button.

        The **Add Test Step** form is shown.

    2.  Click a test configuration category, and then click a test configuration.

        To replicate the **Get Newly Created Resource via REST API Test** test, click **REST** &gt; **Assert Status Code**, and then **Next**.

        The **Assert Status Code** form is shown.

    3.  Enter the information needed for the form, and click **Submit**.

        To replicate the **Get Newly Created Resource via REST API Test** test, in the **Operation** field, select **is** and in the **Status Code** field, enter **200**.

        To replicate the **Get Newly Created Resource via REST API Test** test, repeat this step to create **Assert Response JSON Payload is Valid**, and **Assert JSON Response Payload Element** test steps.


**Parent Topic:**[Automated Test Framework use case examples](../concept/atf-use-cases.md)

