---
title: Set up a use case
description: Create a use case to define the information to extract from a document for processing.Test a use case with a sample document to verify how well it extracts and processes information. Upload a document from a record or your device, then review the test outputs before saving your results.Connect a use case to a workflow by adding an integration. Integrations automate document task creation or value extraction based on triggers in the target table.Review your configuration selections before completing the setup for a use case. Return to any previous step to make changes before finalizing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/set-up-use-case.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
keywords: [Now Assist, Generative AI, Document Intelligence]
breadcrumb: [Information Extraction skill, Configure, Content Understanding, Generative AI skills, Enable AI Experiences]
---

# Set up a use case

Create a use case to define the information to extract from a document for processing.

## Before you begin

Several predefined use cases are available within their defined workflow areas. Check whether the available use cases meet your requirements before creating a new one. For more information, see [Content Understanding integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/content-understanding-integrations.md).

Role required: DocIntel Admin \[sn\_docintel.admin\] or DocIntel Manager \[sn\_docintel.manager\]

## About this task

In a use case, specify the document type to process, the fields and tables to detect, the questions to ask, and where to store the results.

After you define a use case, you can begin processing documents for it in the related workflows.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

2.  In the workflow list, select **Platform**.

3.  From the Platform skills list, search for **Extract information from documents skill**.

4.  Select the options menu \(\[Omitted image "naa-more-options-icon.png"\] Alt text: Options menu icon\), and then select **Edit**.

5.  Select **New use case**.

6.  Define a use case.

    \[Omitted image "cu-define-use-case.png"\] Alt text: Define use case form showing fields for Use case name, Target table, Language of the files, LLM provider, Image mode, and Document intelligence skill.

    1.  Enter a name for the use case.

    2.  Select a target table to store the document processing results for the use case.

    3.  Select the language of the files to process for the use case.

        If the files contain multiple languages, select the primary language.

        For more information, see [Languages supported by Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/languages-supported.md).

    4.  Select a large language model \(LLM\) that will make predictions for the documents processed with this use case.

        For more information, see [Large language models used by Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/cu-llms.md).

    5.  Turn on image mode to process images more efficiently.

        Image mode sends pages to the LLM as images to use the visual capability of the multimodal LLM and any of the languages supported by it.

        **Note:** Selecting image mode reduces the page count limit to 10 pages per file.

        The image mode option is available when a multimodal LLM is selected.

        **Note:** Now LLM Service is a text-only model and doesn't support image mode.

    6.  Select **Save and continue**.

7.  Define information fields, questions, or tables.

    \[Omitted image "cu-add-new-field.png"\] Alt text: New field dialog with three data extraction options: Field, Question, and Table.

    \[Omitted image ""\] Alt text:

    1.  Select **Add a field**.

    2.  Select the type of information to extract from the document.

        You can choose one of the following:

        -   **Field**

            Fields are used to extract a single piece of information in the document. For example, a document number or a customer name.

        -   **Question**

            Define a question to ask about the document.

        -   **Table**

            Tables are used to extract lists or tables of information. A table can have multiple columns. The number of list items or table rows doesn’t have to be known in advance.

        A fieldform displays based on the information type you selected.

    3.  On the form, fill in the fields.

        The type of form depends on the type of field:

        -   [Field form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/field-form.md)
        -   [Question form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/question-form.md)
        -   [Table form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/table-form.md)
    4.  Select **Save**.

        The field, question, or table is added to the Information list for the use case.

    5.  Select **Save and Continue**.


**Parent Topic:**[Configure Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/cu-configure-information-extraction-skill.md)

## Test a use case

Test a use case with a sample document to verify how well it extracts and processes information. Upload a document from a record or your device, then review the test outputs before saving your results.

### Before you begin

Role required: DocIntel Admin \[sn\_docintel.admin\] or DocIntel Manager \[sn\_docintel.manager\]

### Procedure

1.  Select **Test a new document**.

2.  Select a document:

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
 This option appears only when a target table is selected for the use case.

</td></tr><tr><td>

Upload from this device

</td><td>

1.  Select **Upload from this device**.
2.  Select **Add file**.
3.  Select a file and select **Open**.
4.  Select **Upload**.


</td></tr></tbody>
</table>3.  Select **Continue**.

    **Tip:** Select the **Open in a new tab** button \(\[Omitted image "cu-new-tab.png"\] Alt text: Open in new tab icon.\) to view the document in a larger workspace on a separate browser tab.

    The Test Outputs screen appears.

4.  Review the performance of the skill for the test document.

5.  Select **Save and continue**.


### What to do next

1.  [Add integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/set-up-use-case.md)
2.  [Review and activate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/set-up-use-case.md)

## Add integration

Connect a use case to a workflow by adding an integration. Integrations automate document task creation or value extraction based on triggers in the target table.

### Before you begin

Role required: DocIntel Admin \[sn\_docintel.admin\] or DocIntel Manager \[sn\_docintel.manager\] role

### Procedure

1.  Select **Add integration**.

    This option is available when a target table is selected for the use case.

    If you have already defined one or more integrations and you want to add another, select **New integration**.

2.  Enter a name for the integration.

3.  Select the type of integration you want to use.

    The `Process task` type creates an integration point to automatically create and process document tasks based on specific triggers happening in the target table.

    The `Extract values` type creates an integration point to automatically propagate the extracted values to the target table when extraction has been completed.

4.  Use the conditions to select certain fields as specific triggers for the integration.

    Conditions are available if you selected `Process task` in the previous step. For more information on conditions, see [OR conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/c_UsingORConditions.md).

5.  Select the **Create Flow** option to create a flow for this integration in Workflow Studio.

    **Tip:** This option should be selected, unless you're planning to write your own custom script to set up the integration.Be sure the integration is activated on Workflow Studio. For more information, see [Building flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/flows.md).

6.  Select **Save**.

7.  Select **Save and continue**.


### What to do next

[Review and activate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/set-up-use-case.md)

## Review and activate

Review your configuration selections before completing the setup for a use case. Return to any previous step to make changes before finalizing.

### Before you begin

Role required: DocIntel Admin \[sn\_docintel.admin\] or DocIntel Manager \[sn\_docintel.manager\]

### Procedure

1.  Review the configuration selections you’ve made for the use case.

2.  Select **Back** to return to a previous step and make a change.

3.  Select **Complete setup**.


