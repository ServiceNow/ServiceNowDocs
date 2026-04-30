---
title: REST API trigger
description: Start a flow from an inbound API call or webhook from an external system. Configure the trigger start conditions without having to write or maintain custom code.Create a flow that starts when a third-party system sends a REST request to your instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# REST API trigger

Start a flow from an inbound API call or webhook from an external system. Configure the trigger start conditions without having to write or maintain custom code.

For example, you can create a flow that starts when a third-party IT ticket tracking system sends an inbound request to the instance. You can then parse the data from the inbound REST request into a complex data object and use the values to open an Incident on your instance.

Once you activate the flow, the endpoint that you created appears in the API explorer under the namespace you created. You can use this page to help define the webhook in your third-party system and to test your flow.

To learn more about flow triggers, see [Workflow Studio trigger types](https://www.servicenow.com/docs/access?context=flow-triggers&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Note:**

-   Use the REST API Trigger to start flows from REST calls from external systems. To start a flow from a script or API call from the same instance, use a subflow, code snippet, or Workflow Studio API. See [API access to Workflow Studio](https://www.servicenow.com/docs/access?context=api-access-flow-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) and [Create code snippets for flows, sub-flows, and actions](https://www.servicenow.com/docs/access?context=flow-design-code-snippet&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).
-   ServiceNow has partnered with Boomi to deliver Boomi API Management, a cloud-based platform that enables customers to discover, manage, secure, and monetize their APIs. Boomi supports full lifecycle API management, including governance, analytics, and API security.

    Boomi provides [documentation](https://help.boomi.com/docs/Atomsphere/API%20Management/api-links) though their own portal, and customers requesting support with Boomi API Management will contact the Boomi support through their standard channels.

    To get started, see the Boomi API Management listing on the [ServiceNow® Store](https://store.servicenow.com/), which includes information about entitlements and required plugins, as well as a link to the [Boomi API Management documentation](https://help.boomi.com/docs/Atomsphere/API%20Management/api-links).


## Available data pills

Depending on how you configure the endpoint, flow designers have access to these data pills from the trigger:

-   **Path Parameters**

    An object containing path parameters in the inbound request.

-   **Query Parameters**

    An object containing query parameters in the inbound request.

-   **Request Headers**

    An object containing headers in the inbound request.

-   **Request Body**

    Complex data object that defines the body structure of the inbound request. For more information on complex objects, see [Complex data](https://www.servicenow.com/docs/access?context=complex-data&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


When setting up the trigger, define what the inbound data will look like. You can then use the associated data pills within the actions in your flow. When the system receives an inbound request that starts the flow, it uses the runtime values sent in the request.

**Parent Topic:**[Building integrations in Integration Hub](building-integrations-ih.md)

## Create a flow using the REST API trigger

Create a flow that starts when a third-party system sends a REST request to your instance.

### Before you begin

Role required: flow\_designer or admin.

This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

### Procedure

1.  Open Workflow Studio and create a flow.

    See [Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

    Keep in mind that the scope of your flow is included in the REST endpoint you create.

2.  In the **TRIGGER** section, select the **REST API - Asynchronous** trigger.

3.  In the **HTTP Method** field, set the HTTP method for the endpoint.

    Options include:

    -   POST
    -   GET
    -   DELETE
    -   PUT
    -   PATCH
4.  Create any path parameters required for the endpoint and add them to the relative path in the **Path** field.

    The relative path to the endpoint is in the format `/api/<flow-application-scope>/<flow-name>/<path-parameters>`.

    You can click **Copy** to copy the full path to the endpoint. Use this path when configuring the endpoint for the REST call in your third-party system.

    ![](../images/rest-trigger-path.png)

    1.  Create variables in the **Path Parameters** section.

    2.  Drag the data pill that represents the path parameter into the empty input in the **Path** field.

        This field only accepts data pills from the **Path Parameters** section.

        ![](../images/rest-trigger-path-arrows.png)

5.  Select **Requires authentication** to require authentication headers in the inbound REST request.

6.  If **Requires authentication** is selected, add the roles required to authorize the request in the **Requires roles** field.

7.  In the **Body** field under the **Request Content** section, create a complex data object that defines the body structure of the inbound request.

    For more information on building a complex object, see [Complex data](https://www.servicenow.com/docs/access?context=complex-data&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

    **Note:** The **Request Content** section only appears when the **HTTP Method** is POST, PUT, or PATCH.

    This example body finds the Description field in an inbound payload that contains ticket information from a third-party ticket-tracking system.

    ![](../images/rest-trigger-body.png)

8.  In the **Headers** field, define the headers to be sent in the inbound request.

    You can select **Required** to require that the inbound request include them.

9.  In the **Query Parameters** field, define the query parameters to be sent in the inbound request.

    You can select **Required** to require that the inbound request include them.

10. Add actions to your flow that execute when the endpoint is called.

    You can use the data pills from the REST API trigger in your flow actions.

    This action creates an Incident record and maps the Description and Assignment Group fields from the incoming payload to the Incident.

    ![](../images/rest-trigger-action.png)

11. Test and activate the flow.

    For more information, see [Test a flow](https://www.servicenow.com/docs/access?context=flow-test&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) and [Activate a flow](https://www.servicenow.com/docs/access?context=flow-activate&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

    Once activated, the endpoint displays in the REST API Explorer. You can use this page to further test your endpoint, or configure the request from your third-party system.

    ![](../images/rest-trigger-api-explorer.png)

12. Configure the REST request from your third-party system.

    For example, you can send this cURL request to trigger the flow defined in previous steps.

    ```
    curl "https:your-instance.servicenow.com/api/snc/create_incident_from_external_event/assignment_group/287ebd7da9fe198100f92cc8d1d2154e" \
    --request POST \
    --header "Accept:application/json" \
    --header "Content-Type:application/json" \
    --data "{
    fields: {
       description: \"Major outage with data loss\"
       }
    }" \
    --user 'username':'password'
    ```


### Result

The flow executes and the REST request returns the execution ID.

```
{
  "result": {
    "executionId": "ndoxeRhshDSezldeGfbYlviFSeFnBjCO"
  }
}
```

### What to do next

Copy the execution ID in the result and navigate to the Executions tab in Flow Designer. You can filter by execution ID to locate the execution details and view the status of the execution.

![](../images/rest-trigger-execution.png)

To troubleshoot issues, you can debug the REST query or check the flow execution details. See [Debug REST queries](https://www.servicenow.com/docs/access?context=debugging-rest-queries&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) and [Flow execution details](https://www.servicenow.com/docs/access?context=flow-execution-details&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

