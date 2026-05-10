---
title: Create use cases for contract analysis
description: Create a use case for contract analysis that is used by Now Assist to identify non-standard and missing clauses in a contract document.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Contract analysis, Create use case, Contract analysis use case, Now Assist use cases, Now Assist in contract management pro, Now Assist for contract management pro, AI for contract management pro]
breadcrumb: [Configure contract analysis, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Create use cases for contract analysis

Create a use case for contract analysis that is used by Now Assist to identify non-standard and missing clauses in a contract document.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_core.contract\_config

## About this task

The contract analysis use case contains field groups and their associated fields.

Field groups represent the clauses that are used in the contract document. Field groups are linked to clause variations of a clause library. Now Assist uses the mapped clause content to display suggestions for missing or non-standard clause.

Fields are the prompt questions added for a field group. Fields are mapped to an expected response. Now Assist executes these fields \(prompt questions\) on a contract document to identify the non-standard clauses.

When creating a use case, add a field group, and then define the fields within that field group to ensure that the fields are linked to the field group.

The CM Pro - Contract Analysis use case is available in the base system. This use case is not editable.

**Note:** If you create your own use case or customize a copy of an available use case, be sure to test it thoroughly to ensure accuracy.

For more information on the computation of non-standard and missing clauses, see the [KB1704731](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704731) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  Select **Activate skill** on the skill you want to activate.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

4.  In the General details page, view the skill details and select **Save and continue**.

5.  In the Q&amp;A use cases page, select **New use case**.

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

This field should be left empty.

</td></tr><tr><td>

Language of the files

</td><td>

Language of the contract documents this is by Now Assist.For more information on supported languages, see [Languages supported by Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/languages-supported-by-document-intelligence.md).

</td></tr><tr><td>

LLM provider

</td><td>

Large language model \(LLM\) provider for the use case that is used to analyze contracts.**Note:** For contract analysis use cases, select large LLMs such as Now LLM Service Large to ensure more accurate results.

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

    1.  In the New field window, select **Question group**.

        ![Question group card in add field page.](../image/cmpro-na-question-group.png "Question group")

        **Note:** Add a question group, and then define the questions within that question group to ensure that questions are linked to a question group.

    2.  On the form, fill in the fields.

<table id="table_ewn_b2r_bdc"><thead><tr><th>

Question group

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field group name

</td><td>

Unique name of the question group that will be mapped to a clause variation using clause mappings.For example, `Purpose`, `Term`, and so on.

</td></tr><tr><td>

Additional details

</td><td>

More information on the field group.

</td></tr><tr><td>

Target table

</td><td>

This field should be left empty.

</td></tr></tbody>
</table>    3.  Select **Add questions**.

        ![Adding questions in a Question group page.](../image/cmpro-na-add-questions.png "Question group page")

    4.  Enter details for the field.

        For more information on the field form, see [Question form for use case setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/document-qna-single-field-form.md).

        ![Question details in the fields page.](../image/cmpro-na-add-fields.png "Fields page")

    5.  Select **Save**.

    **Note:** After adding question groups and questions, be sure to test them thoroughly to ensure accuracy.

8.  Select **Save and continue**.

9.  Upload a document to test how the contract analysis skill works with the new use case.

    1.  Select **Test a new document**.

    2.  Upload a document from a record or from the device.

        You can test documents in .pdf or .docx format.

    3.  Select **Continue**.

        The contract analysis results for the uploaded document is displayed on the side panel.

        To upload and test another document, select **Test a new document**.

    4.  Add new fields or update the existing fields by selecting **Back**.

    5.  Proceed by selecting **Save and continue**.

10. In the Review and activate page, select **Complete setup**.


## Result

The use case for Contract analysis skill is created.

## What to do next

[Map a field group to a clause](cmpro-na-map-fieldgrp-clause.md)

**Parent Topic:**[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)

**Related topics**  


[Map a field group to a clause](cmpro-na-map-fieldgrp-clause.md)

[Map a field to an expected response](cmpro-na-exp-res-mapping.md)

[Map a use case for contract analysis](cmpro-na-usecase-mappings-ca.md)

[Select large language models for use cases in Now Assist in Contract Management](cmpro-na-manage-llm.md)

