---
title: Script include - AILensActionService
description: Use the AILensActionService script include together with Lens actions to leverage ServiceNow AI Lens as a service for extracting information from the provided images and getting answers to your questions.Creates an AILensActionService instance.Invokes ServiceNow AI Lens as a service.
locale: en-US
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
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

**Parent Topic:**[ServiceNow AI Lens reference](../reference/servicenow-lens-reference.md)

## AILensActionService - AILensActionService\(\)

Creates an AILensActionService instance.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example shows how to initialize AILensActionService.

```
var lensService = new sn_app_lens_core. AILensActionService()
```

## AILensActionService - invokeLens\(String lensActionId, String\[\] attachmentIds, String userPrompt, Object\[\] imageArr, Object inputJSON\)

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
 // Call the method
var result = new sn_app_lens_core. AILensActionService().invokeLens(lensActionId, attachmentIds, userPrompt, imageArr, inputJSON);
 
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

