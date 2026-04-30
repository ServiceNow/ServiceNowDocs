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

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Easily clear a blocked ETL \(extract, transform, and load\) processing flow when an automatic or manual synchronization of ERP data between the ERP system of record and your ServiceNow instance is not successful by using the **Reset AI/ML analysis** option.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   View charts and graphs on the new ERP Semantic Mining home page dashboard.
-   Take guided tours with interactive steps to learn about features and interactively complete tasks in ERP Semantic Mining.

See [ERP Semantic Mining \(ERP-CM\)](https://www.servicenow.com/docs/access?context=erp-customization-mining-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

**Important:** ERP Semantic Mining is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   **[Reset AI/ML analysis to control the ML training](https://www.servicenow.com/docs/access?context=erpcm-check-data-connection&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Use **Reset AI/ML analysis** option to clear the AI/ML analysis so the flow can run again.


[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   **[ERP Semantic Mining dashboard](https://www.servicenow.com/docs/access?context=erpcm-obtaining-statistics-and-mining-analysis&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    View statistics about mining results and candidates on the home page dashboard.

-   **[Guided tours in ERP Semantic Mining](https://www.servicenow.com/docs/access?context=guided-tours-in-erp-customization-mining&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Learn about features and complete tasks through interactive steps by taking guided tours within ERP Semantic Mining.

-   **[Updated home page](https://www.servicenow.com/docs/access?context=erpcm-obtaining-statistics-and-mining-analysis&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    The new home page provides a dashboard showing metrics through charts and graphs related to ERP Semantic Mining.


## Changed in this release

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   **[Faster initialization](https://www.servicenow.com/docs/access?context=how-erp-clean-core-inputs-data&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    In addition to daily total application statistics, the SQLM and APPSTATS initial scan now also retrieves all monthly total application statistics up to the current date.


## Activation information

Install ERP Semantic Mining by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=exploring-erp-integration&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Zero Copy Connector for ERP enables you to simplify the use of ERP data from the system of record such as SAP. You can also create extraction tables on the ServiceNow AI Platform to transform data and create ERP models.

-   **[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    App Engine Studio consumes remote tables and extraction tables from the ERP system to enable you to create custom low-code apps and flows based on the migration candidates.

-   **[Remote tables](https://www.servicenow.com/docs/access?context=remote-tables&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Financial Services Remote Tables connect the ServiceNow AI Platform to third-party sources or to another instance so that you can retrieve external data and optionally cache it in the memory.

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience. Consolidate Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, and Decision Builder into one design environment.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

