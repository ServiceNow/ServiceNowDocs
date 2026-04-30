---
title: Contract metadata extraction use cases
description: In contract metadata extraction, use cases specify the information that you want Now Assist to detect in a document, and the use case mappings define the type of information to process.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Now Assist in Contract Management reference, Now Assist in Contract Management, Contract Management Pro, Employee Service Management]
---

# Contract metadata extraction use cases

In contract metadata extraction, use cases specify the information that you want Now Assist to detect in a document, and the use case mappings define the type of information to process.

The CM Pro - Contract Metadata Extraction use case is available with the Now Assist in the Contract Management base system. This use case is not editable.

**Note:** If you create your own use case or customize a copy of an available use case, be sure to test it thoroughly to ensure accuracy.

The following fields are configured in the CM Pro - Contract Metadata Extraction use case for metadata extraction.

|Field|Description|Default Target Field|
|-----|-----------|--------------------|
|Other party name|The name of the company selling services or goods.|vendor|
|Internal party name|The name of the company buying services or goods.|None|
|Effective date|The date from which the contract becomes effective.|starts|
|End date|The date when the contract is set to expire.|ends|
|Contract number|A unique identifier for the contract.|vendor\_contract|
|Payment terms|The conditions under which payments are to be made.|invoice\_payment\_terms|
|Governing law|The jurisdiction under which the contract will be governed.|None|
|Term|The duration for which a contract is valid.|payment\_schedule|
|Currency|The currency in which the contract is denominated.|None|
|Contract value|The total value of the contract.|payment\_amount|
|Termination notice Days|The notice period required to inform the other party prior to contract termination.|None|
|Termination fees|The fees payable if the contract is explicitly terminated for convenience and the contract mentions that such termination includes a payment.|None|
|Payment frequency|The time interval for making a payment or generating invoice.|payment\_schedule|
|Late payment fees|The fees payable for late payment.|None|

**Parent Topic:**[Now Assist in Contract Management reference](cmpro-na-ref.md)

**Related topics**  


[Supporting information for Now Assist in Contract Management](../concept/cncore-support-info-na.md)

[Contract analysis states in Now Assist in Contract Management](../task/cmpro-na-states.md)

