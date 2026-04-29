---
title: Pure Storage FlashBlade discovery
description: The ServiceNow Discovery application uses the FlashBlade Pure Storage pattern to find FlashBlade components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Pure Storage FlashBlade discovery

The ServiceNow Discovery application uses the FlashBlade Pure Storage pattern to find FlashBlade components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery can find Pure Storage FlashBlade version 4.

**Note:**

Only Linux MID Servers are supported for Pure Storage FlashBlade discovery. Windows MID Servers are not supported.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Configure user permissions for UNIX OS**

    Configure a user for accessing the UNIX OS.

    -   Define the OS user with permissions to run the following commands.

        |Command|Parameter|Mandatory/Optional|Description|
        |-------|---------|------------------|-----------|
        |Pureman|-|Mandatory|Accesses the list of pure storage commands and uses them for classification.|
        |Echo|$$username$$|Mandatory|Fills in the username for the temporary variable.|
        |"pureadmin list "|+ $usr + " --api-token --expose --csv"|Mandatory|Gets the user API token to generate the x-auth for the REST call commands.|

    -   Define the OS user with the required permissions to run the following REST API calls.

        -   `/api/login` – Gets the x-auth token reader from the response in Groovy.
        -   `/api/1.2/file –systems` – Retrieves information about the file systems.
        -   `/api/1.2/blades` – Retrieves information about blades.
        -   `/api/1.2/dns` – Retrieves information about DNS.
        -   `/api/1.2/hardware` – Retrieves information about the storage hardware.
        -   `/api/1.4/network-interfaces` – Retrieves information about network interfaces.
-   **Configure SSH credentials**

    On the ServiceNow AI Platform, configure SSH credentials for the OS user. For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **Configure applicative credentials**

    On the ServiceNow AI Platform, configure applicative credentials for the OS user. The password field is not relevant; you can enter any value for the password or leave it empty. For more information, see [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **Access to the port used for REST calls**

    On relevant Linux MID Servers, provide a user with access to the port used for REST calls.


## Data collected by Discovery for Pure Storage FlashBlade

Discovery populates the data in the CMDB when running the FlashBlade Pure Storage pattern.

|Table and field|Description|
|---------------|-----------|
|Storage Server \[cmdb\_ci\_storage\_server\]|The attributes of the storage server provided by FileShare for PureBlade.|
|IP address \[ip\_address\]|
|Serial number \[serial\_number\]|
|Name \[name\]|
|Pure Storage Processor \[cmdb\_ci\_storage\_processor\_pure\]|The attributes of the PureBlade storage processor.|
|Name \[name\]|
|Serial number \[serial\_number\]|
|Device ID \[device\_id\]|
|Model number \[model\_number\]|
|Serial \[serial\]|
|Slot \[slot\]|
|Type \[type\]|
|Status \[status\]|
|Pure Storage File Share \[cmdb\_ci\_storage\_fileshare\_pure\]|The attributes of the storage FileShare.|
|Name \[name\]|
|Path \[path\]|
|Protocols \[protocols\]|
|Provisioned Space \[provisioned\_space\]|
|Unique Space \[unique\_space\]|
|Snapshots Space \[snapshots\_space\]|
|Total Physical Space \[total\_physical\_space\]|
|Shared space \[shared\_space\]|
|Data Reduction \[data\_reduction\]|
|System Space \[system\_space\]|
|Storage Device \[cmdb\_ci\_storage\_device\]|The attributes of the storage device contained by the storage server.|
|Device ID \[device\_id\]|
|Name \[name\]|
|Serial number \[serial\_number\]|
|Model number \[model\_number\]|
|Storage type \[storage\_type\]|

The graphic illustrates CIs that are part of FlashBlade discovery.

![The FlashBlade components](../image/PureBlade-dependency-views.png)

## CI relationships

Discovery creates these relationships to support the Pure Storage FlashBlade discovery.

|CI|Relationship|CI|
|---|------------|---|
|Pure Storage File Share \[cmdb\_ci\_storage\_fileshare\_pure\]|Provided By::Provides|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Device \[cmdb\_ci\_storage\_device\]|Contains::Contained by|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Contains::Contained by|Pure Storage Processor \[cmdb\_ci\_storage\_processor\_pure\]|

**Parent Topic:**[Available on-premise discovery patterns](available-patterns.md)

