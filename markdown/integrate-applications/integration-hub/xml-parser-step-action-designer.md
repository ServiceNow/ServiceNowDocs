---
title: XML parser step
description: Identify structured data from an XML payload without having to write script. Map incoming XML elements to a complex object output that you can use in other steps or actions. At runtime, values from an XML payload populate the complex object output.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integration steps, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# XML parser step

Identify structured data from an XML payload without having to write script. Map incoming XML elements to a complex object output that you can use in other steps or actions. At runtime, values from an XML payload populate the complex object output.

To learn more about complex objects, see [Complex data](https://www.servicenow.com/docs/access?context=complex-data&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

**Note:** This step requires an Integration Hub subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf). After the required plugin is activated, the step is visible under Integrations.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Payload size limit

At runtime, XML parser step supports payloads up to 10 MB. For larger payloads, create a Data Stream action. For more information, see [Data Stream actions and pagination](../../integrationhub/concept/data-stream-actions.md).

At design time, XML parser step supports sample payloads up to 64,000 characters.

## Fields

<table id="table_d1v_xtr_tgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

In the **Source data** field, select or drag a data pill that contains the source XML data. For example, a REST step **Response Body** data pill. At runtime, values from the data source populate the complex object output.Under Source data and in the scripting window, enter an example payload to generate a complex object. For example, if parsing the response from a REST API step that returns a list of users, enter the expected XML for a single user. This field accepts XML with the following limitations:

 -   XML namespaces are not applied to the complex object. More than one namespace in an XML file is not supported and generates an error message.
-   Multidimensional arrays are not supported.
-   Some special characters are not supported, such as hyphen and period. Double colons \(::\) are not supported in attribute values.
-   Payloads larger than 2 MB cannot be saved and generate an error message. However, if working with a large example, you can generate the complex object and delete the example payload before saving the step.

</td></tr><tr><td>

Structured Payload View

</td><td>

Select a view for the example payload. -   **Raw \(edit mode\)**: Displays editable XML.
-   **Structured**: Displays XML in a tree view. Click an element in the tree to copy the element XPath. If creating complex data in the **Target** field manually, you can paste the XPath into the target XPath field.

</td></tr><tr><td>

Generate Target

</td><td>

Select **Generate Target** to create the step's output structure from your example payload. Your output data structure appears in the **Target** field. Child elements for each object are automatically generated as type String. Alternatively, you can manually create your target complex object by adding elements in the **Target** field.

</td></tr><tr><td>

Target

</td><td>

View or edit the XML payload's output structure. Create a structured output by clicking **Generate Target**, or manually add elements.

 Each element contains the following information in the Edit Object view:

 -   **Label**: Data pill label. By default, the system uses the XML element's name.
-   **Name**: Internal name for the output element.

**Note:** Exclamation marks, double colons, the @ symbol, or numbers only aren't valid values for an element's name.

-   **Type**: Data type, which must be String, Object, Array.String, or Array.Object. The top-level element must be an Object.
-   **Mandatory**: Toggle to make the element required. This only applies to elements of type String.
-   **Add child item**: Select the add child item icon \(![Add child item icon](../images/plus-icon-gray.png)\) to add a nested child element.

 Elements of type Object contain the **Save as Template** advanced option, which allows you to save your object's structure as a complex object template. You can then use this template to define the schema of an Object output for your action.

 For elements of type String, you can also add a max length, hint, and default value as advanced options.

 In the Target header, select **Exit Edit Mode** when you're done making changes to your output's structure. You can then select the toggle advanced inputs icon \(![Toggle advanced inputs icon](../images/toggle-advanced-inputs-icon.png)\) to view the **XPath** option.

 The XPath is the path to the element. Modify the XPath to change how source data elements map to complex data variables. If manually adding complex data variables, you can copy the XPath from the **Payload view** field and paste it in a complex data variable XPath field to ensure the correct hierarchy. Conditional XPath expressions are not supported.

</td></tr></tbody>
</table>