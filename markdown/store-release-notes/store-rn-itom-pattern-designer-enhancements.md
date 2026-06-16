---
title: Pattern Designer Enhancements release notes
description: Version history for the ITOM Pattern Designer Enhancements application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-pattern-designer-enhancements.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - ITOM Visibility release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Pattern Designer Enhancements release notes

Version history for the ITOM Pattern Designer Enhancements application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.10.0 - June 2026**

    New: Control access through predefined query access controls for all Pattern Designer Enhancements tables.

-   **Version 3.9.1 - March 2026**
    -   Fixed:
        -   Command Validation Tool now extracts commands from eval script blocks in discovery patterns, improving command coverage in the command list table.
        -   OS class detection for discovered commands now accounts for shared library inheritance, resulting in more accurate OS classification.
-   **Version 3.9.0 - December 2025**
    -   This release strengthens platform security by enforcing stricter client-side protections and refined access controls.
        -   New:
            -   Improved permissions control by creating a new pde\_viewer role with read-only access to all tables and records within the Pattern Designer Enhancements app.
        -   Fixed:
            -   Fields marked as read-only are now fully protected from any client-side modifications, including client scripts, UI actions, or APIs.
-   **Version 3.8.0 - August 2025**

    New: Command Validation Tool now includes improved capabilities to find commands from nested libraries.

-   **Version 3.7.0 - May 2025**

    Removed: The Discovery CLI feature has been removed. Core functions are still available through the GUI.

-   **Version 3.4.0 - November 2024**
    -   Fixed:
        -   PRB1764642: The system messages have been updated to provide clearer and more accurate feedback to users upon job submission. This ensures better understanding and smoother operation when running commands through the CLI.
        -   PRB1771807: Resolved the issue where the run-command was not returning results for SHELL commands and SNMP queries. The CLI now accurately processes and returns results for these commands, improving functionality and reliability.
-   **Version 3.3.4 - May 2024**

    Fixed: Defects related to Discovery CLI. The authorization issue of preventing Command execution via CLI is resolved.

-   **Version 3.3.3 - February 2024**

    Fixed: Defects related to Discovery CLI, Command execution on Windows via CLI and CVT.

-   **Version 3.3.0 - November 2023**
    -   New:
        -   Discovery CLI:This feature augments your ServiceNow CLI experience by introducing a suite of commands exclusively dedicated to discovery processes.
        -   This powerful suite of commands not only simplifies your discovery processes, but also improves the efficiency of your IT workflows. By integrating these CLI commands into your daily operations, you can ensure that your discovery tasks are executed swiftly and accurately.
        -   Command Validation Tool:
            -   Get the list of commands from the pattern from Command List/UI action in sa\_pattern table.
            -   Prioritisation of Command Validation Tasks.
            -   Ability to skip failover commands from the CVT.
            -   Choosing the hardware Cis instead of providing the IP Addresses manually.
-   **Version 3.1.0 - August 2023**
    -   NewSupport to list pattern commands with temporary variables is added. Framework support to execute is also added.
-   **Version 3.0.1 - May 2023**

    Changed: Bug fixes and support for multi language.

-   **Version 3.0.0 - February 2023**
    -   New: Command Validation Tool
        -   The new command validation tool allows the discovery admin to troubleshoot discovery issues related to credentials. Auto-fetch commands from the Pattern code base can help discovery admin to bootstrap the testing process.
        -   Command validation tool supports the following operation types:
            -   Shell Command
            -   WMI Query
            -   SNMP Query \(Tabular and Scalar\)
            -   SNMP Walk
            -   HTTP GET \(authenticated via Basic Authentication credentials\)
        -   The following MID selection behavior is also provided:
            -   Specific MID Server
            -   Auto Select MID Server
            -   Try All Eligible MID Servers
        -   [KB1123625](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123625)
-   **Version 2.0.0 - August 2022**

    Discovery and Service Mapping provide automated discovery of your on-premises and cloud infrastructure. Pattern frameworks from ITOM Visibility provide codeless content to discover IT landscapes. This store application helps ServiceNow ITOM product teams to release framework enhancements through store releases.


**Parent Topic:**[ServiceNow Store - ITOM Visibility release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-visibility-landing.md)

