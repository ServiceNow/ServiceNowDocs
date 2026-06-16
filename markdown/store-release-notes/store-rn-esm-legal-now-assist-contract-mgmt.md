---
title: Now Assist in Contract Management release notes
description: Version history for the Now Assist in Contract Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-esm-legal-now-assist-contract-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Legal Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Now Assist in Contract Management release notes

Version history for the Now Assist in Contract Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.1 - June 2026**
    -   Changed:
        -   Identify missing clauses in contract revisions with improved accuracy.
        -   Support for upgraded versions of third party LLMs has been provided.
    -   Fixed:
        -   The activity stream now correctly displays the document name when an AI review is initiated, replacing the previous 'null' placeholder.
        -   Email notifications to the contract administrator are now reliably sent when metadata extraction is completed.
-   **Version 2.1.10 - May 2026**
    -   Changed:
        -   Supports upgraded versions of third-party LLMs.
        -   Enhanced UI for visual clarity in AI-assisted features.
-   **Version 2.1.3 - April 2026**

    Refer to the Contract management Pro - Prime release notes.

-   **Version 2.1.0 - March 2026**
    -   New:
        -   Provide feedback on Now Assist identified non-standard and missing clauses to help improve its accuracy over time.
        -   Locate non-standard clauses in Microsoft Word by selecting Now Assist suggestions that automatically scroll to the relevant section using AI citations.
    -   Changed: Conversational search provides an improved user experience for search results in the Now Assist panel.
-   **Version 2.0.5 - December 2025**
    -   New:
        -   Configurable AI powered obligation extraction to automatically extract key contractual obligations from contract documents for user to review and approve.
        -   Now Assist powered conversational search to query contract documents using natural language and dialogue driven queries
    -   Fixed: The Question Group card component now appears correctly when creating or editing Contract analysis use cases in the Now Assist Admin console.
-   **Version 1.4.5 - October 2025**

    Fixed: Improved user experience on Now Assist Admin while configuring the use case mapping for Contract analysis skill.

    Note: If you have already installed Contracts Core\(com.sn\_cm\_core\) and Contract Workspace\(com.sn\_cm\_workspace\) plugins, upgrade them to the latest version.

-   **Version 1.2.8 - October 2025**
    -   New: Security improvements.
    -   Fixed: The configuration pages for the Now Assist Contract Analysis skill displayed additional UI actions that were not functional. These additional UI actions have been removed.
-   **Version 1.4.3 - September 2025**
    -   New: A related list, 'Playbook' has been added to Contract Workspace that appears when the 'Contract repository management' agentic workflow is enabled. The Playbook enables users to review metadata extracted by AI agents. Users can then edit the extracted information as needed and submit updates to the contract repository. If the contract end date is available, the Review contract reminders tab appears in the playbook, enabling you to review and update the AI-calculated contract reminder date and specify recipients for contract renewal or terminations.
        -   New ACLs have been created for AI agents and agentic workflows to control who can discover and trigger the agentic workflows.
-   **Version 1.3.0 - August 2025**
    -   New:
        -   The Manage contract repository agentic workflow is supported with third party LLMs - Azure OpenAI, Anthropic Claude on AWS, and Google Gemini.
        -   Contract analysis and Contract metadata extraction skills are supported with third party LLMs - Azure OpenAI, Anthropic Claude on AWS, and Google Gemini.
        -   In Contract metadata extraction skill, use case mappings can be configured on contract request table.
        -   In Contract analysis skill, use case mappings, clause mappings and expected response mappings can be configured on contract request table.
    -   Changed: Visual improvement in contract analysis skill to display Analyze with Now Assist action with animation.
    -   Fixed: Message has been improved when an ongoing contract analysis is canceled.
-   **Version 1.2.5 - June 2025**
    -   New: Use the Manage contract repository agentic workflow to improve productivity by autonomously creating milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.
    -   Changed:
        -   Create a use case mapping in the Now Assist Admin console to map a use case to specific tables and define conditions to apply the use case for metadata extraction.
        -   Create a use case and its associated question groups for contract analysis in the Now Assist Admin console to identify the non-standard and missing clauses in a contract.
        -   Create a clause mapping in the Now Assist Admin console to map question groups of a use case to the active clauses in the clause library to display suggestions for non-standard clauses in a contract.
        -   Create an expected response mapping in the Now Assist Admin console to map questions of a use case to an expected response to identify the non-standard clause in a contract.
        -   Create a use case mapping in the Now Assist Admin console to map a use case to specific tables and define conditions to apply the use case for contract analysis.
        -   Modify an existing use case by selecting All &gt; Document Intelligence &gt; Document Data Extraction Administration &gt; Use Cases. Note: In this release, creating and editing a use case is not available in the Now Assist Admin console.
-   **Version 1.2.3 - May 2025**
    -   New: Use the Manage contract repository agentic workflow to improve productivity by autonomously creating milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.
    -   Changed:
        -   Create a use case and its associated fields for contract metadata extraction in the Now Assist Admin console to define the information that you want Now Assist to detect in a signed contract.
        -   Create a use case mapping in the Now Assist Admin console to map a use case to specific tables and define conditions to apply the use case for metadata extraction.
        -   Create a use case and its associated question groups for contract analysis in the Now Assist Admin console to identify the non-standard and missing clauses in a contract.
        -   Create a clause mapping in the Now Assist Admin console to map question groups of a use case to the active clauses in the clause library to display suggestions for non-standard clauses in a contract.
        -   Create an expected response mapping in the Now Assist Admin console to map questions of a use case to an expected response to identify the non-standard clause in a contract.
        -   Create a use case mapping in the Now Assist Admin console to map a use case to specific tables and define conditions to apply the use case for contract analysis.
    -   Fixed:
        -   The AI nudge message is not appearing for Group Managers.
        -   The status on AI review tiles does not update in real time when a contract request is canceled.
        -   The "Review extracted metadata" button is visible even when the Contract metadata extraction skill is inactive.
-   **Version 1.1.0 - February 2025**
    -   Changed: In Use case mappings for Contract analysis and Metadata extraction, you can now map the use cases to only active contract types.
    -   Fixed: UI improvements
-   **Version 1.0.9 - December 2024**
    -   Changed:
        -   The Non Disclosure Agreement playbook has updated prompts.
        -   The field description has been updated for the Metadata Extraction use case.
    -   Fixed: Now Assist in Contract Management is creating multiple logs instead of one. This has been fixed.
-   **Version 1.0.6 - November 2024**

    ServiceNow Now Assist in Contract Management provides assisted contract reviews to contract attorneys and metadata extraction on signed contracts. The app enables contract attorneys to efficiently review contracts with missing or non-standard clauses during the contract review and negotiation stage as per the company's standard playbook.


**Parent Topic:**[ServiceNow Store - Legal Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-esm-legal-service-delivery.md)

