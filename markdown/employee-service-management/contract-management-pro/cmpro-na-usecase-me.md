---
title: Create use cases for contract metadata extraction
description: Create a use case for contract metadata extraction to define the information that you want Now Assist to detect in a document.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Use cases for contract metadata extraction, Now Assist use cases, Contract metadata extraction, Now Assist in contract management pro, Now Assist for contract management pro, AI for contract management pro]
breadcrumb: [Configuring contract metadata extraction, Configure, Now Assist in Contract Management, Contract Management Pro, Employee Service Management]
---

# Create use cases for contract metadata extraction

Create a use case for contract metadata extraction to define the information that you want Now Assist to detect in a document.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_contract\_config

## About this task

The CM Pro - Contract Metadata Extraction use case is available with the Now Assist in Contract Management base system. This use case is not editable. For more information about the various fields in the CM Pro - Contract Metadata Extraction use case, see [Contract metadata extraction use cases](../reference/metadata-extraction-use-case.md).

**Note:** If you create your own use case or customize a copy of an available use case, be sure to test it thoroughly to ensure accuracy.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  On the tile for your skill, select **Activate skill**.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

4.  On the General details page, view the skill details and select **Save and continue**.

5.  In the Contract metadata extraction use cases page, select **New use case**.

6.  In the Define use case page, add the use case details.

    1.  In the **Use case name** field, enter a unique name for the use case.

    2.  In the **Target table** field, select the table where extracted information is stored.

    3.  Select **Save and continue**.

7.  In the Define fields page, select **Add a field** to add fields for the use case.

    1.  In the New field window, select **Field**.

    2.  Enter details for the new field.

<table id="table_kdb_mlc_52c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

Name for the field. The field name appears in the Document Intelligence workspace.

</td></tr><tr><td>

Details

</td><td>

Details of the field, with example. Now Assist uses this information to identify the correct information that is extracted from the document.For example, "The contract number or the number of the reference contract. Examples: 'AGR-2023-0042', 'CON2039739', 'BV-22122KEY'.”

</td></tr><tr><td>

Field type

</td><td>

Type of the extracted information. For example, a date field, a text field, a reference field or a number field.

</td></tr><tr><td>

Target table

</td><td>

Table that stores the extracted information. The field is automatically set to the value that is selected for the use case target table.

</td></tr><tr><td>

Target field**Note:** This field appears only when Numbers, Date, or Text field is selected on the **Field type** field.

</td><td>

Field on the target table that is linked to this field. The target field will be updated with the extracted information.

</td></tr><tr><td>

Reference table**Note:** This field appears only when Reference field is selected on the **Field type** field.

</td><td>

Indicates the reference table name.

</td></tr><tr><td>

Reference column

</td><td>

Column in the reference table which will be used to display options for a reference field in a contract while reviewing the extracted metadata.

</td></tr></tbody>
</table>        ![Field information for contract metadata extraction.](../image/cmpro-na-fields-me.png "Field page for contract metadata extraction")

    3.  Turn on the toggle switch for **Create multiple fields** to create multiple fields without closing the window.

    4.  Select **Save**.

    **Note:** After adding fields, be sure to test them thoroughly to ensure accuracy.

8.  Select **Save and Continue**.

9.  Upload a document to test how the contract metadata extraction skill works with the new use case.

    1.  Select **Test a new document**.

    2.  Upload a document from a record or from the device.

        You can test documents that are in .pdf format.

    3.  Select **Continue**.

        The metadata extraction results for the uploaded document is displayed on the side panel.

        Upload and test another document by selecting **Test a new document**.

    4.  Add new fields or update the existing fields by selecting **Back**.

    5.  Select **Save and continue** to proceed.

10. Select **Complete setup**.


## Result

The use case is created for the Contract metadata extraction skill. Now Assist uses the use case to extract metadata from signed contract.

## What to do next

[Map a use case for contract metadata extraction](cmpro-na-usecase-mappings-me.md)

**Parent Topic:**[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

**Related topics**  


[Map a use case for contract metadata extraction](cmpro-na-usecase-mappings-me.md)

[Configure system properties for metadata extraction](cncore-conf-sys-prop-na.md)

[Enable notification for metadata extraction](cncore-config-notf-na-metadata.md)

[Configure the workspace URL for metadata extraction notifications](cncore-config-ext-wrkspc-email.md)

[Configure an extension point to add contract metadata](config-ext-pt-to-add-metadata.md)

[Contract metadata extraction use cases](../reference/metadata-extraction-use-case.md)

