---
title: Exploring Now Assist in Document Intelligence
description: With Now Assist in Document Intelligence, your agents can use generative AI to help review documents for key information and extract document data for use in your workflows.
locale: en-US
release: yokohama
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: concept
last_updated: "2025-04-24"
reading_time_minutes: 4
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Now Assist in Document Intelligence, Enable AI experiences]
---

# Exploring Now Assist in Document Intelligence

With Now Assist in Document Intelligence, your agents can use generative AI to help review documents for key information and extract document data for use in your workflows.

## Now Assist in Document Intelligence overview

Now Assist in Document Intelligence makes the following generative AI capabilities available to an agent:

-   Document extraction: Agents can extract information from documents and review the information in the Document Intelligence workspace. The information can then be stored in mapped fields and used as defined in the workflow.
-   Document Q&amp;A: Agents can save time when reviewing documents by using the predictive capabilities of generative AI to provide answers to predefined questions.
-   Contract metadata extraction and contract analysis. The skills for contract metadata extraction and contract analysis are only available with the Now Assist in Contract Management application. For more information, see [Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).
-   Attachment summarization. Agents can view a summary of attachment content along with the record summary in ITSM. Attachment summarization is available in Now Assist for ITSM. For more information, see [Customize a Now Assist for IT Service Management \(ITSM\) skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).
-   Document chat. Agents can receive chat responses based on document content. Document chat is available in Now Assist for Virtual Agent. For more information, see [Upload documents in a chat](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

## Now Assist in Document Intelligence skills

Now Assist in Document Intelligence skills are enabled in the Platform workflow on the Now Assist Admin Console. For more information on activating the skills, see [Activate a Now Assist in Document Intelligence skill](../task/activate-now-assist-in-document-intelligence-skill.md).

-   **Document extraction**

    The document extraction skill allows agents to use Now Assist predictions in the Document Intelligence workspace to quickly extract data from documents. For more information, see [Extract document data with Now Assist in Document Intelligence](../task/extract-document-data-with-now-assist-document-intelligence.md).

-   **Document Q&amp;A**

    The document Q&amp;A \(question and answer\) skill allows agents to use Now Assist to find answers to predefined questions from a document in the Document Intelligence workspace. For more information, see [Review document Q&amp;As with Now Assist in Document Intelligence](../task/review-document-qnas-with-now-assist-document-intelligence.md).


## Now Assist in Document Intelligence workflow

The following diagram shows how the Now Assist in Document Intelligence skills are set up and used to process documents.

![Diagram showing the activity flow in Now Assist in Document Intelligence.](../image/mmasset0020946-exploring-nadi-vertical.png "Now Assist in Document Intelligence flow")

In this workflow:

-   An admin activates a skill and sets up a use case for it.
-   A workflow integration creates a document task as part of its flow.
-   A document is uploaded for processing in a document task.
-   Now Assist processes the document and makes predictions based on the fields defined in the use case.
-   If the use case is not set to full automation, the task is sent to a live agent for review.
-   The agent provides input to validate or correct the values predicted by Now Assist.
-   The task is completed and the integrated workflow proceeds as defined.

## Now Assist in Document Intelligence benefits

Now Assist in Document Intelligence provides the following benefits.

<table id="table_wk1_3qg_b2c"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

User

</th></tr></thead><tbody><tr><td>

Start fast with a guided set up of your use cases to identify the information you want to get from your documents.

</td><td>

[Set up document intelligence use cases](../task/set-up-use-case-for-now-assist-document-intelligence.md)

</td><td>

[DocIntel Admin \[sn\_docintel.admin\]](../reference/document-intelligence-user-roles.md#)

 [DocIntel Manager \[sn\_docintel.manager\]](../reference/document-intelligence-user-roles.md#)

</td></tr><tr><td>

Accelerate the extraction of information from documents and turn it into structured data in the platform.

</td><td>

[Document extraction](../task/extract-document-data-with-now-assist-document-intelligence.md)

</td><td>

[DocIntel Extraction Agent \[sn\_docintel.extraction\_agent\]](../reference/document-intelligence-user-roles.md#)

</td></tr><tr><td>

Quickly find key information in documents by getting answers to specific questions.

</td><td>

[Document Q&amp;A](../task/review-document-qnas-with-now-assist-document-intelligence.md)

</td><td>

[DocIntel Extraction Agent \[sn\_docintel.extraction\_agent\]](../reference/document-intelligence-user-roles.md#)

</td></tr></tbody>
</table>