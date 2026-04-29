---
title: Data Stream actions and pagination
description: Send REST, SOAP, or JDBC requests from Workflow Studio to APIs that return a stream of response data larger than 10 MB, or that return paginated results. Parse stream data into a series of complex object outputs and use the data pills in other actions in a flow.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Build integrations, Integration Hub, Workflow Data Fabric]
---

# Data Stream actions and pagination

Send REST, SOAP, or JDBC requests from Workflow Studio to APIs that return a stream of response data larger than 10 MB, or that return paginated results. Parse stream data into a series of complex object outputs and use the data pills in other actions in a flow.

For example, create a Data Stream action to import a large quantity of employee data from a third-party HR site. The Data Stream action sends a REST request to the third-party site and processes the response to populate records in the User \[sys\_user\] table.

**Note:** Data Stream actions require an Integration Hub subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Benefits

Data Stream actions offer these benefits.

-   Parse and format a stream of response data larger than 10 MB.
-   Automatically send multiple requests to APIs that paginate results, if applicable.
-   Can be used in [Integration Hub - Import](integrationhub-imports.md) and to [create a data source](../../import-sets/task/create-data-stream-data-source.md).
-   Enable flow designers to process large requests without complex coding or configuration.
-   Enable flow designers to process each object within a data stream using **For each** flow logic. For example, you might create a Data Stream action that imports document data from a third-party site. When you add the action to a flow, Workflow Studio automatically adds the action to a **For each** flow logic block, enabling flow designers to easily create a record in ServiceNow for each object in the data stream. See [Use a Data Stream action in a flow](../tasks/use-data-stream-in-flow.md).
-   Enable flow designers to reuse Data Stream actions in multiple flows, using the same source of data in multiple ways.

## Running a Data Stream action

There are two ways to run a Data Stream action.

-   **From a flow**

    You can process each object within a data stream using **For each** flow logic. For example, you might create a Data Stream action that imports document data from a third-party site. When you add the action to a flow, Workflow Studio automatically adds the action to a **For each** flow logic block, enabling flow designers to easily create a record in ServiceNow for each object in the data stream. See [Use a Data Stream action in a flow](../tasks/use-data-stream-in-flow.md).

-   **From a script**

    You can start a Data Stream using the executeDataStreamAction\(\) method in the FlowAPI class. For more information, see [FlowAPI](https://www.servicenow.com/docs/access?context=ScriptableFlowAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).


## Action outline

Data Stream actions follow a set structure. Follow prompts to add and remove steps from the action outline. You cannot manually add steps to a Data Stream action.

![REST and SOAP Data Stream action.](../images/datastreamactions.gif "REST and SOAP Data Stream actions")

![JDBC Data Stream action](../images/jdbc-data-stream.gif "JDBC Data Stream action")

**Note:** Clearing an option in a configuration page removes the step from the Data Stream outline and deletes all data associated with the step.

## Action error evaluation

Use [error evaluation](https://www.servicenow.com/docs/access?context=action-error-evaluation&version=australia&pubname=australia-build-workflows&ft:locale=en-US) to catch step errors and specify the error behavior of each step you add to a data stream action. You can also create your own error conditions by specifying when an action returns an error state as well as the status codes and messages they return.

## Action Preprocessing

Use the Action Preprocessing category to retrieve connection and credential details or to run a preprocessing script.

Select **Retrieve connection info** to retrieve connection and credential details to use in your action. Selecting this option adds the Get Connection Info step as the first step in the action preprocessing. For more information, see [Get Connection Info step](https://www.servicenow.com/docs/access?context=get-connection-info-action-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

Select **Enable preprocessing script** to run a preprocessing script before the action sends the initial API request. For example, validate action inputs or set default values. Selecting this option adds a script step to the Data Stream action. For more information, see [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

Preprocessing executes once per action, before the first API request.

This is an optional Data Stream action component that runs on either the instance or a MID Server.

## Request

Use the Request category to configure how the action sends API requests. The Request section executes once per page of results. Request components provide these configuration options.

-   **Pagination Setup step**

    Request results in batches. Once one page of data is processed, the Data Stream action runs the request section again to return the next set of results. Use the pagination setup step to set up pagination options required by the API. Configure the Pagination Setup step manually, or select a pre-built template to apply common configurations. For example, apply the **Limit / Offset** template to specify the number of items you want returned per page \(limit\), and the starting number for the first item \(offset\). After applying a template, update the values to ensure that the configuration complies with the API's requirements.

    **Note:** For licensing purposes, each request counts as one transaction, including each request for the next page of results.

    The value of the reserved, read-only `getNextPage` variable determines whether to request another page of results. As long as the `getNextPage` variable is true and the previous page contains data, the action continues to send requests for the next page.

    **Note:** You must explicitly set the value to true in the script or it will default to false.

    This is an optional Request component that only runs on the instance.

    **Note:** Pagination isn't applicable to the JDBC step.

-   **Script step**

    Run a script before every request for the next page of results. Use this script for data validation and transformation when calling a paginated API. For example, generate a JSON payload for the next page request. Selecting this option adds a script step to the Data Stream action. For more information, see [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

    This is an optional Request component that runs on either the instance or a MID Server.

-   **REST or SOAP step**

    Send a REST or SOAP request to a third-party API. Select a data format to add an associated step to the Data Stream action. For more information, see [REST step](../../flow-designer/reference/rest-request-action-designer.md) and [SOAP step](../../flow-designer/reference/soap-step-action-designer.md).

    This is a mandatory Request component that runs on either the instance or a MID Server.

-   **JDBC step**

    Send a JDBC request to a third-party API. Use transform script to format data and add an associated step to the Data Stream action. For more information, see [JDBC step](../../flow-designer/reference/jdbc-step.md) and [Test JDBC step](../../flow-designer/task/test-jdbc-step.md). All data is retrieved and pagination is not needed.

    This is a mandatory Request component that runs on a MID Server.


## Parsing in REST and SOAP steps

Use the Parsing category to configure how the action separates data stream elements into complex data objects. Use the Splitter step to identify and separate items from an XML or JSON stream, and use the Script Parser step to transform each item into a complex object. The Parsing section executes once per item in the stream. You can access outputs from previous steps in your data stream action using the fd\_data object, excluding:

-   REST or SOAP step Response Body, Stream, or Error Message outputs
-   Splitter step outputs

![Splitting and parsing a stream of user records.](../images/data-stream-split-parse.png)

For more information about complex data, see [Complex data](https://www.servicenow.com/docs/access?context=complex-data&version=australia&pubname=australia-build-workflows&ft:locale=en-US). Parsing components provide these configuration options.

-   **Splitter step**

    Identify the parent node in the response stream to map to a complex object. For example, identify a user element in an XML payload to create a complex object for each user in the response stream.

    Select a splitter type to identify and separate repeated items in an XML or JSON data stream.

    -   **JSON**: Identifies objects from a stream of JSON data. Use a JSONPath expression to identify a JSON array containing repeated data.
    -   **XML**: Identify objects from a stream of XML data. Use an XPath expression to identify an XML element containing repeated data.
    This is a mandatory Parsing component that only runs on the instance.

-   **Script Parser step**

    Use JavaScript and ServiceNow APIs to map items in the response stream to a complex object output represented by the `targetObject` global object. For example, map incident record elements identified in the splitter step to a complex object containing incident fields. If the data stream includes siblings to the item identified in the splitter step that you do not want mapped to a complex object, include conditions to exclude those items. You can skip items in the stream by adding `outputs.state = 'SKIP'` wherever needed to the script section of the Script Parser step.

    This is a mandatory Parsing component that only runs on the instance.


![Overview of the REST and SOAP Data Stream action.](../images/ds-action-diagram.png "REST and SOAP Data Stream action overview")

## Generate the parsing phase for REST-based Data Stream actions

You can automatically configure the splitter step, script parser step, and outputs for REST-based Data Stream actions. The Test REST step functionality in REST-based Data Stream actions executes a request to the configured REST endpoint, analyzes the response payload, and automatically sets up the parsing and output components.

When a REST step is added to the Request section of a Data Stream action, you can use the REST step's **Test REST Step** button to [auto-generate the Parsing section and Outputs](../tasks/parsing-rest-data-stream.md). The Parsing section includes the splitter step and parser step. Auto-generating also puts complex object output in the Outputs section.

## Transform script in JDBC step

JDBC data stream action doesn't require pagination. Also, splitter and parser steps aren't required.

The JDBC step generates a complex object for each of the retrieved record. Hence, action preprocessing and transform script in the JDBC data stream action are optional. When using the transform script, action designer must specify the internal name of the table columns in the transform script.

![Overview of the JDBC Data Stream action.](../images/data-stream-jdbc.png "JDBC Data Stream action overview")

## Data Stream outputs in SOAP and REST steps

When designing a Data Stream action, you must create a single output of type Object or Dynamic Object. The Script Parser step maps items in the stream to this object using the `targetObject` global object.

At runtime, the system splits and parses the stream of response data according to the Data Stream configuration. Each item in the stream maps to the complex object structure defined by the Script Parser step and the object output, resulting in a large series of complex objects. For more information about complex data, see [Complex data](https://www.servicenow.com/docs/access?context=complex-data&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Data Stream outputs in JDBC step

The output of JDBC steps is a complex object stream. Entire data is retrieved in one request only.

**Note:**

-   You can only retrieve data and can't update or delete records using the JDBC data stream action.
-   The fields, **Maximum Row** and **Maximum Payload Size \(KB\)** that are available in JDBC step aren't available in the JDBC data stream action.

## Execution details in REST and SOAP steps

View the configuration and runtime results for each item processed by a Data Stream action. Select a record number to see its configuration and runtime details. By default, the execution details include requests for the last 1000 items. To change the number of items in the execution details, update the **com.snc.process\_flow.reporting.datastream.item.lastn** system property.

![Execution details for a Data Stream action.](../images/ds-execution-details.png)

-   **Data stream summary**

    View an overview of the execution that includes this information.

    -   **Page count**: Number of pages returned by a paginated API.
    -   **Total item count**: Number of items in the response stream mapped to complex object outputs.
    -   **Error count**: Number of errors encountered.
-   **Page details**

    View runtime data for each step within the Data Stream action. Select a page to view runtime details for each request to a paginated API. By default, the execution details include requests for the last five pages. To change the number of requests in the execution details, update the **com.snc.process\_flow.page.reporting.lastn** system property. Set the value to `0` to remove pages from the execution details and `-1` to include all pages.

    **Note:** Including all pages can affect performance and is not recommended.

    ![Runtime details](../images/ds-pagination-execution-details.png)


## Execution details in JDBC step

Construction of the output complex object schema isn't needed for the JDBC data stream action. You can test the query and see the query result. See [Test JDBC step](../../flow-designer/task/test-jdbc-step.md) for more information. Configure the MID Server properties **mid.jdbc.datastream.max.record.size** and **mid.jdbc.datastream.fail.when.attachement.limit.exceeded** to retrieve data as per your requirement. See [MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information.

-   **[Data Stream action design considerations](data-stream-design.md)**  
Follow these considerations when creating a Data Stream action and when adding a Data Stream action to a flow to prevent errors and performance issues.
-   **[MID Server support for Data Stream actions](dsa-on-mid.md)**  
Get data through a ServiceNow® MID Server when running a Data Stream action.
-   **[Create a Data Stream action](../tasks/create-data-stream-action.md)**  
Create a reusable action to process a stream of response data within a flow.
-   **[Generate the Parsing phase for REST-based Data Stream actions](../tasks/parsing-rest-data-stream.md)**  
Automatically configure the splitter step, script parser step, and outputs for REST-based Data Stream actions. The Test REST step functionality in REST-based Data Stream actions executes a request to the configured REST endpoint, analyzes the response payload, and automatically sets up the parsing and output components.
-   **[Test a Data Stream action](../tasks/test-data-stream-action.md)**  
Test your Data Stream action to ensure that it works the way you expect before you add it to a flow.
-   **[Use a Data Stream action in a flow](../tasks/use-data-stream-in-flow.md)**  
Data Stream actions use the **For each** flow logic option to process stream data in a flow. For example, suppose that you want to use a Data Stream action that imports document data from a third-party site. When added to a flow, the action appears as a **For each** flow logic block, enabling flow designers to easily create a record in ServiceNow for each object in the data stream.

**Parent Topic:**[Building integrations in Integration Hub](building-integrations-ih.md)

