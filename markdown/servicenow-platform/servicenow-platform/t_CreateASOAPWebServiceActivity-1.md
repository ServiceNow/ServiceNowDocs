---
title: Create a SOAP web service activity
description: Use this template to create a custom SOAP activity.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
---

# Create a SOAP web service activity

Use this template to create a custom SOAP activity.

## Before you begin

Role required: web\_service\_admin, activity\_admin, activity\_creator

## About this task

For instructions on using the activity template process flow, see [create custom activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/create-custom-activities.md).

## Procedure

1.  Create a custom activity.

    This action creates a custom activity using a template.

2.  After setting up [general properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/General-Flds-Templates.md) and [creating input variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/CreateInputVariables.md), configure the SOAP web service Execution Command.

<table id="choicetable_m3f_hcs_d1b"><tbody><tr><td id="d351708e109">

**[Map the input variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/CreateInputVariables.md)**

</td><td>

Use the variables you created to configure the command that Orchestration executes on the SOAP web service.

</td></tr><tr><td id="d351708e125">

**Web service message**

</td><td>

Specify the SOAP web service message to use for this activity. If you need information on SOAP web services messages, see SOAP message.

</td></tr><tr><td id="d351708e138">

**Web service message function**

</td><td>

Specify the SOAP message function available in conjunction with the SOAP web service.

</td></tr><tr><td id="d351708e147">

**Endpoint**

</td><td>

If you enter an endpoint in this field, it overrides the endpoint URL configured in the SOAP message web service. Click the lock icon to open the input field and add the endpoint.

</td></tr><tr><td id="d351708e156">

**SOAP message parameters**

</td><td>

Name-value pairs to pass to the SOAP endpoint. You can create these parameters manually, or drag input variables into the parameter fields and then assign a value. Parameters defined in the SOAP message that use `${}` can be assigned data from this activity template. Use the **Additional attribute** column to configure the system to not escape the text. By default, text sent to the SOAP message is escaped. The **Name** column is auto-populated if the users have provided variables using Variable substitution in outbound REST messages in the SOAP message.

</td></tr><tr><td id="d351708e179">

**Use MID Server**

</td><td>

Check box that determines if a MID Server must be used to invoke the SOAP web service. If the SOAP web service message function defines a MID Server, that MID Server is used instead of the one selected here.

</td></tr><tr><td id="d351708e188">

**Required MID Server capabilities**

</td><td>

MID Server with the appropriate [MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown) for connecting to the SOAP endpoint. By default, the system selects a MID Server with SOAP capabilities. This field is available when the **Use MID Server** check box is selected.

</td></tr><tr><td id="d351708e208">

**Timeout**

</td><td>

Allowed duration of the SOAP web service request before it times out, in seconds. The default is **10**.

</td></tr><tr><td id="d351708e220">

**Authentication**

</td><td>

Determines what type of authentication is required for the endpoint. The options are:-   **Use existing credentials in SOAP message**: Uses credential definitions from the SOAP message definition.
-   **Override with Basic Authentication credentials:** Uses \|Enable basic authentication for outbound SOAP credentials. Overrides the credentials in the SOAP message definition. Basic authentication credentials must be provisioned before they are available for selection.
-   **Override with Certificate Authentication credentials**: Overrides the credentials in the SOAP message definition with certificate authentication credentials.
-   **Override with Both Basic and Certificate Authentication credentials**: Overrides the credentials in the SOAP message definition with both basic authentication or certificate authentication credentials.
-   **Override with WS-Security Username profile**: Overrides the credentials in the SOAP message definition with credentials defined in WS-Security.


</td></tr><tr><td id="d351708e261">

**Credentials**

</td><td>

Required REST endpoint basic authentication credentials. This field is available when **Override with Basic Authentication credentials** is selected in the **Authentication** field. Only basic authentication credentials appear in the selection list, which includes credentials stored on the instance and credential IDs from an external storage system. If you are using credentials stored in a CyberArk safe, you can override the default safe defined in the MID Server configuration file by adding the name of a different safe as a prefix to the credential ID, separated by a colon. For example, **newsafe:orch-test-f5**. See [Configure the MID Server for CyberArk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_CyberArkIntegrationConfiguration.md) for details.

</td></tr><tr><td id="d351708e283">

**Protocol Profile**

</td><td>

Outbound web services mutual authentication to use for authentication. This field is available when the authentication type is either **Override with Certificate Authentication credentials** or **Override with Both Basic and Certificate Authentication credentials**.

</td></tr></tbody>
</table>    **Note:** You can map parameter values in a test payload to variables in the **Outputs** tab automatically. See [automap output variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/automap-output-variable-inputs.md).


## What to do next

-   Use [auto-mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/automap-output-variable-inputs.md) to generate outputs and parsing rules \(recommended for JDBC\)
-   If you do not use auto-mapping, you can manually [create output variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/t_CreateAnOutputVariable.md) and [create parsing rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/t_CreateAParsingRule.md)

-   **[Auto-map SOAP activity output variables]()**  
The ServiceNow activity designer allows you to map parameter values in a SOAP test payload to variables in the **Outputs** stage automatically.
-   **[Configure the SOAP execution command](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/t_MapSOAPVariablesToExecutionComm.md)**  
Use the input variables you created to configure the command that Orchestration executes on the SOAP endpoint.
-   **[SOAP template execution parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/r_SOAPTemplateExecutionParams.md)**  
You use execution parameters to create the input process script in the **Pre processing** form of the activity designer.
-   **[Create a JavaScript array in a SOAP template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/t_CrtJvScrArrSTemplate.md)**  
These are instructions for creating JavaScript arrays using SOAP execution parameters.
-   **[SOAP template post-processing parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/r_STPstPPrm.md)**  
Use these parameters to create a post-processing script.

**Parent Topic:**[Orchestration custom activity templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/c_ActivityDesignerComponents.md)

