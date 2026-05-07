---
title: Configure the SOAP execution command
description: Use the input variables you created to configure the command that Orchestration executes on the SOAP endpoint.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Create a SOAP web service activity, Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the SOAP execution command

Use the input variables you created to configure the command that Orchestration executes on the SOAP endpoint.

## Before you begin

Create the input variables you need in the **Inputs** form before you can advance to the **Execution Command** stage.

Role required: web\_service\_admin, activity\_admin, activity\_creator

**Note:** You can test the SOAP connection between the MID Server and the endpoint without having to run the acvitity in a workflow context. For details, see [test template outputs](CreateInputVariables.md#).

## Procedure

1.  Drag variables from the list of inputs and drop them into command fields.

    The system formats the variable in the proper syntax for the command.

    ![SOAP execution command](../image/SOAPExecutionCommand.png "SOAP execution command")

2.  Complete the fields shown in the table.

<table id="table_ymx_5rn_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input

</td><td>

Input variable builder. [Create input variables](CreateInputVariables.md#) to [map](CreateInputVariables.md#) to available fields.

</td></tr><tr><td>

Web service message

</td><td>

[SOAP message](https://www.servicenow.com/docs/access?context=c_SOAPMessage&version=australia&pubname=australia-api-reference&ft:locale=en-US) to use for this activity. Users must have the web\_service\_admin role to configure this field.

</td></tr><tr><td>

Web service message function

</td><td>

SOAP message [SOAP message functions](https://www.servicenow.com/docs/access?context=c_SOAPMessageFunctions&version=australia&pubname=australia-api-reference&ft:locale=en-US) to use for this activity. Users must have the web\_service\_admin role to configure this field.

</td></tr><tr><td>

Endpoint

</td><td>

Endpoint URL for the SOAP web service this activity uses. Enter an endpoint in this field to override the endpoint configured in the SOAP message. Click the lock icon to open the input field.

</td></tr><tr><td>

SOAP message parameters

</td><td>

Name-value pairs to pass to the SOAP endpoint. You can create these parameters manually, or drag input variables into the parameter fields and then assign a value. Parameters defined in the SOAP message that use `${}` can be assigned data from this activity template. Use the **Additional attribute** column to configure the system to not escape the text. By default, text sent to the SOAP message is escaped. The **Name** column is auto-populated if the users have provided variables using [Variable substitution in outbound REST messages](https://www.servicenow.com/docs/access?context=c_VariableSubstitutionREST&version=australia&pubname=australia-api-reference&ft:locale=en-US) in the SOAP message.

</td></tr><tr><td>

Use MID Server

</td><td>

Check box that determines if a MID Server must be used to invoke the SOAP web service. **Note:**

If the SOAP web service message function defines a MID Server, that MID Server is used instead of the one selected here.

</td></tr><tr><td>

Required MID Server capabilities

</td><td>

MID Server with the appropriate [MID Server capabilities](../../../product/mid-server/reference/r_MIDServerCapabilities.md) for connecting to the SOAP endpoint. By default, the system selects a MID Server with SOAP capabilities. This field is available when the **Use MID Server** check box is selected.

</td></tr><tr><td>

Timeout

</td><td>

Allowed duration of the SOAP web service request before it times out, in seconds. The default is **10**.

</td></tr><tr><td>

Authentication

</td><td>

Determines what type of authentication is required for the endpoint. The options are:-   **Use existing credentials in SOAP message**: Uses credential definitions from the SOAP message definition.
-   **Override with Basic Authentication credentials:** Uses \|[Enable basic authentication for outbound SOAP](https://www.servicenow.com/docs/access?context=t_BasicAuthentication&version=australia&pubname=australia-api-reference&ft:locale=en-US) credentials. Overrides the credentials in the SOAP message definition. Basic authentication credentials must be provisioned before they are available for selection.
-   **Override with Certificate Authentication credentials**: Overrides the credentials in the SOAP message definition with certificate authentication credentials.
-   **Override with Both Basic and Certificate Authentication credentials**: Overrides the credentials in the SOAP message definition with both basic authentication or certificate authentication credentials.
-   **Override with WS-Security Username profile**: Overrides the credentials in the SOAP message definition with credentials defined in WS-Security.


</td></tr><tr><td>

Credentials

</td><td>

Required REST endpoint basic authentication credentials. This field is available when **Override with Basic Authentication credentials** is selected in the **Authentication** field. Only basic authentication credentials appear in the selection list, which includes credentials stored on the instance and credential IDs from an external storage system. If you are using credentials stored in a CyberArk safe, you can override the [Configure the MID Server for CyberArk](https://www.servicenow.com/docs/access?context=t_ConfigureTheMIDServerForCyberArk&version=australia&pubname=australia-platform-security&ft:locale=en-US) defined in the MID Server configuration file by adding the name of a different safe as a prefix to the credential ID, separated by a colon. For example, **newsafe:orch-test-f5**.

</td></tr><tr><td>

Protocol Profile

</td><td>

[Outbound web services mutual authentication](https://www.servicenow.com/docs/access?context=c_OutboundWebServicesMutualAuth&version=australia&pubname=australia-api-reference&ft:locale=en-US) to use for authentication. This field is available when the authentication type is either **Override with Certificate Authentication credentials** or **Override with Both Basic and Certificate Authentication credentials**.

</td></tr></tbody>
</table>3.  Click **Save**.

4.  Click **Continue** to advance to the **Outputs** stage.


**Parent Topic:**[Create a SOAP web service activity](t_CreateASOAPWebServiceActivity.md)

