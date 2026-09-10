---
title: Build Agent Trial release notes
description: Version history for the Build Agent Trial on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-build-agent-trial.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# Build Agent Trial release notes

Version history for the Build Agent Trial on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.6.3 - September 2026**
    -   New:
        -   New model support
        -   Build Agent now supports the following models:
            -   Azure OpenAI GPT 5.6 Sol
            -   Anthropic Claude on AWS Opus 5
        -   Testing
            -   Create and run ATF test suites from Build Agent. Group multiple tests under a single suite and execute the suite to run regression testing without selecting individual tests. Execution status and any errors are reported in the chat panel.
            -   Test Agent can now generate ATF tests that use list and related list test steps, including validate related list visibility and apply filter to list. List step support extends test coverage beyond form-based interactions to include the full list view experience on the ServiceNow AI Platform.
        -   Integrations &amp; metadata
            -   Build Agent now supports integrations with the Box MCP server.
            -   ServiceNow Fluent, which Build Agent uses to create apps, now supports domain separation on records and APIs. You can set the sys\_domainfield and use sys\_overridefields when working with records in domain-separated environments, so ServiceNow Fluent operates correctly across domains in your instance.
            -   The following metadata are now supported in Build Agent:
                -   Service Catalog dependent question support
                -   Transition condition
                -   UI style
        -   Platform &amp; availability
            -   When you right-click a record or artifact and select Configure, the metadata editor now opens in ServiceNow Studio.
            -   Build Agent \(Trial\) is available by default on all instances, without requiring installation.
            -   Build Agent now supports automatic upgrades through the ServiceNow Store. Instances running Australia Patch 5+ or Zurich Patch 12+ that have Build Agent installed receive automatic upgrades when a new version is published.
        -   Playbook support
            -   Build Agent includes the following updates to Playbook support:
            -   Consolidates all records related to a playbook into a single XML update set file.
            -   Can now generate runtime permissions at the playbook level and at the stage level.
            -   Can now generate and configure the Set Playbook Outputs activity for nested playbooks.
            -   Can now configure agentic fields on form-based and record-based activities when the AI Agent plugin is active.
            -   Can now generate on-demand playbook launcher configurations.
            -   Can now define optional activities in a playbook.
    -   Changed:
        -   New agentic-first development experience
        -   ServiceNow Studio and IDE were redesigned for an agentic-first development experience with Build Agent:
            -   The central chat area on the ServiceNow Studio home page is the starting point for new Build Agent conversations.
            -   To open an existing conversation, select the Conversations icon in the Navigator panel.
            -   The Build Agent panel now opens on the Navigator panel of ServiceNow Studio.
-   **Version 2.5.6 - August 2026**
    -   New:
        -   New Build Agent model integrations, including GPT-5.5, Gemini 3.5 Flash, and Opus 4.8
        -   Ability to select model versions directly from the Build Agent chat panel within ServiceNow Studio
        -   Ability to create new custom skills and rules at instance-wide, application, and user levels to tailor Build Agent's behavior
        -   Run background scripts securely within app-build flows, with rollback, scope-restriction, and dry-run containment paths
        -   Ability to handoffServiceNow Otto conversations to Build Agent in ServiceNow Studio
        -   Ability to run Build Agent in Developer Sandboxes, allowing for better collaboration and isolation
        -   Automatically keep all the ATF tests in sync as your Build Agent written code evolves over time, toggled on via the 'Sync ATF tests with app' setting for Build Agent
        -   Automatically keep all the UI tests in sync as your Build Agent written code evolves over time, toggled via the 'Run UI ATF Tests' setting for Build Agent
        -   Get prompted to generate ATF tests anytime you invoke Build Agent, enabled via Build Agent settings
        -   Execute and troubleshoot ATF tests directly from the ServiceNow SDK
        -   Support for new knowledge base access metadata type
        -   More granular overview of tools per connected MCP server in Build Agent settings
        -   Expanded MCP Server support, including AWS DevOps, Box, Postman, and Sentry
    -   Fixed:
        -   Context compaction enhancements
        -   Sub Agent memory improvements
-   **Version 2.4.5 - July 2026 \(Australia\)**
    -   New:
        -   A new web search tool capability enabled Build Agent to find answers from the public internet when its internal knowledge sources don't have them. This tool needs to be toggled on from the settings screen of the Build Agent chat panel.
        -   Consolidated update sets enable you to track changes generated by Build Agent\[ and manual edits in consolidated update sets. All changes to your application are captured in the same scope, making it easier to review what was modified and merge updates to other environments.
        -   Work with more metadata types in Build Agent, which now supports connection and credential alias, data lookup, rest message/HTTP method, and user criteria.
    -   Changed:
        -   Developers can now see the complete history of changes in Build Agent conversations, including both automatic Build Agent updates and manual edits made in Studio. The system automatically creates separate "manual-edit" update sets for manual changes between Build Agent installs, making it easy to distinguish which changes were automated versus hand-crafted. Restore to any point in your workflow, including manual edits between Build Agent prompts, and the system intelligently manages update set reconciliation to keep your change history clean and traceable.
        -   Build Agent handles checkpoints and update sets differently: checkpoint 0 no longer creates an update set, checkpoint 1 is the base update set for all subsequent changes, and update sets use human-readable naming.
        -   An updated semantic metadata search tool improves performance replaces the previous semantic search tool.
        -   Build Agent \(Trial\) is available by default on all instances, without requiring installation.
-   **Version 2.3.3 - June 2026**
    -   New:
        -   Upload files to Build Agent to provide context: images \(PNG, JPEG, GIF, WEBP\), documents \(PDF, DOC, DOCX, XLS, XLSX\), and text/code files \(TS, JS, PY, JSON, MD, HTML, YAML, and more\)
        -   View update sets created by Build Agent from within the chat panel. Each checkpoint includes a button that opens the relevant update set in a new tab.
        -   Connect Build Agent to external MCP servers in ServiceNow Studio. Previously, MCP server connectivity was only available in the ServiceNow IDE.
        -   Validate user interface output during app creation with the UI validation tool in Build Agent, now available in ServiceNow Studio.
        -   Use the Search retrieval tool to enable agents to fetch and present relevant information from configured data sources in response to user queries. Agents can surface knowledge articles, catalog items, and other indexed content directly within the agentic workflow, reducing the need for users to navigate to separate search interfaces.
    -   Changed: New MCP integrations in ServiceNow Studio: Added support for many new connectors including Atlassian Rovo, DocuSign, Figma, GitHub, Linear, Miro, Prisma Postgres, and Zoom \(Chat, Docs, Revenue Accelerator, Whiteboard\)
-   **Version 2.2.6 - May 2026 \(Zurich, Australia\)**
    -   New:
        -   Service Portal support
        -   Inbound email action support
        -   Improved support for actions in flows
        -   Custom skills creation in IDE and ServiceNow Studio
        -   Support for Claude Sonnet 4.6 and GPT-5.4
-   **Version 2.2.5 - May 2026 \(Zurich, Australia\)**
    -   New:
        -   Service Portal support
        -   Inbound email action support
        -   Improved support for actions in flows
        -   Custom skills creation in IDE and ServiceNow Studio
        -   Support for Claude Sonnet 4.6 and GPT-5.4
-   **Version 2.1.3 - April 2026**
    -   New:
        -   Keyword search enhancements
        -   Zurich Compatability:
            -   Build Agent in ServiceNow Studio - AI-assisted development now available directly in Studio, reaching low-code and no-code builders for the first time.
            -   Global &amp; App Customization - Build Agent now edits entire instances, not just individual apps. Simplifies OOB app customization and large-scale implementations.
            -   Upgraded AI Models - Claude Opus 4.6 and Sonnet 4.5 deliver better code quality, reasoning, and performance.
            -   Now supporting: Flows, Service Catalog, Workspaces, UI Components, List Controls, UI Policy, Email, and UI View.
-   **- March 2026**
    -   Key highlights:
        -   Build Agent in ServiceNow Studio - AI-assisted development now available directly in Studio, reaching low-code and no-code builders for the first time.
        -   Global &amp; App Customization - Build Agent now edits entire instances, not just individual apps. Simplifies OOB app customization and large-scale implementations.
        -   Upgraded AI Models - Claude Opus 4.6 and Sonnet 4.5 deliver better code quality, reasoning, and performance.
        -   Now supporting: Flows, Service Catalog, Workspaces, UI Components, List Controls, UI Policy, Email, and UI View.
-   **Version 1.3.13 - October 2025**
    -   With the Build Agent \(Trial\) app, your instance will receive 25 free user interactions for 30 days at no additional charge, enabling you to explore the Build Agent features at no cost. If you exceed the limit of free interactions, you can either wait for your free interactions to reset after 30 days or install the paid Build Agent app on your instance to continue using its services.
    -   Build Agent is an autonomous developer AI agent inside the ServiceNow IDE. It will benefit customers by significantly accelerating application development on the ServiceNow platform. Build Agent automates many of the repetitive and time-consuming tasks that developers currently perform manually. This leads to:
        -   1. Increased developer productivity.
        -   2. Reduced development backlogs.
        -   3. Faster time-to-market for new business applications.
        -   4. A potential reduction in overall development costs.

**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

