---
title: Now Assist for IRM release notes
description: Version history for the Now Assist for IRM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-now-assist-irm.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Now Assist for IRM release notes

Version history for the Now Assist for IRM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.2.0 - May 2026 \(Australia\)**

    Fixed: Updated the protection policy for the 'Suggest Potential Risks use case and the Risk Identification Agent' to read-only to ensure seamless functionality for customers on the IRM Advanced tier.

-   **Version 22.0.0 - March 2026**
    -   New:
        -   Added contextual follow-up questions in the Risk Identification Agent to improve the accuracy of suggested risks.
        -   Introduced a review and feedback step that allows users to update or remove risks before they are created.
        -   Enhanced security for the Risk Assessment Summarization skill through role masking.
    -   Fixed:
        -   Fixed an issue that could result in null reference errors in risk assessment summaries.
        -   Improved the overall performance of the Risk Identification Agent.
        -   Fixed an issue where the Issue Resolution Agent displayed remediation tasks twice, with formatting issues across multiple LLMs.
        -   Fixed an issue where the Issue Submission Agent did not create the issue triage record with the correct details.
        -   Fixed oversized remediation task confirmation header formatting for AWS Claude.
        -   Fixed role mask changes and security issues.
    -   Changed: UCF control objectives are now part of the rationalization process.
-   **Version 21.1.6 - December 2025 \(Zurich\)**
    -   New:
        -   Issue submission agent:
            -   The Issue Submission agent is now available in Employee Center, enabling employee users to report issues through a guided conversational experience. The agent helps structure the issue and recommends relevant controls, entities, and policies based on the input provided. This ensures that the issue is well-defined and enriched with contextual information before it is submitted.
            -   Check product documentation for activation details.
            -   Suggest potential risks agentic workflow
            -   AI-driven risk identification: Conversational AI automatically analyzes entity context and surfaces relevant risks from internal libraries, industry patterns, and optional external sources.
            -   Consolidated risk view: Generates a single, ready-to-triage risk list, reducing manual effort and duplication while ensuring comprehensive coverage.
            -   Guided user experience: Embedded in the Now Assist Panel, the workflow provides step-by-step guidance for risk domain selection, simplifying complex risk discovery.
            -   Proactive intelligence for emerging risks: External scanning capabilities deliver early warnings of new threats, helping organizations stay ahead of evolving regulations and trends.
        -   Control objective impact analyzer:
            -   The citation-driven impacted control objective identifier uses generative AI to analyze changes in citations and identify control objectives that should be reviewed based on the modified citation content. It intelligently matches changed citation requirements with existing COs to suggest potential updates, helping teams maintain alignment between citations and control objectives.
        -   Control objective change agent:
            -   This introduces an AI-driven capability to automatically update a control objective's description and supplemental guidance whenever its associated citations are modified. Leveraging agentic AI, the enhancement analyzes the changes in citation content, identifies their impact on the control objective, and generates precise, contextually relevant updates. Users can review and approve AI-suggested changes directly within the workflow, ensuring that control objectives always reflect the most current regulatory requirements and best practices.
    -   Changed:
        -   Removed the issue summarization step from the issue resolution agentic workflow as part of performance improvements.
        -   Added support for LTS models for previously released Now Assist IRM skills.
        -   Enhanced security by implementing role masking.
        -   Rationalization process now auto-generates recommendations using the skill when the Rationalize button is clicked on a control objective.
        -   Added a quick summary view for each recommendation card and clarified task sequence during the analyze step of the rationalization process.
        -   Control objective requirements and control requirements are now considered in the rationalization process for control objectives.
    -   Fixed:
        -   Implemented a fix to skip redundant approvals in the rationalization process.
        -   Resolved issues related to synchronizing impacted items and automatic refreshes.
-   **Version 21.0.3 - October 2025**

    Changed: Now Assist Platform AI performance improvement uptakes.

-   **Version 21.0.2 - September 2025**
    -   New: Risk Event Summarization We've introduced Risk Event Summarization to improve context-sharing and decision-making throughout the risk event lifecycle.
    -   New "Summary" Section: A section has been added to the Risk Event Overview page to capture a concise summary of the risk event.
        -   Access to Summary by Risk Event State:
            -   Risk Managers and Risk Event Owners can create and save summaries in any state of the risk event.
                -   In New and Analyze states, summaries can be saved to the Summary field.
                -   In Awaiting Approval, Approved, or Closed states, summaries can be saved to the Work Notes field.
            -   Approvers can generate summaries only in the Awaiting Approval state and can save them to the Work Notes field.
        -   Native UI Support: Risk Event Summaries can be generated within the Native UI for a seamless user experience.
        -   LLM Compatibility: Along with NowLLM, the summarization feature works with multiple large language models like Claude, Google Gemini, and Azure OpenAI.
    -   Rationalization of Control objectives
        -   Skill for Creation of common control objective as a part of Rationalization process for control objectives.
        -   Third party model support for Azure Open AI, Amazon Bedrock and Google Gemini for creation of common control objective skill.
    -   Control recommendation on Regulatory alert
        -   New skill for recommending controls for an incoming regulatory alert.
        -   Third party model support for Azure Open AI, Amazon Bedrock and Google Gemini for control recommendation skill.
        -   Base control recommendations to show recommendations on Regulatory alert recommendation framework.
    -   Changed:
        -   All existing and new generative AI skills, AI agents and, agentic workflows invocation is secured through ACLs.
        -   Rationalization of control objectives
            -   UX improvements for auto refreshing actions as a part of Rationalization framework.
    -   Fixed:
        -   Streamlined messages and content for Rationalization framework.
        -   Implemented fix scripts and access control for streamlining security aspects of all skills and agents under the Now Assit IRM application
-   **Version 21.0.0 - August 2025**
    -   New:
        -   Implemented 3P model support for below use cases in Regulatory change management application.
            -   Regulatory alert summarisation
            -   Control objective recommendation for regulatory change alert
            -   Citation recommendation for regulatory change alert
        -   Rationalization of Control objectives
            -   Validations introduced for deactivated and deleted Control objectives in the workflow
            -   Enhanced navigation with "Restart Analyze" option
            -   Third party model support for Azure Open AI, Amazon Bedrock and Google Gemini
        -   Risk Assessment summarisation
            -   Third party model support for Azure Open AI, Amazon Bedrock and Google Gemini
        -   Implemented 3P model support for below use cases.
            -   Issue summarization
            -   Issue remediation agent
    -   Changed:
        -   Rationalization of control objectives
            -   Recommendation panel displayed in the Consolidate state also
    -   Fixed:
        -   Rationalization of control objectives
            -   Reordered UI with highlighted primary actions
-   **Version 20.1.1 - May 2025**
    -   New:
        -   Issue Remediation Agent:
            -   Optimize the GRC issue resolution using agentic AI workflow in the Integrated Risk Management application to help your issue managers and analysts resolve GRC issues with AI agents in the Now Assist panel. This workflow helps by suggesting targeted solutions for key steps during the issue resolution process.
        -   Risk Assessment summarization
            -   Introducing new feature, Risk Assessment summary generation using Generative AI to support assessors during submissions and provide approvers or other stakeholders with a quick overview of assessment progress and key insights.
        -   Control objective rationalization and deduplication:
            -   The AI-powered control objective rationalization and deduplication process leverages Generative AI to help compliance teams streamline their traditionally manual, time-consuming, and error-prone efforts. As regulatory requirements continue to evolve, teams often face an overwhelming number of control objectives many of which are redundant or closely related. This AI-driven approach identifies similar or duplicate objectives, enabling teams to consolidate them by retaining one, retiring duplicates, or merging them into a common control objective enhancing overall efficiency and effectiveness across compliance operations.
-   **Version 20.0.2 - February 2025**

    GenAI features for Integrated Risk Management \(IRM\), powered by Now Assist, improve analysts' productivity, team coordination, and overall efficiency.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

