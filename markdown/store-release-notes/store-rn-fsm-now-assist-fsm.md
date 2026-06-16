---
title: Now Assist for Field Service Management \(FSM\) release notes
description: Version history for the Now Assist for Field Service Management \(FSM\) application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-now-assist-fsm.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Field Service Management release notes, ServiceNow Store release notes]
---

# Now Assist for Field Service Management \(FSM\) release notes

Version history for the Now Assist for Field Service Management \(FSM\) application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.0.1 - June 2026**
    -   New:
        -   AI-powered mobile form auto-fill for field technicians.
            -   Field technicians can use mobile camera to capture images and auto-populate form fields via AI image recognition, supporting smart assessments, input forms, and scripted questionnaires.
        -   Consistent AI visual indicators across applications.
            -   AI features now display unified gradient styles and subtle animations to indicate activity in Workspace, UI16, and mobile experiences, meeting accessibility standards.
        -   Parts Debrief automation in NAP and NAVA.
            -   Agents can automate parts debrief workflows, handling empty work notes, invalid part usage, quantity normalization, and error scenarios.
        -   Expanded AI summarization and knowledge workflows.
            -   Users can trigger work order/sidebar chat summarization and knowledge article generation across platforms with role-based workflows and answer validation.
        -   Create work order agent with enhanced persona coverage.
            -   System supports creating work orders from text/images in NAP/NAVA with persona validation, blocking invalid content.
        -   FSM AI Mandate features available on mobile and workspace.
            -   FSM AI capabilities \(IT automation, NAVA integration, smart assessments\) are now mobile/workspace accessible with role-based access.
        -   Telemetry for AI feature usage.
            -   Admins can track AI lens feature usage for FSM use cases.
        -   Skill refinement for FSM digital agents.
            -   FSM agents enhanced for improved automation and workflow handling.
    -   Changed:
        -   Broadened test and validation coverage for FSM AI use cases.
            -   Testing expanded across mobile/agent/NextWave experiences to certify features.
        -   Enhanced automation for AI SKU and agent studio test cases.
            -   Remaining automation scenarios completed with monitoring on latest NAP version.
        -   Improved parts debrief workflow handling.
            -   Better management of edge cases like unrecognized assets and invalid task states.
        -   Refined questionnaire answer validation in summarization workflows.
            -   Validation improved across NAP/NAVA/UI16/Workspace for task summarization.
        -   Performance testing for Q1 deliveries.
            -   Testing conducted to ensure system stability and responsiveness.
-   **Version 9.1.0 - April 2026**

    New: Supported version for new product tiers

-   **Version 9.0.3 - March 2026**
    -   New:
        -   Parts Manager AI agent: Track and validate parts usage when closing work order tasks. The AI agent interprets activity notes to update parts statuses and automatically adjusts inventory at task closure.
        -   Create Work Order from image: Create work orders by uploading photos of equipment issues. The AI agent extracts relevant information from the image to populate work order fields.
        -   Primary action button for Now Assist Virtual Agent: Access Now Assist Virtual Agent from a primary action button in the ServiceNow Agent mobile app navigation bar.
        -   Voice-to-text input: Use voice input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app.
        -   AI visual indicators: Consistent gradient styles indicate when AI is assisting or augmenting an experience across Workspace, UI16, and mobile interfaces.
        -   Updated icons in Now Assist Virtual Agent: Updated icons for web search, photo upload, and microphone functions.
    -   Changed: Create Work Order AI agent performance improvements: Reduced latency and improved response times. Inter-agent communication was streamlined to minimize redundant processing during work order creation.
-   **Version 8.0.5 - December 2025**
    -   Added new feature to create work order from text in NAP and NAVA.
    -   Included Smart Assessment / Questionnaire summary in work order task summarization.
-   **Version 7.1.1 - October 2025**

    Update on the core platform for better performance.

-   **Version 5.2.1 - October 2025**

    This release is for uptaking platform performance improvements.

-   **Version 7.1.0 - September 2025**

    FSM now assist 7.1.0 supports integration with various AI model providers, including Now LLM Service, Azure OpenAI, Google Gemini, and Anthropic Claude on AWS, allowing you to choose the best fit for your skills and AI agents.

-   **Version 7.0.1 - August 2025**

    FSM now assist 7.0.1 supports integration with various AI model providers, including Now LLM Service, Azure OpenAI, Google Gemini, and Anthropic Claude on AWS, allowing you to choose the best fit for your skills and AI agents.

-   **Version 6.0.1 - June 2025**
    -   Enable Field Service technicians to access a virtual assistant from the mobile application with Now Assist Virtual Agent.
        -   Use Now Assist Virtual Agent for mobile to summarize work order tasks.
        -   Explore conversational search in the Now Assist panel with results from Knowledge Base articles.
    -   Now Assist Virtual Assistant \(NAVA\) in FSM Mobile for Task Summarization
        -   Initiate the NAVA panel from a work order task record or the My tasks tab.
        -   Provide technicians with a consistent and intuitive interface for quick and easy interaction.
        -   Display a summary of work order tasks.
    -   Conversational search in NAVA
        -   Enable technicians to ask questions in natural language for quick and clear answers.
        -   Allow technician to receive accurate and reliable responses sourced exclusively from the Knowledge base.
        -   Provide technicians with context-aware follow-ups, including related parts or steps, for better support.
    -   Now assist Context Menu \[NAcm\] for Work order tasks
        -   The record summarization skill is enabled with NAcm capabilities. The NAcm animated icon is located in the Work Notes and Comment fields of the record. Clicking on the NACM icon initiates a call to the large language model \(LLM\), and the response is displayed in a modal window.
        -   You can Elaborate or Shorten responses, to modify the generated response. The sparkle icon reappears when a part or the entire portion of the generated text is selected, providing a menu with options for elaborating or shortening. The selected and modified text will be replaced with the new text returned from the LLM call, while the unselected text remains unchanged. You can then paste the final generated text after applying any number of iterations of regeneration or quick actions, back into the field from which the text creation call was initiated.
-   **Version 5.1.0 - June 2025**

    Xanadu Patch 9 Compatible Version.

-   **Version 6.0.0 - May 2025**
    -   Release Highlights:
        -   Enable Field Service technicians to access a virtual assistant from the mobile application with Now Assist Virtual Agent.
        -   Use Now Assist Virtual Agent for mobile to summarize work order tasks.
        -   Explore conversational search in the Now Assist panel with results from Knowledge Base articles.
    -   NAVA in FSM Mobile for Task Summarization:
        -   Initiate the NAVA panel from a work order task record or the My tasks tab.
        -   Provide technicians with a consistent and intuitive interface for quick and easy interaction.
        -   Display a summary of work order tasks.
    -   Conversational search in NAVA:
        -   Enable technicians to ask questions in natural language for quick and clear answers.
        -   Allow technician to receive accurate and reliable responses sourced exclusively from the Knowledge base.
        -   Provide technicians with context-aware follow-ups, including related parts or steps, for better support.
-   **Version 5.0.0 - November 2024**
    -   New capability for knowledge generation for multi-language support
    -   Now Assist Context Menu \[NACM\] support in Knowledge generation
-   **Version 4.0.1 - August 2024**
    -   New capability for knowledge generation
    -   New capability for sidebar chat summarization
    -   Generate summaries that include affected products, install baseitems, assets and linear assets
    -   Improvements to the Now Assist admin controller and configuration
-   **Version 3.0.1 - May 2024**
    -   New: Demo Data to view summary for Work Order Task
    -   Fixed: NAP issue during initial set up
-   **Version 2.0.0 - February 2024**
    -   Enable ability to invoke summarization of work order task at any stages of the record in Workspace and UI16.
    -   Enable NAP for work order task summarization for users in desktop.
    -   Role attribution in work order task summary
    -   Condition builder to control the visibility of skills based on roles
    -   Enhance the closure note summary in platform to invoke GenAI feature to auto generate closure notes when agent uses the UI16.
-   **Version 1.0.0 - November 2023**

    Now Assist for FSM improves agent experience by generating closure notes using generative AI.


