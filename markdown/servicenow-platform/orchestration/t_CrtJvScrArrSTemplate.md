---
title: Create a JavaScript array in a SOAP template
description: These are instructions for creating JavaScript arrays using SOAP execution parameters.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a SOAP web service activity, Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a JavaScript array in a SOAP template

These are instructions for creating JavaScript arrays using SOAP execution parameters.

## Before you begin

Role required: web\_service\_admin, activity\_admin, activity\_creator

## About this task

To add more name-value pairs to the parameter's array, append the values to the existing array.

## Procedure

1.  Create a JavaScript object with the following syntax, and add it to the `executionParam.parameter` array:

    ```
    var newParameter = {"name":"parameterName","value":"parameterValue","additional_attribute":"none"}; 
    executionParam.parameters.push(newParameter);
    ```

    By adding the new parameter JavaScript object to the array, you ensure that any elements already available in the array are not impacted.

2.  Make sure to set the value in the **Additional attribute** column in the **SOAP message parameters** input field to **Do not escape text**.

    In this case, the system does not escape the value specified for the **value** attribute. An example of this is:

    ```
    var newParameter = {"name":"parameterName","value":"parameterValue","additional_attribute":"do_not_escape_text"}; 
    executionParam.parameters.push(newParameter);
    ```

    **Note:** If the value for the **additional\_attribute** field is **None**, then the system escapes the value specified by the **value** attribute. In the first example, `parameterValue` is escaped.


**Parent Topic:**[Create a SOAP web service activity](t_CreateASOAPWebServiceActivity.md)

