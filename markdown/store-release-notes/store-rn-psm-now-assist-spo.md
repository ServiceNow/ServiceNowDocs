---
title: Now Assist for Sourcing and Procurement Operations \(SPO\) release notes
description: Version history for the Now Assist for Sourcing and Procurement Operations \(SPO\) on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-psm-now-assist-spo.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Now Assist for Sourcing and Procurement Operations \(SPO\) release notes

Version history for the Now Assist for Sourcing and Procurement Operations \(SPO\) on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.0.0 - June 2026**
    -   New:
        -   The Intent to Action agentic workflow analyzes incoming emails to automatically identify the appropriate procurement intent and create corresponding procurement case records. Procurement teams can review the generated cases and take the necessary actions to efficiently manage procurement requests.
        -   The Savings Opportunity Discovery agentic workflow analyzes contracts, spend data, sourcing pipeline data, and supplier performance on a recurring schedule to automatically identify a prioritized list of savings opportunities. Category managers can review each opportunity in the Now Assist Panel and create a pipeline project or dismiss the opportunity directly from the panel.
-   **Version 9.2.2 - May 2026**

    Minor defect fixes to ensure stable operation across supported environments.

-   **Version 9.1.0 - April 2026**
    -   AI-native initiatives:
        -   Pricing and packaging updates including revised tier structures
        -   Minor defect fixes to enhance system stability and user experience
-   **Version 9.0.0 - March 2026**
    -   New:
        -   Conversational Intake Enhancements. Faster procurement intake with reduced wait times, fewer confirmations, multi-attachment uploads, and integrated product recommendations.
        -   Intelligent SOW Document Processing. AI Agents extract key data from uploaded SOWs, autofill request forms, and create sourcing requests automatically.
        -   Automatic Category Assignment. AI assigns Product and Spend Categories at the line level during SR/PR/PO creation using metadata and historical data. Users can review and override.
        -   Continuous Category Audit &amp; Correction. A background engine validates categories when key fields change, flags inconsistencies, and notifies users for correction.
        -   Invoice Spend Categorization. Spend categories auto-propagate from PO lines to Invoice lines during matching, ensuring consistent data for analytics.
        -   Category Correction via Now Assist. Specialists can validate and correct spend categories across SR, PR, PO, and Invoice records from the Now Assist Panel.
        -   Procurement Case Sentiment Analysis. Detects requester sentiment from case fields and chats, surfacing indicators to help specialists prioritize sensitive cases.
        -   Email Response Generation. Now Assist drafts context-aware email responses across procurement cases, sourcing requests, requisitions, sourcing events, and negotiations.
        -   AI Canvas for S2P Reporting. Business users create dynamic reports and visualizations using natural language prompts, no technical expertise required.
-   **Version 8.0.0 - December 2025**

    New: Quote-to-request automation: Employees no longer need to manually copy information from vendor quotes into procurement request forms.They can now upload a quote file, and the system automatically extracts key details, such as supplier information, item descriptions, quantities, and pricing, to pre-fill the appropriate request form for quick review and submission.

-   **Version 7.0.0 - October 2025**
    -   Changed:
        -   The "Help fulfill procurement requests" agentic workflow has been renamed to "Conversational intake for sourcing and procurement" to better reflect its expanded scope and capabilities. Employees can now initiate sourcing and procurement requests conversationally, with the Agent automatically applying organizational policies, routing logic, and pre-filling request details for faster completion.
        -   Multi-product requests: Employees can request up to three items in a single session. The Agent intelligently routes each item within the conversation before presenting a web form - pre-filled for Shopping Hub checkout \(on-catalog\) or Employee Center request forms \(off-catalog\).
        -   Policy-based reasoning: Employees directly describe their business need, and the agent leverages codified procurement policies via a decision table to recommend and route the request according to policy.
        -   Include attachments in requests: Supporting documents and links can now be attached directly to sourcing requests and purchase requisitions at the time of submission.
        -   Optimized AI agent structure: To enhance performance and simplify maintenance, the workflow now operates with three core AI agents. The Procurement purchasing plan and Procurement sourcing plan AI agents have been consolidated into a single, unified Procurement product recommendation AI agent.
            -   Procurement inquiry analysis: Analyzes employee inquiries to determine next steps, routes tasks to the appropriate Agent, provides knowledge-based answers, and manages fallback handling for unsupported requests.
            -   Procurement product recommendation: Recommends products based on organizational buying criteria, creates purchasing or sourcing plans, and guides employees through the checkout or request process.
            -   Procurement request tracking: Finds and summarizes request status details to answer employee inquiries.
-   **Version 5.5.0 - October 2025**
    -   Changed:
        -   The following updates have been made in the Help fulfill procurement requests agentic workflow:
            -   Optimized AI agent structure: To enhance performance and simplify maintenance, the workflow now operates with three core AI agents. The Procurement purchasing plan and Procurement sourcing plan AI agents have been consolidated into a single, unified Procurement product recommendation AI agent.
                -   Procurement inquiry analysis: Analyzes employee inquiries to determine next steps, routes tasks to the appropriate Agent, provides knowledge-based answers, and manages fallback handling for unsupported requests.
                -   Procurement product recommendation: Recommends products based on organizational buying criteria, creates purchasing or sourcing plans, and guides employees through the checkout or request process.
                -   Procurement request tracking: Finds and summarizes request status details to answer employee inquiries.
-   **Version 2.5.1 - October 2025**
    -   Fixed:
        -   Minor bug fixes
-   **Version 6.0.2 - September 2025**
    -   New in this release:
        -   Off-catalog request capture with complete, actionable details.
        -   Tailored product suggestions based on organizational buying behavior.
        -   Request placement with approved suppliers.
        -   Self-service visibility into request and order progress.
        -   Knowledge article summaries for faster issue resolution.
-   **Version 5.2.0 - September 2025 \(Yokohama\)**

    Changed: Added minor updates for all summarization skills.

-   **Version 5.0.1 - August 2025**
    -   New:
        -   Third-party model support
            -   Description:
                -   Customers can build and scale GenAI workflows using their model of choice \(now includes GPT, Claude or Gemini; in addition to the standard Now LLM\). All GenAI Skills are shipped with four models selectable out of the box.
            -   Customer benefits:
                -   Maximize performance from supported testing of the best industry models \(GPT, Claude or Gemini\) per use case
                -   Seamlessly switch between models without compromising on quality
                -   Stay adaptable with broad model support that aligns to evolving enterprise AI strategies and innovations
-   **Version 4.0.3 - May 2025**
    -   Launched a new Agentic workflow, Help fulfill procurement requests', to help requesters get the right procurement support by guiding them to the appropriate request type, while reducing manual effort for procurement teams through intelligent intake and inquiry deflection. This is an experience invoked within Portal through Virtual Agent. For customers to take advantage of this agentic workflow, they would need to deactivate purpose-built Virtual Agent Topics within Now Assist in Virtual Agent. Agentic workflows within Virtual Agent is the next generation of experience for requesters.
    -   New roles were introduced to access Now Assist Sourcing and Procurement Operations GenAI features for both requesters \(sn\_spend\_gen\_ai.now\_assist\_requester\) and fulfillers \(sn\_spend\_gen\_ai.now\_assist\_fulfiller\) to allow customers to control access of GenAI features for their users. Customers would need to explicitly grant these roles to users for access to GenAI features and capabilities.
    -   Introduced summarization for purchase orders, negotiation events and negotiations for fulfillers through surfacing relevant context and past activity in one place, helping fulfillers quickly understand the current state of work.Introduced summarization for purchase requisition, sourcing requests and purchase order summarization for requesters. This experience is enabled in Shopping Hub, allowing requesters to receive a swift summary of actions completed and next steps enabling increased transparency and clarity on request progress.
    -   Disambiguation is a new Platform capability embedded within Virtual Agent which reduces trial-and-error by intelligently routing users based on intent. This will help requesters quickly understand where to go and what to do for their procurement needs.
    -   Now Assist Panel for summarization will allow fulfillers to summarize work \(eg sourcing requests, purchase requisitions, negotiation events, negotiations and procurement cases\) and converse with Now Assist without needing to navigate away from their current work. The Now Assist Panel can be activated within in the navigation bar in the Platform experience. System administrators can enable this experience simply within the Now Assist Admin Console.
-   **Version 3.0.3 - February 2025**
    -   New:
        -   Utilize "synthesized answers" driven by Now Assist in the Virtual Agent to assist requesters in making IT or Procurement-related requests aligned with their business requirements.
        -   Improved the "Request to buy something" Virtual Agent topic by introducing a new user interface that suggests products and suppliers, thus minimizing non-compliant purchases.
        -   Improved AI Search and the RAG framework to recommend suppliers and products through semantic search and contextual filters, enhancing recommendations with criteria like preferred suppliers and previous purchases.
-   **Version 2.0.0 - November 2024**
    -   New:
        -   Provide fulfillers with a summary of procurement-related records. This enables them to get visibility into the status of the record in the procurement process and consequently enables them to take the necessary actions quickly. The fulfillers can get a summary of the following procurement records in the Source-to-Pay Workspace.
            -   Sourcing request summarization
            -   Purchase requisition summarization
            -   Procurement case summarization
        -   Enable requesters to inquire about their submitted procurement purchases and requests in Now Assist in Virtual Agent. They can check the progress of purchase requisitions, sourcing requests, and procurement cases by asking about the record number, description, or submission timeframe \(e.g., this week, this month, last quarter\). Now Assist in Virtual Agent will support the following actions:
            -   Answer questions about the status
            -   Provide updates on work remaining to close out the purchase or request
-   **Version 1.0.2 - August 2024**

    Now Assist for Sourcing and Procurement Operations \(SPO\) leverages the platform's Now Assist conversational skills, Now Assist in Virtual Agent, to guide requesters through a conversation-like experience to address their procurement needs. This reduces the need to rely on fulfillers by empowering requesters to submit their procurement requests accurately with an AI companion.


