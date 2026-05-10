---
title: Zero Copy Connectors release notes
description: The ServiceNow Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Zero Copy Connectors release notes

The ServiceNow® Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.

## Zero Copy Connectors highlights for the Australia release

-   Retrieve real-time data from external systems using new primary connectors.
-   Fetch real-time data from another ServiceNow® instance using the ServiceNow® Remote Instance connector.
-   Connect to Databricks, Oracle, and Snowflake using OAuth authentication.
-   Query time-series monitoring data from Prometheus using the new community connector.
-   Include either primary connectors only both primary and community connectors.
-   Connect to Teradata using Bearer Token and OAuth authentication.

See [Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/zero-copy-connectors.md) for more information.

**Important:** The Zero Copy Connectors app is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Cloudera Impala](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/cloudera-impala-zcc.md)**

    Retrieve data from Cloudera Impala in real time without copying or duplicating the data.

-   **[Australia Patch 1](../quality/australia-patch-1.md)**

    [Connect to Prometheus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/prometheus-zcc.md)

    Retrieve data from Prometheus in real time without copying or duplicating the data.

-   **[Connect to another ServiceNow® instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/servicenow-remote-instance-zcc.md)**

    Retrieve data from another ServiceNow® instance in real time without copying or duplicating the data.

-   **[OAuth authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-databricks-connection-zcc.md)**

    Configure OAuth authentication in Databricks, Oracle, and Snowflake connectors.


## UI changes

-   **[New application name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/zero-copy-connectors.md)**

    Workflow Data Fabric Hub is now Zero Copy Connector Hub.

-   **[Australia Patch 1](../quality/australia-patch-1.md)**

    [New connector package options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/zero-copy-connectors.md)

    When installing Zero Copy Connectors, you can either include primary connectors only by selecting Zero Copy Connectors Primary \(sn\_zcc\_primary\), or include both primary and community connectors by selecting Zero Copy Connectors \(sn\_data\_fabric\_zcc\).


## Changed in this release

-   **[Apache Iceberg primary connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/apache-iceberg-primary-zcc.md)**

    The Apache Iceberg connector is now certified as a primary connector.

-   **[Primary connectors in preview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/primary-connectors-zcc.md)**

    Primary connectors that are still being enhanced to include all planned functionality are now marked with a Preview label. These connectors are fully supported by ServiceNow®.

-   **[Australia Patch 1](../quality/australia-patch-1.md)**

    [Amazon S3 Tables connector — Preview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/primary-connectors-zcc.md)

    The Amazon S3 Tables connector is now available with a Preview label, indicating that enhancements are ongoing. This connector is fully supported by ServiceNow®.

-   **[Australia Patch 1](../quality/australia-patch-1.md)**

    [Apache Iceberg connector — Preview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/primary-connectors-zcc.md)

    The Apache Iceberg connector is now available with a Preview label, indicating that enhancements are ongoing. This connector is fully supported by ServiceNow®.

-   **[Australia Patch 2](../quality/australia-patch-2.md)**

    [Teradata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/teradata-zcc.md)

    The Teradata connector now supports Bearer Token and OAuth authentication methods.

-   **[Australia Patch 2](../quality/australia-patch-2.md)**

    [Apache Iceberg](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/apache-iceberg-primary-zcc.md)

    The Apache Iceberg connector now supports S3-compatible object storage systems.


## Activation information

Install Zero Copy Connector Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Zero Copy Connector Hub is also available with activation of the Zero Copy Connectors app \(sn\_data\_fabric\_zcc\), which requires a separate subscription. For details, see [Request Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/request-zcc.md).

## Plugin information

-   **Renamed or changed plugins**

    The following plugins were renamed or changed in Australia:

    -   Workflow Data Fabric Hub \(sn\_data\_fabric\): Renamed to Zero Copy Connector Hub \(sn\_data\_fabric\).
    -   [Australia Patch 1](../quality/australia-patch-1.md): Zero Copy Connectors \(sn\_data\_fabric\_zcc\): Now contains primary and community connectors. Previously contained all connectors in a single package.

-   **New plugins**

    The following plugin was added in Australia:

    -   Zero Copy Connectors Primary \(sn\_zcc\_primary\): New plugin that includes primary connectors only.

**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

