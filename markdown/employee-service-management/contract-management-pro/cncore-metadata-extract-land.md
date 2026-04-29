---
title: Contract metadata extraction using Now Assist in Contract Management
description: As a contract fulfiller, use Now Assist in Contract Management Pro to extract metadata from a signed contract and add the information to the mapped fields in the contract repository.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract metadata extraction using Now Assist in Contract Management

As a contract fulfiller, use Now Assist in Contract Management Pro to extract metadata from a signed contract and add the information to the mapped fields in the contract repository.

You can review the extracted information and make necessary corrections on the Document Intelligence workspace before adding the information to the contract repository. On completion of the extraction process, the **Extraction results** tab opens on the contract repository record displaying the status of the extracted metadata.

## Metadata extraction workflow for a contract fulfiller

The following end-to-end workflow shows how a contract manager extracts metadata from a signed contract and adds the information in contract repository.

1.  The contract repository record is created once the signed contract is attached to the contract request.
2.  A contract manager with the appropriate role \(sn\_cm\_gen\_ai.ai\_contract\_fulfiller\) initiates metadata extraction in the contract repository record.

    The metadata extraction is automatically initiated on creation of the contract repository record, if the automatic extraction process is enabled in system properties. For more information, see [Configure system properties for contract metadata extraction](../task/cncore-conf-sys-prop-na.md).

3.  The contract manager receives a notification once the metadata extraction is successfully completed.

    **Note:** The **Metadata extraction-Completed** notification as is not active by default.

4.  The contract manager selects the **Review extracted metadata** button to view the extracted information in the Document Intelligence workspace.
5.  The contract manager submits the verified information to update it in the contract repository.
6.  When the extraction process is completed, the **Extraction results** tab opens on the contract repository record displaying the status of the processed information.

-   **[Initiate metadata extraction from a contract](../task/cncore-extract-metadata.md)**  
Use generative AI capabilities to extract metadata from a signed contract attached in a contract repository record.
-   **[Work with extracted metadata](../task/cncore-review-metatdata.md)**  
Review the metadata extracted from a contract and add it to the contract repository.
-   **[Metadata extraction results](../reference/cncore-metadata-ext-results.md)**  
The Extraction results tab in the contract repository record displays the processed metadata and their statuses, indicating whether the metadata have been successfully added to the mapped fields in the contract repository.

**Parent Topic:**[Using Now Assist in Contract Management](cncore-use-now-assist-land.md)

**Related topics**  


[Contract analysis using Now Assist in Contract Management](cncore-NA-review-land.md)

