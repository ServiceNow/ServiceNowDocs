---
title: Configure an extension point to add contract metadata
description: Update the script in an extension point to specify fields in a related contract repository table where you want to add the extracted information for unmapped fields of a metadata extraction use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/config-ext-pt-to-add-metadata.html
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring contract metadata extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Configure an extension point to add contract metadata

Update the script in an extension point to specify fields in a related contract repository table where you want to add the extracted information for unmapped fields of a metadata extraction use case.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** field, search for `sn_cm_gen_ai.NowAssistUpdateMetadataExtractedValuesExt`.

3.  Select the record.

4.  Select the **Create implementation** related link.

5.  On the Script Include form, fill in the fields.

    For a description of the field values, see [Scripted Extension Point form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/legal-request-management/scripted-extension-point-form-fields.md).

6.  In the **Script** field, update the script to specify the contract repository related table and the field mapping

    -   In the `canHandle` function, add the request table name where you want to update the extracted information.
    -   In the `updateContractRepositoryFields` function, add a script to update the fields. The extracted metadata will be fetched from the `retrievedFieldsData` parameter.
7.  Select **Update**.


**Parent Topic:**[Configuring contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-conf-metadata-extraction.md)

**Related topics**  


[Create use cases for contract metadata extraction]()

[Map a use case for contract metadata extraction]()

[Configure system properties for contract metadata extraction]()

[Enable notification for contract metadata extraction]()

[Configure the workspace URL for contract metadata extraction notifications]()

