---
title: Rubrik Cluster discovery
description: Discovery uses multiple patterns to find all Rubrik cluster data. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/rubrik-discovery.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 18
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Rubrik Cluster discovery

Discovery uses multiple patterns to find all Rubrik cluster data. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

All of the information for the main CI \(Rubrik Cluster\) and its corresponding CI types is returned by REST API calls.

Take note of the following limitations:

-   Reference fields aren't supported due to the Large Payload mechanism limitations in the Paris and Quebec releases.
-   All the entities returned from the Rubrik REST API for Hosts \(Servers\) with IP addresses not resolved to hostnames are filtered out \(excluded\) from the Rubrik discovery. This is done to prevent the creation of duplicates across the CMDB.

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
    -   Visibility Content
-   **Configure Basic Auth permissions**

    Configure Basic Auth credentials for a user with Read-Only Administrator role in Rubrik, and create a credential alias. For more information, see [Create a basic authentication credential alias for Rubrik discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-rubrik.md).

-   **Verify MID Server can access target**

    Verify that the MID Server can access the target appliance device.

-   **Create a serverless discovery schedule**

    Create a serverless discovery schedule to perform targeted discovery of Rubrik cluster resources. For more information, see [Create a serverless discovery schedule for Rubrik cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-rubrik.md).


## Data collected by Discovery during horizontal discovery

-   **Resources discovered by the Rubrik AIX Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the host.|
    |Host name \[host\_name\]|Host name of the host.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Operating System \[os\]|Operating system type configured on the host.|
    |OS Version \[os\_version\]|Operating system version, edition, or distribution configured on the host.|
    |Operational status \[operational\_status\]|Current operational status of the host.|

-   **Resources discovered by the Rubrik Cluster \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Cluster ID \[cluster\_id\]|Unique ID of the Rubrik cluster.|
    |Name \[name\]|Name of the Rubrik cluster.|
    |Cluster Version \[cluster\_version\]|Current version of the Rubrik cluster.|
    |API Version \[api\_version\]|API version of the Rubrik cluster.|
    |Timezone \[timezone\]|Timezone used by the Rubrik cluster.|

    The Dependency Views map shows discovered cluster resources and the relationships between them.

    \[Omitted image "Rubrik-cluster-dependency.jpg"\] Alt text: Rubrik cluster dependency view

-   **Resources discovered by the Rubrik EC2 Instance \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|ID of the EC2 instance in the AWS context.|
    |Name \[name\]|Name of the EC2 instance in the AWS context.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Effective SLA domain \[effective\_sla\_domain\]|ID of the Rubrik SLA Domain.|
    |Effective SLA domain name \[effective\_sla\_domain\_name\]|Name of the Rubrik SLA Domain.|
    |Account ID \[account\_id\]|ID of the AWS account associated with the EC2 instance.|
    |Account name \[account\_name\]|Name of the AWS account associated with the EC2 instance.|
    |Instance ID \[instance\_id\]|ID of the EC2 instance in the AWS context.|
    |Instance name \[instance\_name\]|Name of the EC2 instance in the AWS context.|
    |Instance type \[instance\_type\]|Template type of the EC2 instance.|
    |Region \[region\]|Geographical region where the EC2 instance is located, in the AWS context.|

    The Dependency Views map shows discovered EC2 instances and the relationships between them.

    \[Omitted image "rubrik-ec2-dependency.jpg"\] Alt text: Rubrik EC2 dependency view

-   **Resources discovered by the Rubrik Fileset \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|ID of the Rubrik Fileset.|
    |Name \[name\]|Name of the Rubrik Fileset.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Effective SLA domain \[effective\_sla\_domain\]|ID of the Rubrik SLA Domain.|
    |Effective SLA domain name \[effective\_sla\_domain\_name\]|Name of the Rubrik SLA Domain.|
    |Host ID \[host\_id\]|ID of the host associated with the Rubrik Fileset.|
    |Template ID \[template\_id\]|ID of the Rubrik Fileset Template from which the Rubrik Fileset defines resources.|
    |Share ID \[share\_id\]|ID of the Rubrik Share owning the Rubrik Fileset.|

    The Dependency Views map shows discovered filesets and the relationships between them.

    \[Omitted image "Rubrik-fileset-dependency.jpg"\] Alt text: Rubrik fileset dependency view

-   **Resources discovered by the Rubrik Fileset Template \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|ID of the Rubrik Fileset Template.|
    |Name \[name\]|Name of the Rubrik Fileset Template.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Share count \[share\_count\]|Number of shares associated with the Rubrik Fileset Template.|
    |Share type \[share\_type\]|Type of shares associated with the Rubrik Fileset Template.|
    |Host count \[host\_count\]|Number of hosts associated with the Rubrik Fileset Template.|
    |OS type \[os\_type\]|Operating system type associated with the Rubrik Fileset Template.|

    The Dependency Views map shows discovered fileset templates and the relationships between them.

    \[Omitted image "Rubrik-fileset-template-dependency.jpg"\] Alt text: Rubrik fileset template dependency view

-   **Resources discovered by the Rubrik Hyper-V Instance \(LP\) pattern**

    **Note:** Discovery of Hyper-V instances only updates existing CIs. This is due to a limitation in the Rubrik REST API not returning the GUID \(object\_id\) of the Hyper-V instance. If there is no match between the data from the REST API and the CMDB, no CIs are updated. In addition, when there is no match, the Rubrik Hyper-V Instance \(LP\) pattern completes in an 'Error' state, which is expected behavior.

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the Hyper-V instance.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Effective SLA domain \[effective\_sla\_domain\]|ID of the Rubrik SLA Domain.|
    |Effective SLA domain name \[effective\_sla\_domain\_name\]|Name of the Rubrik SLA Domain.|
    |Host ID \[host\_id\]|ID of the host associated with the Hyper-V instance.|

    The Dependency Views map shows discovered Hyper-V instances and the relationships between them.

    \[Omitted image "Rubrik-hyperV-dependency.jpg"\] Alt text: Rubrik Hyper-V dependency view

-   **Resources discovered by the Rubrik Linux Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the host.|
    |Host name \[host\_name\]|Host name of the host.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Operating System \[os\]|Operating system type configured on the host.|
    |OS Version \[os\_version\]|Operating system version, edition, or distribution configured on the host.|
    |Operational status \[operational\_status\]|Current operational status of the host.|

    The Dependency Views map shows discovered hosts and the relationships between them.

    \[Omitted image "rubrik-linux-host-dependency.jpg"\] Alt text: Rubrik Linux Host dependency view

-   **Resources discovered by the Rubrik Managed Volume \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|ID of the managed storage volume.|
    |Volume ID \[volume\_id\]|Volume ID of the managed storage volume.|
    |Name \[name\]|Name of the managed storage volume.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Effective SLA domain \[effective\_sla\_domain\]|ID of the Rubrik SLA Domain.|
    |Effective SLA domain name \[effective\_sla\_domain\_name\]|Name of the Rubrik SLA Domain.|
    |Size bytes \[size\_bytes\]|Total capacity size in bytes of the storage volume.|
    |Used Size bytes \[used\_size\_bytes\]|Total used capacity size in bytes.|
    |Snapshot count \[snapshot\_count\]|Snapshot count of the managed storage volume.|
    |Share type \[share\_type\]|Share type of the managed storage volume.|
    |State \[state\]|State of the managed storage volume.|

    The Dependency Views map shows discovered managed storage instances and the relationships between them.

    \[Omitted image "Rubrik-managed-volume-dependency.jpg"\] Alt text: Rubrik managed volume dependency view

-   **Resources discovered by the Rubrik MS SQL DB \(LP\) pattern**

    **Note:** Relationships between MS SQL instances hosted on Windows clusters and the associated MS SQL databases are not supported from the 1.0.79 release onwards of the Discovery and Service Mapping Patterns application. This is due to insufficient information returned from the Rubrik REST API for Windows clusters. The MS SQL Instances and MS SQL databases associated to Windows clusters are filtered out from the Rubrik discovery associated patterns.

    |Field|Description|
    |-----|-----------|
    |Data Base \[database\]|ID of the MS SQL database.|
    |Name \[name\]|Name of the MS SQL database.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Effective SLA domain \[effective\_sla\_domain\]|ID of the Rubrik SLA Domain.|
    |Effective SLA domain name \[effective\_sla\_domain\_name\]|Name of the Rubrik SLA Domain.|
    |Host ID \[host\_id\]|ID of the host where the MS SQL database is running.|
    |Instance ID \[instance\_id\]|ID of the database instance associated with the MS SQL database.|
    |State \[state\]|State of the MS SQL database.|
    |Recovery model \[recovery\_model\]|Recovery model type of the MS SQL database.|
    |Last Snapshot \[last\_snapshot\]|Last snapshot of the MS SQL database, in the format YY-MM-DD HH-MM-SS.|
    |Missed Snapshot count \[missed\_snapshot\_count\]|Missed snapshot count of the MS SQL database.|

    The Dependency Views map shows discovered MS SQL DBs and the relationships between them.

    \[Omitted image "Rubrik-mssql-db-dependency.jpg"\] Alt text: Rubrik MS SQL dependency view

-   **Resources discovered by the Rubrik MS SQL Instance \(LP\) pattern**

    **Note:** Relationships between MS SQL instances hosted on Windows clusters and the associated MS SQL databases are not supported from the 1.0.79 release onwards of the Discovery and Service Mapping Patterns application. This is due to insufficient information returned from the Rubrik REST API for Windows clusters. The MS SQL Instances and MS SQL databases associated to Windows clusters are filtered out from the Rubrik discovery associated patterns.

    |Field|Description|
    |-----|-----------|
    |Instance Name \[instance\_name\]|ID of the MS SQL instance.|
    |Name \[name\]|Name of the MS SQL instance.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Host ID \[host\_id\]|ID of the host associated with the MS SQL instance.|
    |Version \[version\]|Version of the MS SQL instance.|

    The Dependency Views map shows discovered MS SQL instances and the relationships between them.

    \[Omitted image "Rubrik-mssql-instance-dependency.jpg"\] Alt text: Rubrik MS SQL instances dependency view

-   **Resources discovered by the Rubrik NAS Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the host.|
    |Host name \[host\_name\]|Host name of the host.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Description \[short\_description\]|Vendor type of the NAS storage.|
    |Operational status \[operational\_status\]|Current operational status of the host.|

    The Dependency Views map shows discovered hosts and the relationships between them.

    \[Omitted image "rubrik-nas-dependency.png"\] Alt text: Rubrik host dependency view

-   **Resources discovered by the Rubrik Node \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Brik ID \[brik\_id\]|Chassis ID of the Rubrik node.|
    |Name \[name\]|Unique name of the Rubrik node, serving as the ID of the Rubrik node.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Unavailable disks \[unavailable\_disks\]|Indicates whether any disks on the Rubrik node are unavailable. The value is true or false.|
    |IP Address \[ip\_address\]|IP address of the Rubrik node associated with the Rubrik cluster.|
    |Tunnel enabled \[tunnel\_enabled\]|Indicates whether tunneling is enabled for the Rubrik node. The value is true or false.|
    |CPU core count \[cpu\_core\_count\]|Number of CPU cores on the Rubrik node.|
    |RAM \(MB\) \[ram\]|Amount of RAM in MB allocated for the Rubrik node.|

    |Field|Description|
    |-----|-----------|
    |Node Name \[node\_name\]|Name of the Rubrik node associated with the disk.|
    |Device ID \[device\_id\]|ID of the Rubrik node disk, concatenated with the Rubrik node name in the format `ID@NODE_NAME`.|
    |Name \[name\]|Name of the disk associated with the Rubrik node, in the format `NODE_NAME@DISK_ID@DISK_TYPE`.|
    |Size bytes \[size\_bytes\]|Total capacity size in bytes.|
    |Unallocated size bytes \[unallocated\_size\_bytes\]|Total unallocated capacity size in bytes.|
    |Usable size bytes \[usable\_size\_bytes\]|Total available capacity size in bytes.|
    |Storage type \[storage\_type\]|Type of the storage disk: SSD or HDD.|
    |Storage path \[storage\_path\]|Location path of the storage disk.|
    |Operational status \[operational\_status\]|Operational status of the storage disk.|

    The Dependency Views map shows discovered nodes and node disks, and the relationships between them.

    \[Omitted image "rubrik-node-dependency.jpg"\] Alt text: Rubrik node dependency view

    \[Omitted image "rubrik-node-disk-dependency.jpg"\] Alt text: Rubrik node disk dependency view

-   **Resources discovered by the Rubrik Nutanix Instance \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|ID of the Nutanix VM instance.|
    |VM Instance ID \[vm\_inst\_id\]|ID of the Nutanix VM instance.|
    |Name \[name\]|Name of the Nutanix VM instance.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Effective SLA domain \[effective\_sla\_domain\]|ID of the Rubrik SLA Domain.|
    |Effective SLA domain name \[effective\_sla\_domain\_name\]|Name of the Rubrik SLA Domain.|
    |VM Cluster ID \[vm\_cluster\_id\]|ID of the cluster to which the Nutanix VM instance belongs.|
    |VM Cluster name \[vm\_cluster\_name\]|Name of the cluster to which the Nutanix VM instance belongs.|
    |OS type \[os\_type\]|Operating system type configured on the Nutanix VM instance.|

    The Dependency Views map shows discovered Nutanix instances and the relationships between them.

    \[Omitted image "Rubrik-nutanix-dependency.jpg"\] Alt text: Rubrik Nutanix dependency view

-   **Resources discovered by the Rubrik Oracle DB \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |SID \[sid\]|Oracle system ID of the database.|
    |Name \[name\]|ID of the Oracle database in the Rubrik context.|
    |DB Name \[database\_name\]|Name of the Oracle database.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Effective SLA domain \[effective\_sla\_domain\]|ID of the Rubrik SLA Domain.|
    |Effective SLA domain name \[effective\_sla\_domain\_name\]|Name of the Rubrik SLA Domain.|
    |RAC\_ID \[rac\_id\]|ID of the Oracle RAC \(Real Application Cluster\) to which the database belongs.|
    |Host ID \[host\_id\]|ID of the host where the Oracle database is running.|
    |Instance \[instance\]|Oracle instance ID managing the database data.|
    |Instance count \[instance\_count\]|Number of Oracle instances managing the database data.|
    |Last Snapshot \[last\_snapshot\]|Last snapshot of the Oracle database, in the format YY-MM-DD HH-MM-SS.|
    |Missed Snapshot count \[missed\_snapshot\_count\]|Missed snapshot count of the Oracle database.|
    |Tablespaces count \[tablespaces\_count\]|Number of logical storage units associated with the Oracle database.|

    The Dependency Views map shows discovered Oracle DBs and the relationships between them.

    \[Omitted image "Rubrik-oracle-db-dependency.jpg"\] Alt text: Rubrik Oracle DB dependency view

-   **Resources discovered by the Rubrik Oracle RAC \(Real Application Cluster\) \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|ID of the Rubrik Oracle RAC.|
    |Name \[name\]|Name of the Rubrik Oracle RAC.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |DB count \[db\_count\]|Number of databases associated with the Rubrik Oracle RAC.|
    |Node count \[node\_count\]|Number of nodes participating in the Rubrik Oracle RAC.|
    |State \[state\]|State of the Rubrik Oracle RAC.|

    The Dependency Views map shows discovered Oracle RACs and the relationships between them.

    \[Omitted image "Rubrik-oracle-rac-dependency.jpg"\] Alt text: Rubrik Oracle RAC dependency view

-   **Resources discovered by the Rubrik Share \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|ID of the host share.|
    |Path \[path\]|Export point of the host share.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Host ID \[host\_id\]|ID of the host associated with the host share.|
    |Share type \[share\_type\]|Share type of the host share.|
    |Vendor type \[vendor\_type\]|Vendor type of the host share.|

    The Dependency Views map shows discovered host shares and the relationships between them.

    \[Omitted image "Rubrik-share-view-dependency.jpg"\] Alt text: Rubrik host share dependency view

-   **Resources discovered by the Rubrik SLA Domain \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|ID of the Rubrik SLA domain policy.|
    |Name \[name\]|Name of the Rubrik SLA domain policy.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Max Local Retention limit \[max\_local\_retention\_limit\]|Maximum local retention limit of the SLA domain policy.|

    The Dependency Views map shows discovered SLA domains and the relationships between them.

    \[Omitted image "Rubrik-sla-domain-dependency.jpg"\] Alt text: Rubrik SLA domain dependency view

-   **Resources discovered by the Rubrik Solaris Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the host.|
    |Host name \[host\_name\]|Host name of the host.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Operating System \[os\]|Operating system type configured on the host.|
    |OS Version \[os\_version\]|Operating system version, edition, or distribution configured on the host.|
    |Operational status \[operational\_status\]|Current operational status of the host.|

-   **Resources discovered by the Rubrik VMware Instance \(LP\) pattern**

    **Note:** Discovery of VMware instances only updates existing CIs. This is because the regular vCenter discovery does not use the IRE \(Identification and Reconciliation Engine\) and the Rubrik VMware pattern will create duplicates. If there is no match between the data from the REST API and the CMDB, no CIs are updated. In addition, when there is no match, the Rubrik VMware Instance \(LP\) pattern completes in an 'Error' state, which is expected behavior.

    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|ID of the VMware instance.|
    |Name \[name\]|Name of the VMware instance.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Effective SLA domain \[effective\_sla\_domain\]|ID of the Rubrik SLA Domain.|
    |Effective SLA domain name \[effective\_sla\_domain\_name\]|Name of the Rubrik SLA Domain.|
    |Host ID \[host\_id\]|ID of the VMware host.|
    |Host name \[host\_name\]|Name of the VMware host.|
    |VM Cluster name \[vm\_cluster\_name\]|Name of the cluster to which the virtual machine instance belongs.|
    |IP Address \[ip\_address\]|IP address of the VMware instance, if assigned.|
    |Guest OS Name \[guest\_os\_fullname\]|Guest operating system type.|
    |State \[state\]|State of the VMware instance.|

    The Dependency Views map shows discovered VMware instances and the relationships between them.

    \[Omitted image "Rubrik-vmware-dependency.jpg"\] Alt text: Rubrik VMware instances dependency view

-   **Resources discovered by the Rubrik Volume Group \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|ID of the volume group.|
    |Volume ID \[volume\_id\]|Volume ID of the volume group.|
    |Name \[name\]|Name of the volume group.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Effective SLA domain \[effective\_sla\_domain\]|ID of the Rubrik SLA Domain.|
    |Effective SLA domain name \[effective\_sla\_domain\_name\]|Name of the Rubrik SLA Domain.|
    |Host ID \[host\_id\]|ID of the host associated with the volume group.|

    The Dependency Views map shows discovered volume groups and the relationships between them.

    \[Omitted image "Rubrik-volume-group-dependency.jpg"\] Alt text: Rubrik volume group dependency view

-   **Resources discovered by the Rubrik Windows Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the host.|
    |Host name \[host\_name\]|Host name of the host.|
    |Cluster ID \[cluster\_id\]|ID of the Rubrik cluster.|
    |Cluster Name \[cluster\_name\]|Name of the Rubrik cluster.|
    |Operating System \[os\]|Operating system type configured on the host.|
    |OS Version \[os\_version\]|Operating system version, edition, or distribution configured on the host.|
    |Operational status \[operational\_status\]|Current operational status of the host.|

    The Dependency Views map shows discovered hosts and the relationships between them.

    \[Omitted image "rubrik-windows-host-dependency.jpg"\] Alt text: Rubrik Windows Host dependency view


## CI relationships

-   **Relationships discovered using the Rubrik AIX Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |AIX Server \[cmdb\_ci\_aix\_server\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|

-   **Relationships discovered using the Rubrik EC2 Instance \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Rubrik Virtual Machine Instance \[cmdb\_ci\_rubrik\_vm\_instance\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |Rubrik Virtual Machine Instance \[cmdb\_ci\_rubrik\_vm\_instance\]|Protected by::Protects|Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|

-   **Relationships discovered using the Rubrik Fileset \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Server \[cmdb\_ci\_server\]|Owns::Owned by|Rubrik Fileset \[cmdb\_ci\_rubrik\_fileset\]|
    |Storage File Share \[cmdb\_ci\_storage\_fileshare\]|Owns::Owned by|Rubrik Fileset \[cmdb\_ci\_rubrik\_fileset\]|
    |Rubrik Fileset Template \[cmdb\_ci\_rubrik\_fileset\_template\]|Defines resources for::Gets resources from|Rubrik Fileset \[cmdb\_ci\_rubrik\_fileset\]|
    |Rubrik Fileset \[cmdb\_ci\_rubrik\_fileset\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |Rubrik Fileset \[cmdb\_ci\_rubrik\_fileset\]|Protected by::Protects|Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |NAS Storage \[cmdb\_ci\_nas\_storage\]|Owns::Owned by|Rubrik Fileset \[cmdb\_ci\_rubrik\_fileset\]|

-   **Relationships discovered using the Rubrik Fileset Template \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Rubrik Fileset Template \[cmdb\_ci\_rubrik\_fileset\_template\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|

-   **Relationships discovered using the Rubrik Hyper-V Instance \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Hyper-V Virtual Machine Instance \[cmdb\_ci\_hyper\_v\_instance\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |Hyper-V Virtual Machine Instance \[cmdb\_ci\_hyper\_v\_instance\]|Protected by::Protects|Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|

-   **Relationships discovered using the Rubrik Linux Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Linux Server \[cmdb\_ci\_linux\_server\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|

-   **Relationships discovered using the Rubrik Managed Volume \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Storage Volume \[cmdb\_ci\_storage\_volume\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |Storage Volume \[cmdb\_ci\_storage\_volume\]|Protected by::Protects|Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|

-   **Relationships discovered using the Rubrik MS SQL DB \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |MS SQL DataBase \[cmdb\_ci\_db\_mssql\_database\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |MS SQL DataBase \[cmdb\_ci\_db\_mssql\_database\]|Protected by::Protects|Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |MSFT SQL Instance \[cmdb\_ci\_db\_mssql\_instance\]|Contains::Contained by|MS SQL DataBase \[cmdb\_ci\_db\_mssql\_database\]|

-   **Relationships discovered using the Rubrik MS SQL Instance \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |MSFT SQL Instance \[cmdb\_ci\_db\_mssql\_instance\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |MSFT SQL Instance \[cmdb\_ci\_db\_mssql\_instance\]|Runs on::Runs|Server \[cmdb\_ci\_server\]|

-   **Relationships discovered using the Rubrik NAS Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |NAS Storage \[cmdb\_ci\_nas\_storage\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|

-   **Relationships discovered using the Rubrik Node \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Rubrik Node \[cmdb\_ci\_rubrik\_node\]|Cluster of::Cluster|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |Rubrik Node \[cmdb\_ci\_rubrik\_node\]|Uses::Used by|Rubrik Node Disk \[cmdb\_ci\_rubrik\_node\_disk\]|

-   **Relationships discovered using the Rubrik Nutanix Instance \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]|Protected by::Protects|Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|

-   **Relationships discovered using the Rubrik Oracle DB \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|Protected by::Protects|Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|Runs on::Runs|Server \[cmdb\_ci\_server\]|
    |Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|Cluster of::Cluster|Rubrik Oracle RAC \[cmdb\_ci\_rubrik\_db\_ora\_rac\]|

-   **Relationships discovered using the Rubrik Oracle RAC \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Rubrik Oracle RAC \[cmdb\_ci\_rubrik\_db\_ora\_rac\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|

-   **Relationships discovered using the Rubrik Share \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Storage File Share \[cmdb\_ci\_storage\_fileshare\]|Managed by::Manages|NAS Storage \[cmdb\_ci\_nas\_storage\]|
    |Storage File Share \[cmdb\_ci\_storage\_fileshare\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|

-   **Relationships discovered using the Rubrik SLA Domain \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|

-   **Relationships discovered using the Rubrik Solaris Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Solaris Server \[cmdb\_ci\_solaris\_server\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|

-   **Relationships discovered using the Rubrik VMware Instance \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |VMware Virtual Machine Instance \[cmdb\_ci\_vmware\_instance\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |VMware Virtual Machine Instance \[cmdb\_ci\_vmware\_instance\]|Protected by::Protects|Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|

-   **Relationships discovered using the Rubrik Volume Group \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Rubrik Volume Group \[cmdb\_ci\_rubrik\_volume\_group\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |Rubrik Volume Group \[cmdb\_ci\_rubrik\_volume\_group\]|Protected by::Protects|Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |Server \[cmdb\_ci\_server\]|Owns::Owned by|Rubrik Volume Group \[cmdb\_ci\_rubrik\_volume\_group\]|

-   **Relationships discovered using the Rubrik Windows Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Windows Server \[cmdb\_ci\_win\_server\]|Managed by::Manages|Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|


-   **[Create a basic authentication credential alias for Rubrik discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-rubrik.md)**  
Create an alias and add it to a basic authentication credential to discover Rubrik clusters.
-   **[Create a serverless discovery schedule for Rubrik cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-rubrik.md)**  
Set up a dedicated discovery schedule for each Rubrik cluster \(Brik\) to identify cluster resources using a serverless pattern and credential alias.

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

