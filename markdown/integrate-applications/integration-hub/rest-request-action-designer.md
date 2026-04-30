---
title: REST step
description: Send an outbound REST web service request to an external system.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Integration steps, Build integrations, Integration Hub, Workflow Data Fabric]
---

# REST step

Send an outbound REST web service request to an external system.

**Note:** REST step is not available in the base system and requires the ServiceNow® Integration Hub subscription. After the required plugin is activated, the step is visible under Integrations.

[Outbound REST web service](https://www.servicenow.com/docs/access?context=c_OutboundRESTWebService&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) is a platform feature that enables you to retrieve, create, update, or delete data on a web services server that supports the REST architecture.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Fields

<table id="table_p4n_cht_3cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection

</td><td>

Type of connection to use. -   **Define Connection Inline**: Define connection information within the action step.
-   **Use Connection Alias**: Define connection information using the Connection Alias table. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action.

 To learn more about connections and credentials, see [Introduction to credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Connection Alias

</td><td>

Connection &amp; Credential alias record that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action. To learn more about connections and credentials, see [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=zurich&pubname=zurich-platform-security&ft:locale=en-US). The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel.

 **Note:** This field is available when **Use Connection Alias** is selected from the Connection list.

</td></tr><tr><td>

Credential Alias

</td><td>

Credential alias that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials when using an action in multiple environments. Likewise, if the credential information changes, you don't need to update your custom action. To learn more about connections and credentials, see [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=zurich&pubname=zurich-platform-security&ft:locale=en-US). The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel.

 **Note:** This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Use MID

</td><td>

Option to use a ServiceNow® MID Server to run the REST step. Select this check box to display the **MID Application** and **Capabilities** fields.**Note:** The system doesn't log REST request, response, and parameter runtime data sent via a MID server in the same way that [Outbound web services logging](https://www.servicenow.com/docs/access?context=outbound-request-logging&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) occurs. Instead, you can view this data in the [Flow execution details](https://www.servicenow.com/docs/access?context=flow-execution-details&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Base URL

</td><td>

Base URL for the REST request. -   If **Use Connection Alias** is selected, this field displays the base URL associated with the alias. You can override the base URL by clicking the lock icon \(![Lock icon](../images/lock-icon.png)\) and entering your own.
-   If **Define Connection Inline** is selected, enter a base URL for the connection.

</td></tr><tr><td>

Test REST Step

</td><td>

Button to test the REST step. To test, select the **Test REST Step** button. Enter any required input values and select the **Run Test** button. After the test runs, any step outputs or error messages are displayed in the Test Results section of the test window.

</td></tr><tr><td>

Connection Timeout

</td><td>

Number of milliseconds the system waits for a successful host connection. If the step does not make a successful connection during this time, the connection request times out. If **Define Connection Inline** is selected, enter a timeout value for the connection. Leave this field empty to use the system default connection timeout value.

**Note:** Avoid setting the **Connection Timeout** value to zero, as this may cause a stale connection.

</td></tr><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).


 This field is available when **Define Connection Inline** is selected from the Connection list, and **Use MID** is checked.

</td></tr><tr><td>

MID Application

</td><td>

Capabilities the MID Server must support to be eligible for selection. The system runs the action step from a MID Server that supports the selected capabilities. This field is available when **Define Connection Inline** is selected from the Connection list, **Use MID** check box is enabled, and **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

Capabilities

</td><td>

Capabilities the MID Server must support to be eligible for selection. The system runs the action step from a MID Server that supports the selected capabilities. This field is available when **Define Connection Inline** is selected from the Connection list, **Use MID** check box is enabled, and **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Server

</td><td>

Data pill of the required MID Server. This field is available when **Define Connection Inline** is selected from the Connection list, **Use MID** check box is enabled, and **Specific MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Cluster

</td><td>

Data pill for the MID Cluster you want to use. This field is available when **Define Connection Inline** is selected from the Connection list, **Use MID** is checked, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr><tr><td>

Build Request

</td><td>

Option to create the request manually, import an OpenAPI Specification, or import a REST message. -   **Manually**: Create action inputs and complete the REST step form manually.
-   **From OpenAPI specification**: Import an OpenAPI Specification to generate action inputs and complete the REST step form. For more information, see [OpenAPI support in the REST step](../../integrationhub/concept/open-api-integration.md).
-   **From REST Message**: Import a Platform REST message. For more information, see [Import a REST message into a REST step](../task/import-rest-message-step.md).

</td></tr><tr><td>

API Source

</td><td>

Option to select an OpenAPI Specification used to construct the request, or select **Import OpenAPI** to import a new OpenAPI Specification. You can import specifications by providing a URL to the YAML or JSON, or copying and pasting content.

 **Note:** This field is available when you select **From OpenAPI specification** from the Build Request list.

</td></tr><tr><td>

API Operation

</td><td>

Option to select an operation from the list. Available operations are provided by the OpenAPI Specification in the **API Source** field.

 **Note:** This field is available when you select **From OpenAPI specification** from the Build Request list.

</td></tr><tr><td>

REST Message

</td><td>

Name of the REST message to import. Select a REST message from the list.**Note:** This field is available when you select **From REST Message** from the Build Request list.

</td></tr><tr><td>

REST Message Function

</td><td>

Name of the function to import from REST message. The available options are determined by the HTTP methods associated with the selected REST message.**Note:** This field is available when you select **From REST Message** from the Build Request list.

</td></tr><tr><td>

Import REST Message

</td><td>

Button to import the REST message. **Note:** This field is available when you select a REST message from the **REST Message** field.

</td></tr><tr><td>

Resource Path

</td><td>

Path for the resource.

</td></tr><tr><td>

HTTP Method

</td><td>

HTTP method used to process the request.-   **GET**
-   **POST**
-   **PUT**
-   **PATCH**
-   **DELETE**

</td></tr><tr><td>

Query Parameters

</td><td>

Name-value pairs to pass to the REST endpoint. You can create these parameters manually, or drag input variables into the parameter fields, and then assign a value.

 Support REST step requests that contain duplicate query parameter names. If you create a REST request that contains duplicate query parameter names, Workflow Studio adds the query parameters to the request in the same order as you defined them.

 **Note:** When importing an OpenAPI Specification, the system adds all parameters and headers present in the specification to the REST step. Review the final REST step values and remove parameters you do not want to send in the request. For example, if the API accepts content type headers for both JSON and XML, the system adds both headers to the REST step. Remove one of the headers depending on the content type you want to receive in the response.

</td></tr><tr><td>

Headers

</td><td>

Headers to send with the request. You can create headers manually, or drag input variables into the parameter fields, and then assign a value.

 Support REST step requests that contain duplicate request headers. If you create a REST request that contains duplicate request headers, the headers are sent in the same order as you defined them.

 **Note:** When importing an OpenAPI Specification, the system adds all parameters and headers present in the specification to the REST step. Review the final REST step values and remove parameters you do not want to send in the request. For example, if the API accepts content type headers for both JSON and XML, the system adds both headers to the REST step. Remove one of the headers depending on the content type you want to receive in the response.

</td></tr><tr><td>

Request Type

</td><td>

Format of the request. Options include.-   **Text**: A request in JSON, XML, or other text format.
-   **Binary**: A request in a binary file format.
-   **Multipart**: A request consisting of multiple content types.
-   **Form URL-Encoded**: A request in a URL-encoded query.

 **Note:** This field is editable when the **HTTP Method** is **POST**, **PUT**, **PATCH**, or **DELETE**.

</td></tr><tr><td>

Request Body \[Text\]

</td><td>

Body of the request in JSON or XML format. The flow execution details display the response body as either a link to the embedded text viewer or the sys\_id of the attachment record containing the response.**Note:** This field is editable if you select **Text** from the Request Type list.

</td></tr><tr><td>

Attachment

</td><td>

Attachment record that contains the request. You can look up or create this record in a prior step and define it as an input variable. Create it by using the [JSONStreamingBuilder](https://www.servicenow.com/docs/access?context=JSONStreamingBuilderScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) and [XMLStreamingBuilder](https://www.servicenow.com/docs/access?context=XMLStreamingBuilderScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) APIs in the Script step. **Note:** This field is available when you select **Binary** from the Request Type list.

</td></tr><tr><td>

Name, Part Type, Value

</td><td>

Content of a multipart request. For each part, specify its name, part type, and value either using the fields individually or using an inline script for all the parts. You can specify the multipart values by clicking the toggle scripting icon \(![Toggle inline scripting icon](../images/flow-designer-inline-script-icon.png)\) and editing the script. For more information about inline scripting, see [Inline scripts](https://www.servicenow.com/docs/access?context=inline-scripts&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

 -   **Name**:The name of the part. It can be any valid string.
-   **Part Type**: The type of the part. Select either **Text** or **File**.
    -   **Text**:The text for the part. Once **Text** is selected, you can specify the content type.
    -   **File**:The file for the part. When **File** is selected, the **Value** must be the sys\_id of the attachment record containing the content. You can look up this record in a prior step or define it as an input value. Once **File** is selected, you can specify the file name and content type.
        -   For **Set Filename**, select **From Attachment** to use the attached record’s file name, or select **From Filename input** to enter your own.
        -   For **Set Content Type**, select **From Attachment** to use the attached record's content type, or select **From Content Type input** to enter your own.
-   **Value**: The content of the part. For text, the value is the text content. For a file, the value is the sys\_id of the attachment record containing the content.

**Note:** These fields are available when you select **Multipart** from the Request Type list.

</td></tr><tr><td>

Name, Value

</td><td>

Content of a form URL-encoded request. Specify each part of the URL-encoded request with a name-value pair using the fields individually or using an inline script for all parts. You can specify the form URL-encoded values inline script by clicking the toggle scripting icon\(![Toggle inline scripting icon](../images/flow-designer-inline-script-icon.png)\) and editing the script. For more information about inline scripting, see [Inline scripts](https://www.servicenow.com/docs/access?context=inline-scripts&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).**Note:** This field is available when you select **Form URL-Encoded** from the Request Type list.

</td></tr><tr><td>

Enable Retry Policy

</td><td>

Option to enable the retry policy. For more information, see [Retry policy](https://www.servicenow.com/docs/access?context=retry-policy&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Override Default Policy for Alias

</td><td>

Option to override the default retry policy. This check box is not applicable when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Retry Policy

</td><td>

Default retry policy associated with **Connection Alias**. If **Override Default Policy for Alias** is selected, you can override the default retry policy and select another existing retry policy based on your requirement.

</td></tr><tr><td>

Save As Attachment

</td><td>

Option to specify whether to save the response as a record in the Attachment \[sys\_attachment\] table.

</td></tr><tr><td>

Attachment File Name

</td><td>

Name of the attachment created by the REST response. For example, `rest-response.txt`.**Note:** This field is available when **Save As Attachment** is selected.

</td></tr><tr><td>

Attachment File Record

</td><td>

Target record to which the attachment is associated. The target record must be a data pill of type **Record**. For example, a specific incident record. You can look up this record in a prior step or define it as an input variable. The flow execution details display the sys\_id of the associated record. **Note:** This field is available when **Save As Attachment** is selected.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](https://www.servicenow.com/docs/access?context=action-error-evaluation&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


## REST response size limits

By default, the system limits the size of REST responses that are not saved as attachments to 5 MB. Direct REST responses that exceed this limit generate an error. To support larger response sizes, either save the response as an attachment or increase the response size limit with the **glide.pf.rest.response\_payload\_max\_size** system property. This system property supports a maximum value of 10240 KB, which limits the REST response to 10 MB in size.

## Parsing a REST response

REST API calls return data in the Response Body. The response body data is usually structured in JSON or XML format. You can use a [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) to parse the structured data into variables to use elsewhere in the action or in a flow. There is also an [XML parser step](xml-parser-step-action-designer.md) to parse a response body that's in an XML format.

The general strategy to get extracted data from the response is to do the following.

1.  Review the response body to select the data to return.
2.  Create input and output variables in the Script step.
    -   Create an input variable to pass in the Response Body from the REST step.
    -   Create output variables to return data from the response.
3.  Create a script to parse and map data.
    -   Use the `JSON.parse()` method in a Script step to parse a JSON response body.
    -   Map the parsed data to the output variables.
4.  Create action outputs for the output variables to make the data available to a flow.

For a detailed example, see the section on Parsing a REST Response in the [REST in IntegrationHub developer training \(Zurich\)](https://developer.servicenow.com/dev.do#!/learn/courses/zurich/app_store_learnv2_rest_zurich_rest_integrations/app_store_learnv2_rest_zurich_rest_in_integration_hub/app_store_learnv2_rest_zurich_rest_in_integration_hub_objectives).

-   **[Import a REST message into a REST step](../task/import-rest-message-step.md)**  
Transfer data from an existing Platform REST message into a REST step.

**Parent Topic:**[Integration steps](../../integrationhub/concept/integration-steps.md)

