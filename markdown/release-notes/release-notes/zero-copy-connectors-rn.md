---
title: Zero Copy Connectors release notes
description: The ServiceNow Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.The ServiceNow Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.The ServiceNow Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.The ServiceNow Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.The ServiceNow Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.The ServiceNow Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.The ServiceNow Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Zero Copy Connectors release notes

The ServiceNow® Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.

## About Zero Copy Connectors

-   Retrieve real-time data from external systems using new primary connectors.
-   Fetch real-time data from another ServiceNow® instance using the ServiceNow® Remote Instance connector.
-   Connect to Databricks, Oracle, and Snowflake using OAuth authentication.
-   Query time-series monitoring data from Prometheus using the new community connector.
-   Include either primary connectors only or both primary and community connectors.
-   Retrieve real-time data from Oracle HCM \(Discovery\), and Acumatica using new REST connectors.
-   Connect to MySQL and PostgreSQL using newly promoted primary connectors.
-   Authenticate to external data sources using your own credentials with personal authentication support.

See [Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/zero-copy-connectors.md) for more information.

## Activation and other requirements

**Important:** The Zero Copy Connectors app is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Zero Copy Connector Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    Zero Copy Connector Hub is also available with activation of the Zero Copy Connectors app \(sn\_data\_fabric\_zcc\), which requires a separate subscription. For details, see [Request Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/request-zcc.md).


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-automate-rn-landing.md)

## September 2026

The ServiceNow® Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.

### What's new

-   **[Australia Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-6.md)**
    -   [Oracle HCM \(Discovery\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/oracle-hcm-discovery-zcc.md): Retrieve discovery-related data from Oracle HCM in real-time without copying or duplicating the data.
    -   [Acumatica](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/acumatica-zcc.md): Retrieve data from Acumatica in real-time without copying or duplicating the data.
    -   [REST connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rest-connectors.md), Oracle HCM \(Discovery\) and Acumatica, display dedicated connector icons and a REST tag in the connector selection UI.
    -   Authenticate to [Databricks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/databricks-zcc.md) and [Snowflake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/snowflake-zcc.md) using your own credentials instead of a shared service account, so that access is individually authenticated and auditable at the source system.

### What's changed

-   **[Australia Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-6.md)**
    -   [MySQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mysql-zcc.md): The MySQL connector moved from the Community connector list to the Primary connector list. This connector is available with a Preview label, indicating that performance enhancements are ongoing.
    -   [PostgreSQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/postgresql-zcc.md): The PostgreSQL connector moved from the Community connector list to the Primary connector list.
    -   Authentication options for MySQL and PostgreSQL connections: The connection form for MySQL and PostgreSQL now includes additional authentication drop-down options, including AWS IAM and OAuth, alongside basic authentication.

## June 2026

The ServiceNow® Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.

### What's new

-   **[Cloudera Hive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/cloudera-hive-zcc.md)**

    Retrieve data from Cloudera Hive in real time without copying or duplicating the data. This connector is available with a Preview label, indicating that enhancements are ongoing.

-   **[Microsoft OneLake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/microsoft-onelake-zcc.md)**

    Retrieve data from Microsoft OneLake in real time without copying or duplicating the data. This connector is available with a Preview label, indicating that enhancements are ongoing.


## Australia General Availability

The ServiceNow® Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.

### What's changed

-   **[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)**
    -   [Teradata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/teradata-zcc.md): The Teradata connector now supports Bearer Token and OAuth authentication methods.
    -   [Apache Iceberg](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/apache-iceberg-primary-zcc.md): The Apache Iceberg connector now supports S3-compatible object storage systems.

## April 2026

The ServiceNow® Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.

### What's new

-   **[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)**

    [Connect to Prometheus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/prometheus-zcc.md)Retrieve data from Prometheus in real time without having to copy or duplicate the data.


### What's changed

-   **[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)**
    -   [Amazon S3 Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/amazon-s3-tables-zcc.md)
    -   [Apache Iceberg](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/apache-iceberg-primary-zcc.md)

## Australia Early Availability

The ServiceNow® Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.

### What's new

-   **[Cloudera Impala](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/cloudera-impala-zcc.md)**

    Retrieve data from Cloudera Impala in real time without copying or duplicating the data.

-   **[Connect to another ServiceNow® instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/servicenow-remote-instance-zcc.md)**

    Retrieve data from another ServiceNow® instance in real time without copying or duplicating the data.

-   **[OAuth authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-databricks-connection-zcc.md)**

    Configure OAuth authentication in Databricks, Oracle, and Snowflake connectors.


### What's changed

-   **[Apache Iceberg primary connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/apache-iceberg-primary-zcc.md)**

    The Apache Iceberg connector is now certified as a primary connector.

-   **[Primary connectors in preview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/primary-connectors-zcc.md)**

    Primary connectors that are still being enhanced to include all planned functionality are now marked with a Preview label. These connectors are fully supported by ServiceNow®.


## Australia

The ServiceNow® Zero Copy Connectors application unifies data from across the enterprise, providing access to external data in real time without needing to copy it to your instance. Zero Copy Connectors was enhanced and updated in the Australia release.

### What's changed

-   **[New application name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/zero-copy-connectors.md)**

    Workflow Data Fabric Hub is now Zero Copy Connector Hub.

-   **[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)**

    [New connector package options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/zero-copy-connectors.md)When installing Zero Copy Connectors, you can include primary connectors only by selecting Zero Copy Connectors Primary \(sn\_zcc\_primary\). Alternatively, select Zero Copy Connectors \(sn\_data\_fabric\_zcc\) to include both primary and community connectors.

-   **[Australia Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-6.md)**
    -   Authenticate to [Databricks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/databricks-zcc.md) and [Snowflake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/snowflake-zcc.md) using your own credentials with personal authentication support.
    -   Retrieve real-time metadata and data from REST-enabled systems without copying or duplicating the data. This release adds [REST connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rest-connectors.md) for [Oracle HCM \(Discovery\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/oracle-hcm-discovery-zcc.md) and [Acumatica](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/acumatica-zcc.md).
    -   [MySQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mysql-zcc.md) and [PostgreSQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/postgresql-zcc.md) connectors moved from Community connectors to Primary connectors.

### Plugin information

-   **Renamed or changed plugins**

    The following plugins were renamed or changed in Australia:

    -   Workflow Data Fabric Hub \(sn\_data\_fabric\): Renamed to Zero Copy Connector Hub \(sn\_data\_fabric\).
    -   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md): Zero Copy Connectors \(sn\_data\_fabric\_zcc\): Now available as two separate installation options — Zero Copy Connectors Primary \(sn\_zcc\_primary\) for primary connectors only, or Zero Copy Connectors \(sn\_data\_fabric\_zcc\) for both primary and community connectors.

