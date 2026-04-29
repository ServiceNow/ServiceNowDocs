---
title: Uploading Software Bill of Materials files using a REST API
description: Review the following information prior to uploading Software Bill of Materials files using an API.
locale: en-US
release: australia
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Uploading Software Bill of Materials files using a REST API

Review the following information prior to uploading Software Bill of Materials files using an API.

## Using the REST API

To upload an SBOM file with an API, the sn\_sbom\_core.sbom\_ingest role is required.

Upload API.

This API is used for uploading and ingesting an SBOM file \(CycloneDX/SPDX\) into your instance.

Version 4.0 of SBOM Core supports:

-   XML and JSON in CycloneDx \(versions 1.0 - 1.6\).
-   JSON in SPDX \(versions 2.2-2.3\)
-   **Note:** Files over 32 MB might not load properly.


HTTP method: \(POST\)

API URL: &lt;host\_name&gt;/api/sbom/core/upload

**Note:** &lt;host\_name&gt; is your ServiceNow instance name.

All below request parameters are optional; the request body is the SBOM file content. If you are using DevOps as part of your development process, the value of 'requestedBy' should be 'devops'. See [Uploading Software Bill of Materials for DevOps SBOM files](vr-sbom-uploading-devops.md) for more general information about DevOps. If the value for 'requestedby' is "devops" \(devlopment operations\), these parameters are mandatory:

-   buildId
-   lifecycleStage

In addition, if 'requestedBy' is 'devops', data for fetchVulenrabilityInfo, and fetchPackageInfo is included.

-   buildId- string you send
-   lifecycleStage- two values, production or pre\_production
-   fetchVulenrabilityInfo- t/f
-   fetchPackageInfo-t/f

|Request parameters|Possible values|Description|
|------------------|---------------|-----------|
|productModelId|Sys id|Sys id of product model to map with the root application of given SBOM.|
|businessApplicationId|Sys id|Sys id of business application to map with the root application of given SBOM.|
|businessApplicationName \(deprecated\)|Your business application name|Name of business application to map with the root application of given SBOM.|
|sbomSource|A product such as Veracode, for example|The source for your SBOM file.|
|requestedBy|A tool, or name of a methodology, Jenkins. If you use "devops", buildId and lifecycleStage are mandatory.|Upload requested by|
|buildId|A string requester sends.|Build ID of the SBOM build.|
|lifecycleStage|production or pre\_production|Life cycle stage of the entity.|
|fetchVulenrabilityInfo|t/f|If true, triggers vulnerability intelligence integration.|
|fetchPackage Info|t/f|If true, triggers package intelligence integration.|

Upload API Response: included 'status' success/fail, 'message' \(string\), 'bomRecordId' \(this is the sys id of the SBOM that is returned through the upload API for a successful SBOM upload\).

```
{

"result": {

"status": "success",

"message": "Queued for processing.",

"bomRecordId": "f207059b4393c290629aa597cbb8f247"

}

}
```

## Status API

This API gets the status and summary of an SBOM that Is queued for ingestion.

-   API URL: /api/sbom/core/upload/status
-   HTTP method \(GET\)

|Request parameters|Possible values|Description|
|------------------|---------------|-----------|
|bomRecordId|Sys id|SBOM record ID that is returned the through the upload API for a successful SBOM upload.|

Status API default response example.

```

{
   "result": {
      "bomRecordId": "0407c0fea3e70a505df340f5251e617e",
      "uploadStatus": "processed",
      "additionalInfoStatus": "not_requested",
      "uploadSummary": {
         "components": {
            "added": 0,
            "removed": 0,
            "total": 70
         }
       }
    } 
}
```

Status API response with additional parameters example. If you requested fetchVulenrabilityInfo for that SBOM, you get the vulnerability breakdown as part of the response.

```

{
 "result": {

  "bomRecordId": "93af349b4393c290629aa597cbb8f258",

  "uploadStatus": "processed",

  "additionalInfoStatus": "complete",

  "uploadSummary": {

    "components": {
 
     "added": 0,

     "removed": 0,

     "total": 3

   },

   "vulnerabilityInfo": {

    "critical": 0,

    "high": 0,

    "medium": 0,

    "low": 0,

    "none": 0

   }

  },

  "buildId": "1"

 }

}
```

If you requested fetchPackageInfo for that SBOM, you get stale and abandoned counts as part of the response.

After an SBOM is successfully processed, where you view the uploaded records depends on the applications you’re using.

-   If you’re using SBOM Response, the BOM Entity record is displayed on the SBOM Ingestion Status list in the BOM Queue module in the SBOM Workspace.
-   If you’re using SBOM Core, navigate to **SBOM Core** &gt; **BOM Ingestion Status**.

## Enhancements to supported SBOM standards and general usage information

Version 4.0 of SBOM Core supports:

-   XML and JSON in CycloneDx \(versions 1.0 - 1.6\).
-   JSON in SPDX \(versions 2.2-2.3\)
-   **Note:** Files over 32 MB might not load properly.


Starting with v4.0 of SBOM Core, the following enhancements were made to support CycloneDx standards for versions 1.0 - 1.6:

-   Import additional information in CycloneDX SBOM files with the \(sn\_sbom\_core.collect\_properties\) property. This property is deactivated by default. Activate the property to import information that is generally not supported. Any information imported from these properties is uploaded to the SBOM Component Property \[sn\_sbom\_comp\_property\] table for the following:
    -   Uploaded SBOM files
    -   Metadata
    -   Individual vulnerabilities
    -   Components
-   View imported component data for declared and concluded licenses for SBOM files in versions 1.4 and later of CycloneDX in two new license fields:
    -   **Declared**
    -   **Concluded**
-   SBOM parsing support is extended for the following CycloneDX component types:
    -   Version 1.5: Platform, Data, Device driver, Machine Learning model
    -   Version 1.6: Cryptographic

Version 3.0 of SBOM Core supports:

-   XML and JSON in CycloneDx \(up to and including version 1.4\).
-   JSON in SPDX \(up to and including v2.3\).

If the calling user is successfully authenticated and has the sn\_sbom\_core.sbom\_ingest role in your ServiceNow instance, you can access the API from outside of your instance to upload the SBOM data.

After data is uploaded, it is parsed. Before data is parsed, the following requirements are verified:

-   Incoming data is checked that it is valid JSON or XML.
-   The BOM format is supported. Starting with v2.1 of SBOM Core, CycloneDX \(JSON and XML\) and SPDX \(XML\) formats are supported.
-   The minimum fields are available so that data can be parsed.

After these checks are verified, an entry is made into the Bill of Materials \[sn\_sbom\_doc\] table with incoming SBOM data as an attachment.

The **Process BOM file** business rule is triggered automatically as a result of the record insertion and data parsing.

**Note:** This business rule is activated during installation of SBOM Core by default.

All the components listed in an SBOM have a defined `type`.

-   Components for which SBOM files were uploaded are considered BOM Entities.
-   Components listed as `type=library` are considered third-party components.

**Related topics**  


[View upload status for Software Bill of Materials files](../task/vr-sbom-bom-queue.md)

[Viewing reports and dashboards in the Software Bill of Materials workspace](vr-sbom-viewing-data-overview.md)

