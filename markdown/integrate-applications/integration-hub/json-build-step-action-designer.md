---
title: JSON Builder step
description: Create a JSON payload to use in another step. Enter values or use data pills to produce a dynamic payload. This step supports several data types, including objects and arrays for nested structures.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration steps, Build integrations, Integration Hub, Workflow Data Fabric]
---

# JSON Builder step

Create a JSON payload to use in another step. Enter values or use data pills to produce a dynamic payload. This step supports several data types, including objects and arrays for nested structures.

## Roles and availability

This step requires an Integration Hub subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf). After the required plugin is activated, the step is visible under Integrations.

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Name**

    Data type: **String**

    Name part of a name-value pair. Enter a value or use a data pill to produce a dynamic payload.

-   **Value**

    Data type: **String**

    Value part of a name-value pair. Enter a value or use a data pill to produce a dynamic payload. You can use a complex object pill to populate a row with an object data type, but doing so deletes any children the complex object pill already has.

-   **Type**

    Data type: **Choice**

    Data type for the name-value pair. If you're using a data pill for the name or value, make sure the data type for the pill matches the data type selected here. The options are:

    -   **String**
    -   **Object**
    -   **Number**
    -   **Boolean**
    -   **Array**
    For arrays and objects, use the plus icon \(![plus icon](../../../build/app-engine-studio/image/plus-icon.png)\) to add name-value pairs to the array or object.

-   **In case of empty value**

    Data type: **Choice**

    Option to specify what to do if a name-value pair has an empty or null value.

    -   **Leave as is**: Keeps the empty or null value as an empty string.
    -   **Omit property**: Excludes a name-value pair if the value is empty or null.
    -   **Set as null**: Returns an empty or null value as a null data type.
    -   **Throw error**: Returns an error if a name-value pair has an empty or null value.
-   **Include Outer Structure**

    Data type: **True/False**

    Option to include the curly braces for a top-level JSON container.

-   **Omit Empty Structure**

    Data type: **True/False**

    Option to omit an empty payload. Empty payloads can occur when you select **Omit property** for the **In case of empty value** input for every name-value pair and all name-value pairs in the payload produce empty values.

-   **Structure**

    Data type: **Structure**

    Read-only payload the step produces.

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see Action error evaluation.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your action.

-   **Output**

    Data type: **String**

    JSON payload as a string. If you want to use the payload as an object, you can use the [JSON parser step](json-parser-step-action-designer.md) to parse the string.

-   **Step Status**

    Data type: **Object**

    Object data pill containing runtime details about the step. Each step in an action returns a Step Status.

-   **Step Status &gt; Code**

    Data type: **Integer**

    Integer data pill indicating whether the step produced an error. By default, a value of 1 indicates that the step produced an error. A value of 0 indicates that the step ran successfully. You can't customize these codes.

-   **Step Status &gt; Message**

    Data type: **String**

    String data pill containing the error message produced by the step or system operation. You can't customize this message.


## Generate a JSON Payload

Automatically generate a JSON payload with the **Add JSON for Payload** button. This button opens the Add Payload script editor where you can enter a JSON payload to be automatically de-serialized into structured input.

There are a few details to be aware of when using the JSON payload generator.

-   If the JSON has empty keys, the payload is still generated.
-   If there are duplicate keys in the script editor, the last key entry in the object overrides the value of any previous keys with the same name.
-   If the root object is an array, the root array is wrapped into a root object.
-   If an array contains multiple objects, all the keys in the objects are coalesced into one parent object.

The JSON payload generator doesn’t support the following.

-   empty payloads
-   non-complex object types
-   invalid JSON
-   empty root objects, such as an empty array
-   payloads larger than 65,000 bytes

**Note:** Generating a JSON payload overrides any existing structures in the JSON Builder step.

