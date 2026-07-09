---
title: ERP Semantic Mining release notes
description: The ServiceNowERP Semantic Mining \(ERP-CM\) product enables ERP \(Enterprise Resource Planning\) consultants and architects to identify customizations and recommend candidates for replatforming from the ERP system onto the ServiceNow AI Platform. ERP Semantic Mining was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# ERP Semantic Mining release notes

The ServiceNow®ERP Semantic Mining \(ERP-CM\) product enables ERP \(Enterprise Resource Planning\) consultants and architects to identify customizations and recommend candidates for replatforming from the ERP system onto the ServiceNow AI Platform. ERP Semantic Mining was enhanced and updated in the Yokohama release.

## ERP Semantic Mining highlights for the Yokohama release

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   Easily clear a blocked ETL \(extract, transform, and load\) processing flow when an automatic or manual synchronization of ERP data between the ERP system of record and your ServiceNow instance is not successful by using the **Reset AI/ML analysis** option.

[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   View charts and graphs on the new ERP Semantic Mining home page dashboard.
-   Take guided tours with interactive steps to learn about features and interactively complete tasks in ERP Semantic Mining.

See [ERP Semantic Mining \(ERP-CM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-customization-mining-overview.md) for more information.

**Important:** ERP Semantic Mining is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   **[Reset AI/ML analysis to control the ML training](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpcm-check-data-connection.md)**

    Use **Reset AI/ML analysis** option to clear the AI/ML analysis so the flow can run again.


[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   **[ERP Semantic Mining dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpcm-obtaining-statistics-and-mining-analysis.md)**

    View statistics about mining results and candidates on the home page dashboard.

-   **[Guided tours in ERP Semantic Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/guided-tours-in-erp-customization-mining.md)**

    Learn about features and complete tasks through interactive steps by taking guided tours within ERP Semantic Mining.

-   **[Updated home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpcm-obtaining-statistics-and-mining-analysis.md)**

    The new home page provides a dashboard showing metrics through charts and graphs related to ERP Semantic Mining.


## Changed in this release

[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   **[Faster initialization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/how-erp-clean-core-inputs-data.md)**

    In addition to daily total application statistics, the SQLM and APPSTATS initial scan now also retrieves all monthly total application statistics up to the current date.


## Activation information

Install ERP Semantic Mining by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/exploring-erp-integration.md)**

    Zero Copy Connector for ERP enables you to simplify the use of ERP data from the system of record such as SAP. You can also create extraction tables on the ServiceNow AI Platform to transform data and create ERP models.

-   **[App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/aes-overview.md)**

    App Engine Studio consumes remote tables and extraction tables from the ERP system to enable you to create custom low-code apps and flows based on the migration candidates.

-   **[Remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/remote-tables.md)**

    Financial Services Remote Tables connect the ServiceNow AI Platform to third-party sources or to another instance so that you can retrieve external data and optionally cache it in the memory.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio.md)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience. Consolidate Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, and Decision Builder into one design environment.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/build-automate-rn-landing.md)

