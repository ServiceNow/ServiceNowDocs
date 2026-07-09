---
title: Now Assist in Document Intelligence release notes
description: The ServiceNow Now Assist in Document Intelligence application uses generative AI to extract information from documents, summarize document content, and provide answers to predefined questions. Now Assist in Document Intelligence was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
---

# Now Assist in Document Intelligence release notes

The ServiceNow® Now Assist in Document Intelligence application uses generative AI to extract information from documents, summarize document content, and provide answers to predefined questions. Now Assist in Document Intelligence was enhanced and updated in the Zurich release.

## Now Assist in Document Intelligence highlights for the Zurich release

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   View citations for multiple attachments using the document and visual insights AI agent.
-   Create skills with data extraction, question answering, and summarization capabilities using document and visual intelligence in Now Assist Skill Kit.
-   Now Assist in Document Intelligence skills are now turned on by default.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   View a test document in a larger workspace on a separate browser tab during use case setup.
-   Use the document and visual insights AI agent to upload files, extract information without a predefined use case using a selected LLM, and display the results in a dedicated document view.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Leverage document data extraction and document Q&amp;A capabilities in a single Extract information from documents skill.
-   Create skills with data extraction, question answering, and summarization capabilities by using document and visual intelligence in Now Assist Skill Kit.
-   Choose the language for a use case to help the optical character recognition \(OCR\) model better detect the text to extract from your files.
-   Extract information from files with text written in Simplified Chinese or Japanese.
-   Extract information from documents for Operational Sustainability Management \(Operational Sustainability Risk Management\) workflows.

[Early Availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

See [Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/docintel-nowassist-landing.md) for more information.

**Important:** Now Assist in Document Intelligence is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Document and visual insights AI agent enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/document-and-visual-insights-ai-agent.md)**

    The document and visual insights AI agent can recognize and provide citations for multiple attachments.


-   **[Open document in a new tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/set-up-use-case-for-now-assist-document-intelligence.md)**

    View a test document in a larger workspace on a separate browser tab during use case setup.

-   **[Image captioning in Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-center.md)**

    Extract information from images to support accessibility captioning in knowledge base articles.

-   **[Document and visual insights AI agent enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/document-and-visual-insights-ai-agent.md)**

    Leverage features that enable you to use the document and visual insights AI agent with selected LLMs to upload files, extract information without a predefined use case, and display results in a dedicated document view.

    -   Select an LLM for the AI agent to use when processing documents and images.
    -   Now LLM Service is not an available option for LLM selection.
    -   Prompt the AI agent to upload a file to process.
    -   View the results of the AI agent actions in a document view screen.

-   **[Document Intelligence for Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/add-document-intelligence.md)**

    Use document and visual intelligence to leverage extraction, question answering, and summarization capabilities for a skill created with Now Assist Skill Kit.

-   **[Language model selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/languages-supported-now-assist-document-intelligence.md)**

    Select the language for a use case to help the optical character recognition \(OCR\) model to detect text in the document and image files.

-   **[Image mode selection for use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/set-up-use-case-for-now-assist-document-intelligence.md)**

    Turn on image mode to process images more efficiently for use cases that use a multimodal AI model.

-   **[Model provider flexibility at the use case level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/llms-now-assist-document-intelligence.md)**

    Choose a model provider at the use case level, including a Now Assist default option that uses the instance-level model selected in AI Control Tower.

-   **[Information extraction for Operational Sustainability Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/environmental-social-governance/filter-citations-and-authority-documents-for-esg.md)**

    Extract ESG-related information from invoices to support Operational Sustainability Risk Management initiatives and regulatory compliance.

-   **[Improved security for the document and visual insights AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-security-implementation.md)**

    Enable access control lists \(ACLs\) to improve the security for the document and visual insights AI agent. ACLs provide you with the capability to run AI agents and agentic workflow executions either as a dynamic user or an AI user.

    The document and visual insights AI agent and its skills are classified as a worker or helper agent. A worker can act as an AI user with different privileges than the human user. A helper only has the privileges of a human user.


-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.


## UI changes

-   **[Updated banner in the extraction review panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/document-intelligence-workspace-with-now-assist.md)**

    Changed the label in the extraction review panel banner from Document Q&amp;A to Extracted data.


-   **[Usability changes for the Extract information from documents skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/docintel-exploring-now-assist.md)**

    Various features for the Extract information from documents skill are updated to unify the experience for data extraction and document Q&amp;A.

    -   The Extract information from documents skill has been added to the list of Platform skills in the Now Assist Admin console to incorporate both the Document extraction and the Document Q&amp;A skills.
    -   In the use case setup, the panel for defining a field displays the options for **Field**, **Question**, and **Table**.
    -   Table columns defined for a use case are displayed in a group in the fields list on the use case page.
    -   The Document Intelligence workspace displays the fields, tables, and questions in the same review panel.

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Document and visual insights AI agent enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/document-and-visual-insights-ai-agent.md)**

    Tools used by the document and visual insights AI agent are consolidated to improve performance.

-   **[Changes to limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-document-intelligence-limitations.md)**

    The file size limit for uploading a file using the attachment summarization feature is changed from 10MB to 20MB.

-   **[Document Intelligence for Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/add-document-intelligence.md)**

    The document and visual intelligence capabilities used to leverage extraction, question answering, and summarization capabilities for skills created with Now Assist Skill Kit are available to users with the appropriate role\(s\).

-   **[Now Assist in Document Intelligence skills are now turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading: Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Changes to limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-document-intelligence-limitations.md)**

    The page count limit decreases to 20 pages per file for an extraction based on a use case with a table defined.

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


-   **Merged skills**

    Document data extraction and document Q&amp;A capabilities are available in a single Extract information from documents skill.

    -   The Extract information from documents skill is available in the list of Platform skills in the Now Assist Admin console.
    -   Data extraction and document Q&amp;A capabilities can be set up for the same use case.
    -   Agents can review the AI predictions for the fields, tables, and questions in the same task.
-   **[Document and visual insights AI agent enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/document-and-visual-insights-ai-agent.md)**

    Leverage added tools that enable the AI agent to display the extracted data and to look up existing use cases or create use cases based on descriptions and document attachments.

-   **[Changes to limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-document-intelligence-limitations.md)**

    The limitations set for Now Assist in Document Intelligence properties are updated to support processing larger documents.

    -   DOCX files are supported for information extraction.
    -   The page count limit is 200 pages per file If image mode is turned off for the use case. If image mode is turned on, the page count limit is 10 pages per file.
    -   The file size limit is 20 MB.

## Removed in this release

-   The Document extraction skill has been removed from the list of Platform skills in the Now Assist Admin console.
-   The Document Q&amp;A skill has been removed from the list of Platform skills in the Now Assist Admin console.

## Activation information

Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-apo.md)
-   [Now Assist for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-landing-cmdb.md)
-   [Now Assist for Collaborative Work Management \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/now-assist-for-cwm-landing.md)
-   [Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/now-assist-for-creator-landing.md)
-   [Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm.md)
-   [Now Assist for Employee Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assisit-employee-exp.md)
-   [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-portfolio-management/now-assist-ea.md)
-   [Now Assist for Operational Sustainability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/environmental-social-governance/now-assist-for-esg.md)
-   [Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/now-assist-fsm.md)
-   [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/now-assist-for-financial-services-operations.md)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-ham.md)
-   [Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-hs-landing.md)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-hrsd.md)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/now-assist-for-irm.md)
-   [Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-itom.md)
-   [Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm.md)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-lsd-landing.md)
-   [Now Assist for Operational Technology Manager \(OTM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-for-otm-landing.md)
-   [Now Assist for Operational Technology Service Management \(OTSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-for-operational-technology-service-management.md)
-   [Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/now-assist-order-management.md)
-   [Now Assist for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/government-industry/now-assist-for-psds.md)
-   [Now Assist for Sales Force Automation \(SFA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/now-assist-for-sales-and-order-management-som.md)
-   [Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-security-incident-landing.md)
-   [Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-sam.md)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-slo.md)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-spo.md)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/now-assist-spm.md)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-spmc.md)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/now-assist-tprm.md)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-wsd-landing.md)
-   [Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-vulnerability-response-landing.md)
-   [Now Assist for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/now-assist-for-zero-copy-connector-for-erp.md)

For more information, see [Configuring Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/docintel-configuring-now-assist.md).

## Additional requirements

Now Assist in Document Intelligence requires the installation of the Document Intelligence application \(sn\_docintel\) and at least one Now Assist product.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Localization information

-   **[Support for files in multiple languages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/languages-supported-now-assist-document-intelligence.md)**

    Process files with text in multiple languages, including Simplified Chinese and Japanese.


## Related ServiceNow applications and features

-   **[Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/document-intelligence-landing.md)**

    Use ServiceNow® Document Intelligence to streamline the extraction and classification of data from a variety of documents. Document Intelligence is designed to work with existing automated systems, making operations more efficient and saving effort.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skill-kit-landing.md)**

    Use the generative AI skills in ServiceNow® Now Assist products to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.

-   **[Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-now-assit-landing.md)**

    Use ServiceNow® Now Assist in Contract Management to analyze contracts for non-standard and missing clauses, and extract information from signed contracts to automatically add in the contract repository.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

