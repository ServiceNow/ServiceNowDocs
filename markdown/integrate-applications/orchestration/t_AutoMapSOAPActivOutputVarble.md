---
title: Auto-map SOAP activity output variables
description: The ServiceNow activity designer allows you to map parameter values in a SOAP test payload to variables in the Outputs stage automatically.If the SOAP WSDL you are requesting in a test payload requires authentication, you must provide basic auth credentials in either the SOAP message or the SOAP activity.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a SOAP web service activity, Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, Data and Automation]
---

# Auto-map SOAP activity output variables

The ServiceNow activity designer allows you to map parameter values in a SOAP test payload to variables in the **Outputs** stage automatically.

## Before you begin

Role required: web\_service\_admin, activity\_admin, activity\_creator

## About this task

**Note:** You can test input variables from any stage in the activity designer if you have provided enough information for Orchestration to contact the endpoint and return data. Typically, the **Execution Command** stage is the point at which your inputs are ready for testing.

## Procedure

1.  In the activity designer, proceed to the **Execution Command** stage.

2.  Define an appropriate MID Server, if requested.

    The test fails if the MID Server cannot be found or if it cannot connect to the target.

3.  Click **Test Activity** to test the input parameters.

    If you added actual values for the parameters and fields, the system runs those values against the specified target and returns the resulting payload. If you mapped input variables to fields and parameters, the system displays a dialog box for assigning test values to those variables.

4.  Provide test values, if requested, and click **OK** to display the payload.

    The entire payload appears in the **Raw Output** tab of the Response form.

    ![Auto-mapping controls](../image/AutoMappingButtons.png)

5.  Select one of these auto-mapping options.

    -   **Auto-Map to Local**: Directly maps values to a local variable for use within the activity.
    -   **Auto-Map to Output**: Directly maps values to the output variable to pass to other activities in the workflow. Auto-mapping to an output variable creates an array of objects, each of which contains the column names from the query result.

**Parent Topic:**[Create a SOAP web service activity](t_CreateASOAPWebServiceActivity.md)

## Provide credentials to access a SOAP message WSDL

If the SOAP WSDL you are requesting in a test payload requires authentication, you must provide basic auth credentials in either the SOAP message or the SOAP activity.

### Before you begin

Role required: web\_service\_admin, activity\_admin, activity\_creator

The ServiceNow instance only supports basic auth credentials for accessing a WSDL. If the SOAP function or the SOAP message does not provide these credentials, you must configure them in the SOAP activity template. Orchestration uses these priorities for deciding which basic authentication credentials to use:

-   SOAP message: Credentials for a SOAP message are used if no other credentials are defined.
-   SOAP function: Credentials for a SOAP function override the credentials configured for the SOAP message.
-   SOAP activity template: Credentials for a SOAP activity template override both the SOAP function and SOAP message credentials.

### Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **SOAP Message**.

2.  Select the SOAP message you want the activity to use.

3.  In the SOAP Message record, select the **Download WSDL** check box.

4.  In the **Authentication type** field, select **Basic**.

    The **Basic auth profile** field appears.

5.  Select the basic auth profile to use with this SOAP message.

    ![Basic authentication for a SOAP message](../image/SOAPMessageBasicAuth.png "Basic authentication for a SOAP message")

6.  Alternately, you can configure basic authentication credentials in [Configure the SOAP execution command](t_MapSOAPVariablesToExecutionComm.md).

    1.  In the **Authentication** field, select **Override with Basic Authentication credentials**.

        The **Credentials** field appears.

    2.  Select the basic auth credentials to use to access the WSDL.

        This setting overrides any credentials configured in the SOAP message.

        ![Override basic auth credentials](../image/SOAPBasicAuthOverride.png "Override basic auth credentials")


