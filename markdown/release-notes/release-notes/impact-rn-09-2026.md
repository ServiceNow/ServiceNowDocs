---
title: Version 11.0.0
description: The Version 11.0.0 introduces standalone Product Adoption functionality, new Accelerators across multiple domains, Scan Engine API and exception workflow enhancements, Business Outcomes improvements. It also retires legacy Accelerators and Impact Health Diagnostics
locale: en-US
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
---

# Version 11.0.0

The Version 11.0.0 introduces standalone Product Adoption functionality, new Accelerators across multiple domains, Scan Engine API and exception workflow enhancements, Business Outcomes improvements. It also retires legacy Accelerators and Impact Health Diagnostics

## What's new

-   **[Product adoption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/product-adoption.md)**

    Access core Product adoption functionality, Capabilities Map and Product Adoption Roadmap without connecting to Service Exchange.

    -   View the capabilities map with a list of capabilities and their entitlement status. You can also edit the usage status manually for relevant capabilities.
    -   Create product adoption roadmaps using templates or manually, and manage capabilities for those new product adoption roadmaps.
    -   Receive a consistent message when functionality is limited by unavailable status or inability to edit existing product adoption roadmaps until Service Exchange connects with Guided Setup.
-   **[Latest Accelerators by Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/new-accelerators-australia-release.md)**
    -   Accelerate AI adoption and time to value by generating complete applications, surfacing automation opportunities, measuring AI investment impact, and migrating Virtual Agent topics.
    -   Reduce onboarding friction and technical risk by orienting teams to scoped app development and enabling secure, integration-free access to external data sources. Activate Field Encryption Enterprise as a core part of your Vault security strategy.
    -   Strengthen your governance foundation by structuring your CSDM data model, establishing sound IRM Entity Framework design, managing your demand pipeline, and improving Knowledge Management process maturity.
-   **[Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/platform-health-idi.md)**
    -   Call the Scan Engine API to provide trigger scans on demand, check scan status and results, and integrate findings into pipeline approval gates.
    -   Use exception approval workflows with explicit Save Draft and Submit actions.
    -   Use configurable exception reason scope controls.
-   **[Value management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-in-platform-business-outcomes.md)**
    -   View the same product line label in Impact Delivery Instance as Impact Store Application for the same product for example, IT Service Management instead of ITSM. Both legacy and current models in Impact Delivery Instance now map to the correct product line taxonomy.
    -   Filter outcomes by version using the new Outcome version filter, available on the Objectives &amp; Outcomes landing page and the Outcome Insights page in Impact Delivery Instance.

## What's changed

-   **Accelerator Catalog**
    -   Success Readiness Assessment changed to Success Foundation Review.
    -   UX Accelerators moved from Architecture to Technical sub-catalog
    -   AI Readiness Assessment moved from Architecture to Technical sub-catalog
    -   Tuneup Your IT Asset Management changed to Tuneup Your ITSM Asset Management
    -   Jumpstart Your App Engine changed to Jumpstart Your App Deployment Governance
-   **[Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/platform-health-idi.md)**
    -   Use exception workflows in update set scans now provide multiple governance improvements.
    -   Assign a dedicated exception approver role for governance separation
    -   As and Instance administrator, control which finding levels are eligible for exception reasons.
    -   Access update set origin tracking on all scan findings
    -   View the captured update set data that contains the violating code whenever a full or delta scan runs and produces a finding.
    -   Full-scan scope updates so only definitions explicitly configured for single-finding-per-table scanning are included.
    -   The Scan Engine Properties page now displays a dedicated warning when the company code is unset, with a link to the system property for resolution.
-   **[Value management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-in-platform-business-outcomes.md)**

    Access Hardware Asset Management \(HAM\) and Software Asset Management \(SAM\) functionality through a single, unified ITAM app, grouped under IT Asset Management. All previously collected data and configuration is carried over with no manual reinstallation, reconfiguration, required during the upgrade.


## What's deprecated or removed

-   **Accelerators Retirement**

    Jumpstart Your Virtual Agent, Jumpstart Your Natural Language Understanding \(NLU\), Jumpstart Your Multi-Lingual Virtual Agent, Jumpstart Your Issue Auto Resolution, and Jumpstart Your CSDM - Crawl technical Accelerators are no longer available.

-   **Impact Proactive Code Check**

    Impact Proactive Code Check/Health Diagnostics UI artifacts, navigation entries, and background jobs are being removed. Ensure your customizations don't depend on Impact Health Diagnostics navigation or diagnostics-specific tables.


