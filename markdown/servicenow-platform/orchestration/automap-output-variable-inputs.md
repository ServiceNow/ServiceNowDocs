---
title: Auto-map activity output variables
description: You can map parameter values in a test payload to variables in the Outputs tab automatically.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Create custom activities using custom activity designer templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Auto-map activity output variables

You can map parameter values in a test payload to variables in the **Outputs** tab automatically.

## Before you begin

Role required: admin

## Procedure

1.  From the Execution Command in the template, select the **Inputs** tab.

2.  Click **Test Inputs** to test the input parameters.

    If you added actual values for the parameters and fields, the system runs those values against the specified target and returns the resulting payload. If you mapped input variables to fields and parameters, the system displays a dialog box for assigning test values to those variables.

3.  Provide test values, if requested, and click **OK** to display the payload.

    The entire payload appears in the **Raw Output** tab of the Response form.

    ![Auto-mapping controls](../image/AutoMappingButtons.png)

4.  Select an auto-mapping option.

<table id="choicetable_wkc_2t4_sz"><tbody><tr><td id="d440424e110">

**Auto-Map to Local**

</td><td>

Translates the entire payload into a JSON object and places it in the data bus. This allows for post-processing manipulation in JavaScript. This selection causes the entire data field on the right to disappear and the inputs structure to be auto-populated with these default variables:-   output
-   totalRows
-   errorMessage
-   eccSysId


</td></tr><tr><td id="d440424e134">

**Auto-Map to Output**

</td><td>

Automatically populates the output variables in the activity with the same default variables used as inputs for the local variable.

</td></tr></tbody>
</table>    **Note:** No parsing rules are available with auto-mapping selections.


**Parent Topic:**[Create custom activities using custom activity designer templates](create-custom-activities.md)

