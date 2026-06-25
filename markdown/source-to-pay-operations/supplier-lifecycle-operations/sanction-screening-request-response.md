---
title: Sanction screening parameters
description: Request and response parameters for screening entities against sanction lists through the Relish Data Assure API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/sanction-screening-request-response.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2026-06-06"
reading_time_minutes: 1
breadcrumb: [Conduct sanction screening, Review supplier information using Relish, Manage supplier cases, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Sanction screening parameters

Request and response parameters for screening entities against sanction lists through the Relish Data Assure API.

## Sanctions list validation input parameters

Parameters for sanctions list validation within the validations array.

|Parameter|Required|Length|Type|Description|
|---------|--------|------|----|-----------|
|**type**|Yes|Varies|Enum|Validation type. Use `sanctionList` for sanction screening.|
|**input**|Yes|Varies|Object|Sanctions list validation input object containing entity details.|
|**externalId**|Yes|Varies|String|Unique identifier for the sanction screening. Must be unique across all validations of this type.|
|**companyName**|Conditional|1+ characters|String|Full name of the company being validated. Required if last name is not provided.|
|**country**|Yes|2-3 characters|String|ISO 3166-1 alpha-2 or alpha-3 country code. Default value is `US`.|

## Response parameters

Parameters returned in API responses for sanction screening requests.

|Parameter|Type|Description|
|---------|----|-----------|
|**status**|Enum|Transaction status: PENDING, PROCESSING, COMPLETED, or ERROR|
|**result**|Enum|Overall transaction result: PASSED, PASSED WITH CAUTIONS, FAILED, REVISION REQUIRED, or NOT VALIDATED|
|**validationSummary**|Array|Summary of results for each validation type.|
|**validations**|Array|Array of detailed validation results.|

**Parent Topic:**[Conduct sanction screening](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/conduct-sanction-screening.md)

**Related topics**  


[Verify supplier location change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-supplier-location.md)

[Address verification parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/location-change-request-response.md)

[Verify banking information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-banking-information.md)

[Banking verification parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/banking-information-request-response.md)

[Conduct sanction screening](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/conduct-sanction-screening.md)

