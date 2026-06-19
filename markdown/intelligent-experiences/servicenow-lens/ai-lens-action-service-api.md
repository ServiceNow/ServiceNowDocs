---
title: Script include - AILensActionService
description: Use the AILensActionService script include together with Lens actions to leverage ServiceNow AI Lens as a service for extracting information from the provided images and getting answers to your questions.Creates an AILensActionService instance.Invokes ServiceNow AI Lens as a service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/servicenow-lens/ai-lens-action-service-api.html
release: zurich
product: ServiceNow Lens
classification: servicenow-lens
topic_type: concept
last_updated: "2025-08-28"
reading_time_minutes: 5
breadcrumb: [Reference, ServiceNow AI Lens, Enable AI experiences]
---

# Script include - AILensActionService

Use the AILensActionService script include together with Lens actions to leverage ServiceNow AI Lens as a service for extracting information from the provided images and getting answers to your questions.

This script include is part of the ServiceNow AI Lens \(sn\_ai\_lens\) store application and is located within the `sn_app_lens_core` scope.

This script include provides methods that enable the following:

-   Calls Lens as a back-end service
-   Analyzes and comprehends data from provided images
-   Gets response from Now Assist as per provided directions
-   Does not require ServiceNow AI Lens desktop app

**Parent Topic:**[ServiceNow AI Lens reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/servicenow-lens-reference.md)

## AILensActionService - AILensActionService\(\)

Creates an AILensActionService instance.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example shows how to initialize AILensActionService.

```
var lensService = new sn_app_lens_core. AILensActionService()
```

## AILensActionService - invokeLens\(String lensActionId, String\[\] attachmentIds, String userPrompt, Object\[\] imageArr, Object inputJSON, Object\[\] additionalContext, Boolean skipACL\)

Invokes ServiceNow AI Lens as a service.

<table id="table_v4d_qzt_lgc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

lensActionId

</td><td>

String

</td><td>

Sys\_id of the Lens Actions record created for your use case, or you can select the out-of-the-box option that fits your requirements.Example: 842bfc8e37066210b97528c734924baf

This parameter is mandatory.

</td></tr><tr><td>

attachmentIds

</td><td>

String\[\]

</td><td>

Array of sys\_ids for existing image attachments.Example: `["0067e66f93f022108319f9ed1dba108b", "0000e8a42c9a7110f877137af4eab4b5"]`

You must pass either `attachmentIds` or `imageArr` parameter.

</td></tr><tr><td>

userPrompt

</td><td>

String

</td><td>

An instruction or question for Now Assist to answer after analyzing the contents of the attachments.Example: `Analyze this production issue and create an incident ticket`

</td></tr><tr><td>

imageArr

</td><td>

Object\[\]

</td><td>

Array of objects containing name of the screenshot and base64 encoded image data.Example:

```
[
    {
        name: "screenshot1.png",
        data: "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNkYPhfDwAChwGA60e6kgAAAABJRU5ErkJggg=="
    },
    {
        name: "screenshot2.png",
        data: "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNk+M9Qz0AEYAJMgkU1f5kAAAAASUVORK5CYII="
    }
];
```

You must pass either `attachmentIds` or `imageArr` parameter.

</td></tr><tr><td>

inputJSON

</td><td>

Object

</td><td>

Additional JSON input parameters that you want to pass in the pre-processing script of the Lens action.Example:

```
{
      "type" : "object",
      "properties" : {
        "short_description" : {
          "type" : "string",
          "label" : "Short description"
        },
        "description" : {
          "type" : "string",
          "label" : "Description"
        },
      },
      "required" : [ "short_description", "comments" ],
   }
```

</td></tr><tr><td>

additionalContext

</td><td>

Object

</td><td>

An optional parameter that you can use to pass any extra key–value information while you're performing a Lens service call. The examples show the key–value information that you can pass.-   **Example**:

    ```
{IsFileUploadEnabled: true}
    ```

-   **Example**: As part of the Excel mapping services, you can pass key-value information to:

    -   auto-map the column headers of an Excel file with ServiceNow table fields
    -   auto-map Excel values to ServiceNow drop-down values
    -   auto-map Excel values to referenced records in ServiceNow tables
For more information on the various key-values of the Excel mapping service, see [Key-values of the Excel auto-mapping services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/ai-lens-action-service-api.md)

**Key-values of the Excel auto-mapping services**

    -   **Schema mapping** — Maps Excel column headers to ServiceNow table fields and identifies the field type of each mapped field. Key-values for schema mapping are:

        -   `mappingStrategy`: Set to `'schema_mapping'`
        -   `rowContextSize`: Number of sample data rows to use for mapping context. Default: `10`.
        -   `randomizeRowOrder`: If `true`, Lens selects rows randomly from the Excel file. If `false`, Lens uses rows in order from the top.
        -   `sheetName`: Name of the Excel Sheet. If no name is specified, the first sheet is chosen by default.
        -   `headerRowNumber`: The row number from which the header with column names start with.
        ```
**Request example**: var response = new sn_app_lens_core.AILensActionService().invokeLens(  
     'b7fbd8694730c310dbc4964a516d431e',  
     ['0c0b1c6d4730c310dbc4964a516d43f2'],  
     '', [], {},  
     true, {"mappingStrategy":"schema_mapping", sheetName: "Incident Data",headerRowNumber: 2,"rowContextSize":5,"randomizeRowOrder":false 

} 
);    
gs.info("Lens Response : " + JSON.stringify(response));

**Response example**: {
  "Owner":           { "type": "string",     "mappings": { "0.8": ["assigned_to", "parent", "epic"] } },
  "Age":             { "type": "integer",    "mappings": { "0.8": ["story_points"] } },
  "Status":          { "type": "choice",     "mappings": { "0.8": ["state", "priority"] }, "choiceValues": ["Retired", "On Boarding", "Working"] },
  "Start Date":      { "type": "glide_date", "mappings": { "1.0": ["expected_start"], "0.8": ["due_date"] } },
  "End Date":        { "type": "glide_date", "mappings": { "1.0": ["due_date"], "0.8": ["expected_start"] } },
  "Project Assigned":{ "type": "string",     "mappings": { "0.8": ["short_description", "task", "description"] } }
}
        ```

    -   **Choice mapping** — For fields identified as Choice type, maps the unique values from the Excel column to the valid choice values in the ServiceNow table field. Key-values for Choice mapping are:

        -   `mappingStrategy`: Set to `'choice_mapping'`.
        -   `columnConfigs`: An array of objects that specifies the ServiceNow choice field and the corresponding Excel column to map, including the field name, column header, and optionally the cell values to use instead of reading from the file.
        ```
**Request example**: { 
    mappingStrategy: 'choice_mapping', 

    SheetName:’Incident Data’, 

    SheetNameheaderRowNumber:2, 
    columnConfigs: [ 
        { field: 'priority', name: 'Priority' }, 
        { field: 'state',    name: 'Ticket Status' } 
    ] 
} 
**Response example**: [ 
  { 
      "name": "Priority", 
      "field": "priority", 
      "mappings": [ 
        { "key": "High",   "value": "1", "label": "1 - Critical", "score": 1.0 }, 
        { "key": "Medium", "value": "3", "label": "3 - Moderate", "score": 0.9 } 
      ] 
  } 
]
        ```

    -   **Reference mapping** — Maps Excel cell values to the corresponding ServiceNow reference field records. Key-values for Reference mapping are:

        -   `mappingStrategy`: Set to `'reference_mapping'`.
        -   `columnConfigs`: Configuration for the specific column being mapped, including the source column name and the target reference table details.
        ```
**Request example**: var response = new sn_app_lens_core.AILensActionService().invokeLens( 
    'b7fbd8694730c310dbc4964a516d431e', 
    ['0c0b1c6d4730c310dbc4964a516d43f2'], 
    '', [], {}, 
    true, { 
        mappingStrategy: 'reference_mapping', 

  SheetName:’Incident Data’, 

  SheetNameheaderRowNumber:2, 

  columnConfigs: [{ 
            field: 'assignment_group', 
            name: 'Assignment Group', 
        }] 
    } 
); 

**Response example**: [ 
  { 
      "name": "Assignment Group", 
      "field": "assignment_group", 
      "mappings": [ 
        { "key": "IT Help Desk",  "value": "abc123...", "label": "IT Help Desk",  "score": 1.0  } 
      ] 
  } 
]
        ```


</td></tr></tbody>
</table><table id="table_w4d_qzt_lgc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;object&gt;

</td><td>

Returned success object```
{
    "status": "success",
    "lensResponse": "{\"short_description\":\"Service Degradation Error in Order Processing System\",\"description\":\"The Order Processing API v2.1 encountered a service degradation issue in the Production environment.\" }"
}
```

</td></tr><tr><td>

error

</td><td>

Returned error object```
{
    "status": "error",
    "error": {
        "errorType": "Execution Error",
        "message": "Detailed error message here"
    }
}
```

</td></tr></tbody>
</table>This example shows how to call Lens service from a script block.

```
var lensActionId = "cd6570cdf36a2210b9751f09f6968c42";
var attachmentIds = ["3fe930093b626210aba1fadc73e45a38", "0000e8a42c9a7110f877137af4eab4b5"];
var userPrompt = "Analyze this production issue and create an incident ticket";
var imageArr = [
    {
        name: "screenshot1.png",
        data: "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNkYPhfDwAChwGA60e6kgAAAABJRU5ErkJggg=="
    },
    {
        name: "screenshot2.png",
        data: "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNk+M9Qz0AEYAJMgkU1f5kAAAAASUVORK5CYII="
    }
];
var inputJSON = {
      "type" : "object",
      "properties" : {
        "short_description" : {
          "type" : "string",
          "label" : "Short description"
        },
        "description" : {
          "type" : "string",
          "label" : "Description"
        },
      },
      "required" : [ "short_description", "comments" ],
   }
var additionalContext = {
      IsFileUploadEnabled: true};

 // Call the method
var result = new sn_app_lens_core. AILensActionService().invokeLens(lensActionId, attachmentIds, userPrompt, imageArr, inputJSON, skipACL, additionalContext);
 
// Handle the response
if (result.status === 'success') {
    var response = JSON.parse(result.lensResponse);
    gs.info("AI Lens Analysis Complete:");
    gs.info("Title:", response.short_description);
    gs.info("Description:", response.description);
} else {
    gs.error("Error occurred:", result.error.message);
}
```

