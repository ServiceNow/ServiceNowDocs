---
title: Data collected for Oracle Cloud Discovery
description: ServiceNow Discovery uses the Oracle Cloud Infrastructure \(OCI\) discovery patterns to provide real-time elasticity for enterprise applications by combining Oracle autonomous services, integrated security, and cloud compute. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-11-09"
reading_time_minutes: 6
keywords: [Patterns]
breadcrumb: [Cloud resource discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Data collected for Oracle Cloud Discovery

ServiceNow Discovery uses the Oracle Cloud Infrastructure \(OCI\) discovery patterns to provide real-time elasticity for enterprise applications by combining Oracle autonomous services, integrated security, and cloud compute. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Starting with version 1.29.0, Discovery and Service Mapping Patterns supports the discovery of OCI GovCloud accounts.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the following applications are installed**

    Verify that the following applications are installed and up to date:

    -   Cloud Access Interface \(starting from version 1.0.0\)
    -   Visibility Content
    -   CMDB CI Class Models
    -   Discovery and Service Mapping Patterns
-   **Configure Oracle API credentials**

    Ensure that your OCI credentials are configured and that your private and public keys are converted to the RSA format. For more information, see [Create Oracle API credentials](../../it-operations-management/task/create-oracle-api-credentials.md).

-   **Create OCI service account**

    For more information, see [Create OCI service accounts](../../it-operations-management/task/create-oci-service-accounts.md).

-   **Create a cloud discovery schedule**

    To run a cloud discovery at scale, see [Create an OCI Discovery schedule in Discovery Admin Workspace](../../discovery/task/create-oci-schedule-DAW.md).

    Create a discovery schedule to run LDCs on.

    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Click the **Cloud Discovery** button.
    3.  In the **Provider** field, select **OCI**. Fill in the form to create a new account or select an existing one. For more information, see [Create OCI service accounts](../../it-operations-management/task/create-oci-service-accounts.md).
    4.  On the **Select Datacenters** page, filter which LDCs you want to run the discovery.
    5.  Under the **Discover Virtual Machines \(optional\)** page, select if you want to run VM OS Discovery.
    6.  When you're finished, navigate to the **Create Schedule** page and select the **Finish and Run** button.
-   **\(Optional\) Populate Service Account and Logical Datacenter fields in cloud CIs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating Service Account and Logical Datacenter fields directly in cloud CIs. For more information, see [Improved query performance with direct field population in CI tables](../concept/query-service-account-ldc-fields.md).


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Data collected by Discovery during horizontal discovery

The discovered Oracle configuration data includes the following table and fields.

|Field|Description|
|-----|-----------|
|Cloud Database \(cmdb\_ci\_cloud\_database\)|
|name|The name of the database.|
|object\_id|Unique identifier of the database.|
|operational\_status|Operational status of the database.|
|vendor|The vendor, **Oracle**.|
|type|The Oracle database type.|
|version|Version of the database.|
|state|State of the database.|
|comments|The attribute is issued for the delete strategy.|
|install\_status|Install status.|
|Image​ \(cmdb\_ci\_os\_template\)|
|name|The image name.|
|object\_id|Unique identifier of the image.|
|version|The version of the guest OS.|
|guest\_os|The name of the guest OS.|
|Service Account \(cmdb\_ci\_cloud\_service\_account\)|
|name|The account name.|
|datacenter\_type|Datacenter type.|
|account\_id|Unique identifier of the account.|
|object\_id|Unique identifier of the account \(same value as the account id\).|
|discovery\_credentials|The credentials related to the service account.|
|is\_master\_account|**true** when it is the root compartment. **false** when it is not the root compartment.|
|Network \(cmdb\_ci\_network\)|
|name|The network name.|
|object\_id|Unique identifier of the network.|
|cidr|The cidr of the network.|
|domain\_name|The domain name.|
|state|The state of the network.|
|NIC \(cmdb\_ci\_nic\)|
|name|The NIC name.|
|object\_id|Unique identifier of the NIC.|
|public\_ip|The public IP address.|
|mac\_address|The MAC address.|
|primary|Set **true**/**false** according to the setup.|
|private\_ip|The private ip address.|
|state|The state of the NIC.|
|Storage Volume \(cmdb\_ci\_storage\_volume\)|
|name|The name of the storage volume.|
|object\_id|Unique identifier of storage volume.|
|state|The state of the storage volume.|
|volume\_id|Unique identifier of the storage volume \(same value as the account id\).|
|size|The storage volume size.|
|size\_bytes|The storage volume size in bytes.|
|Subnet \(cmdb\_ci\_cloud\_subnet\)|
|name|The name of the subnet.|
|object\_id|Unique identifier of subnet.|
|cidr|The cidr of the subnet.|
|domain\_name|The domain name.|
|state|The state of the subnet.|
|Virtual Machine \(cmdb\_ci\_vm\_instance\)|
|name|The VM name.|
|object\_id|Unique identifier of VM.|
|state|The state of the VM.|
|memory|Memory size.|
|cpus|Number of CPUs.|

Tags are populated to the **cmdb\_key\_value** table and related to the relevant cmdb ci resource. In order to support it, the extension sections were created for the following resources:

-   Autonomous DB
-   Exadata DB
-   Image
-   Network
-   NIC
-   Storage Volume
-   Account
-   Subnet
-   Virtual Machine

## CI Relationships

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_oci\_datacenter|Contains::Contained by|cmdb\_ci\_availablity\_zone|

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_vm\_instance|Use End Point To::Use End Point From|cmdb\_ci\_endpoint\_block|
|cmdb\_ci\_endpoint\_block|Implement End Point To::Implement End Point From|cmdb\_ci\_storage\_volume|

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_oci\_datacenter|Contains::Contained by|cmdb\_ci\_availability\_zone|

**Note:** When configuring a Cloud Discovery scheduler for part of the LDCs, the Oracle OCI - Fault Domain \(LP\) pattern will not trigger.

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_os\_template|Hosted on::Hosts|cmdb\_ci\_oci\_datacenter|

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_oci\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_network|Hosted on::Hosts|cmdb\_ci\_oci\_datacenter|

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_vm\_instance|Use End Point To::Use End Point From|cmdb\_ci\_endpoint\_subnet|
|cmdb\_ci\_vm\_instance|Use End Point To::Use End Point From|cmdb\_ci\_endpoint\_vnic|
|cmdb\_ci\_endpoint\_vnic|Implement End Point To::Implement End Point From|cmdb\_ci\_nic|
|cmdb\_ci\_cloud\_subnet|Implement End Point To::Implement End Point From|cmdb\_ci\_endpoint\_subnet|

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_nic|Hosted on::Hosts|cmdb\_ci\_oci\_datacenter|

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_availablity\_zone|Contains::Contained by|cmdb\_ci\_storage\_volume|
|cmdb\_ci\_storage\_volume|Hosted on::Hosts|cmdb\_ci\_oci\_datacenter|

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_network|Contains::Contained by|cmdb\_ci\_cloud\_subnet|

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_vm\_instance|Hosted on::Hosts|cmdb\_ci\_oci\_datacenter|
|cmdb\_ci\_vm\_instance|Provisioned From::Provisioned|cmdb\_ci\_os\_template|
|cmdb\_ci\_vm\_instance|Provisioned From:Provisioned|cmdb\_ci\_compute\_template|
|cmdb\_ci\_vm\_instance|DR provided by::Provides DR for|cmdb\_ci\_avaliability\_zone|
|cmdb\_ci\_avaliability\_zone|Contains::Contained by|cmdb\_ci\_vm\_instance|

**Parent Topic:**[Cloud resource discovery](../../discovery/reference/cloud-discovery-collected-data.md)

