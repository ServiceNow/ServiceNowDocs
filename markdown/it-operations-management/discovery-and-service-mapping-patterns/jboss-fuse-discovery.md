---
title: Red Hat JBoss Fuse discovery
description: The ServiceNow Discovery and Service Mapping applications can find and map the Fuse application server using the JBoss Fuse pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Red Hat JBoss Fuse discovery

The ServiceNow Discovery and Service Mapping applications can find and map the Fuse application server using the JBoss Fuse pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Credentials**

    Configure SSH credentials in the Credentials module of the ServiceNow platform for accessing the server hosting the Fuse server.

-   **User**

    Provide a user with the read rights for accessing the following directories:

    -   `$install_directory + "/readme.txt"`

        Access to this directory allows getting version information.

    -   /etc/services

        Access to this directory allows reading the hosts service definition.


## Data collected by Discovery during horizontal discovery

|Table and Field|Description|
|---------------|-----------|
|Jboss Fuse \[cmdb\_ci\_appl\_jboss\_fuse\]|
|config\_directory|The configuration directory of the Fuse server.|
|config\_file|The configuration file of the Fuse server.|
|install\_folder|The installation folder of the Fuse server.|
|version|The version of the Fuse server.|
|name|The name configured for the Fuse server during installation.|

## Data collected by Service Mapping during top-down discovery

Service Mapping discovers the connection between the JBoss Fuse server and the IBM Informix Dynamic server.

**Parent Topic:**[Available discovery patterns](available-patterns.md)

