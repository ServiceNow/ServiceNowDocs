---
title: Create a data gathering action for a dynamic object
description: Create an action to collect output values. Then, pass the values to a parent action as a dynamic object.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Dynamic outputs, Create an action in Workflow Studio, Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a data gathering action for a dynamic object

Create an action to collect output values. Then, pass the values to a parent action as a dynamic object.

## Before you begin

Role required: action\_designer or admin

**Note:** Dynamic outputs are not available in the base system. To use dynamic outputs in Workflow Studio, you must [Request an Integration Hub plugin](https://www.servicenow.com/docs/access?context=request-integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

## About this task

These steps allow you to create a generic data gathering action for a dynamic output. To see working examples of data gathering actions for dynamic outputs, see [Get started with dynamic outputs](getting-started-dynamic-output.md#).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Actions**.

3.  Select **New** &gt; **New Action**.

4.  In the **Name** field, enter a name for your action, choose the proper **Application** scope, and then select **Submit**.

5.  In the Action Outline, select the add a new step icon \(![Add a new step icon](../images/add-new-step-icon.png)\) under Inputs and select the **REST** step.

    Configure your REST step to get data from the proper Base URL and Resource Path with any applicable Query Parameters for the HTTP Method `GET`. For more information on using the REST step in Integration Hub, see [REST step](../reference/rest-request-action-designer.md) and [REST in IntegrationHub](https://developer.servicenow.com/app.do#!/training/article/app_store_learnv2_rest_paris_rest_in_integrationhub/app_store_learnv2_rest_paris_rest_in_integrationhub_objectives?v=paris).

6.  In the Action Outline, select the add a new step icon \(![Add a new step icon](../images/add-new-step-icon.png)\) under your REST step and select the **Script** step.

    This script step must transform the response from the REST step's Response Body into a format that defines the schema of a dynamic object output for a parent action. Your script step must:

    -   Have a single JSON output variable. The script step can have other output variables, but only one must be of type JSON.
    -   Format the JSON output variable so that it contains a property named `data`. For a complex object output, your `data` property must have a format similar to the following example:

        ```
        {
               data: {
                   type: "object",              
                   //Required
        
                   children: [                  
                   //Required - This is a collection of field definitions
        
                       {
                           name: "Name 1",      
                           //Required - Unique name
        
                           label: "Label 1",    
                           //Required - Display name
        
                           type: "string"       
                           //Required - Supported field type (See the Note below)
        
                       },
        
                       {
                           name: "Name 2",
                           label: "Label 2",
                           type: "string"
                       }
                   ]
               }
           }
        
        ```

        For a complex object array output, your `data` property must have a format similar to the following example:

        ```
        {
               data: {
                   type: "object",                          
                   //Required
        
                   attributes: { child_type: "object" }     
                   //Required - Indicates that the array's children are of type object
        
                   children: [                              
                   //Required - This is a collection of field definitions
        
                       {
                           name: "Name 1",                  
                           //Required - Unique name
        
                           label: "Label 1",                
                           //Required - Display name
        
                           type: "string"                   
                           //Required - Supported field type (See the Note below)
                       },
        
                       {
                           name: "Name 2",
                           label: "Label 2",
                           type: "string"
                       }
                   ]
               }
           }
        ```

        **Note:** Supported [action data types](../reference/action-inputs-outputs.md) for the `type` property include:

        -   `string`
        -   `integer`
        -   `datetime`
        -   `choice`
        -   `boolean`
        -   `object`
        -   `array.string`
        -   `array.integer`
        -   `array.datetime`
        -   `array.choice`
        -   `array.boolean`
        -   `array.object`
7.  In the Action Outline, select **Outputs**.

    1.  Create an output of type **Dynamic Output**.

        **Note:** If you don't see Dynamic Outputs as a data type option, then you're missing an Integration Hub subscription.

    2.  In the Dynamic Options, select a data gathering action for the **Action** option.

        For examples of dynamic output data gathering actions, see [Get started with dynamic outputs](getting-started-dynamic-output.md#).

    3.  If needed set the **Depends On Another input** option, and select the input.

    Create an outputs of type Dynamic Object.

8.  Select **Save** and [test the action](test-action.md).

    In the execution details, your data gathering action runs successfully if the runtime value for `output` contains the `data` property in the proper format.

9.  Select **Publish** to make the action available to other flows or actions within the same application scope.

    ![Use your data gathering action to populate schema values for a dynamic object.](../images/create-data-gathering-action-dynamic-object-result.png)

    You can now use your data gathering action to populate the schema values for a dynamic object in a parent action.


**Parent Topic:**[Dynamic outputs](../concept/dynamic-outputs.md)

**Related topics**  


[Get started with dynamic outputs](getting-started-dynamic-output.md#)

[Dynamic output configuration options](../reference/dynamic-output-options.md)

