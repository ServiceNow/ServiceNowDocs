---
title: Create custom activities using custom activity designer templates
description: You can create and update different types of custom activities in the Workflow Editor using a custom template.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create custom activities using custom activity designer templates

You can create and update different types of custom activities in the Workflow Editor using a custom template.

## Before you begin

Roles required: workflow\_admin or activity\_creator

## About this task

The Activity Designer contains common steps which are applicable to all the activities that you create. This procedure guides you through the common steps and the order they should be set up. You specify an activity template before you create a custom activity.

## Procedure

1.  Navigate to **All** &gt; **Orchestration** &gt; **Workflow Editor**.

    The **Welcome** tab of the Workflow Editor opens.

2.  On the **Custom** tab in the palette, click **+** to create a new activity select the appropriate [template](../concept/c_ActivityDesignerComponents.md) from the list.

    ![Arrow pointing to the plus sign on the Custom tab](../image/custom-activity-icon.png)

    The Activity Designer form appears, with a stage indicator at the top. All new activities start at the **General** stage. The current stage shows with a blue underscore.

    ![Activity designer stage indicator](../image/ActivityDesignerStepIndicator.png "Activity designer stage indicator")

3.  Add the [general properties](https://www.servicenow.com/docs/access?context=General-Flds-Templates&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

    This information is standard for each custom activity, include a name, description, and other related information.

4.  Create the template [Create input variables](https://www.servicenow.com/docs/access?context=CreateInputVariables&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) for the template.

    Create the variables to pass into the activity in the Inputs form of the activity designer.

5.  Add a [pre-processing script](../reference/PreprocessFields.md).

    For input validation or transforming input data, you might need a pre-processing script.

    **Note:** This step is not included in the Run Script activity.

6.  Click **Continue** to open the Execution Command form, then fill out the **Execution Command** step based on the corresponding execution templates:

    -   [Create a SOAP web service activity](t_CreateASOAPWebServiceActivity.md)
    -   [Create a JDBC activity](t_CreateAJDBCActivity.md#)
    -   [Create a JavaScript Probe activity](t_CreateAJavaScriptProbeActivity.md#)
    -   [Create a PowerShell activity](t_CreateAPowershellActivity.md#)
    -   [Create a REST web service activity](t_CreateARESTWebServiceActivity.md#)
    -   [Create a Probe activity](t_CreateAProbeActivity.md#)
    -   [Create an SFTP activity](t_CreateAnSFTPActivity.md#)
    -   [Create a Run Script activity](t_CreateARunScriptActivity.md#)
    -   [Create an SSH activity](t_CreateAnSSHActivity.md#)
    -   [Create a JMS activity](t_CreateAJMSActivity.md#)
7.  [Test your inputs](CreateInputVariables.md#).

8.  In the Outputs form, define local and/or output variables.

    Local variables can be used for temporary storage when cascading parsing rules. For example, you might extract an XML payload from within a JSON payload. A local variable can access the XML document and use that as a source for another parsing rule. The graphic shows a *Local1* variable source to parse data for *Output2*.

    ![Drop-down list for defining a local variable](../image/definelocalvariable.png "Define local variable")

9.  Use one of the options to assign values to Outputs.

<table id="choicetable_lh4_h3j_4y"><tbody><tr><td id="d511566e333">

**Parsing rule**

</td><td>

You can create a parsing rule and map them to the output fields by dragging and dropping the variables into the [parsing rules](t_CreateAParsingRule.md#) structure. The REST, SOAP, and JDBC templates provide auto-mapping to create the parsing rules automatically. If available from the test inputs form, auto-mapping should be used when possible.

</td></tr><tr><td id="d511566e349">

**[Post-processing](t_CreateAParsingRule.md#)**

</td><td>

Post-processing scripts allow you to code your own output data validation, output parsing code, and related tasks. Post-processing executes after the execution command results have been returned and before the parsing rules and conditions are run. Click **Go to Post-Processing \(Advanced\)** to create a post-processing script. **Note:** If you create a script, this step reflects as a stage in the indicator.

</td></tr></tbody>
</table>10. Click **Continue** to open the [Conditions](https://www.servicenow.com/docs/access?context=conditions&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) form to create exit condition rules for your activity and then click **Save**.


-   **[General properties for activity designer templates](../reference/General-Flds-Templates.md)**  
The following General Property fields are common to all activity designer templates.
-   **[Create input variables](CreateInputVariables.md#)**  
Create the variables to pass into the activity in the **Inputs** form of the activity designer.
-   **[Data encryption for activity variables](../concept/c_DataEncryptActivityVariables.md)**  
You can protect sensitive data passed from Orchestration activities by encrypting input and output variables.
-   **[Activity designer template pre-processing fields](../reference/PreprocessFields.md)**  
Use the **Pre Processing** form of the activity designer to define a script to run before the activity executes.
-   **[Template post-processing fields](../reference/template-post-process-field.md)**  
From the **Post Processing** form in the activity designer you can define a script to run after the activity executes.
-   **[Auto-map activity output variables](automap-output-variable-inputs.md)**  
You can map parameter values in a test payload to variables in the **Outputs** tab automatically.
-   **[Create an output variable](t_CreateAnOutputVariable.md#)**  
The **Outputs** form in the designer contains a variable builder for creating data structures of objects and arrays.
-   **[Create a parsing rule](t_CreateAParsingRule.md#)**  
Populate output variables defined in a custom activity with payload data returned from an inputs test on an external host or endpoint.
-   **[Activity conditions](../reference/conditions.md)**  
Create the exit conditions for your activity in the **Condition** column and set the order for each..

**Parent Topic:**[Orchestration activity designer](../concept/c_WorkflowActivityDesigner.md)

