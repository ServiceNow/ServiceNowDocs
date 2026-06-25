---
title: Address verification parameters
description: Request and response parameters for location change requests sent to and received from the Relish Data Assure API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/location-change-request-response.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2026-06-06"
reading_time_minutes: 1
breadcrumb: [Verify supplier location change request, Review supplier information using Relish, Manage supplier cases, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Address verification parameters

Request and response parameters for location change requests sent to and received from the Relish Data Assure API.

## Address validation input parameters

Parameters for address validation within location change requests.

|Parameter|Required|Length|Type|Description|
|---------|--------|------|----|-----------|
|**type**|Yes|Varies|Enum|Validation type. Use `address` for location changes.|
|**externalId**|Yes|Varies|String|Unique identifier for this validation. Copied to output for matching.|
|**addressLine1**|Yes|1-64 characters|String|Street number and name in the first line of the address.|
|**city**|No|1-64 characters|String|City or locality name. For non-US users, this field acts as the locality.|
|**state**|Yes|32 characters|String|State or administrative area name. For non-US users, this field acts as the administrative area.|
|**zipcode**|No|16 characters|String|ZIP or postal code. For non-US users, this field acts as the postal code.|
|**country**|Yes|2-3 characters|String|ISO 3166 alpha-2 or alpha-3 country code.|

## Response parameters

Parameters returned in API responses for location change requests.

|Parameter|Type|Description|
|---------|----|-----------|
|**status**|Enum|Transaction status: PENDING, PROCESSING, COMPLETED, or ERROR|
|**result**|Enum|General transaction result: PASSED, PASSED WITH CAUTIONS, FAILED, REVISION REQUIRED, or BYPASS|
|**validationSummary**|Array|Summary of results for each validation type.|
|**validations**|Array|Array of validation results processed by the API.|

**Parent Topic:**[Verify supplier location change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-supplier-location.md)

**Related topics**  


[Verify supplier location change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-supplier-location.md)

[Verify banking information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-banking-information.md)

[Banking verification parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/banking-information-request-response.md)

[Conduct sanction screening](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/conduct-sanction-screening.md)

[Sanction screening parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/sanction-screening-request-response.md)

