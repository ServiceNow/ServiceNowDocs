---
title: GRC: Operational Resilience release notes
description: Version history for the GRC: Operational Resilience on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-operational-resilience.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Operational Resilience release notes

Version history for the GRC: Operational Resilience on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   Scenario Analysis:
        -   Organisations conducting operational resilience planning need a structured, repeatable way to assess the potential impact of adverse scenarios on their critical business services. In the current experience, analysts are required to manually answer every question for each scenario event while accounting for all scoped services and dependencies — with no guided workflow to follow. Steps open as independent tabs, causing users to lose their place, and results are limited to a flat "breached / not breached" output that offers little analytical depth.
        -   The revamped Scenario Analysis experience addresses these gaps by introducing a guided, Playbook-style workflow that walks users through each stage of the analysis sequentially, eliminating navigational confusion. It also introduces a Statistical Modeling method that uses reference data as inputs and runs simulations through a mathematical model to produce quantified, data-driven results — such as average annual loss and probability of loss exceedance. This makes the analysis faster, more consistent, and more defensible. For organisations that prefer expert judgment over modeled outputs, the Manual SME method is retained alongside the new flow.
        -   Security Vulnerability Remediation:Enforces security on cross-scope data access by restricting the getRefRecord\(\) method, providing upgrade paths and guidance for secure application usage.
-   **Version 22.0.5 - March 2026**

    By default, the Operational resilience scheduled jobs will be inactive for new clients.

-   **Version 21.1.3 - December 2025 \(Zurich\)**

    New: Resilience Map for visualization of hierarchies and impact tracing: The Resilience Map is a configurable, reusable visualization component designed to represent relationships and dependencies across entities within the GRC domain. It provides an interactive, hierarchical view of how key business elements—such as business services, processes, applications, and dependencies—are connected, enabling users to explore resilience, risk, and impact pathways seamlessly.

-   **Version 21.0.7 - September 2025**
    -   Fixes:
        -   The issue doesn't show up in the related list, but it shows up in the dashboard report.
        -   We need to skip integration when the applies\_to is empty for incident, outage, etc
        -   If multiple sn\_oper\_res\_issue records are created for the same issue with 'N' other entities, we are passing the same record as part of the API call which seems incorrect. Hence we see the chain reaction.
-   **Version 21.0.5 - August 2025**
    -   Leverage the improved capabilities of the Common Service Data Model for improved Operational Resilience.
    -   Perform Smart Assessments when evaluating the importance and impact tolerance of services and self-attesting their status.
    -   Use the improved DORA capabilities in the Operational Resilience Workspace.
    -   Track third-party risk assessments as red flags in Operational Resilience reports and overview pages of the business services, service offerings, and business processes.
-   **Version 20.2.1 - July 2025**

    Fixed: Scenario analysis search is broken on related lists.

-   **Version 20.2.0 - June 2025**

    Fixed: Important security fixes.

-   **Version 20.1.3 - May 2025**
    -   New:
        -   Align with the CSDM model to set up configurable main node configurations, which are used to retrieve CSDM and their dependency data
        -   Add the primary origin to an operational vulnerability, and the impacted areas are automatically included \(the vulnerability can then be viewed from any impacted area\)
        -   All CSDM objects, dependencies, and their red flags can be rolled up based on the entity hierarchy
        -   Use Smart Assessment for evaluating an operational vulnerability
    -   Updated: Enhanced security for addEncodedQuery and scriptedACL
-   **Version 20.0.1 - February 2025**
    -   Changed: Improved performance for export pdf in operational vulnerability
    -   Fixed:
    -   -   Localization gaps for homepage
-   Duplicate UI actions on Business Services
-   Opres user access issue to impacted areas and issues related list on vulnerabilities
-   **Version 19.1.4 - November 2024**
    -   New:
        -   Added modules, list views, and record pages for Digital Operational Resilience Management
        -   Added Digital Operational Resilience roles to Operational Resilience roles
-   **Version 19.0.1 - August 2024**
    -   New: Added Discuss UI action for Operational Resilience workspace to enable discussion for Task record pages
    -   Fixed:
        -   Fixed task performance issue
        -   Fixed Importance assessment - when due date is updated, its not error message in classic view
        -   Fixed few translation gaps
-   **Version 18.1.1 - July 2024**

    Fixed: Fixed app compatibility for the glide family releases.

-   **Version 18.1.0 - June 2024**

    Changed: Updated base dependent apps for latest security features.

-   **Version 18.0.3 - February 2024**
    -   New:
        -   Added new OpRes personas to support IRM and BCM products
        -   Show/hide reports based on OpRes personas
        -   Pulled assets from CMDB for child services and processes
        -   Added report "Top vulnerabilities to be fixed" to OpRes homepage
    -   Fixed:
        -   Fix pillars dashboard drilldown
        -   Fix assessment instance creation
        -   Fix breadcrumb labels
-   **Version 17.0.0 - September 2023**
    -   Fixed:
        -   Planned ACL changes for OpRes
        -   Fixed the 'no table found' error in OpRes scheduled job
        -   Fixed new buttons in business services for parent and child services that were not creating relationships in Utah, Vancouver
-   **Version 16.0.7 - February 2023**
    -   New:
        -   Use Operational Resilience Workspace to monitor the resilience metrics and manage your business services.
        -   Perform an assessment to measure the importance and impact tolerance of your business service.
        -   Analyze the impact of a scenario and an event on your business service and complete the associated response tasks.
        -   Complete the self-attestation process for your business service and generate a PDF of the report.
        -   Visualize the relationship of a business service with its related entities such as the red flags, dependencies, and assessments in a 360-degree view.
    -   Fixed:
        -   Fixed WCAG and dark theme-related issues
        -   Fixed report view ACLs security issues
        -   Fixed scenario analysis duration dates
        -   Fixed failed BCP plans in business services
-   **Version 15.0.3 - August 2022**
    -   New:
        -   Added scenario analysis for important business services
        -   Added feature to analyze impact tolerance and important for business services
        -   Added new and improved relationships in the Business Service form
        -   Added self-attestation for operational resilience status
-   **Version 14.1.0 - March 2022**

    Fixed: Security bug

-   **Version 12.0.2 - June 2021**
    -   Fixed:
        -   Security issue
        -   Metric related to BCM for failed tests
-   **Version 12.0.0 - March 2021**

    Fixed: Fixed form section of the entity form used by OR.

-   **Version 11.0.2 - November 2020**

    The Operational Resilience application enables organizations to anticipate and plan for adverse operational events. The business unit heads can also ensure rapid recovery from adverse events using the application. The application provides a 360-degree view of risk, control, and business continuity planning posture across functions such as facility, people, technology, and supply chain management.


