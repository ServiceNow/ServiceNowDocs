---
title: Impact release notes
description: ServiceNow Impact is built on the ServiceNow AI Platform and combines customized service with a digital interface to provide tailored recommendations and guidance. Impact was enhanced and updated in the Brazil release. See the following sections for release notes by version.Version 11.0.0 introduces standalone product adoption functionality, new Accelerators across multiple domains, Scan Engine API and exception workflow enhancements, and Business Outcomes improvements. It also retires legacy Accelerators and Impact Health Diagnostics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/impact-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Impact release notes

ServiceNow® Impact is built on the ServiceNow AI Platform and combines customized service with a digital interface to provide tailored recommendations and guidance. Impact was enhanced and updated in the Brazil release. See the following sections for release notes by version.

## About Impact

-   Achieve success your way with tailored resources, driving outcomes aligned to your business priorities.
-   Accelerate business outcomes faster with the AI Control Tower, reducing time to measurable impact.
-   Adopt ServiceNow products and AI innovations rapidly, ensuring your team moves at the speed of transformation.
-   Maximize your ServiceNow investment, proving its value to stakeholders through measurable adoption and outcomes.
-   Improve platform health with proactive guidance, keeping your instance optimized and future-ready.

See [Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Impact by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    Impact configuration requires a sequence of tasks in a unified registration process. See [Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-impact-platform.md).


**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/new-features-changes.md)

## September 2026 store \(v11.0.0\)

Version 11.0.0 introduces standalone product adoption functionality, new Accelerators across multiple domains, Scan Engine API and exception workflow enhancements, and Business Outcomes improvements. It also retires legacy Accelerators and Impact Health Diagnostics.

### What's new

-   **[Product adoption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/product-adoption.md)**

    Access core product adoption functionality, capabilities map and product adoption roadmap, without connecting to Service Exchange.

    -   View the capabilities map with a list of capabilities and their entitlement status. You can also edit the usage status manually for relevant capabilities.
    -   Create product adoption roadmaps using templates or manually, and manage capabilities for those new product adoption roadmaps.
    -   Receive a consistent message when functionality is limited by unavailable status or inability to edit existing product adoption roadmaps until Service Exchange connects with Guided Setup.
-   **[Latest Accelerators by Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/new-accelerators-australia-release.md)**
    -   Accelerate AI adoption and time to value by generating complete applications, surfacing automation opportunities, measuring AI investment impact, and migrating Virtual Agent topics.
    -   Reduce onboarding friction and technical risk by orienting teams to scoped app development and enabling secure, integration-free access to external data sources. Activate Field Encryption Enterprise as a core part of your Vault Suite security strategy.
    -   Strengthen your governance foundation by structuring your CSDM data model, establishing sound IRM Entity Framework design, managing your demand pipeline, and improving Knowledge Management process maturity.
-   **[Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/platform-health-idi.md)**
    -   Call the Scan Engine API to provide trigger scans on demand, check scan status and results, and integrate findings into pipeline approval gates.
    -   Use exception approval workflows with explicit **Save Draft** and **Submit** actions.
    -   Use configurable exception reason scope controls.
-   **[Value management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-in-platform-business-outcomes.md)**
    -   View the same product line label in the Impact Delivery Instance as in the Impact Store Application for the same product. For example, IT Service Management instead of ITSM. Both legacy and current models in the Impact Delivery Instance now map to the correct product line taxonomy.
    -   Filter outcomes by version using the new Outcome version filter, available on the Objectives &amp; Outcomes landing page and the Outcome Insights page in Impact Delivery Instance.

### What's changed

-   **Accelerator Catalog**
    -   Success Readiness Assessment changed to Success Foundation Review.
    -   UX Accelerators moved from Architecture to the Technical sub-catalog.
    -   AI Readiness Assessment moved from Architecture to the Technical sub-catalog.
    -   Tuneup Your IT Asset Management changed to Tuneup Your ITSM Asset Management.
    -   Jumpstart Your App Engine changed to Jumpstart Your App Deployment Governance.
-   **[Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/platform-health-idi.md)**
    -   Exception workflows in update set scans provide multiple governance improvements.
    -   Assign a dedicated exception approver role for governance separation.
    -   Control which finding levels are eligible for exception reasons, as an instance administrator.
    -   Access update set origin tracking on all scan findings.
    -   View the captured update set data that contains the violating code whenever a full or delta scan runs and produces a finding.
    -   Full-scan scope updates so only definitions explicitly configured for single-finding-per-table scanning are included.
    -   The Scan Engine Properties page now displays a dedicated warning when the company code is unset, with a link to the system property for resolution.
-   **[Value management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-in-platform-business-outcomes.md)**

    Access Hardware Asset Management \(HAM\) and Software Asset Management \(SAM\) functionality through a single, unified ITAM app, grouped under IT Asset Management. All previously collected data and configuration is carried over with no manual reinstallation, reconfiguration, required during the upgrade.


### What's deprecated or removed

-   **Accelerators Retirement**

    Jumpstart Your Virtual Agent, Jumpstart Your Natural Language Understanding \(NLU\), Jumpstart Your Multi-Lingual Virtual Agent, Jumpstart Your Issue Auto Resolution, and Jumpstart Your CSDM - Crawl technical Accelerators are no longer available.

-   **Impact Proactive Code Check**

    Impact Proactive Code Check/Health Diagnostics UI artifacts, navigation entries, and background jobs are being removed. Ensure your customizations don't depend on Impact Health Diagnostics navigation or diagnostics-specific tables.


