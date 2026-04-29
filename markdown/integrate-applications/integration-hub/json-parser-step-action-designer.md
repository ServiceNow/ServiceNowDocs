---
title: JSON parser step
description: Identify structured data from a JSON payload without having to write a script. Map incoming JSON content to a complex object output that you can use in other steps or actions. At runtime, values from a JSON payload populate the complex object output.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration steps, Build integrations, Integration Hub, Workflow Data Fabric]
---

# JSON parser step

Identify structured data from a JSON payload without having to write a script. Map incoming JSON content to a complex object output that you can use in other steps or actions. At runtime, values from a JSON payload populate the complex object output.

To learn more about complex objects, see [Complex data](https://www.servicenow.com/docs/access?context=complex-data&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

**Note:** This step requires an Integration Hub subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf). After the required plugin is activated, the step is visible under Integrations.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Payload size limit

At runtime, JSON parser step supports payloads up to 10 MB. For larger payloads, create a Data Stream action. For more information on Data Stream actions, see [Data Stream actions and pagination](../../integrationhub/concept/data-stream-actions.md).

## Fields

<table id="table_d1v_xtr_tgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

In the **Source data** field, select or drag a data pill that contains the source JSON payload. For example, a REST step **Response Body** data pill. At runtime, values from the data source populate the complex object output.Under **Source data** and in the scripting window, enter an example payload to generate your complex object. For example, if parsing the response from a [REST step](rest-request-action-designer.md) that returns a list of users, enter the expected JSON object for a single user. You can create any example JSON payload with the following limitations:

 -   Multidimensional arrays are not supported.
-   Hyphens, periods, spaces, double colons, and the @ symbol in JSON keys are not supported.
-   Your example payload can't exceed 2 MB.

</td></tr><tr><td>

Structured Payload View

</td><td>

View your example payload as regular JSON, or toggle **Structured Payload View** to view the payload in a structured node tree. Select a node in the tree to copy the element's JSONPath. If you add new elements in the **Target** field manually, you can paste this JSONPath under an element's advanced options.

</td></tr><tr><td>

Generate Target

</td><td>

Select **Generate Target** to create the step's output structure from your example payload. Your output data structure appears in the **Target** field. Child elements for each object are automatically generated as type String. Alternatively, you can manually create your target complex object by adding elements in the **Target** field.

</td></tr><tr><td>

Target

</td><td>

View or edit the JSON payload's output structure. Create a structured output by clicking **Generate Target**, or manually add elements.

 Each element contains the following information in the Edit Object view:

 -   **Label**: Data pill label. By default, the system uses the JSON key name.
-   **Name**: Internal name for the output element.

**Note:** Exclamation marks, double colons, the @ symbol, or numbers only aren't valid values for an element's name.

-   **Type**: Data type, which must be String, Object, Array.String, or Array.Object. The top-level element must be an Object.
-   **Mandatory**: Toggle to make the element required. This only applies to elements of type String.
-   **Add child item**: Select the add child item icon \(![Add child item icon](../images/plus-icon-gray.png)\) to add a nested child element.

 Elements of type Object contain the **Save as Template** advanced option, which allows you to save your object's structure as a complex object template. You can then use this template to define the schema of an Object output for your action.

 For elements of type String, you can also add a max length, hint, and default value as advanced options.

 In the Target header, select **Exit Edit Mode** when you're done making changes to your output's structure. You can then select the toggle advanced inputs icon \(![Toggle advanced inputs icon](../images/toggle-advanced-inputs-icon.png)\) to view the **JSONPath** option.

 The JSONPath is the path to the element. Modify the JSONPath to change how your source data elements map to elements in your output. If manually adding elements, you can copy the JSONPath from a node in your example payload and paste it under an element's advanced options.

</td></tr></tbody>
</table>## JSON parser step example

This example tracks newly created problems from a production instance as defects in a test instance. First, create a new action named **Parse Problems from Production**. Add a REST step to retrieve a list of problems from the production instance. Then, add the JSON parser step to parse the REST step's **Response Body** and provide a complex object output that represents the Problem \[problem\] table's schema. Finally, create an action output of type Object named **Problems from Production**. Drop the **root** data pill from the JSON parser step into this output's value field.

![The JSON parser step structures a complex object output that represents Problem records.](../images/json-parser-step-example-01.png "Parse Problems from Production action") ![The action's output is then mapped to the JSON parser step's complex object output.](../images/json-parser-step-example-02.png "Parse Problems from Production action")

Next, create a new flow named **Sync New Problems**, which is triggered daily at midnight. The first action in the flow is the **Parse Problems from Production** action. Then, add a **For Each** flow logic block and drop the **Problems from Production** &gt; **response** data pill into the **Item** field. Within the **For Each** block, add an **If** flow logic block that checks if each problem's state is new, then creates a defect record in the test instance whose assignment group and short description is mapped to each new problem from the production instance.

![The flow creates a new defect in our test instance for each new problem in our production instance.](../images/json-parser-step-example-03.png "Sync New Problems flow")

