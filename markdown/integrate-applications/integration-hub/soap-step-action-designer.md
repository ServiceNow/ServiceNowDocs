---
title: SOAP step
description: Enable action designers to send outbound SOAP web service requests to external systems.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Integration steps, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# SOAP step

Enable action designers to send outbound SOAP web service requests to external systems.

**Note:** SOAP step is not available in the base system and requires the ServiceNow® Integration Hub subscription. After the required plugin is activated, the step is visible under Integrations.

## Roles and availability

-   Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.
-   Action designers need the web\_service\_admin role to perform these web services tasks.
    -   Select WSDL
    -   Load new WSDL
    -   Select a WS-Security policy
-   The ServiceNow® MID Server doesn't support WS-Security policies.

## Fields

<table id="table_ndq_3kp_2fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connection Details

</td></tr><tr><td>

Connection

</td><td>

The type of connection to use. -   **Define Connection Inline**: Define connection information within the action step.
-   **Use Connection Alias**: Define connection information using the Connection Alias table. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action.

 To learn more about connections and credentials, see [Introduction to credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Connection Alias

</td><td>

Connection &amp; Credential alias record that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action. To learn more about connections and credentials, see [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US). The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. **Note:** This field is available when **Use Connection Alias** is selected from the Connection list.

</td></tr><tr><td>

Credential Alias

</td><td>

Credential alias that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials when using an action in multiple environments. Likewise, if the credential information changes, you don't need to update your custom action. To learn more about connections and credentials, see [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US). The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. **Note:** This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Use MID

</td><td>

Option to use a MID Server to run the SOAP step. Select this check box to display the **MID Selection**,**MID Application**, and **Capabilities** fields.**Note:** This field is available when **Use Connection Alias** is selected from the Connection list.

</td></tr><tr><td>

Endpoint

</td><td>

The URL endpoint for the SOAP request. If **Use Connection Alias** is selected, this field is read-only and displays the endpoint URL associated with alias. If **Define Connection Inline** is selected, enter an endpoint URL for the connection.

</td></tr><tr><td>

Test SOAP Step

</td><td>

Button to test the SOAP step. To test, select the **Test SOAP Step** button. Enter any required input values and select the **Run Test** button. After the test runs, any step outputs or error messages are displayed in the Test Results section of the test window.

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

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).


 This field is available when **Define Connection Inline** is selected from the Connection list, and **Use MID** is checked.

</td></tr><tr><td>

MID Cluster

</td><td>

Data pill for the MID Cluster you want to use. This field is available when **Define Connection Inline** is selected from the Connection list, **Use MID** is checked, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr><tr><td class="sub-head" colspan="2">

Request Details

</td></tr><tr><td>

Build Envelope

</td><td>

The method to use when building the SOAP envelope. -   **From WSDL**: Select this option to display the **Select a WSDL** and **Operation** fields.
-   **Manually**: Select this option to manually enter or paste WSDL text.

</td></tr><tr><td>

Select a WSDL

</td><td>

The WSDL to use to build the SOAP envelope. Select an existing WSDL record or click **Load New WSDL** to download or manually enter a WSDL file. The selected WSDL populates the values of the **Operation**, **SOAP action**, and **SOAP Envelope** fields.**Note:** This field is available when you select **From WSDL** from the Build Envelope list.

</td></tr><tr><td>

Load New WSDL

</td><td>

Option to download or manually enter a WSDL file.

</td></tr><tr><td>

Operation

</td><td>

The operation to run from the selected WSDL. Each WSDL has its own list of available operations.

</td></tr><tr><td>

SOAP Action

</td><td>

The URL to run the SOAP action. If **Build Envelope** is set to **From WSDL**, this field is read-only and displays the URL to run SOAP action. If **Build Envelope** is set to **Manually**, enter a URL to run the SOAP action.

</td></tr><tr><td>

Request Type

</td><td>

Format of the request. Options include.-   **Text**: A request in JSON, XML, or other text format.
-   **Binary**: A request in a binary file format.

</td></tr><tr><td>

SOAP Envelope

</td><td>

The XML text sent to the endpoint. If **Build Envelope** is set to **From WSDL**, the system adds the necessary XML for the **Operation** that you select. If **Build Envelope** is set to **Manually**, enter the XML text that you want to use. Enter record values in the appropriate SOAP envelope elements. For example, enter an incident short description in the `<short_description>` element.**Note:** This field is available when the **Request Type** is **Text**.

</td></tr><tr><td>

Attachment

</td><td>

Attachment record that contains the request. You can look up or create this record in a prior step and define it as an input variable. Create it by using the [JSONStreamingBuilder](https://www.servicenow.com/docs/access?context=JSONStreamingBuilderScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) and [XMLStreamingBuilder](https://www.servicenow.com/docs/access?context=XMLStreamingBuilderScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) APIs in the Script step. **Note:** This field is available when the **Request Type** is **Binary**.

</td></tr><tr><td>

Reset Envelope

</td><td>

Option to discard all manual changes that you made to the SOAP envelope. Select this check box to revert the SOAP envelope to its original state.**Note:** This field is available when you select **From WSDL** from the Build Envelope list.

</td></tr><tr><td class="sub-head" colspan="2">

New WSDL

</td></tr><tr><td>

Name

</td><td>

The name of the WSDL record you want to create.

</td></tr><tr><td>

Import Method

</td><td>

The method to enter WSDL.-   **Download from URL**: Select to display the **WSDL URL**, **User name**, and **Password** fields to retrieve the WSDL from an external source, typically the web service provider.
-   **Manually Populate WSDL Content**: Select to display the **WSDL Content** field to manually enter or paste WSDL text.

</td></tr><tr><td>

WSDL URL

</td><td>

The URL to the SOAP web service.**Note:** This field is available when you select **Download from URL** from the Import Method list.

</td></tr><tr><td>

User name

</td><td>

The user name to authenticate with the SOAP web service.**Note:** This field is available when you select **Download from URL** from the Import Method list.

</td></tr><tr><td>

Password

</td><td>

The password to authenticate with the SOAP web service. The system always masks passwords in the user interface and prevents exporting them as plain text.**Note:** This field is available when you select **Download from URL** from the Import Method list.

</td></tr><tr><td>

WSDL Content

</td><td>

The XML document describing the SOAP web service and its operations.**Note:** This field is available when you select **Manually Populate WSDL Content** from the Import Method list.

</td></tr><tr><td>

Import

</td><td>

Option to add the SOAP web service WSDL to the instance.

</td></tr><tr><td class="sub-head" colspan="2">

WS-Security

</td></tr><tr><td>

Enable WS-Security Policy

</td><td>

Option to restrict the SOAP web service to a security policy. Select this check box to display the **Policy** field.

</td></tr><tr><td>

Policy

</td><td>

The policy record that you want to use to restrict web service connections. Select an existing policy record.

</td></tr><tr><td colspan="2">

Retry Policy

</td></tr><tr><td>

Enable Retry Policy

</td><td>

Option to enable the retry policy. For more information, see [Retry policy](https://www.servicenow.com/docs/access?context=retry-policy&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Override Default Policy for Alias

</td><td>

Option to override the default retry policy. This check box is not applicable when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Retry Policy

</td><td>

Default retry policy associated with **Connection Alias**. If **Override Default Policy for Alias** is selected, you can override the default retry policy and select another existing retry policy based on your requirement.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Advanced Options

</td></tr><tr><td>

Headers

</td><td>

The name-value pairs to include in the SOAP message as HTTP headers. Click the plus icon ![Plus icon](../images/plus-icon-soap-step.png) to add headers. Add a **Name** and **Value** for each HTTP header.

</td></tr><tr><td>

**Headers** &gt; **Omit if empty**

</td><td>

Option to exclude a header if the value is empty or null.**Note:** This check box is available after clicking the down arrow to display the advanced options.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](https://www.servicenow.com/docs/access?context=action-error-evaluation&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


## SOAP response size limit

The system limits the size of SOAP responses to 5 MB. Direct SOAP responses that exceed this limit generate an error. To support larger response sizes, increase the response size limit with the **glide.pf.soap.response\_payload\_max\_size** system property. This system property supports a maximum value of 10 MB.

