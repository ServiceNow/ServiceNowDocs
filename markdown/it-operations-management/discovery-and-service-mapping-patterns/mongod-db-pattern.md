---
title: mongod DB pattern-based discovery
description: Discovery and Service Mapping Patterns uses the mongod DB pattern to find MongoDB servers that run the mongod process on UNIX and Windows servers. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/mongod-db-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-11-03"
reading_time_minutes: 2
keywords: [mongod DB, MongoDB, Mongo Config Server, pattern discovery]
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# mongod DB pattern-based discovery

Discovery and Service Mapping Patterns uses the mongod DB pattern to find MongoDB servers that run the mongod process on UNIX and Windows servers. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

For information on probe-based MongoDB discovery, see [MongoDB probe-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/r_DiscoverMongoDBInstances.md).

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
    -   CMDB CI Class Models
-   **Verify permission to run the version commands**

    Verify you have permission for the following commands:

    -   `<mongod_install_directory>/mongod --version`
    -   On Windows servers: `<mongod_install_directory>\mongod.exe --version`
    -   If the version isn't found: `<mongod_install_directory>/mongo --version`
-   **Verify permission to run the database name command**

    Verify you have permission for the following commands:

    -   `echo 'db.getName()' | <mongod_install_directory>/mongo`
    -   On Windows servers: `echo 'db.getName()' | <mongod_install_directory>\mongo.exe`
-   **Verify read access to the MongoDB configuration file**

    Verify you have read access to the configuration file that is specified by the `--config` or `-f` option of the mongod process.

-   **Create credentials for the operating system**

    Create credentials for the operating system of the servers you want to discover:

    -   For UNIX, see [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_SSHCredentialsForm.md)
    -   For Windows, see [Windows credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_WindowsCredentialsForm.md)
-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/t_CreateADiscoverySchedule.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the mongod DB pattern.

<table id="table_mongo_config_serv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the MongoDB database. If the name isn't available, the value is set to Mongo DB.

</td></tr><tr><td>

Port \[port\]

</td><td>

Port on which the MongoDB server listens.

</td></tr><tr><td>

Version \[version\]

</td><td>

Version of MongoDB.

</td></tr><tr><td>

Installation directory \[install\_directory\]

</td><td>

Directory in which MongoDB is installed.

</td></tr><tr><td>

Configuration file \[config\_file\]

</td><td>

Path to the MongoDB configuration file.

</td></tr><tr><td>

Running process command \[running\_process\_command\]

</td><td>

Command of the running MongoDB process.

</td></tr><tr><td>

Running process key parameters \[running\_process\_key\_parameters\]

</td><td>

Key parameters of the running MongoDB process.

</td></tr><tr><td>

Discovery source \[discovery\_source\]

</td><td>

Source of discovery. The value depends on the **mid.discovery\_source\_field\_legacy.default** MID Server property and is one of the following:-   CredentiallessDiscovery: when the property is set to true, which is the default.
-   ServiceNow: when the property is set to false.

</td></tr></tbody>
</table>**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

