---
title: Continuous Authorization and Monitoring release notes
description: The ServiceNow Continuous Authorization and Monitoring application provides a structured approach to defining an authorization package and completing the seven stages of the NIST Risk Management Framework. Release notes are organized by version.Continuous Authorization and Monitoring streamlines authorization package management with shared document versioning and approvals, AI-powered summarization, OSCAL import/export enhancement, and a dedicated POAM user role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/grc-cam-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [continuous authorization, monitoring, NIST RMF, release notes, CAM version 23.0.1, OSCAL, POAM, authorization package]
breadcrumb: [Governance, Risk, and Compliance release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Continuous Authorization and Monitoring release notes

The ServiceNow® Continuous Authorization and Monitoring application provides a structured approach to defining an authorization package and completing the seven stages of the NIST Risk Management Framework. Release notes are organized by version.

## About Continuous Authorization and Monitoring

-   Applies a standardized approach to automate the NIST Risk Management Framework, a U.S. Federal mandate for information system security.
-   Defines clear accountability across System Owners, Authorizing Officials, Security Control Assessors, Information System Security Officers, and other roles
-   Provides continuous monitoring and centralized management of NIST RMF compliance, including control implementation and assessment, authorization boundaries and impact levels, and Plans of Action &amp; Milestones \(POA&amp;M\)

See [Continuous Authorization and Monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-cam-landing-page.md) for more information.

## Activation and other requirements

Continuous Authorization and Monitoring is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Continuous Authorization and Monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-rn-landing.md)

## September 2026

Continuous Authorization and Monitoring streamlines authorization package management with shared document versioning and approvals, AI-powered summarization, OSCAL import/export enhancement, and a dedicated POAM user role.

### What's new

-   **[Document reuse and version control across records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/c_cam_document_management_system.md)**

    Link documents as shared resources across authorization packages, boundaries, and engagements. Set approval workflows to control who reviews and activates documents before they take effect.

-   **[Analyze documents with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/t_use_smart_docs_with_documents.md)**

    Summarize documents, generate frequently asked questions with answers, or ask specific questions about document content, all from the Documents side panel in an authorization package, boundary, or engagement.

-   **[Voice-based document analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/t_use_smart_docs_with_documents.md)**

    Generate spoken audio summaries of documents and conduct voice-based Q&amp;A using the Voice Assist panel, from the Documents side panel in an authorization package, boundary, or engagement.

-   **[Connect documents to external cloud storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/t_connect_documents_to_external_cloud.md)**

    Link documents from Google Drive, OneDrive, or SharePoint and keep them synchronized with authorization packages, boundaries, and engagements. Pull updates from cloud storage or push approved versions back, without manual downloads and uploads.

-   **[AI-generated authorization package summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/t_generate_authorization_package_summary.md)**

    Using generative AI, the Authorization package summarization skill generates a summary of authorization package records. Each summary consolidates system purpose, impact level, operational status, and open POA&amp;M counts to show the package's current state.

-   **[POAM user role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/cam-roles-list.md)**

    Users with the POAM User role can view and update their assigned Plan of Action and Milestones \(POA&amp;Ms\), including viewing and updating tasks, accepting or rejecting acceptance tasks, and completing milestone tasks.


### What's changed

-   **[OSCAL enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/oscal-cam-ws.md)**

    The OSCAL enhancements include:

    -   Import system-generated authority documents \(SSP, POA&amp;M, SAR, SAP, ATO Letter, Executive Summary reports\) and user-attached files at Authorization Package and Authorization Boundary levels during OSCAL import.
    -   Control objective IDs include source values during OSCAL import and export.
    -   Policy fields are included during OSCAL import and export.

### What's deprecated or removed

### Now LLM Service Plugin information

-   **Plugins planned for deprecation**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


