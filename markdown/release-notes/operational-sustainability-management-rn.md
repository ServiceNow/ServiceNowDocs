---
title: Operational Sustainability Management release notes
description: The ServiceNow Operational Sustainability Management application helps organizations manage sustainability data, metrics, and reporting requirements. See the following sections for release notes by version.This release enhances sustainability reporting and content management with improved Document Designer capabilities and framework content updates that are delivered independently of application upgrades.This release adds historical data generation for metrics and improves threshold rating accuracy for metric data tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/operational-sustainability-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Operational Sustainability Management release notes

The ServiceNow® Operational Sustainability Management application helps organizations manage sustainability data, metrics, and reporting requirements. See the following sections for release notes by version.

## About Operational Sustainability Management

-   Streamline sustainability data collection, management, and reporting across your organization.
-   Monitor sustainability performance using configurable metrics, thresholds, campaigns, and workflows.
-   Improve data quality and reporting accuracy through automation, integrations, and AI-powered capabilities.
-   Support sustainability reporting and disclosure requirements with centralized governance and data management.

See [Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/environmental-social-governance/esg-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Operational Sustainability Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/new-features-changes.md)

## September 2026

This release enhances sustainability reporting and content management with improved Document Designer capabilities and framework content updates that are delivered independently of application upgrades.

### What's changed

-   **[Enhanced content generation in Document Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configure-data-columns.md)**

    With Document Designer version 23.0.3, you can create HTML-based scripted columns for content blocks in your reports.


-   **[Framework and regulatory content updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/environmental-social-governance/esg-content-accelerator.md)**

    With Unified Content Management version 23.0.4, you receive updated framework and regulatory content without waiting for application upgrades.


### Plugin information

-   **New plugins**

    Operational Sustainability Management Prime \(com.sn\_osm\_ai\_prime\): Provides the components required to activate the Prime subscription tier of Operational Sustainability Management.


## October 2026

This release adds historical data generation for metrics and improves threshold rating accuracy for metric data tasks.

### What's new

-   **[Historical data for metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/environmental-social-governance/historical-data-generation-for-metrics.md)**

    With GRC: Metrics version 23.1.2, you can create historical data for past periods on manual and automated metrics. When you create historical data, the system generates metric definition data, metric data and metric data tasks from the historical start date up to the most recent completed period. If the metric belongs to an active, published campaign, the system also creates campaign cycles for those periods.

    To create historical data, select the **Create historical data** option on a metric and enter a historical start date. The records are generated during the next metric data run or when you execute the associated metric definition.

    The new historical records start in the following states:

    |Record|Manual metric|Automated metric|
    |------|-------------|----------------|
    |Metric data|Pending|Pending, or Completed when no task is created|
    |Metric data task|New|In progress|
    |Campaign cycle \(campaign-enabled metrics only\)|Data collection|Data collection|


### What's changed

-   **[Threshold rating recalculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/environmental-social-governance/thresholds-for-metrics.md)**

    With GRC: Metrics version 23.1.2, threshold ratings and breach status are recalculated when you edit a threshold, delete a threshold, reopen a metric data task, or move it to the Estimated state. Ratings also update when you save or override a metric data value.


