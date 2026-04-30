---
title: Dell Data Domain storage discovery using Patterns
description: Discovery and Service Mapping use the Dell EMC Data Domain serverless pattern to find the Data Domain storage systems registered in the Data Domain Management Center \(DDMC\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Dell Data Domain storage discovery using Patterns

Discovery and Service Mapping use the **Dell EMC Data Domain** serverless pattern to find the Data Domain storage systems registered in the Data Domain Management Center \(DDMC\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To learn about Data Domain components and their versions that you can discover, refer to [Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md)

## Prerequisites

-   **Verify that the applications are up to date**

    Discovery and Service Mapping Patterns

    CMDB CI Class Models

-   **Verify the creation of the credential alias**

    role: DDMC admin.

    1.  Set the scope to: **Global**.
    2.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.
    3.  Select **New**.
    4.  Fill in the fields in the form.

        |Field|Description|
        |-----|-----------|
        |Name|Enter a unique name for the alias. For example: `ddmc_discovery_ceredential_alias`. Make note of the alias name to use it for configuring the **Basic Auth** credentials.|
        |Type|From the list, select **Credential**.|
        |ID|The **ID** field is populated automatically when submitting the form. Make note of the alias ID to use it for configuring the parameters for the **Dell EMC Data Domain** pattern. For example: `ddmc_credential_alias_id`.|

    5.  Select **Submit**.

-   **Verify the configuration of the __Basic Auth__ credentials**

    role: DDMC admin.

    **Note:** To run discovery with Patterns, you can create only one credential per one alias.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.
    2.  In the list, search for the alias unique name and open the record.
    3.  From the list, select **Basic Auth** Credentials.
    4.  Fill in the fields in the form.

        |Field|Description|
        |-----|-----------|
        |Name|Fill in a unique name for the credentials. For example: `ddmc_discovery_basic_auth_ceredentials`.|
        |User name|Fill in the user name that can access the DDMC. This user is created in the DDMC. The user should have minimum read-only permissions. Alternatively, fill in the REST API interface for the DDMC.|
        |Password|Fill in the password that can access the DDMC. This password is created in the DDMC.|
        |Active|Enabled by default.|
        |Credential alias|If you entered the form through the alias, you don't need to configure this field.|

    5.  Select **Submit**.

-   **Verify the configuration of a Serverless Discovery schedule**

    role: Discovery\_admin.

    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Select **New**.
    3.  Fill in the fields in the form.

        |Field|Description|
        |-----|-----------|
        |Name|Fill in the name of your choice.|
        |Discover|In the list, select `Serverless`.|
        |MID Server|Select the search button to open the list of MID Servers and select the MID Server that has network access to the DDMC.|
        |Active|Enabled by default.|
        |Credential alias|No need to configure this field.|

        For more information about setting the **Max run time**, **Run**, and **Time** fields, see: [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md)

    4.  Select **Submit**.

-   **Associate the __Dell EMC Data Domain__ pattern with the Serverless Discovery schedule**

    role: Discovery\_admin.

    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Select the schedule that you configured.
    3.  Select the **Serverless Execution Patterns** tab.
    4.  Select **New**.
    5.  Fill in the fields in the form.

        |Field|Description|
        |-----|-----------|
        |Name|Fill in the name of your choice. For example: `dell_emc_data_domain_serverless_discovery`|
        |Pattern|Select the search button to open the list of patterns, and select the **Dell EMC Data Domain** pattern.|
        |Proxy Host|No need to configure this field.|
        |Extended Parameters|No need to configure this field.|

    6.  Select **Submit**.

-   **Configure the parameters for the __Dell EMC Data Domain__ pattern**

    role: Discovery\_admin.

    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Select the schedule that you configured.
    3.  Select the **Serverless Execution Pattern** tab.
    4.  Select the record created for the **Dell EMC Data Domain** pattern.
    5.  In the **Discovery Pattern Launcher parameters** tab, set the value for the fields as follows:

<table id="table_u15_q41_ybc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Credential Alias

</td><td>

Fill in the alias ID configured for DDMC. You can find the alias in the **Connection &amp; Credential Aliases** list. For example: `ddmc_credential_alias_id`.

</td></tr><tr><td>

DDMC Port

</td><td>

\(Optional\) by default the pattern uses port 3009.

</td></tr><tr><td>

DDMC IP Address

</td><td>

Fill in the host name or the IP Address of the DDMC. These details can be provided by the DDMC Admin.

 For example: `101.10.10.101` or `ddmc.demo.local`.

</td></tr></tbody>
</table>    6.  To run the discovery, you can select **Discover now** from the **Related Links** or wait for the run time.

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the **Dell EMC Data Domain** Patterns.

<table id="table_w2j_l53_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The unique identifier of the storage server. The name is typically the Domain Name System \(DNS\) hostname or the computer name, which corresponds to the **host\_name** attribute.

</td></tr><tr><td>

Host Name \[host\_name\]

</td><td>

The DNS hostname of the Data Domain system. The host that is used to register the system with the Data Domain Management Center \(DDMC\).

</td></tr><tr><td>

FQDN \[fqdn\]

</td><td>

The Fully Qualified Domain Name of the Data Domain system. The complete domain name used to register the system with the DDMC.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

The IP address of the Data Domain storage server. The name is the specific IP address used to register the Data Domain system with the DDMC.

</td></tr><tr><td>

OS Version \[os\_version\]

</td><td>

The version of the operating system running on the Data Domain system. The versions supported are from DD OS 7.3.

</td></tr><tr><td>

Model \[model\]

</td><td>

The specific model of the Data Domain \(DD\) system. For example, the name for the DD Virtual Edition \(VE\) is **DELL EMC DD VE**.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

The manufacturer is Dell EMC.

</td></tr><tr><td>

Serial Number \[serial\_number\]

</td><td>

The unique serial number assigned to the DD system.

</td></tr><tr><td>

Operating System \[os\]

</td><td>

The Data Domain OS is: **DD OS**.

</td></tr></tbody>
</table><table id="table_zrg_jqx_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The name of the DDMC associated with the storage cluster.

</td></tr><tr><td>

Cluster ID \[cluster\_id\]

</td><td>

The universally unique identifier \(UUID\) of the DDMC, which uniquely identifies the cluster.

</td></tr><tr><td>

Cluster Version \[cluster\_version\]

</td><td>

The software version of the DDMC that is currently installed on the cluster.

</td></tr><tr><td>

Serial Number \[serial\_number\]

</td><td>

The unique serial number assigned to the Virtual Data Domain Management Center \(VDDMC\) system.

</td></tr><tr><td>

Model ID \[model\_id\]

</td><td>

The specific model of the Data Domain system in use. For the DDMC, the model ID is 'DELL EMC DD Management Center'.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

The manufacturer is Dell EMC.

</td></tr></tbody>
</table><table id="table_gzd_fvx_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The name assigned to the disk device within the storage system.

</td></tr><tr><td>

Device ID \[device\_id\]

</td><td>

The unique identifier for the disk device, which is the same as the device name.

</td></tr><tr><td>

Model ID \[model\_id\]

</td><td>

The model of the disk device. For example: **VMware Virtual\_disk**.

</td></tr><tr><td>

Size \[size\]

</td><td>

The capacity of the disk device, measured in gigabytes \(GB\).

</td></tr></tbody>
</table>The Disk Shelf Chassis database is populated only for physical DD systems that support disk expansion shelves.

<table id="table_clw_w3f_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The name of the disk expansion shelf.

</td></tr><tr><td>

Serial Number \[serial\_number\]

</td><td>

The unique serial number of the disk expansion shelf.

</td></tr></tbody>
</table><table id="table_yfg_pjf_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Serial Number \[serial\_number\]

</td><td>

The unique serial number of the Dell EMC Data Domain storage system, as registered in the DDMC.

</td></tr><tr><td>

Serial Number Type \[serial\_number\_type\]

</td><td>

The format of the serial number for the Dell EMC Data Domain storage system, indicating whether it's a system serial number or a Universally Unique Identifier \(UUID\).

</td></tr><tr><td>

Valid \[valid\]

</td><td>

The validity of the data, with a value of **true** confirming that the serial number has been successfully verified.

</td></tr></tbody>
</table><table id="table_kr2_wjf_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The identifier or label of the network adapter, such as **eth1**.

</td></tr></tbody>
</table>The DDMC REST API doesn’t provide the MAC address of network adapters. As a result, the MAC address field for network adapters remains empty.

<table id="table_n1r_ckf_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP Address \[ip\_address\]

</td><td>

The IP address that is assigned to the device.

</td></tr><tr><td>

Netmask \[netmask\]

</td><td>

The netmask associated with the IP address, defining the subnet to which the IP address belongs.

</td></tr></tbody>
</table>## CI relationships

Discovery and Service Mapping Patterns create these relationships to support the Data Domain discovery.

<table id="table_jtg_dtm_pu832"><thead><tr><th>

CI

</th><th>

Relationship Type

</th><th>

CI

</th></tr></thead><tbody><tr><td>

cmdb\_ci\_storage\_server

</td><td>

Managed by::Manages

</td><td>

cmdb\_ci\_storage\_cluster

</td></tr><tr><td>

cmdb\_ci\_storage\_server

</td><td>

Contains::Contained By

</td><td>

cmdb\_ci\_disk

</td></tr><tr><td>

cmdb\_ci\_disk\_shelf\_chassis

</td><td>

Hosted on:: hosts

</td><td>

cmdb\_ci\_storage\_server

</td></tr><tr><td>

cmdb\_ci\_serial\_number

</td><td>

reference

</td><td>

cmdb\_ci\_storage\_server

</td></tr><tr><td>

cmdb\_ci\_storage\_server

</td><td>

Owns::Owned by

</td><td>

cmdb\_ci\_network\_adapter

</td></tr><tr><td>

cmdb\_ci\_storage\_server

</td><td>

Owns::Owned by

</td><td>

cmdb\_ci\_ip \_address

</td></tr></tbody>
</table>**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

