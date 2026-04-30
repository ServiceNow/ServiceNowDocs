---
title: Resource generator inputs form
description: The form provides information about the generator type and generator inputs.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a resource generator in Recommended Actions, Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Resource generator inputs form

The form provides information about the generator type and generator inputs.

## Resource Generators form fields

The Task Intelligence Admin Console \(com.sn\_ti\_admin\) plugin must be installed for selecting the Task Intelligence Classification resource generator type.

**Note:**

-   You can enter static values for the generator input fields. If the **Generator type** is Flow or Decision table, you can use the pill picker to select dynamic values. The context record is available for selection in the pill picker.
-   If the context inputs are defined for a context, they appear in the pill picker for selection. The context inputs are supported for Flow and Decision table generator types only.

|Generator type|Generator inputs|Description|
|--------------|----------------|-----------|
|Flow|Generator|The subflow for the resource generator.|
|Inputs for flow|Inputs for the selected subflow.|
|Decision table|Generator|The decision table for the resource generator.|
|Inputs for decision table|Inputs for the selected decision table.|
|Similarity|Similarity definitions|The similarity solution definition to find records that are relevant to the context record.|
|Top N Results|The number of records to return from the most relevant records found by the similarity solution definition.|
|Scripting|Script include|The script include record, which is an implementation of the ScriptingGeneratorFactory template.|
|AI search|Search field|The context field on which the AI search is performed.|
|Top N Results|The number of records to return from the AI search.|
|Similarity with Trend|Similarity definitions|The similarity solution definition to find records that are relevant to the context record.|
|Trend definitions|The trend definition you want to associate with this solution definition.|
|Classification|Classification definition|The classification definition with a classification solution to return the predicted values or record references for a field on a table.|
|Top N Results|The number of values or records to return from the values or records predicted by the classification definition.|
|Task Intelligence Classification|Solution|The solution record that contains configuration for recommended input fields and recommended output fields for prediction. The solution also contains preferences whether the fields are auto-filled or recommendation messages are displayed.|
|Top N Results|The number of values or records to return from the relevant records predicted by the solution definition.|

