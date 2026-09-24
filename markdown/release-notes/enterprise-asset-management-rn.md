---
title: Enterprise Asset Management release notes
description: The ServiceNow Enterprise Asset Management application manages the entire life cycle of your enterprise's connected and non-connected assets. You can extend the life of your assets while reducing any costly downtime. See the following sections for release notes by version.The version 11.0 release adds AI-assisted enterprise model and asset import capabilities, seeded templates for manual enterprise model and asset imports, and an application installation option from the Admin Home page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/enterprise-asset-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Enterprise Asset Management, Enterprise Asset Management]
breadcrumb: [Asset Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Enterprise Asset Management release notes

The ServiceNow® Enterprise Asset Management application manages the entire life cycle of your enterprise's connected and non-connected assets. You can extend the life of your assets while reducing any costly downtime. See the following sections for release notes by version.

## About Enterprise Asset Management

-   Track and manage your enterprise assets throughout their entire life cycles, from planning to disposal.
-   Optimize costs and maximize your return on investments through comprehensive cost analysis and monitoring capabilities.
-   Maintain accurate asset tracking through standardized onboarding, deployment workflows, and asset audits.
-   Minimize downtime, improve performance, and extend the asset lifespan by using various workflows and capabilities, such as planned maintenance, asset performance and KPI tracking, and asset repairs.

See [Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management.md) for more information.

## Activation and other requirements

**Note:** The following applications are available in the ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   Enterprise Asset Management for Facilities
-   Operational Technology \(OT\) Asset Management
-   Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)
-   Enterprise Asset Management for Providers

For details, see the following activation information.

-   **Activation information**

    Install the following applications by requesting them from the ServiceNow Store:

    -   Enterprise Asset Management
    -   Enterprise Asset Management for Healthcare
    -   Enterprise Asset Management for Facilities
    -   OT Asset Management
    -   Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)
    -   Enterprise Asset Management for Providers
    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


## Accessibility and localization

-   **Accessibility information**
    -   Reflow support for Enterprise Asset Management: Content can be zoomed up to 400% through your browser settings, with page layouts automatically transforming into a vertical, stacked view without loss of content or functionality. This enhancement helps users with low vision or who have trouble seeing web content due to monitor size, device type, poor lighting, or other situations.

**Parent Topic:**[Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-asset-management-rn-landing.md)

## Version 11.0

The version 11.0 release adds AI-assisted enterprise model and asset import capabilities, seeded templates for manual enterprise model and asset imports, and an application installation option from the Admin Home page.

### What's new

-   **[Bulk import enterprise models and assets by using AI-assisted import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/importing-data-ai-eam.md)**

    Streamline the bulk import process for your enterprise models and assets by using AI-assisted import. AI-assisted import automatically analyzes the external model and asset data that you upload into your ServiceNow instance. It then uses AI-powered column and value mappings to automatically align this data with ServiceNow table fields and values, eliminating the need for manual mapping. You can save your completed mappings as templates, further simplifying the import process across future imports. AI-assisted import also provides real-time feedback that helps you identify and resolve errors before you import any data. With AI-assisted import, you can reduce the time and effort that you spend on importing your enterprise models and assets.

-   **[Import enterprise models and assets through enhanced seeded templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/download-seeded-template-manual-bulk-imports.md)**

    Use enhanced seeded templates to manually import enterprise models and assets into your ServiceNow instance. Each template is preconfigured for a specific import scenario and includes a detailed implementation aid, providing immediate guidance on the fields and formatting required for a successful import.

-   **[Install the Enterprise Asset Management application from the Admin Home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/install-eam-admin-home-page.md)**

    Install the Enterprise Asset Management application or any Enterprise Asset Management dependent applications from the Admin Home page. The Admin Home page provides an overview of each application that you're entitled to install and configure.


### What's deprecated or removed

-   **[Enterprise model and asset import templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/download-seeded-template-manual-bulk-imports.md)**

    Enterprise model and asset import templates that were previously generated from Enterprise Asset Management staging tables have been replaced with seeded import templates.


### Plugin information

-   **New plugins**
    -   Enterprise Data Transform \(sn\_ent\_datamap\): Provides access to all enterprise data transform tables.
    -   Enterprise Data Transform Components \(sn\_ent\_datamap\_components\): Provides access to seismic workspace components.
    -   AI Agents for Enterprise \(sn\_ent\_aia\): Provides AI skills related to model categories and classifications.

