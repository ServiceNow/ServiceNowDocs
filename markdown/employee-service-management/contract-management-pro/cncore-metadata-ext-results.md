---
title: Metadata extraction results
description: The Extraction results tab in the contract repository record displays the processed metadata and their statuses, indicating whether the metadata have been successfully added to the mapped fields in the contract repository.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2024-10-01"
reading_time_minutes: 1
breadcrumb: [Metadata extraction using Now Assist in Contract Management, Using Now Assist in Contract Management, Now Assist in Contract Management, Contract Management Pro, Employee Service Management]
---

# Metadata extraction results

The Extraction results tab in the contract repository record displays the processed metadata and their statuses, indicating whether the metadata have been successfully added to the mapped fields in the contract repository.

|Status|Description|
|------|-----------|
|Successful|Metadata has been successfully added to the mapped field in contract repository.|
|Failed - Access denied|The contract fulfiller performing the metadata extraction does not have the write access to update the field in contract repository.|
|Failed - Field not mapped|The extracted metadata is not mapped to any contract repository field.|
|Failed - Invalid value|The extracted metadata does not match the expected format or type for the mapped contract repository field. For example, a contract repository field expects an integer, but the extracted value is not a numeric value.|
|Failed - Processing error|The extracted metadata for the mapped field violated a business rule on the repository, leading to the process being aborted.|

**Parent Topic:**[Metadata extraction using Now Assist in Contract Management](../concept/cncore-metadata-extract-land.md)

