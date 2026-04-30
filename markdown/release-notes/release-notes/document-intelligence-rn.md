---
title: Document Intelligence release notes
description: The ServiceNow Document Intelligence application is an artificial intelligence \(AI\) solution that quickly and accurately categorizes and extracts information from documents. Document Intelligence was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-09-30"
reading_time_minutes: 5
---

# Document Intelligence release notes

The ServiceNow® Document Intelligence application is an artificial intelligence \(AI\) solution that quickly and accurately categorizes and extracts information from documents. Document Intelligence was enhanced and updated in the Xanadu release.

## Document Intelligence highlights for the Xanadu release

[Xanadu Patch 9](../quality/xanadu-patch-9.md)

-   Boost productivity by using the document and visual insights AI agent in Now Assist to autonomously analyze and extract data from documents and images.
-   Streamline document data extraction by automating document tasks.
-   Use Virtual Agent to ask questions about the document content.

[Xanadu Patch 3](../quality/xanadu-patch-3.md)

-   Extract information from contract documents by using Now Assist in Document Intelligence.

[Early Availability](../quality/xanadu-all-other-fixes.md)

-   Extract the data from single fields by using the Draw tool to select a document area and extract the information.
-   Standardize the extracted data by determining how to interpret ambiguous field values and by matching extracted values with data in a referenced table.
-   Process documents that are written in Simplified Chinese or Japanese.
-   Monitor your Document Intelligence implementation with improved dashboard charts.

See [Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

**Important:** Document Intelligence is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Improved security for the document and visual insights AI agent](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Enable access control lists \(ACLs\) to improve the security for the document and visual insights AI agent. ACLs provide you with the capability to run AI agents and agentic workflow executions either as a dynamic user or an AI user.

    The document and visual insights AI agent and its skills are classified as a worker or helper agent. A worker can act as an AI user with different privileges than the human user. A helper only has the privileges of a human user.


-   **[Document and visual insights AI agent](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use an AI agent to help process tasks that analyze and extract data from documents and images.

-   **[Full automation for document data extraction](https://www.servicenow.com/docs/access?context=data-extraction-modes-now-assist-document-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Automatically extract document data and process the document task without agent review.

-   **[Document chat in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Integrate Now Assist for Virtual Agent with Now Assist in Document Intelligence to enable chat responses based on document content.

-   **[Attachment summarization in ITSM](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    View the summaries of attachments with the record summary in ITSM.


-   **[Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=docintel-nowassist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use Now Assist in Document Intelligence to extract information from contract documents with generative AI.


-   **[Draw tool enhancements](https://www.servicenow.com/docs/access?context=use-draw-mode-to-extract-fields&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Extract the data from single fields by using the draw tool to select a document area and extract the information.

-   **[Data normalization](https://www.servicenow.com/docs/access?context=data-normalization&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Standardize the data extracted from documents with the following improvements:

    -   Determine a default interpretation of the ambiguous values for the date and number fields.
    -   Create a Reference field type to match the extracted field values with the fields in a referenced table record.
-   **[Dashboards in the Admin experience](https://www.servicenow.com/docs/access?context=monitoring-document-intelligence-performance&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Monitor the overall performance of Document Intelligence in the Document Intelligence monitoring dashboard. You can monitor the performance at the use case level in the use case performance dashboard.

-   **[Document classification integration workflow](https://www.servicenow.com/docs/access?context=configure-integration-setup&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Integrate document classification use cases with a custom application or workflow.


## UI changes

-   **[Usability enhancements to Draw tool features](https://www.servicenow.com/docs/access?context=use-draw-mode-to-extract-fields&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Various Draw tool features are updated to create an effective user experience.


## Removed in this release

Starting in the Xanadu release, the Platform Document Intelligence Usage dashboard is no longer supported or available through the Document Intelligence application. Performance metrics are available in the Document Intelligence Admin experience. For more information, see [Document Intelligence monitoring dashboard](https://www.servicenow.com/docs/access?context=document-intelligence-monitoring-dashboard&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Activation information

Install Document Intelligence by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). The Document Intelligence application \(sn\_docintel\) depends on the Document Intelligence plugin \(com.glide.platform\_ml\_di\), the Predictive Intelligence plugin \(com.glide.platform\_ml\), and the Document Intelligence UIB component \(com.sn\_docintel\_iframe\). For more details, see [Install Document Intelligence](https://www.servicenow.com/docs/access?context=install-document-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Accessibility information

-   **Support for reflow**

    The sn-docintel-iframe component was updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


## Localization information

-   **[Chinese and Japanese language support](https://www.servicenow.com/docs/access?context=languages-supported-by-document-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Process documents in additional languages with added support for Simplified Chinese and Japanese.


## Related ServiceNow applications and features

-   **[Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    Use Now Assist in Contract Management to review contracts and extract information from signed contracts to add in the contract repository.

-   **[Accounts Payable Operations](https://www.servicenow.com/docs/access?context=integrate-docintel-apo&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use Document Intelligence for Accounts Payable Operations to extract information quickly and accurately from invoice documents that are received as attachments via email, as well as create invoice records in the Accounts Payable Operations application.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=integrate-docintel-csm&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use Document Intelligence for Customer Service Management \(CSM\) to extract relevant information from email and case attachments, such as account numbers or customer addresses, and add that information to cases.

-   **[Financial Services Operations](https://www.servicenow.com/docs/access?context=integrate-docintel-fso&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use Document Intelligence integrated with the digital workflows in the Financial Services Operations applications to help your organization quickly automate document processing and accurately extract information from documents to the ServiceNow AI Platform.

-   **[Automation Center](https://www.servicenow.com/docs/access?context=automation-center-landing-page&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Use Document Intelligence for Automation Center to discover automation opportunities for document processing using DocIntel automation metrics.


**Parent Topic:**[Intelligent Experiences release notes](intelligent-experiences-rn-landing.md)

