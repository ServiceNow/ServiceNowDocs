---
title: Now Assist for CMDB release notes
description: Version history for the Now Assist for CMDB application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-now-assist-cmdb.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Now Assist for CMDB release notes

Version history for the Now Assist for CMDB application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.8.0 - June 2026**

    Fixed: Security fixes

-   **Version 3.6.0 - May 2026**
    -   New: MCP connectivity: The Search CMDB and Create configuration item agentic workflows now expose MCP endpoints, enabling agentic tool integration.
    -   Changed: 3P \(third-party\) Model support updates.
-   **Version 2.5.4 - May 2026**

    Fixed: Fixed dependency issue that caused upgrade issues on Yokohama patch 11 \(YP11\).

-   **Version 3.2.1 - April 2026**
    -   New: The 'Keyword Search' capability now supports focused IP address search of CMDB data. Users can enter IP addresses directly to find all CIs associated with those addresses.
    -   Fixed: Defect fixes related to 3P model \(third-party model provider\) support.
-   **Version 3.0.2 - March 2026**

    New: Get detailed information about any CI attribute while creating a CI or while viewing a CI form in the CMDB workspace. ServiceNow product documentation provides the information.

-   **Version 2.5.3 - January 2026**
    -   Fixed:
        -   Performance fixes for 'Search CMDB'
        -   Security fixes
-   **Version 2.5.2 - December 2025**
    -   Changed:
        -   All skills and agentic workflows are now enabled by default when the plugin is installed.
        -   Admins can turn them off using the Now Assist Admin Panel.
    -   Fixed:
        -   The sn\_cmdb\_admin role is required to execute the Create configuration item agentic workflow \(PRB1961894\)
        -   Security fixes
-   **Version 2.4.1 - October 2025**
    -   Fixed:
        -   Performance fixes
        -   Bug fixes
-   **Version 1.3.0 - October 2025**

    Fixed: Security fixes.

-   **Version 2.3.0 - September 2025**

    Fixed: Security fixes.

-   **Version 2.2.1 - August 2025**
    -   New:
        -   Improvements to the CMDB governance agentic workflow:
            -   To help users understand the value of each step in the process, responses include richer context 
            -   Performance improvements
        -   Improvements to Search CMDB agentic workflow:
            -   UX improvements to keyword search:
                -   Users can now select the CI inline when multiple CIs are returned as matches
                -   A summary of the CI now appears in the conversation
            -   Performance improvements
        -   Performance improvements to the CI creator agentic workflow
-   **Version 2.1.1 - August 2025**

    Fixed: Bug fixes.

-   **Version 2.1.0 - May 2025**
    -   New:
        -   Agentic Workflows
            -   Provide advice on CMDB governance: Data admins and owners need help with the overwhelming task of data governance.​ This workflow supports admins and owners with data health and ongoing governance, as data models and integrations grow. The objective is to ensure that you trust you data for the evolving outcomes you want to achieve.
            -   Search CMDB: Consumers of CMDB find it hard to get insights from CMDB data without having a deep knowledge of the data model.​ This team of agents tackles different types of CMDB search queries including keyword searches, single table searches with dot walks, and multi-table searches involving relationship navigation.
            -   Create Configuration Item: This workflow can help in scenarios where a CMDB editor has to manually create a CI record correctly with the right set of attributes. The IRE application processes each prospective CI to ensure that the CI record is complete, correct, and is not a duplicate.
-   **Version 2.0.0 - March 2025**

    New: An OOB agent built using Agentic AI framework, which given a CI guid looks up a CI and generates the summary for that CI. This agent can now be leveraged in any use cases which involve looking up a CI and getting concise information about that CI.

-   **Version 1.1.0 - February 2025**

    New: Select Review existing templates and then follow the suggestions to preview the results of applying a remediation template. Now Assist generates a preview of the results of applying a template without actually running the remediation process. You can preview the results for any existing template. When you see the desired result in a preview, you can specify that template and proceed with the deduplication process.

-   **Version 1.0.3 - November 2024**

    CMDB is ServiceNow's system of record, pivotal to driving a host of business outcomes. CMDB admins and owners ingest and manage the data within the CMDB. Now Assist for Configuration Management Database \(CMDB\) provides Generative AI powered skills that are built to help CMDB owners and admins do their work more seamlessly.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

