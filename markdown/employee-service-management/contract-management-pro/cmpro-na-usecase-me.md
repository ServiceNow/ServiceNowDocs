---
title: Create use cases for contract metadata extraction
description: Create a use case for contract metadata extraction to define the information that you want Now Assist to detect in a document.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Use cases for contract metadata extraction, Now Assist use cases, Contract metadata extraction, Now Assist in contract management pro, Now Assist for contract management pro, AI for contract management pro]
breadcrumb: [Configure metadata extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Create use cases for contract metadata extraction

Create a use case for contract metadata extraction to define the information that you want Now Assist to detect in a document.

## About this task

The following video walks you through the process of creating use cases for the contract metadata extraction skill.Video explaining how to create use cases for contract metadata extraction. 

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_core.contract\_config

## About this task

The CM Pro - Contract Metadata Extraction use case is available with the base system. This use case is not editable. For more information about the various fields in the CM Pro - Contract Metadata Extraction use case, see [Contract metadata extraction use cases](../reference/metadata-extraction-use-case.md).

**Note:** If you create your own use case or customize a copy of an available use case, be sure to test it thoroughly to ensure accuracy.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  Select **Activate skill** on the skill you want to activate.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

4.  On the General details page, view the skill details and select **Save and continue**.

5.  In the Contract metadata extraction use cases page, select **New use case**.

6.  In the Define use case page, add the use case details and select **Save and continue**.

<table id="table_czf_dpc_chc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use case name

</td><td>

Unique name of the use case.

</td></tr><tr><td>

Target table

</td><td>

Table where extracted information is stored.

</td></tr><tr><td>

Language of the files

</td><td>

Language of the contract documents from which you want to extract the metadata.For more information on supported languages, see [Languages supported by Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/languages-supported-by-document-intelligence.md).

</td></tr><tr><td>

LLM provider

</td><td>

Large language model \(LLM\) provider for the use case that is used to extract metadata.**Note:** For contract metadata extraction use cases, select large LLMs such as Now LLM Service Large to ensure more accurate results.

</td></tr><tr><td>

Image mode

</td><td>

Improves the efficiency of processing images for third-party multi-modal LLMs like Google Gemini, Azure OpenAI.The field is available only when a third-party multi-modal LLM is selected in the **LLM provider** field.

**Note:** Selecting image mode reduces the page count limit to 10 pages per file.

</td></tr><tr><td>

Document intelligence skill

</td><td>

Displays the skill name for which you’re creating the use case.

</td></tr></tbody>
</table>7.  In the Define fields page, select **Add a field** to add fields for the use case.

    1.  In the New field window, select **Field**.

    2.  Enter details for the new field.

        For more information on the field form, see [Field form for use case setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/document-extraction-single-field-form.md).

        ![Field information for contract metadata extraction.](../image/cmpro-na-fields-me.png "Field page for contract metadata extraction")

    3.  Select **Save**.

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

-   **[Contract metadata extraction use cases](../reference/metadata-extraction-use-case.md)**  
In contract metadata extraction, use cases specify the information that you want Now Assist to detect in a document.

**Parent Topic:**[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

**Related topics**  


[Map a use case for contract metadata extraction](cmpro-na-usecase-mappings-me.md)

[Configure system properties for contract metadata extraction](cncore-conf-sys-prop-na.md)

[Enable notification for contract metadata extraction](cncore-config-notf-na-metadata.md)

[Configure the workspace URL for contract metadata extraction notifications](cncore-config-ext-wrkspc-email.md)

[Configure an extension point to add contract metadata](config-ext-pt-to-add-metadata.md)

[Contract metadata extraction use cases](../reference/metadata-extraction-use-case.md)

[Select large language models for use cases in Now Assist in Contract Management](cmpro-na-manage-llm.md)

