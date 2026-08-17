---
title: Now Assist in Document Intelligence release notes
description: The ServiceNow Now Assist in Document Intelligence application uses generative AI to extract information from documents, summarize document content, and provide answers to predefined questions. Now Assist in Document Intelligence was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-01-23"
reading_time_minutes: 7
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
---

# Now Assist in Document Intelligence release notes

The ServiceNow® Now Assist in Document Intelligence application uses generative AI to extract information from documents, summarize document content, and provide answers to predefined questions. Now Assist in Document Intelligence was enhanced and updated in the Yokohama release.

## Now Assist in Document Intelligence highlights for the Yokohama release

[Yokohama Patch 13](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-13.md)

-   Now Assist in Document Intelligence skills are on by default.

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Yokohama Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-6.md)

-   Summarize the content in document and image attachments with the document and visual insights AI agent.
-   Choose a large language model \(LLM\) to generate predictions for extraction and Q&amp;A \(question &amp; answer\) use cases.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   Boost productivity by using the document and visual insights AI agent to autonomously analyze and extract data from documents and images.
-   Streamline document data extraction by automating document tasks.
-   Use Virtual Agent to ask questions about the document content.
-   Extract the data from invoices with Now Assist for Accounts Payable Operations \(APO\).

[Early Availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-all-other-fixes.md)

-   Speed up your document processing workflows and quickly extract the text and tables from your documents.
-   Save time looking for the information that you need in a document, and quickly find the answers to predefined questions.

See  for more information.

**Important:** Now Assist in Document Intelligence is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Now Assist in Document Intelligence release

-   **Document and visual insights AI agent enhancements**

    The document and visual insights AI agent can recognize and provide citations for multiple attachments.


-   **LLM selection for use cases**

    Configure a different LLM to generate predictions for extraction and Q&amp;A use cases.

-   **New third-party AI model provider options available for all Now Assist applications**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   ****

    Use an AI agent to help process the tasks that analyze and extract data from documents and images.

-   **Full automation for document data extraction**

    Automatically extract the document data and process the document task without agent review.

-   **[Data extraction from accounts payable \(AP\) invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/exploring-now-assist-apo.md)**

    Extract data from invoices with Now Assist for APO.

-   **[Document chat in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/upload-documents-na-va.md)**

    Integrate Now Assist for Virtual Agent with Now Assist in Document Intelligence to enable the chat responses that are based on the document content.

-   **Attachment summarization in ITSM**

    View the summaries of attachments with the record summary in ITSM.


-   **Document extraction**

    Extract the data from documents by using LLMs to provide the recommended field values.

-   **Document Q&amp;A**

    Use generative AI to find the answers to the predefined questions in a document.

-   **Setting up use cases for Now Assist in Document Intelligence**

    Set up Document Intelligence use cases to enable agents to use the document extraction and document Q&amp;A skills.


## UI changes

-   **Usability enhancements to use case setup features**

    Various features for the use case setup are updated to create a more effective user experience:

    -   **Field** is changed to **question** in the field form for Q&amp;A use case setup.
    -   **Single field** is changed to **Field** in the field form for the document extraction use case setup.
    -   An **Additional Details** field is added to the table form for the document extraction use case setup as a way to help the large language model \(LLM\) extract the relevant information from the document.

## Changed in this release

-   **Document and visual insights AI agent enhancements**

    Tools used by the document and visual insights AI agent are consolidated to improve performance.

-   **Now Assist in Document Intelligence skills are now turned on by default**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading: Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **Changes to Now Assist usage measurement**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **Some Now Assist skills are turned on by default**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **Configure ACLs for AI agents and agentic workflows**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **Document and visual insights AI agent enhancements**

    Generate a summary of document and image attachments with the document and visual insights AI agent.


## Activation information

Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

-   [ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-apo.md)
-   
-   
-   [ServiceNow Otto for Collaborative Work Management \(CWM\) \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-cwm-landing.md)
-   
-   [ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-csm.md)
-   
-   [ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-ea.md)
-   [ServiceNow Otto for Operational Sustainability \(formerly ESG\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/now-assist-for-esg.md)
-   [ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/now-assist-fsm.md)
-   [ServiceNow Otto for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/now-assist-for-financial-services-operations.md)
-   
-   
-   
-   
-   
-   
-   
-   [Operational Technology \(OT\) Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/now-assist-for-otm-landing.md)
-   [ServiceNow Otto for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/now-assist-order-management.md)
-   [ServiceNow Otto for PSDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/now-assist-for-psds.md)
-   [ServiceNow Otto for Security Incident Response \(SIR\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-security-incident-landing.md)
-   
-   [ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo.md)
-   [ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo.md)
-   [ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-spm.md)
-   [ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-spmc.md)
-   
-   
-   [ServiceNow Otto for Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-vulnerability-response-landing.md)

For more information, see .

## Additional requirements

Now Assist in Document Intelligence requires the installation of the Document Intelligence application \(sn\_docintel\) and at least one Now Assist product.

## Related ServiceNow applications and features

-   ****

    Use Document Intelligence to streamline the extraction and classification of data from a variety of documents. Document Intelligence is designed to work with existing automated systems, making operations more efficient and saving effort.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   ****

    Use the generative AI skills in Now Assist products to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.

-   ****

    Use Now Assist in Contract Management to analyze contracts for non-standard and missing clauses, and extract information from signed contracts to automatically add in the contract repository.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

