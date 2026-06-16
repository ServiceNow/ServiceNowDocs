---
title: Now Assist for Accounts Payable Operations release notes
description: Version history for the Now Assist for Accounts Payable Operations \(APO\) application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-source-to-pay-ops-na-accounts-payable-ops.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Accounts Payable Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Now Assist for Accounts Payable Operations release notes

Version history for the Now Assist for Accounts Payable Operations \(APO\) application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.0.0 - June 2026**
    -   New:
        -   Leveraging Intent to Action Agentic Workflow for emails to be parsed and categorized as the correct intent to create a invoice inquiry case record.
        -   Enhanced workflow to enable requesters to accept/reject the case resolution.
-   **Version 7.2.1 - May 2026**

    Minor defect fixes

-   **Version 7.1.0 - April 2026**

    Enhanced to support APO foundation and Prime apps

-   **Version 7.0.0 - March 2026**
    -   Sentiment analysis capability has been added to invoice cases to surface the emotional tone of the inquiry based on available case communication
    -   Email response generation capability enables AP specialists and agents to quickly compose context‑aware emails from invoice cases using GenAI, leveraging relevant invoice, approval, and payment information to improve productivity.
    -   Text‑to‑Analytics capability allows AP users to create reports, insights, and visual analytics on demand by using natural language prompts. This removes the need for technical reporting skills and speeds up data-driven decision-making.
    -   New 3p model offering enablement
        -   Small model track
            -   OpenAI GPT-5 mini
            -   Claude Haiku 4.5
            -   Gemini 3.0 Flash
        -   Large model track:
            -   OpenAI GPT-5.2
            -   Claude Sonnet 4.5
            -   Gemini 3.0 Pro
-   **Version 6.0.1 - December 2025**
    -   New: "Recommend invoice owner" AI agent is created to automatically identify and recommend the right business owner for non-PO invoices, reducing manual effort and speeding up invoice processing.
    -   Changed:
        -   Enhanced "Resolve supplier questions" to auto-classify invoice inquiries and to enable AP help desk agents to view and accept resolution recommendation using the Now Assist Panel.
        -   Summary Skill Migration to Now Assist Skill Kit \(NASK\)
-   **Version 5.5.0 - October 2025**

    Optimized the Resolve Supplier Questions workflow by consolidating multiple AI agents and tools into a single agent with one unified tool, improving performance and reducing operational costs.

-   **Version 4.5.0 - October 2025**

    Optimised the Resolve Supplier Questions workflow by consolidating multiple AI agents and tools into a single agent with one unified tool, improving performance and reducing operational costs.

-   **Version 1.5.0 - October 2025**
    -   Security-related changes implemented for invoice case summarization on Release Xanadu.
    -   Apriel model capabilities adopted for invoice case summarization.
-   **Version 5.0.0 - September 2025**
    -   Resolve Supplier Questions:
        -   Expanded Scope: The agent now includes payment-related information, enabling broader case coverage and more comprehensive responses.
        -   Faster Activation: The trigger condition has been updated to assigned', ensuring the workflow activates immediately when a case is assigned no delays.
        -   3P Model Support: Compatibility has been extended to include the 3P model, offering greater flexibility across supplier engagement scenarios.
        -   Field Extractor Skill: A new skill automatically extracts the invoice number from the email description and updates the reference field minimising manual effort and improving data accuracy.
    -   GenAI-Powered Multi-Record Summarisation for SuppliersGet a complete supplier view at a glance. This feature uses generative AI to summarise multiple records into a single, coherent snapshot saving time, enabling confident decision-making, and reducing the risk of missing critical details. Compatibility has been extended to include the 3P model.
    -   Unified AI Search with Genius ResultsSay goodbye to tedious searches. Unified AI search intelligently surfaces the most relevant records across multiple tables, helping users instantly find what they need and focus on higher-value work.
-   **Version 4.1.0 - September 2025 \(Yokohama\)**
    -   GenAI-Powered Multi-Record Summarisation for SuppliersGet a complete supplier view at a glance. This feature uses generative AI to summarise multiple records into a single, coherent snapshot saving time, enabling confident decision-making, and reducing the risk of missing critical details. Compatibility has been extended to include the 3P model.
    -   Unified AI Search with Genius ResultsSay goodbye to tedious searches. Unified AI search intelligently surfaces the most relevant records across multiple tables, helping users instantly find what they need and focus on higher-value work.
-   **Version 4.0.0 - August 2025**
    -   Customers can now choose their preferred LLM for GenAI skills and agents, enabling better accuracy and alignment with enterprise AI strategies.
        -   Supported LLMs: Now LLM, Azure OpenAI, Google Gemini, Anthropic Claude
        -   Supported Skills: PO line mapping, Invoice case summarisation
-   **Version 3.0.1 - May 2025**
    1.  In additional to processing invoices and paying suppliers on time, Accounts payable teams are bogged down by loads of invoice inquiries. In this release, we are introducing an AI agent-powered workflow "Resolve supplier questions" designed to reduce manual effort in answering basic invoice inquiries. Once after invoice inquiry is received and assigned to a user, AI agents will work autonomously to understand the context of the inquiry and will propose a resolution, which can be reviewed and accepted by AP user. As a result, accounts payable team will be able to save significant amount of time that can be used to handle strategic initiatives.
    2.  Now Assist Panel for summarization will allow fulfillers to summarize invoice cases and converse with Now Assist without needing to navigate away from their current work. The Now Assist Panel can be activated within in the navigation bar in the Platform experience. System administrators can enable this experience simply within the Now Assist Admin Console.
    3.  Enhanced invoice case summarization feature with multi-language support powered by Now Assist. Summaries are now available in multiple languages beyond English, enabling broader accessibility and improved global collaboration.
    4.  A new requester role is added to access Now Assist Accounts Payable Operations features powered by generative AI. Customers need to explicitly grant these roles to users for access to GenAI features and capabilities.
    5.  Added new skill to allow AP users generate and view purchase order summary using Now Assist.
-   **Version 2.0.0 - February 2025**

    New: Conversational intake flows for suppliers provide an easy, automated and faster way to get queries answered and request status updates.

-   **Version 1.0.1 - November 2024**

    Now Assist for Accounts Payable Operations \(APO\) leverages the platform's Now Assist record summarization skill and enables the Accounts Payable team to view the summary of amount of work done and next steps that are needed to be performed on complex cases like invoice processing and invoice inquiry. Users can gain this insight without needing to navigate multiple screens or perform extra actions.


