---
title: Configure an extension point to add contract metadata
description: Update the script in an extension point to specify fields in a related contract repository table where you want to add the extracted information for unmapped fields of a metadata extraction use case.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure metadata extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
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

    ![Script for adding metadat extraction values in related table.](../image/cmpro-ext-pt-me.png "Extension point for fields in related tables")

    For a description of the field values, see [Scripted Extension Point form fields](../../legal-request-management/reference/scripted-extension-point-form-fields.md).

6.  In the **Script** field, update the script to specify the contract repository related table and the field mapping

    -   In the `canHandle` function, add the request table name where you want to update the extracted information.
    -   In the `updateContractRepositoryFields` function, add a script to update the fields. The extracted metadata will be fetched from the `retrievedFieldsData` parameter.
7.  Select **Update**.


## Result

The script specifies the related contract repository tables and their field mappings. After metadata extraction, values from these fields are added according to the defined mapping.

For more information on metadata extraction use case mapping, see [Map a use case for contract metadata extraction](cmpro-na-usecase-mappings-me.md).

**Parent Topic:**[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

**Related topics**  


[Create use cases for contract metadata extraction](cmpro-na-usecase-me.md)

[Map a use case for contract metadata extraction](cmpro-na-usecase-mappings-me.md)

[Configure system properties for contract metadata extraction](cncore-conf-sys-prop-na.md)

[Enable notification for contract metadata extraction](cncore-config-notf-na-metadata.md)

[Configure the workspace URL for contract metadata extraction notifications](cncore-config-ext-wrkspc-email.md)

