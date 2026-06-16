---
title: Now Assist for Telecommunications, Media, and Technology \(TMT\) release notes
description: Version history for the Now Assist for Telecommunications, Media, and Technology \(TMT\) application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-now-assist-tmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Now Assist for Telecommunications, Media, and Technology \(TMT\) release notes

Version history for the Now Assist for Telecommunications, Media, and Technology \(TMT\) application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.0.7 - June 2026**

    Mosaic migration done for couple of Skills

-   **Version 6.0.6 - April 2026**

    Defect fix for Customer Success Management AI skills related to rules and polices around ACLs.

-   **Version 6.0.2 - March 2026**
    -   We are releasing the three new skills in this release:
        -   Product Release Content Generator:- The Product Release Content Generator is a Generative AI–powered skill that standardizes and structures raw product release notes across multiple products into a consistent, predefined product release format.
        -   Renewal Insight Engine:- AI-powered renewal analysis assistant that evaluates customer engagement performance data to generate actionable renewal likelihood assessments, expansion opportunity identification, and prioritized CSM action recommendations.
        -   Lookup similar engagements skill:- This feature looks up similar engagements to a starting engagement. It does so by first filtering records in the engagement table \(sn\_acct\_lc\_engagement\) using predefined, scripted conditions, then retrieving context details for the top 20 candidates, and finally asking the LLM to analyze and compare them and return the top 3 most similar engagements.
-   **Version 5.1.9 - February 2026**

    Removing now assist for SOMT dependency.

-   **Version 5.1.8 - January 2026**

    Changed: Dependency versions for now assist for TMTsn\_tmt\_agentic ai 4.0.5sn\_genai\_platform 10.0.3sn\_somt\_gen\_ai 1.0.2sn\_sb\_gen\_ai 1.0.2.

-   **Version 5.1.7 - December 2025**
    -   The following is the list of features that we are shipping in the December Z Release:
        -   Risk signal and Issue record summarisation:
            -   The Risk Signal and Issues Summary skill provides you with a summary of the risk signal and issues record, along with associated risk occurrences and solutions. This skill is available in the CSM/FSM Configurable Workspace and in Core UI.
-   **Version 5.1.0 - October 2025**

    Defect fixes and performance improvements

-   **Version 5.0.1 - September 2025**
    -   For Customer Success Management:
        -   NEW: AI agents
            -   Support renewal and expansion
            -   Trigger risk mitigation touchpoint
        -   NEW: GEN AI Summarization
            -   Success Initiative, Customer Play, and Internal Plays
    -   For Service Bridge:
    -   -   NEW: AI agents
    -   Onboarding
    -   For Customer Service Problem Management:
-   **Version 4.0.3 - May 2025**

    Changes.

-   **Version 1.0.5 - March 2025**
    -   Changed:
        -   Prompt Configurability for Customer Service Problem management
        -   Knowledge Article generation for CSPM
        -   Now Assist Context Menu for Resolution notes generation in CSPM
        -   Account Lifecycle Events case summarization
        -   Customer Success Engagement and touchpoint summarization.
-   **Version 2.0.0 - February 2025**
    -   Changed:
        -   Prompt Configurability for Customer Service Problem management
        -   Knowledge Article generation for CSPM
        -   Now Assist Context Menu for Resolution notes generation in CSPM
        -   Account Lifecycle Events case summarization
        -   Customer Success Engagement and touchpoint summarization
-   **Version 1.0.0 - August 2024**
    -   Now Assist for TMT leverages generative AI to streamline three critical aspects of customer service problem management:
        1.  Service problem summarization: Automatically generate concise and accurate summaries of customer interaction cases. This allows customer support agents to quickly understand the context and details of each case without going through through extensive documentation. The result is a faster response time and more informed decision-making.
        2.  Resolution Notes Generation: Simplify the process of documenting resolutions to customer issues. With Now Assist for TMT, the system can create detailed and precise resolution notes, ensuring all pertinent information is captured. This not only aids in maintaining comprehensive records but also ensures consistency and clarity in communication with customers.
        3.  Test Summarization: Improve service desk support by helping agents summarizing Service Test API responses \(TM Forum compliant TMF653\) and also determining a pass/fail test response. This accelerates the diagnostics process, reducing mean time to repair while delivering the most effective resolution path for the customer

