---
title: Create use cases for contract obligation extraction
description: Create obligation extraction use cases to specify the types of key contractual obligation that you want Now Assist to detect and extract from contract documents.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-10-25"
reading_time_minutes: 4
keywords: [Obligation extraction use case]
breadcrumb: [Configure obligation extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Create use cases for contract obligation extraction

Create obligation extraction use cases to specify the types of key contractual obligation that you want Now Assist to detect and extract from contract documents.

## About this task

The following video walks you through the process of creating use cases for the contract obligation extraction skill.Video explaining how to create use cases for contract obligation extraction. 

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_core.contract\_config

## About this task

In the contract obligation extraction skill, you can create a use case to define the category and subcategory of obligations that you want to extract from a contract.

For each use case, you can add fields with detailed prompts to define the obligation category, subcategory, and description of the subcategory. The information is used by the large language model \(LLM\) to identify and extract obligations from a contract. You must add a separate field for each obligation category that you want to extract.

Comprehensive use cases ensure that obligation extraction is precise, consistent, and aligned with your compliance requirements.

The CM Pro - Contract Obligation Extraction use case is available with the Now Assist in Contract Management base system. This use case isn’t editable.

**Note:** If you create your own use case or customize a copy of an available use case, be sure to test it thoroughly to ensure accuracy.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  Select **Activate skill** on the skill that you want to activate.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

4.  On the General details page, view the skill details and select **Save and continue**.

5.  In the Contract obligation extraction use cases page, select **New use case**.

6.  In the Define use case page, add the use case details and select **Save and continue**.

    ![Define use case form for obligation extraction.](../image/cmpro-na-ob-use-case.png "Define use case form")

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

This field should be left empty.

</td></tr><tr><td>

Language of the files

</td><td>

Language of the contract documents from which you want to extract the obligations.For more information on supported languages, see [Languages supported by Document Intelligence](https://www.servicenow.com/docs/access?context=languages-supported-by-document-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

LLM provider

</td><td>

Large language model \(LLM\) provider for the use case that is used to extract obligations.**Note:** For contract obligation extraction use cases, select large LLMs such as Now LLM Service Large to ensure more accurate results.

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
</table>7.  In the Define information page, select **Add a field** to add fields for the use case.

    1.  In the New field window, select **Question**.

    2.  Enter the details for the new question.

<table id="table_kdb_mlc_52c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Question

</td><td>

Details of the obligation that you want to extract. The information is used by the LLM to identify and extract obligations from contracts.The details must include the category and subcategory of the obligation that you want to extract along with a description that explains the specified subcategory.

For an example of a description, refer to the **Details** field of a question in the CM Pro - Contract Obligation Extraction use case that is available with the base system.

</td></tr><tr><td>

Field type

</td><td>

Type of the information to be extracted.For obligation extraction, select `Text`.

</td></tr><tr><td>

Target table

</td><td>

This field should be left empty.

</td></tr><tr><td>

Target field

</td><td>

This field should be left empty.

</td></tr></tbody>
</table>        For more information on the field form, see [Question form for use case setup](https://www.servicenow.com/docs/access?context=document-qna-single-field-form&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

        ![Field information for contract obligation extraction.](../image/cmpro-ob-ext-field.png "Field page for contract obligation extraction")

    3.  Turn on the toggle switch for **Create multiple fields** to create multiple fields without closing the window.

    4.  Select **Save**.

    **Note:** After adding questions, be sure to test them thoroughly to ensure accuracy.

8.  Select **Save and Continue**.

9.  Upload a document to test how the contract metadata extraction skill works with the new use case.

    ![Test output tab with the option to test a document for obligation extraction.](../image/cmpro-na-ob-test-output.png "Test document for obligation extraction")

    1.  Select **Test a new document**.

    2.  Upload a document from a record or from the device.

        You can test documents that are in .pdf format.

    3.  Select **Continue**.

        The obligation extraction results for the uploaded document are displayed in the side panel.

        Upload and test another document by selecting **Test a new document**.

    4.  Add new fields or update the existing fields by selecting **Back**.

    5.  Select **Save and continue** to proceed.

10. Review the use case details and select **Complete setup**.

    ![Complete setup button to activate the obligation extraction skill.](../image/cmpro-na-ob-complete-setup.png "Review and activate obligation extraction")


## Result

The use case is created for the contract obligation extraction skill. The LLM uses the use case to extract obligations from signed contracts.

## What to do next

[Map a use case for contract obligation extraction](cmpro-na-map-usecase-obext.md)

**Parent Topic:**[Configuring contract obligation extraction](cncore-conf-obligation-extraction.md)

**Related topics**  


[Map a use case for contract obligation extraction](cmpro-na-map-usecase-obext.md)

