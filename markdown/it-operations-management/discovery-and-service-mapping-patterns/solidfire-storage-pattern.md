---
title: NetApp SolidFire storage system discovery
description: ServiceNow Discovery uses the NetApp SolidFire storage system discovery pattern to find clusters and nodes on the SolidFire storage system. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# NetApp SolidFire storage system discovery

ServiceNow Discovery uses the NetApp SolidFire storage system discovery pattern to find clusters and nodes on the SolidFire storage system. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Discovery and Service Mapping Patterns store app**

    Verify the Discovery and Service Mapping Patterns store app \(version 1.0.74\) is installed.

-   **Basic Auth permissions**

    Ensure Basic Auth credentials are configured for authenticating the Element API calls. Save the following SolidFire Cluster Admin credentials as Basic Auth credentials to ensure proper access:

    -   read
    -   clusterAdmins
    -   reporting
    -   drives
-   **MID server**

    Ensure the MID server can access the target device.

-   **Discovery credentials**

    Ensure you have the credentials for running Discovery on the host machine running the SolidFire storage system​.

-   **Create a serverless discovery schedule**

    Create a discovery schedule to perform targeted discovery of SolidFire clusters and nodes.

    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Click **New** and then fill in the form.

<table id="table_tt1_3z5_54b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the Discovery schedule. For example, `Discover SolidFire`.

</td></tr><tr><td>

Discover

</td><td>

Discover type. Select **Serverless**.

</td></tr><tr><td>

MID Server

</td><td>

Name of the MID Server.

</td></tr><tr><td>

Active

</td><td>

Option for enabling this schedule for discovery. Select this check box to enable discovery.

</td></tr></tbody>
</table>    3.  Right-click the header of the Discovery Schedule form and select **Save**.
    4.  Click the **Serverless Execution Patterns** tab, click **New**, and then fill in the form.

        ![Serverless execution pattern](../image/serverless-execution-pattern.png)

        |Field|Description|
        |-----|-----------|
        |Name|Name for this Serverless Execution Pattern. For example, `SolidFire Storage Pattern`.|
        |Pattern|Name of the pattern to run: NetApp SolidFire Storage System.|
        |Proxy Host|Fully qualified domain name of the machine on which you are installing the proxy server. Specify **Global**.|
        |Active|Option for enabling this schedule for discovery. Select this check box to enable discovery.|

    5.  Under **Discovery Pattern Launcher Parameters**, configure the launch parameters with the relevant values. Ensure the Management IP of the cluster and Credentials Alias are defined.

## Data collected by Discovery during horizontal discovery

The discovered SolidFire configuration data includes the following tables and fields.

|Table and field|Description|
|---------------|-----------|
|Main Configuration Item \[cmdb\_ci\_storage\_server\]​|
|name|The name of the CI.|
|serial\_number​|The serial number associated with the CI.|
|firmware\_version|The firmware version of the CI.|
|ip\_address|The IP address of the CI.|
|short\_description|A short textual description of the CI.|
|manufacturer|The device manufacturer.|
|model\_id|The device model ID.|
|os\_version|The version of the OS running on the CI.|
|os|The OS running on the CI.|
|Storage cluster \[cmdb\_ci\_storage\_cluster\]​|
|ip\_address|The IP address of the storage cluster.|
|manufacturer|The device manufacturer.|
|short\_description|A short textual description of the CI.|
|cluster\_version​|Element OS API version running on the cluster.|
|name|The name of the CI.|
|Storage cluster node \[cmdb\_ci\_storage\_cluster\_node\]|
|name|The name of the CI.|
|operational\_status|Indicates if the device is in active state.|
|cluster|Reference for the cluster CI.|
|Storage node element \[cmdb\_ci\_storage\_node\_element\]|
|short\_description|A short textual description of the CI.|
|manufacturer|The device manufacturer.|
|serial\_number|The serial number associated with the CI.|
|model\_id​|The device model ID.|
|chassis\_type​|The type of chassis that contains the server.|
|ram|The memory size of the CI.|
|cpu\_type|The CPU type.|
|cpu\_manufacturer|The CPU manufacturer.|
|Storage disk \[cmdb\_ci\_disk\]|
|name|The name of the CI.|
|device\_id|The ID of the device.|
|serial\_number|The serial number associated with the CI.|
|storage\_type​|The storage type.|
|size\_bytes|The available storage size in bytes.|
|manufacturer|The device manufacturer.|
|model\_id|The device model ID.|
|computer|Reference for the storage server.|
|Network adapter \[cmdb\_ci\_network\_adapter\]​|
|name|The name of the CI.|
|ip\_address|The IP address of the CI.|
|netmask|The netmask of the server hosting the network adapter.|
|mac\_address|The MAC address of the network adapter.|
|IP address \[cmdb\_ci\_ip\_address\]|
|ip\_address|The IP address of the CI.|
|netmask|The netmask of the server hosting the CI.|

The Dependency Views map shows all discovered SolidFire storage system clusters and nodes in your organization and the relationships between them.

![SolidFire storage system dependency view](../image/storage-system-dependency.jpg)

## CI relationships

|CI|Relationship/Reference|CI|
|---|----------------------|---|
|Storage cluster|Cluster Of::Cluster|Storage cluster node|
|Storage cluster node|Hosted On::Hosts|Storage node element|
|Storage node element|Managed By::Manages|Storage cluster|
|Storage server \(main CI\)|Allocated To::Allocated From|Storage node element|
|Storage server \(main CI\)|Runs On::Runs|Storage cluster|
|Storage server \(main CI\)|Contains::Contained By|Disk|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

