---
title: Exploring Now Assist in Document Intelligence
description: With Now Assist in Document Intelligence, you can use generative AI to extract key information from your documents and images for use in your workflows.
locale: en-US
release: australia
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Now Assist in Document Intelligence, Enable AI experiences]
---

# Exploring Now Assist in Document Intelligence

With Now Assist in Document Intelligence,you can use generative AI to extract key information from your documents and images for use in your workflows.

## Now Assist in Document Intelligence overview

Now Assist in Document Intelligence makes the following generative AI capabilities available:

-   Extract information from documents. Extract information in the form of fields, tables, and answers to predefined questions from documents and image files. The information can be reviewed by agents in the Document Intelligence workspace, stored in mapped fields, and used as defined in the workflow.
-   Document Q&amp;A: Agents can save time when reviewing documents by using the predictive capabilities of generative AI to provide answers to predefined questions.
-   Document and visual insights AI agent. The AI agent gathers context from user input and document or image attachments, generates the requested information based on the content, and provides the information along with any relevant task details. For more information on AI agents, see [Document and visual insights AI agent](../reference/document-and-visual-insights-ai-agent.md).
-   Contract metadata extraction and contract analysis. The skills for contract metadata extraction and contract analysis are only available with the Now Assist in Contract Management application. For more information, see [Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-now-assit-landing.md).
-   Attachment summarization. Agents can view a summary of attachment content along with the record summary in ITSM. Attachment summarization is available in Now Assist for ITSM. For more information, see [Customize a Now Assist for IT Service Management \(ITSM\) skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/cust-now-assist-itsm-skill.md).
-   Document chat. Agents can receive chat responses based on document content. Document chat is available in Now Assist for Virtual Agent. For more information, see [Upload documents in a chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/upload-documents-na-va.md).
-   Invoice data extraction. Extract invoice details from PDFs submitted through email or supplier portal and automatically process the digitized invoice within Accounts Payable Operations \(APO\). For more information, see .
-   ESG information extraction. Extract ESG-related information from invoices to support Operational Sustainability Management \(ESG\) initiatives and regulatory compliance. For more information, see [Filter citations documents for Operational Sustainability Management \(formerly ESG Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/filter-citations-and-authority-documents-for-esg.md).

## Now Assist in Document Intelligence skills

Now Assist in Document Intelligence skills are enabled in the Platform workflow on the Now Assist Admin Console. For more information on activating the skills, see [Activate a Now Assist in Document Intelligence skill](../task/activate-now-assist-in-document-intelligence-skill.md).

-   **Extract information from documents**

    The extract information from documents skill allows you to use Now Assist predictions to extract fields and tables and find answers to predefined questions from a document or image. Agents can review and edit predictions in the Document Intelligence workspace. For more information, see [Review extracted information in the Document Intelligence workspace](../task/review-extracted-information.md).

-   **Multimodal chat**

    The multimodal chat skill is used to enable chat responses about the content of uploaded documents and images. It is only used on the server side by the document and visual insights AI agent and by the question answering capability in Now Assist for Virtual Agent. This skill doesn’t require configuration in the Now Assist Admin console.

    For more information on these capabilities, see [Document and visual insights AI agent](../reference/document-and-visual-insights-ai-agent.md) and [Upload documents in a chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/upload-documents-na-va.md).


## Now Assist in Document Intelligence workflow

The following diagram shows how the Now Assist in Document Intelligence skills are set up and used to process documents.

![Diagram showing the activity flow in Now Assist in Document Intelligence.](../image/mmasset0021089-docIntel-admin-nowassistssist-vertical.svg "Now Assist in Document Intelligence flow")

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

Accelerate the extraction of information from documentsin the form of fields, tables, and answers to predefined questions, and turn it into structured data in the platform.

</td><td>

[Review extracted information in the Document Intelligence workspace](../task/review-extracted-information.md)

</td><td>

[DocIntel Extraction Agent \[sn\_docintel.extraction\_agent\]](../reference/document-intelligence-user-roles.md#)

</td></tr></tbody>
</table>