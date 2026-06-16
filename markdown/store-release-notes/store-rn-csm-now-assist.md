---
title: Now Assist for CSM release notes
description: Version history for the Now Assist for CSM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-now-assist.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Now Assist for CSM release notes

Version history for the Now Assist for CSM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.0.3 - June 2026 \(Australia\)**

    New: Dependency on store app Now Assist for CSM Major Issue Management

-   **Version 13.0.3 - June 2026**
    -   Changed: Enhanced case insights card with customer details
    -   Enabled sentiment analysis on email interactions.
-   **Version 12.2.0 - May 2026**
    -   New: Uptake of Automated quality assurance skill from Service Quality capability
    -   Changed: Email Reply Recommendation supports case extensions
-   **Version 12.1.0 - April 2026**
    -   New:
        1.  Availability of 3 new Now Assist Guardian filters -
            -   Active Data Loss or security breach
            -   Threatening legal action
            -   Reputational incident/issue
        2.  Support for product tiers.
-   **Version 12.0.0 - March 2026**
    -   New:
        -   Monitor how users engage with GenAI and Agentic skills in Now Assist for CSM to provide actionable dashboards and reports for workflow optimization.
        -   Easily access all relevant case information by navigating to customer 360° insights from the summary card.
    -   Changed:
        -   Enhancements in Sentiment analysis dashboard
            -   Expanded Sentiment Analysis Dashboard support to include Interaction records, and consolidated positive and negative sentiment drivers into a single Sentiment Drivers view.
            -   Merged the top negative assignment group and number of cases by channel visualizations into the new Impact Explorer for more streamlined analysis.
            -   Optimized widget placement in the Workforce Optimization dashboard for easier access to insights and trends across interfaces.
    -   Enhancements in Trending topics dashboard
        -   Consolidated the Accounts, Products, Assignment Groups, and Channels graphs into a single card, Impact Explorer, for a more streamlined experience.
        -   Added search and pagination to the list view, enabling faster navigation and topic discovery.
        -   Introduced a new graph to surface historical trends at a glance.
        -   Expanded Trending Topics beyond the top 10 results to provide deeper insight into emerging patterns.
        -   Added the Trending Topics widget in Workforce Optimization dashboard as AI insights tab for quicker, more convenient access.
-   **Version 11.1.0 - January 2026**
    -   New: A new agent Complaint Case AI Agent has been added to automate and enhance the complaint resolution process.
    -   Changed:
        -   Added support to clone and customize any base system Gen AI skill in the Now Assist Skill Kit.
        -   Added a navigation path for sentiment analysis dashboard in the Core UI interface.
-   **Version 11.0.3 - December 2025**
    -   New:
        -   Use the trending topics dashboard to get a comprehensive view of trending topics across cases, along with insights and visualizations to facilitate deeper analysis. This feature helps support teams track trend progression, regional impact, and see more into specific trends using customizable filters.
        -   Use sentiment trends analysis to access a unified view of customer sentiment across cases, accounts, and live agent interactions. The dashboard uses LLM-powered insights to explain sentiment changes and lets you see more to find root causes—helping teams take targeted actions that improve customer satisfaction.
        -   Use the activity response generation skill to automatically generate recommendations for work notes and comments. This feature helps agents quickly add meaningful updates to case records, improving efficiency, and interaction quality.
        -   Availability of Now Assist Context Menu Config setup for extended tables within resolution notes.
    -   Changed:
        -   Added sentiment scoring to both the case record page and list view across cases. The sentiment scale ranges from very positive, positive, neutral, negative to very negative.
        -   Skills cloned in Now Assist Admin console \(NAA\) can now be edited in Now Assist Skill Kit \(NASK\). This allows users to add headers, configure prompts, and manage GenAI skills in one location. The migration supports case summarization, resolution notes generation, and sentiment analysis.
        -   Define trigger step has been added to the case summarization flow that provides the option to choose how the skill will be triggered - User Trigger and Automatic.
        -   Enhanced email response skill with the option to generate reply suggestions in the compose area using preset templates that include headers, footers, and signatures.
-   **Version 10.1.3 - October 2025**
    -   New: Enabled security implementation on Now Assist for CSM skills through Access Control Lists \(ACLs\) and user identities.
    -   Changed: Resolved translation inconsistencies by enhancing multilingual support in chat summarization, resolution notes, and knowledge generation, and leveraging native multilingual LLMs for improved fluency and domain specificity.
-   **Version 10.1.0 - September 2025**

    New: CSM Gen AI Security directives - Enable security implementation on Now Assist for CSM skills through Access Control Lists \(ACLs\) and user identities.

-   **Version 10.0.0 - August 2025**
    -   Added support for 3P models:
        -   Azure OpenAI.
        -   Claude Anthorpic.
        -   Google Gemini.
-   **Version 8.2.0 - October 2025**

    NewCSM Gen AI Security directives - Enabled security implementation on Now Assist for CSM skills through Access Control Lists \(ACLs\) and user identities.

-   **Version 8.1.1 - June 2025**
    -   New: Speed up case resolution with the suggested steps from Recommended Actions.
    -   Changed: Improved the self-service resolution in Portal case form by handing off conversation to Virtual agent if no answers are found or if a case needs to be opened.
-   **Version 9.0.1 - May 2025**
    -   New:
        -   Minimize case escalations by providing a detailed explanation of customer sentiment.
        -   Speed up case resolution with the suggested steps from Recommended Actions.
        -   Use natural language to describe your intent and trigger a subflow or action in the Now Assist panel.
        -   Support for searching public web content in both standard and conversational search. Easily distinguish between internal and external content, with direct links to the source.
    -   Changed: Improved the self-service resolution in Portal case form by handing off conversation to Virtual agent if no answers are found or if a case needs to be opened.
-   **Version 8.0.0 - February 2025**
    -   New:
        -   Schedule, reschedule, or cancel appointments conversationally within the Virtual Agent with LLM-based scheduling assistant.
        -   Availability of an AI widget that gathers responses from relevant knowledge bases, products, and catalogs when requesters open a case and enter the description.
        -   Availability of multi-turn Q&amp;A feature in Now Assist panel that allows agents to ask follow-up questions, clarify details, switch between topics, and receive synthesized answers from the knowledge base.
    -   Changed:
        -   Additional tonal change options, including formal, casual, and sympathetic, are now available, and the admin experience is on par with the admin experience for chat summarization in chat reply recommendations.
        -   Additional tonal change options, such as formal, casual, and sympathetic are now available in email reply recommendation.
        -   Availability of detailed feedback option for negative feedback on the generated case summary in case summarization.
-   **Version 7.0.0 - November 2024**
    -   New:
        -   Multilingual support for all Now Assist for CSM skills.
        -   Support for outbound calls from agents to the customers.
        -   Generate a call summary when the real-time transcript is not available.
    -   Changed:
        -   Get recommendations for email responses when starting new emails, forwarding messages, or finalizing drafts.
        -   Select suggested response email templates and adjust the tone of your email when composing new emails, forwarding emails, or completing drafts.
        -   Rewrite resolution notes by selecting the text and using the Now Assist icon to shorten or elaborate the content.
        -   Revise content in existing knowledge articles using the Now Assist icon, accessible as an inline capability, and create and refine knowledge articles. You can also generate knowledge articles in multiple languages.
-   **Version 6.0.0 - August 2024**
    -   New:
        -   Get a summary of sidebar discussions between agents, requesters, and subject matter experts.
        -   Reply faster with chat response recommendations in real time.
        -   Respond quickly with recommended email replies.
    -   Changed:
        -   Create knowledge articles based on insights from other related case.
        -   Generate a summary during live agent-to-agent call transfer.
-   **Version 5.1.2 - July 2024**

    Fixed: Domain separation is supported for case, chat and resolution notes generation.

-   **Version 5.0.0 - May 2024**
    -   New:
        -   Post-call summarization
        -   Knowledge generation
        -   Dynamic translation
    -   Changed:
        -   Related records summarization including emails
        -   Chat summarization enhancement to support Live agent to Live agent transfer use case
-   **Version 4.0.0 - February 2024**
    -   Role attribution in case summary
    -   Condition builder to control the visibility of skills based on roles
    -   Virtual Agent topic creation with LLM support for data collection
    -   Demo data
-   **Version 3.0.1 - November 2023**

    Conversational Virtual Agent for catalog item requests.

-   **Version 2.0.2 - September 2023**

    Now Assist for CSM helps customer support organizations improve customer experiences by resolving issues faster with rapidly generated case and chat summaries and improved customer self-service.


