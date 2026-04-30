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

Yokohama Patch 13

-   Now Assist in Document Intelligence skills are on by default.

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Summarize the content in document and image attachments with the document and visual insights AI agent.
-   Choose a large language model \(LLM\) to generate predictions for extraction and Q&amp;A \(question &amp; answer\) use cases.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Boost productivity by using the document and visual insights AI agent to autonomously analyze and extract data from documents and images.
-   Streamline document data extraction by automating document tasks.
-   Use Virtual Agent to ask questions about the document content.
-   Extract the data from invoices with Now Assist for Accounts Payable Operations \(APO\).

[Early Availability](../quality/yokohama-all-other-fixes.md)

-   Speed up your document processing workflows and quickly extract the text and tables from your documents.
-   Save time looking for the information that you need in a document, and quickly find the answers to predefined questions.

See [Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=docintel-nowassist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

**Important:** Now Assist in Document Intelligence is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Now Assist in Document Intelligence release

-   **[Document and visual insights AI agent enhancements](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The document and visual insights AI agent can recognize and provide citations for multiple attachments.


-   **[LLM selection for use cases](https://www.servicenow.com/docs/access?context=set-up-use-case-for-now-assist-document-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure a different LLM to generate predictions for extraction and Q&amp;A use cases.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[Document and visual insights AI agent](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use an AI agent to help process the tasks that analyze and extract data from documents and images.

-   **[Full automation for document data extraction](https://www.servicenow.com/docs/access?context=turn-on-full-automation-for-document-extraction-na&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Automatically extract the document data and process the document task without agent review.

-   **[Data extraction from accounts payable \(AP\) invoices](https://www.servicenow.com/docs/access?context=exploring-now-assist-apo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

    Extract data from invoices with Now Assist for APO.

-   **[Document chat in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Integrate Now Assist for Virtual Agent with Now Assist in Document Intelligence to enable the chat responses that are based on the document content.

-   **[Attachment summarization in ITSM](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    View the summaries of attachments with the record summary in ITSM.


-   **[Document extraction](https://www.servicenow.com/docs/access?context=extract-document-data-with-now-assist-document-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Extract the data from documents by using LLMs to provide the recommended field values.

-   **[Document Q&amp;A](https://www.servicenow.com/docs/access?context=review-document-qnas-with-now-assist-document-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use generative AI to find the answers to the predefined questions in a document.

-   **[Setting up use cases for Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=set-up-use-case-for-now-assist-document-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Set up Document Intelligence use cases to enable agents to use the document extraction and document Q&amp;A skills.


## UI changes

-   **[Usability enhancements to use case setup features](https://www.servicenow.com/docs/access?context=set-up-use-case-for-now-assist-document-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Various features for the use case setup are updated to create a more effective user experience:

    -   **Field** is changed to **question** in the field form for Q&amp;A use case setup.
    -   **Single field** is changed to **Field** in the field form for the document extraction use case setup.
    -   An **Additional Details** field is added to the table form for the document extraction use case setup as a way to help the large language model \(LLM\) extract the relevant information from the document.

## Changed in this release

-   **[Document and visual insights AI agent enhancements](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Tools used by the document and visual insights AI agent are consolidated to improve performance.

-   **[Now Assist in Document Intelligence skills are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading: Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Document and visual insights AI agent enhancements](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Generate a summary of document and image attachments with the document and visual insights AI agent.


## Activation information

Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)
-   [Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)
-   [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)
-   [Now Assist for Employee Experience](https://www.servicenow.com/docs/access?context=now-assisit-employee-exp&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)
-   [Now Assist for Operational Sustainability \(formerly ESG\)](https://www.servicenow.com/docs/access?context=now-assist-for-esg&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Operational Technology Manager \(OTM\)](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)
-   [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)
-   [Now Assist for PSDS](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=yokohama&pubname=yokohama-government-industry&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)

For more information, see [Configuring Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=docintel-configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Additional requirements

Now Assist in Document Intelligence requires the installation of the Document Intelligence application \(sn\_docintel\) and at least one Now Assist product.

## Related ServiceNow applications and features

-   **[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use Document Intelligence to streamline the extraction and classification of data from a variety of documents. Document Intelligence is designed to work with existing automated systems, making operations more efficient and saving effort.

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the generative AI skills in Now Assist products to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.

-   **[Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use Now Assist in Contract Management to analyze contracts for non-standard and missing clauses, and extract information from signed contracts to automatically add in the contract repository.


**Parent Topic:**[AI Experiences release notes](intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

