---
title: Set up a use case for Now Assist in Document Intelligence
description: Create a use case record to define a document you want to process with Now Assist in Document Intelligence.
locale: en-US
release: zurich
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: task
last_updated: "2025-07-28"
reading_time_minutes: 6
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Configure, Now Assist in Document Intelligence, Enable AI experiences]
---

# Set up a use case for Now Assist in Document Intelligence

Create a use case record to define a document you want to process with Now Assist in Document Intelligence.

## Before you begin

-   If the Now Assist in Document Intelligence skill has been deactivated, activate the skill. For more information, see [Activate a Now Assist in Document Intelligence skill](activate-now-assist-in-document-intelligence-skill.md).
-   Role required: Admin, DocIntel Admin, DocIntel Manager

## About this task

In a use case, you define the information you want Now Assist to get from a document by specifying the type of document to process, the fields and tablesto detector questions you want to ask, and the location where document processing results are stored.

Once you have defined a use case, users can begin processing documents for it in the related workflows.

For more information on use cases, see [Use cases in Now Assist in Document Intelligence](../concept/use-cases-now-assist-document-intelligence.md).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the workflow list, select **Platform**.

3.  In the Platform skills list, find the applicable document intelligence skill and select **Edit** in the options menu \( ![Field options menu icon](../image/icon-docintel-field-options-menu.png)\).

4.  Select **New use case**.

    The guided use case setup opens.

5.  Define the use case.

    1.  Enter a name for the use case.

    2.  Select a target table to store the document processing results for this use case.

    3.  Select the language of the files processed for the use case.

        If the files contain multiple languages, select the primary language.

        For more information, see [Languages supported by Now Assist in Document Intelligence](../reference/languages-supported-now-assist-document-intelligence.md).

    4.  Select the large language model \(LLM\) that will make predictions for the documents processed with this use case.

        For more information, see [Large language models used by Now Assist in Document Intelligence](../reference/llms-now-assist-document-intelligence.md).

    5.  Turn on image mode to process images more efficiently.

        Image mode sends pages to the LLM as images to leverage the visual capability of the multimodal LLM as well as any of the languages supported by it.

        **Note:** Selecting image mode reduces the page count limit to 10 pages per file.

        The image mode option is available when a multimodal LLM is selected.

        **Note:** Now LLM Service is a text-only model and doesn't support image mode.

    6.  Select **Save and continue**.

6.  Defineinformationor questions.

    1.  Select **Add a field**.

        If you have already defined one or more fields, tables,or questions and you want to add another, select **New field**.

    2.  Select the type of information you want to get from the document.

        You can choose one of the following:

        -   **Field**

            Fields are used to extract a single piece of information in the document. For example, a document number or a customer name.

        -   **Table**

            Tables are used to extract lists or tables of information. A table can have multiple columns. The number of list items or table rows doesn’t have to be known in advance.

        -   **Question**

            Define the question you want to ask about the document.

        A form displays based on the information type you selected.

    3.  On the form, fill in the fields.

        The type of form depends on the type of field.

        -   [Question form for use case setup](../reference/document-qna-single-field-form.md)
        -   [Field form for use case setup](../reference/document-extraction-single-field-form.md)
        -   [Table form for use case setup](../reference/document-extraction-table-form.md)
        ![Form used to define a piece of information to extract from a document.](../image/docintel-na-de-field-form.png "Field form for document extraction")

    4.  Select **Save**.

        The system adds the new fields, tables, or questions to the Informationlist associated with the use case.

    5.  To edit or delete a field, table, or question, select the appropriate option in the options menu \( ![Field options menu icon](../image/icon-docintel-field-options-menu.png)\) of the row.

    6.  Select **Save and Continue**.

7.  Test the use case performance with a sample document.

    Select **Test a new document**.

    1.  Select a document.

<table id="table_i25_b2f_y2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Upload from record

</td><td>

1.  Select **Upload from record**.
2.  Enter search criteria in the search field.
3.  Select a record from the list.
 This option is available when a target table is selected for the use case.

</td></tr><tr><td>

Upload from this device

</td><td>

1.  Select **Upload from this device**.
2.  Select **Add file**.
3.  Select a file and select **Open**.
4.  Select **Upload**.


</td></tr></tbody>
</table>    2.  Select **Continue**.

        **Tip:** Select the **Open in a new tab** button \(![Open in a new tab icon.](../image/icon-docintel-na-test-tab.png)\) to view the document in a larger workspace on a separate browser tab.

        The Document Intelligence workspace appears in a frame on the Test output screen.

    3.  Review the performance of the skill for the test document.

    4.  Select **Save and continue**.

8.  Add integrations.

    Integrate the document intelligence use case with a workflow.

    This option is available when a target table is selected for the use case.

    For more information on Document Intelligence integrations, see [Integrate with a custom application or workflow](configure-integration-setup.md).

    1.  Select **Add integration**.

        If you have already defined one or more integrations and you want to add another, select **New integration**.

    2.  Enter a name for the integration.

    3.  Select the type of integration you want to use.

        The `Process task` type creates an integration point to automatically create and process document tasks based on specific triggers happening in the target table.

        The `Extract values` type creates an integration point to automatically propagate the extracted values to the target table when extraction has been completed in Now Assist in Document Intelligence.

    4.  Use the conditions to select certain fields as specific triggers for the integration.

        Conditions are available if you selected `Process task` in the previous step. For more information on conditions, see [OR conditions](https://www.servicenow.com/docs/access?context=c_UsingORConditions&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    5.  Select the **Create Flow** option to create a flow for this integration in Workflow Studio.

        **Tip:** This option should be selected, unless you are planning to write your own custom script to set up the integration.Be sure the integration is activated on Workflow Studio. For more information, see [Building flows](https://www.servicenow.com/docs/access?context=flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

    6.  Select **Save**.

    7.  Select **Save and continue**.

9.  Review and activate.

    1.  Review the configuration selections you’ve made for the use case.

    2.  Select **Back** to return to a previous step and make a change

    3.  Select **Complete setup**.


**Parent Topic:**[Configuring Now Assist in Document Intelligence](../concept/docintel-configuring-now-assist.md)

**Related topics**  


[Activate a Now Assist in Document Intelligence skill](activate-now-assist-in-document-intelligence-skill.md)

[Turn on Full automation mode for a use case](turn-on-full-automation-for-document-extraction-na.md)

[Change the language models for a use case](change-llm-for-use-case.md)

[Edit a use case in Now Assist in Document Intelligence](edit-now-assist-document-intelligence-use-case.md)

[Make a copy of a use case in Now Assist in Document Intelligence](make-copy-of-now-assist-document-intelligence-use-case.md)

[Deactivate a use case in Now Assist in Document Intelligence](deactivate-now-assist-document-intelligence-use-case.md)

[Delete a use case in Now Assist in Document Intelligence](delete-now-assist-document-intelligence-use-case.md)

