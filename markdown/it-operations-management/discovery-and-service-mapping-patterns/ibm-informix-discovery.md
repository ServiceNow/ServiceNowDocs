---
title: IBM Informix Dynamic Server discovery
description: The ServiceNow Discovery and Service Mapping applications can find and map the Informix Dynamic Server. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM Informix Dynamic Server discovery

The ServiceNow Discovery and Service Mapping applications can find and map the Informix Dynamic Server. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **User**

    Provide a user with permissions to run the following commands without elevated rights:

    -   `$install_directory/bin/onstat -g dis`

        This command gets the status and configuration of Informix Dynamic server.

    -   `$install_directory/bin/dbaccess sysmaster`

        This command runs an sql query against the master schema.

    The same user must have read permission for the following directories:

    -   install\_directory + "/etc/sqlhosts

        Access to this directory is necessary to get information about the port, host, and service definition of the Informix Dynamic server.

    -   /etc/services

        Access to this directory is required to get information about the host service definition.

-   **Credentials**

    Configure SSH credentials in the Credentials module of the ServiceNow platform for accessing the server hosting the Informix Dynamic server.


## Data collected by Discovery during horizontal discovery

|Table and Field|Description|
|---------------|-----------|
|Informix Instance \[cmdb\_ci\_db\_informix\_instance\]|The Informix instance attributes.|
|tcp\_port|
|running\_process|
|version|
|install\_directory|
|config\_file|
|name|
|Informix Catalog \[cmdb\_ci\_db\_informix\_catalog\]|The database included in the Informix Instance.|
|database|

## CI Relationships

|CI|Relationship/Reference|CI|
|---|----------------------|---|
|Informix Instance \[cmdb\_ci\_db\_informix\_instance\]|Contains::Contained by|Informix Catalog \[cmdb\_ci\_db\_informix\_catalog\]|

## Top-down

During top-down discovery, Service Mapping discovers connections between the Informix Instance and the Informix Catalogs that the instance contains and displays them as an inclusion on the application service map.

**Parent Topic:**[Available on-premise discovery patterns](available-patterns.md)

