---
title: Now Assist for Financial Services Operations release notes
description: Version history for the Now Assist for Financial Services Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-now-assist-fso.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Now Assist for Financial Services Operations release notes

Version history for the Now Assist for Financial Services Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.2.0 - June 2026**
    -   New:
        -   Added Insurance Customer Profile Summarization skill for Customer 360
        -   AddedInsurance interaction context summary skill
-   **Version 3.1.0 - May 2026**

    Changed: Updated role masking for CSR skills to use CSR sn\_fso\_csr.personal\_agent and sn\_fso\_csr.business\_agent roles.

-   **Version 3.0.0 - April 2026**
    -   New:
        -   Added Friendly Fraud Agent capability for Advanced and Prime tiers
        -   Added subscription profile support for customer management
        -   AddedCustomer Profile Summarization skill to provide overview of customer information including owned financial accounts, recent activities
        -   AddedCustomer Interaction Context Summary skill to provide context aware summaries of customer based on call intent
        -   Enabled AI Search capabilities for Customer Service Representatives to search and retrieve relevant information
        -   Introduced accessibility support for the Interaction page
    -   Changed:
        -   Improved prompts across multiple skills to support all AI models \(3P and 5P\)
        -   Improved error messages for skill failure scenarios
-   **Version 2.0.5 - January 2026 \(Zurich\)**

    Fixed: Fixed app dependency in package.json

-   **Version 1.2.1 - January 2026 \(Yokohama\)**
    -   New:
        -   Added support for the LTS model for skills.
        -   Added role masking security for all skills.
-   **Version 2.0.4 - December 2025**
    -   New:
        -   Added support for latest Now LLM Service models on all skills.
        -   New skill configuration added for financial task email draft.
    -   Changed: Added dependency on CSM Gen AI application.
-   **Version 1.1.4 - October 2025**
    -   Changed
        -   Version number update. No net new changes.
-   **Version 1.0.7 - October 2025**
    -   New
        -   Added security ACLs for Dispute Summarization
        -   Added security ACLs for Claim Summarization
-   **Version 1.1.3 - September 2025**
    -   New:
        -   Added security ACLs for Dispute Summarization
        -   Added security ACLs for Claim Summarization
        -   Added security ACLs for Report a dispute via Virtual Agent functionality
-   **Version 1.1.2 - August 2025**
    -   New: Support for the following models - Amazon Bedrock, GCP Vertex AI \(Google Gemini\), Azure OpenAI, and Now LLM - across all FSO skills and AI agents.
    -   Changed: Dispute Summarization - Financial transaction on Dispute Task has been added to the Now Assist Admin configuration to improve summarization results.
-   **Version 1.0.6 - June 2025**

    Changed: Version number update. No net new changes.

-   **Version 1.1.1 - May 2025**
    -   New:
        -   Added a demo data KB article that is used for the Friendly Fraud AI agent.
        -   Added a recognition word to facilitate asking questions.
    -   Changed:
        -   Enhanced the utilization of dispute transactions for summarization and updated the dispute skill configuration.
        -   In default LLM-enabled Text Input, disabled the Enforce User Input option to allow rephrasing and asking different questions based on user input.
    -   Removed:
        -   Removed the read-only restriction from sys\_one\_extend\_definition\_config and sys\_generative\_ai\_prompt\_config.
-   **Version 1.1.0 - March 2025**

    Changed: Version number update; no net new changes.

-   **Version 1.0.5 - March 2025 \(Xanadu\)**

    Fixed: Fixed an issue with dispute summarization by removing the obsolete chargeback reason code field from the Now Assist configuration.

-   **Version 1.1.0 - February 2025**

    Changed: Version number update; no net new changes.

-   **Version 1.0.5 - February 2025**

    Fixed an issue with dispute summarization by removing the obsolete chargeback reason code field from the Now Assist configuration.

-   **Version 1.0.2 - February 2025**
    -   New: New skill added: Disputes intake via Virtual Agent.
    -   Changed: Plugin name changed to Now Assist for Financial Services Operations \(FSO\).
    -   Fixed: Summarization prompt for dispute and claims.
    -   Removed: Removed chargeback reason code.
-   **Version 1.0.1 - November 2024**

    Changed: Updated the plugin name from Now Assist for Financial Services Operations to Now Assist for Financial Services Operations \(FSO\).

-   **Version 1.0.0 - August 2024**

    Now Assist for Financial Services Operations \(FSO\) leverages generative AI capabilities to address complex cases in the financial services industry like credit card disputes and insurance claims. Features like dispute case summarization and claim summarization use generative AI to quickly and accurately summarize key case details, streamline workflows, and significantly reduce processing times and mistakes. By quickly extracting the most important information employees need to action their work, financial institutions can reduce manual effort, improve customer satisfaction, and drive growth.


**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

