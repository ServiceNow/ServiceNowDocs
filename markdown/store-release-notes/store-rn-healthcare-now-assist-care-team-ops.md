---
title: Now Assist for Care Team Operations release notes
description: Version history for the ServiceNow Now Assist for Care Team Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-now-assist-care-team-ops.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# Now Assist for Care Team Operations release notes

Version history for the ServiceNow® Now Assist for Care Team Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 2.0.1 - May 2026**

    Fixed: Inconsistencies within plugin.xml and pom files.

-   **Version 1.0.4 - April 2026 \(Australia\)**
    -   Case Intake AI Agent: An AI-powered agent that classifies incoming requests by case type \(Biomed, EVS, HCIT, Facilities\), and orchestrates case creation through a multi-step agentic workflow. Supports conversational slot filling for reference fields and presents case summaries with valid case type assignment before submission.
    -   Duplicate Case Detection: The Case Creation AI Agent identifies potential duplicate cases during the creation process and can mark new cases as duplicates when a match is found, reducing redundant case volumes.
    -   Virtual Agent Integration with Card Display: The Case Intake AI Agent is integrated into Virtual Agent as a conversational topic, enabling case creation through the VA interface with rich card display of case details.
    -   Interaction Trigger: Automated trigger that initiates the Case Intake AI Agent based on interaction events, enabling seamless handoff from live conversations.
    -   Voice AI Agent for Care Team Operations: A voice-enabled AI agent that supports telephony-based case intake through CCaaS integration \(Twilio/Genesys\). Allows callers to create and manage care team cases via natural voice interaction.
    -   AI Search for Care Team Portal: AI-powered search integrated into the Care Team Portal, enabling unified search across Knowledge Base articles, Catalog Items, and Case records. Features include search history, intelligent recommendations with dynamic dropdowns, and proper portal-native navigation for search results.
    -   Conversational Now Assist AI Search: Conversational search experience where users can type queries in the search bar and receive interactive AI-powered responses. Includes NLU Workbench-trained utterances for accurate result matching and Genius Results.
-   **Version 1.0.3 - April 2026 \(Zurich\)**
    -   Now Assist for Care Team Operations brings AI agent capabilities to healthcare service desk teams managing Biomed, EVS, HCIT, and Facilities cases. Service desk staff spend significant time manually classifying, creating, and routing cases across multiple channels — slowing response times and increasing error rates.
    -   This application deploys a Case Intake AI Agent that converses with the clinician, classifies requests by case type, detects duplicates, and creates cases through a guided conversational workflow. AI-powered search unifies access to KB articles, catalogs, and case records directly from the Care Team Portal with intelligent recommendations.
    -   What sets this apart is multi-channel AI coverage: chat-based agents through Virtual Agent, voice-based case intake through CCaaS telephony integration, and conversational AI search — all purpose-built for healthcare operations workflows and case types.

**Parent Topic:**[ServiceNow Store - Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-healthcare-highlights.md)

