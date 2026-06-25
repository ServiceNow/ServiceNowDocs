---
title: Banking verification parameters
description: Request and response parameters for verifying banking information through the Relish Data Assure API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/banking-information-request-response.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2026-06-06"
reading_time_minutes: 1
breadcrumb: [Verify banking information, Review supplier information using Relish, Manage supplier cases, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Banking verification parameters

Request and response parameters for verifying banking information through the Relish Data Assure API.

## Bank validation input parameters

Parameters for bank validation within the validations array.

|Parameter|Required|Length|Type|Description|
|---------|--------|------|----|-----------|
|**type**|Yes|Varies|Enum|Validation type. Use `bank` for banking verification.|
|**input**|Yes|Varies|Object|Bank validation input object containing bank details.|
|**externalId**|Yes|Varies|String|Unique identifier for the bank validation. Must be unique across all validations of this type.|
|**name**|Yes|1+ characters|String|Name of the financial institution to be validated.|
|**iban**|No|1+ characters|String|International Bank Account Number \(IBAN\).|
|**swiftCode**|Conditional|1+ characters|String|SWIFT code associated with the account. Required if routing number is not present.|
|**routingNumber**|Conditional|Varies|String|Routing number associated with the account. Required if SWIFT code is not present.|
|**country**|Yes|2-3 characters|String|ISO 3166-1 alpha-2 or alpha-3 country code for the financial institution.|

## Response parameters

Parameters returned in API responses for banking verification requests.

|Parameter|Type|Description|
|---------|----|-----------|
|**status**|Enum|Transaction status: PENDING, PROCESSING, COMPLETED, or ERROR|
|**result**|Enum|Overall transaction result: PASSED, PASSED WITH CAUTIONS, FAILED, REVISION REQUIRED, or NOT VALIDATED|
|**validationSummary**|Array|Summary of results for each validation type.|
|**validations**|Array|Array of detailed validation results.|

**Parent Topic:**[Verify banking information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-banking-information.md)

**Related topics**  


[Verify supplier location change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-supplier-location.md)

[Address verification parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/location-change-request-response.md)

[Verify banking information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-banking-information.md)

[Conduct sanction screening](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/conduct-sanction-screening.md)

[Sanction screening parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/sanction-screening-request-response.md)

