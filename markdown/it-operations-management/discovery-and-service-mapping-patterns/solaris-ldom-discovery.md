---
title: Oracle Solaris LDOM discovery
description: Discovery uses the Solaris Logical Domain \(LDOM\) infrastructure pattern and Solaris LDOM shared library pattern to find all LDOM data. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle Solaris LDOM discovery

Discovery uses the Solaris Logical Domain \(LDOM\) infrastructure pattern and Solaris LDOM shared library pattern to find all LDOM data. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses these patterns to run horizontal discovery. You can use the patterns on the ServiceNow AI Platform using the Yokohama release or later.

The Solaris LDOM infrastructure pattern is triggered automatically on Solaris Server discovery. The pattern verifies if there is an LDOM controller, and stops running if it doesn't find a controller.

The Solaris LDOM shared library pattern is run as an Extension Section to the Solaris Server pattern​. The pattern modifies the Serial Number \(SN\) on LDOM machines so that it matches the SN populated by the Solaris LDOM infrastructure pattern. For further information about Solaris Server, see [Solaris discovery](../../discovery/reference/r_DataCollDiscoSolarisComputers.md).

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **LDOM commands when running the Solaris LDOM infrastructure pattern**

    Ensure the relevant users have permissions to execute the following used commands for the Solaris LDOM infrastructure pattern:

    -   `"sudo /usr/sbin/virtinfo -a”`
    -   `"sudo /usr/sbin/ldm -V”​`
    -   `"hostname”`
    -   `"svcs ldmd”​`
    -   `"sudo /usr/sbin/ldm list-rsrc-group -a”​`
    -   `"sudo /usr/sbin/sneep -T | grep ChassisSerialNumber 2> /dev/null”​`
    -   `"/usr/sbin/prtdiag -v | awk '/Chassis Serial/{getline; getline; print}'"`
    -   `"sudo /usr/sbin/ldm list"​`

        **Note:** Some of these commands are used with conditions, and will not be executed on each discovery. For example, the main way to get the SN for servers is by using the `‘sneep’`command. However, this is not available by default on Solaris servers, so `‘prtdiag’` is used as an alternative method to get the SN.​

-   **Important LDOM commands when running the Solaris LDOM shared library pattern**

    Ensure the relevant users have permissions to execute the following used commands for the Solaris LDOM shared library pattern:

    -   `"sudo /usr/sbin/virtinfo -a”`​
    -   `"sudo /usr/sbin/sneep -T | grep ChassisSerialNumber 2> /dev/null”​`
    -   `"hostname”​`
    Ensure the relevant users have the permissions to execute the LDOM `virtinfo` command. This command ensures the proper LDOM role can be established.

    Ensure the relevant users have the permissions to execute the LDOM `"sudo /usr/sbin/ldm list”` command for listing Guest VMs on the LDOM controller. This is required in order to set relations between the LDOM controller and the LDOM Guest VMs.

    One of the `‘sneep’` or `‘prtdiag’` Serial Number commands has to return a correct response in order to correctly set the SN.


## Data collected by Discovery during horizontal discovery

The data discovered by both patterns includes the following tables and fields.

|Table and field|Description|
|---------------|-----------|
|Solaris Server \[cmdb\_ci\_solaris\_server\]|
|ldom\_version|The LDOM version installed on the LDOM controller.|
|ldom\_role|The LDOM role; "controller” or "guest”.​|
|ldom\_state|The state of the LDOM implementation on the LDOM controller.|
|serial\_number|The serial number of the machines.|
|virtual|Whether or not a virtual machine \(for Guest VMs\) is used for the LDOM controller.​|
|ram|The memory available on the LDOM controller.​|
|cpu\_core\_count|The number of CPU cores on the LDOM controller.|

## CI relationships

|CI|Relationship|CI|
|---|------------|---|
|LDOM controller|Hosted on::Hosts|LDOM Guest VM|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

