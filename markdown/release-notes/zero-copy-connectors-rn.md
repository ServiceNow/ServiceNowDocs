---
title: Zero Copy Connectors release notes
description: ServiceNow Zero Copy Connectors unifies data from across the enterprise, providing access to external data in real-time without needing to copy it to your instance.Zero Copy Connectors was enhanced and updated in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/zero-copy-connectors-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Zero Copy Connectors, REST connector, personal authentication, MySQL, PostgreSQL, OAuth, Zero Copy Connectors, REST connector, personal authentication, MySQL, PostgreSQL, Jira, Oracle HCM, Acumatica, OAuth]
breadcrumb: [App development and low-code release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Zero Copy Connectors release notes

ServiceNow® Zero Copy Connectors unifies data from across the enterprise, providing access to external data in real-time without needing to copy it to your instance.

## About Zero Copy Connectors

-   Retrieve real-time data from external systems using primary and community connectors, without copying or duplicating the data.
-   Connect to REST-enabled systems such as Oracle HCM \(Discovery\) and Acumatica using REST connectors.
-   Connect to MySQL and PostgreSQL databases using primary connectors.
-   Authenticate to Databricks and Snowflake using your own credentials with personal authentication support.

See [Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/zero-copy-connectors.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Zero Copy Connector Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    Zero Copy Connector Hub is also available with activation of the Zero Copy Connectors app \(sn\_data\_fabric\_zcc\), which requires a separate subscription. For details, see [Request Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/request-zcc.md).

-   **Additional requirements**
    -   Role required: df\_connection\_admin to create connections. Data steward access is also required to view mapped tables.
    -   REST connectors require network connectivity to the target REST-enabled system.

**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/build-automate-rn-landing.md)

## Brazil Early Availability

Zero Copy Connectors was enhanced and updated in the Brazil release.

### What's new

-   **[REST connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/rest-connectors.md)**

    Retrieve real-time metadata and data from REST-enabled systems without copying or duplicating the data. This release adds REST connectors for Oracle HCM \(Discovery\) and Acumatica, built on a generic metadata connector framework that supports filter, limit, and groupBy pushdown operations.

-   **Personal authentication for Databricks and Snowflake**

    Authenticate to [Databricks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/databricks-zcc.md) and [Snowflake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/snowflake-zcc.md) using your own credentials instead of a shared service account, so that access is individually authenticated at the source system.


### What's changed

-   **MySQL connector moved to Primary with Preview label**

    The [MySQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/mysql-zcc.md) connector moved from the Community connector list to the Primary connector list. This connector is available with a **Preview** label, indicating that performance enhancements are ongoing.

-   **PostgreSQL connector moved to Primary**

    The [PostgreSQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/postgresql-zcc.md) connector moved from the Community connector list to the Primary connector list.


