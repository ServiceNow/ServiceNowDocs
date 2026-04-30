---
title: Dell PowerMax storage discovery with Patterns
description: ServiceNow Discovery uses the EMC PMAX phase1 and EMC PMAX phase2 patterns to find Dell PowerMax storage components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-11-09"
reading_time_minutes: 7
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Dell PowerMax storage discovery with Patterns

ServiceNow Discovery uses the **EMC PMAX phase1** and **EMC PMAX phase2** patterns to find Dell PowerMax storage components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To learn about PowerMax storage components and their versions that you can discover, refer to [Detailed information on products discovered by ITOM Visibility](../../service-mapping/reference/r_SupportedApplications.md).

## Prerequisites

-   **Verify that the applications are up to date**

    Discovery and Service Mapping Patterns

    CMDB CI Class Models

-   **Verify the creation of the credential alias**
    1.  Set the scope to: **Global**.
    2.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**
    3.  Select **New**.
    4.  Fill in the fields in the form.

        |Field|Description|
        |-----|-----------|
        |Name|Enter a unique name for the alias. For example: `powermax_discovery_ceredential_alias`. Make note of the alias name to use it for configuring the **Basic Auth** credentials.|
        |Type|From the list, select **Credential**.|
        |ID|The **ID** field is populated automatically when submitting the form. Make note of the alias ID to use it for configuring the parameters for the **EMC PMAX phase1** pattern. For example: `powermax_credential_alias_id`.|

    5.  Select **Submit**.
-   **Verify the configuration of the __Basic Auth__ credentials**

    Configure the **Basic Auth** credentials to enable the connection to the PowerMax REST API. For the procedure, see [Create Basic Auth credentials](../concept/c_DiscoveryConfigurationConsole.md#).

    Fill in the form.

    |Field|Description|
    |-----|-----------|
    |Name|Fill in a unique name for the credentials. For example: `powermax_discovery_basic_auth_ceredentials`.|
    |User name|Fill in the user name that can access the PowerMax. The user should have minimum read-only permissions.|
    |Password|Fill in the password that can access the PowerMax.|

-   **Verify the configuration of a Serverless Discovery schedule**

    Make sure to select `Serverless` in the **Discover** field. For information about the procedure, see: [Schedule a horizontal discovery](../task/t_CreateADiscoverySchedule.md)

-   **Associate the __EMC PMAX Phase1__ and __EMC PMAX Phase2__ patterns with the Serverless Discovery schedule**
    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Select the schedule that you configured.
    3.  Select the **Serverless Execution Patterns** tab.
    4.  Verify that the **Run Child Patterns** field is set to **true**.
    5.  Select **New**.
    6.  Fill in the fields in the form as follows:

        |Parameter|Description|
        |---------|-----------|
        |IP Address \[emc\_ip\_address\]|The IP Address of the Navisphere, which serves as the EMC Management Console capable of managing multiple storages.|
        |Alias \[credential\_alias\]|The Alias ID that is configured for the EMC PowerMax credentials. For example: `powermax_credential_alias_id`.|

    7.  Select **Submit**.

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the **EMC PowerMAX** Patterns.

<table id="table_w2j_l53_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The user-assigned identifier or label for a specific storage array or component within the system.

</td></tr><tr><td>

Model ID \[model\_id\]

</td><td>

The particular variant or model of the storage array.

</td></tr><tr><td>

Serial Number \[serial\_number\]

</td><td>

The serial number that uniquely identifies each individual storage array unit.

</td></tr><tr><td>

OS \[os\]

</td><td>

The operating system environment hosted on the storage array. For example, embedded management software or operating systems.

</td></tr><tr><td>

OS Version \[os\_version\]

</td><td>

The software version that's installed on the storage array, which includes the core operating system and management software.

</td></tr><tr><td>

Firmware Version \[firmware \_version\]

</td><td>

The software embedded in the hardware components of the storage array, including controllers, drives, and other subsystems.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

The company responsible for designing, producing, and supporting the PowerMax storage array which is Dell EMC.

</td></tr><tr><td>

Physical Capacity \(GB\) \[physical\_capacity\]

</td><td>

The maximum physical capacity that can be utilized for storing data or other content, measured in gigabytes \(GB\).

</td></tr><tr><td>

Used Physical Capacity \(GB\) \[used\_physical\_capacity\]

</td><td>

Amount of physical storage space currently allocated and utilized within the PowerMax system, measured in GB. It indicates how much of the available physical storage resources are actively storing data or other content.

</td></tr><tr><td>

Free Physical Capacity \(GB\) \[free\_physical\_capacity\]

</td><td>

Available physical storage space within the PowerMax system, measured in GB.

</td></tr><tr><td>

Virtual Capacity \(GB\) \[virtual\_capacity\]

</td><td>

Total virtual storage capacity provisioned within the PowerMax system, measured in GB.

</td></tr><tr><td>

Free Virtual Capacity \(GB\) \[free\_virtual\_capacity\]

</td><td>

Available virtual storage capacity within the PowerMax system, measured in GB.

</td></tr><tr><td>

Used Virtual Capacity \(GB\) \[used\_virtual\_capcity\]

</td><td>

Used virtual storage capacity within the PowerMax system, measured in GB.

</td></tr></tbody>
</table><table id="table_rqt_ppx_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The cluster node name.

</td></tr><tr><td>

Cluster \[cluster\]

</td><td>

The host group associated with this cluster node in the PowerMax environment.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

The manufacturer name, which is Dell EMC.

</td></tr></tbody>
</table><table id="table_zrg_jqx_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The storage cluster name.

</td></tr><tr><td>

Correlation ID \[correlation\_id\]

</td><td>

Combines the cluster name and the storage's serial number to create a unique identifier.

</td></tr></tbody>
</table><table id="table_ek2_mqx_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The combination of asset and asset tag.

</td></tr><tr><td>

Assigned \[assigned\]

</td><td>

The availability status.

</td></tr><tr><td>

Asset \[asset\]

</td><td>

The director slot number.

</td></tr><tr><td>

Asset Tag \[asset\_tag\]

</td><td>

The director number.

</td></tr><tr><td>

Device ID \[device\_id\]

</td><td>

A unique label for the controller.

</td></tr><tr><td>

Short Description \[short\_description\]

</td><td>

The director slot and number.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

The manufacturer name, which is Dell EMC.

</td></tr></tbody>
</table><table id="table_ezv_zqx_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

WWPN \[wwpn\]

</td><td>

The World Wide Port Name \(WWPN\) of the storage port.

</td></tr><tr><td>

Name \[name\]

</td><td>

The port identifier.

</td></tr><tr><td>

PO Number \[po\_number\]

</td><td>

The port number.

</td></tr><tr><td>

State \[state\]

</td><td>

The port status.

</td></tr><tr><td>

Speed \[speed\]

</td><td>

The port transmission speed.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

The manufacturer name, which is Dell EMC.

</td></tr><tr><td>

Short Description \[short\_description\]

</td><td>

A list of the port IP addresses.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

The connected IP address.

</td></tr></tbody>
</table><table id="table_uhb_t5x_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The World Wide Name \(WWN\) unique identifier.

</td></tr><tr><td>

State \[state\]

</td><td>

The current operational status of the volume. For example: **Write Disabled** or **Ready**.

</td></tr><tr><td>

Size \[size\]

</td><td>

The capacity in Gigabytes \(GB\).

</td></tr></tbody>
</table><table id="table_gzd_fvx_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The Spindle ID.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

The disk manufacturer.

</td></tr><tr><td>

Model ID \[model\_id\]

</td><td>

The disk model.

</td></tr><tr><td>

Size \[size\]

</td><td>

The disk capacity in Gigabytes \(GB\).

</td></tr><tr><td>

Device ID \[device\_id\]

</td><td>

The combination of the storage system serial number with the disk name that uniquely identifies each disk within the PowerMax environment.

</td></tr></tbody>
</table><table id="table_usm_5vx_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Export ID \[export\_id\]

</td><td>

The Fibre Channel identifier.

</td></tr><tr><td>

Initiator WWPN \[initiator\_wwpn\]

</td><td>

A unique identifier combining the Director ID, Port Number, and Initiator ID.

</td></tr><tr><td>

PO Number \[po\_number\]

</td><td>

The port number.

</td></tr><tr><td>

Assigned to \[assigned\_to\]

</td><td>

The specific host assigned to the export and manages the Fibre Channel connection.

</td></tr><tr><td>

Attributes \[attributes\]

</td><td>

The director ID that identifies the specific director responsible for managing the Fibre Channel exports.

</td></tr><tr><td>

Name \[name\]

</td><td>

The initiator ID.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

The manufacturer name, which is Dell EMC.

</td></tr><tr><td>

Lun \[lun\]

</td><td>

The Logical Unit Number \(LUN\) that is connected within PowerMax systems, indicating the specific storage unit allocated for the Fibre Channel export.

</td></tr><tr><td>

Asset Tag \[asset\_tag\]

</td><td>

A combination of the Director ID with the Port Number that uniquely identifies the asset within the Fibre Channel exports.

</td></tr></tbody>
</table><table id="table_ngr_ys1_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Export ID \[export\_id\]

</td><td>

The unique identifier for an iSCSI export within PowerMax systems, facilitating the management and tracking of iSCSI connections.

</td></tr><tr><td>

Initiator WWPN \[initiator\_wwpn\]

</td><td>

A combination of the Director ID, Port Number, and Initiator ID that forms a unique identifier for the initiator within the iSCSI exports.

</td></tr><tr><td>

Name \[name\]

</td><td>

The Initiator ID in PowerMax systems, serving as a unique identifier for the initiator in the context of iSCSI exports.

</td></tr><tr><td>

PO Number \[po\_number\]

</td><td>

The port number identifying the specific port used for the iSCSI export.

</td></tr><tr><td>

Attributes \[attributes\]

</td><td>

The Director ID, which identifies the specific director responsible for managing the iSCSI export.

</td></tr><tr><td>

Assigned to \[assigned\_to\]

</td><td>

The host assigned to the iSCSI export within the PowerMax environment and specifies the particular host system that is connected to the export.

</td></tr></tbody>
</table><table id="table_dyj_nt1_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The name of the pool.

</td></tr></tbody>
</table>## CI relationships

Discovery creates these relationships to support the PowerMax discovery with the **EMC PMAX phase2** pattern.

<table id="table_jtg_dtm_pu832"><thead><tr><th>

CI

</th><th>

Relationship Type

</th><th>

CI

</th></tr></thead><tbody><tr><td>

cmdb\_ci\_disk

</td><td>

Contains::Contained by

</td><td>

cmdb\_ci\_storage\_server

</td></tr><tr><td>

cmdb\_ci\_fc\_export

</td><td>

Allocated from::Allocated to

</td><td>

cmdb\_ci\_storage\_volume

</td></tr><tr><td>

cmdb\_ci\_fc\_export

</td><td>

Exports to::Imports from

</td><td>

cmdb\_ci\_storage\_cluster\_node

</td></tr><tr><td>

cmdb\_ci\_isci\_export

</td><td>

Hosted::Hosts

</td><td>

cmdb\_ci\_storage\_server

</td></tr><tr><td>

cmdb\_ci\_isci\_export

</td><td>

Allocated from::Allocated to

</td><td>

cmdb\_ci\_storage\_volume

</td></tr><tr><td>

cmdb\_ci\_isci\_export

</td><td>

Exports to::Imports from

</td><td>

cmdb\_ci\_storage\_cluster\_node

</td></tr><tr><td>

cmdb\_ci\_storage\_cluster\_node

</td><td>

Cluster of::Cluster

</td><td>

cmdb\_ci\_storage\_cluster

</td></tr><tr><td>

cmdb\_ci\_storage\_controller

</td><td>

Contains::Contained By

</td><td>

cmdb\_ci\_storage\_server

</td></tr><tr><td>

cmdb\_ci\_storage\_controller

</td><td>

Contains::Contained By

</td><td>

cmdb\_ci\_storage\_port

</td></tr><tr><td>

cmdb\_ci\_storage\_port

</td><td>

Owns::Owned by

</td><td>

cmdb\_ci\_fc\_export

</td></tr><tr><td>

cmdb\_ci\_storage\_port

</td><td>

Owns::Owned by

</td><td>

cmdb\_ci\_isci\_export

</td></tr><tr><td>

cmdb\_ci\_storage\_port

</td><td>

Owns::Owned by

</td><td>

cmdb\_ci\_isci\_export

</td></tr><tr><td>

cmdb\_ci\_storage\_port

</td><td>

Owns::Owned by

</td><td>

cmdb\_ci\_fc\_export

</td></tr><tr><td>

cmdb\_ci\_storage\_server

</td><td>

Owns::Owned by

</td><td>

cmdb\_ci\_storage\_port

</td></tr><tr><td>

cmdb\_ci\_storage\_server

</td><td>

Runs on::Runs

</td><td>

cmdb\_ci\_storage\_cluster

</td></tr><tr><td>

cmdb\_ci\_storage\_server

</td><td>

Allocated from::Allocated to

</td><td>

cmdb\_ci\_storage\_cluster\_node

</td></tr><tr><td>

cmdb\_ci\_storage\_server

</td><td>

Contains::Contained By

</td><td>

cmdb\_ci\_storage\_pool

</td></tr></tbody>
</table>**Parent Topic:**[Available discovery patterns](../../service-mapping/concept/available-patterns.md)

