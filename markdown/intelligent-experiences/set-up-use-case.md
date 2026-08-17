---
title: Set up a use case
description: Create a use case to define the information to extract from a document for processing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/set-up-use-case.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, Generative AI, Document Intelligence]
breadcrumb: [Information Extraction skill, Configure, Content Understanding, Enable AI experiences]
---

# Set up a use case

Create a use case to define the information to extract from a document for processing.

## Before you begin

Several predefined use cases are available within their defined workflow areas. Check whether the available use cases meet your requirements before creating a new one. For more information, see [Content Understanding integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/content-understanding-integrations.md).

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

        For more information, see [Languages supported by Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/languages-supported.md).

    4.  Select a large language model \(LLM\) that will make predictions for the documents processed with this use case.

        For more information, see [Large language models used by Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-llms.md).

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

        -   [Field form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/field-form.md)
        -   [Question form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/question-form.md)
        -   [Table form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/table-form.md)
    4.  Select **Save**.

        The field, question, or table is added to the Information list for the use case.

    5.  Select **Save and Continue**.


## What to do next

1.  [Test a use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-the-use-case.md)
2.  [Add integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-integration.md)
3.  [Review and activate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/review-and-activate.md)

