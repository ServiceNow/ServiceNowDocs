---
title: Export to OpenAPI specification
description: Export a REST API as an OpenAPI specification to import it into another web services tool.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the REST API Explorer, REST APIs, Web services, API implementation, API implementation and reference]
---

# Export to OpenAPI specification

Export a REST API as an OpenAPI specification to import it into another web services tool.

## Before you begin

Role required: web\_service\_admin, rest\_api\_explorer, or admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST** &gt; **REST API Explorer**.

2.  Select the API you want to export.

    For example, use these choices to select the Table API for export.

    |Field|Value|
    |-----|-----|
    |Namespace|now|
    |API Name|Table API|
    |API Version|latest|

3.  Below the list of API methods, select the link for the export format you want to use.

<table id="choicetable_un2_fp2_25b"><tbody><tr><td id="d233998e136">

**Export OpenAPI Specification \(YAML\)**

</td><td>

Format the export in YAML.

</td></tr><tr><td id="d233998e145">

**Export OpenAPI Specification \(JSON\)**

</td><td>

Format the export in JSON.

</td></tr></tbody>
</table>    The browser displays a window to select a download location.

4.  Select the download location and file name.

5.  Save the file.


## Result

The system downloads the API in the format you selected.

## What to do next

Import the API into a web services tool such as Postman or Insomnia.

**Parent Topic:**[Use the REST API Explorer](../concept/use-REST-API-Explorer.md)

