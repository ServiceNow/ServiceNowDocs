---
title: Rubrik Cluster discovery
description: Discovery uses multiple patterns to find all Rubrik cluster data. Discovering these resources requires installing the Discovery and Service Mapping Patterns and the CMDB CI Class Models applications from the ServiceNow Store, as each application is dependent on the other.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 19
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Rubrik Cluster discovery

Discovery uses multiple patterns to find all Rubrik cluster data. Discovering these resources requires installing the Discovery and Service Mapping Patterns and the CMDB CI Class Models applications from the ServiceNow Store, as each application is dependent on the other.

You can use the patterns for discovering the Rubrik components on the ServiceNow AI Platform using the Paris release or later.

**Note:** The update applied in version 1.0.78 of the Discovery and Service Mapping Patterns application resolves an issue of duplicate CI types in the CMDB. If you are using Rubrik discovery patterns and already installed versions 1.21.0, 1.23.0, 1.24.0 or 1.25.0 of the CMDB CI Class Models store app \(sn\_cmdb\_ci\_class\), or versions 1.0.73, 1.0.74, 1.0.75 or 1.0.76 of the Discovery and Service Mapping Patterns application \(sn\_itom\_pattern\), you should follow the instructions in [KB0957523](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0957523).

All of the information for the main CI \(Rubrik Cluster\) and its corresponding CI types is returned by​ REST API calls.

Take note of the following limitations:

-   Reference fields are not supported due to the Large Payload mechanism limitations in the Paris and Quebec releases.
-   All the entities returned from the Rubrik REST API for Hosts \(Servers\) with IP addresses not resolved to hostnames are filtered out \(excluded\) from the Rubrik discovery. This is done to prevent the creation of duplicates across the CMDB.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Discovery and Service Mapping Patterns store app**

    Deploy the 1.0.73 release or later from the ServiceNow Store.

-   **CMDB CI Class Models store app**

    Deploy the 1.21.0 release or later from the ServiceNow Store.

-   **Basic Auth permissions**

    Ensure Basic Auth credentials are configured for authenticating the REST API calls.

    Credential aliases associated with the Rubrik credentials of type Basic Auth must also be created. These aliases serve as input parameters, along with the IP address.

    These are used for discovery of all the CI types associated with the Rubrik cluster.

    -   Security Scheme Type: HTTP
    -   HTTP Authorization Scheme: basic
-   **MID server**

    Ensure that the MID server can access the target appliance device.

-   **Create a serverless discovery schedule**

    Create a serverless discovery schedule to perform targeted discovery of Rubrik cluster resources.

    **Note:** The Discovery schedule that triggers all the Rubrik related patterns supports only the serverless discovery type. In addition, for each different Rubrik cluster \(Brik\), a different serverless discovery schedule should be created. The schedule should include the IP address of any of the Rubrik nodes associated with the Rubrik cluster, and the credential alias associated with the Rubrik Basic Authentication credential record.

    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Click **New** and then fill in the form.

<table id="table_ut3_sby_hhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the Discovery schedule. For example, `Discover Rubrik`.

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
    4.  Navigate to **Connections &amp; Credential Aliases** and create a new Credential record type. In the Credentials related list form, create a new Basic Auth credential record type.

        ![Rubrik credentials](../image/Rubrik-credentials.png)

        **Note:** The credential alias can be associated with existing credentials. When creating a credential record you can also associate to it the credential alias. Click the **Credential alias** padlock icon in the Connections &amp; Credential Aliases record type you created above, and associate as required.

        ![Rubrik credentials](../image/Rubrik-credentials-alias.png)

    5.  Click the **Serverless Execution Patterns** tab.

        ![Rubrik serverless discovery](../image/Rubrik-serverless.jpg)

    6.  Ensure the Run Child Patterns column for the Rubrik discovery pattern is set to **true**. This triggers all the child patterns associated with the Rubrik discovery pattern. This is needed due to the Large Payload \(LP\) mechanism, used for discovery of the Rubrik cluster and all corresponding CI types.
    7.  Under **Discovery Pattern Launcher Parameters**, set the **credential\_alias** and **ip\_address** parameters, which serve as input parameters for triggering the Discovery schedule and the associated Rubrik discovery pattern.

        Set the **ip\_address** with one of the IP addresses of any of the Rubrik nodes associated with the Rubrik cluster. Set the **credential\_alias** with the ID of the Credential record type created in **Connections &amp; Credential Aliases**, which is related with the Rubrik credential Basic Auth record type.

        ![Rubrik IP address parameter](../image/rubrik-serverless-ip.png)


## Data collected by Discovery during horizontal discovery

-   **Resources discovered by the Rubrik AIX Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik AIX Host \[cmdb\_ci\_aix\_server\]|
    |name|The name of the host.|
    |host\_name|The host name of the host.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |os|The operating system type configured on the host.​|
    |os\_version|The operating system version, edition or distribution configured on the host.|
    |operational\_status|The current operational status of the host.​|

-   **Resources discovered by the Rubrik Cluster \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Cluster \[cmdb\_ci\_rubrik\_cluster\]|
    |cluster\_id|Unique ID of the Rubrik cluster.|
    |name|The name of the Rubrik cluster.|
    |cluster\_version|The current version of the Rubrik cluster.|
    |api\_version|The API version of the Rubrik cluster.|
    |timezone|The timezone used by the Rubrik cluster.|

    The Dependency Views map shows discovered cluster resources and the relationships between them.

    ![Rubrik cluster dependency view](../image/Rubrik-cluster-dependency.jpg)

-   **Resources discovered by the Rubrik EC2 Instance \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik EC2 Instance \[cmdb\_ci\_rubrik\_vm\_instance\]|
    |object\_id|The ID of the EC2 instance in the Rubrik context.|
    |name|The name of the EC2 instance in the AWS context.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |effective\_sla\_domain|The ID of the Rubrik SLA Domain.​|
    |effective\_sla\_domain\_name|The name of the Rubrik SLA Domain. See also: \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |account\_id|The ID of the AWS account associated with the EC2 instance.​|
    |account\_name|The name of the AWS account associated with the EC2 instance.​|
    |instance\_id|The ID of the EC2 instance in the AWS context.|
    |instance\_name|The name of the EC2 instance in the Rubrik context.​|
    |instance\_type|The template type of the EC2 instance.​|
    |region|The geographical region where the EC2 instance is located, in the AWS context.|

    The Dependency Views map shows discovered EC2 instances and the relationships between them.

    ![Rubrik EC2 dependency view](../image/rubrik-ec2-dependency.jpg)

-   **Resources discovered by the Rubrik Fileset \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Fileset \[cmdb\_ci\_rubrik\_fileset\]|
    |object\_id|The ID of the Rubrik Fileset.|
    |name|The name of the Rubrik Fileset.|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |effective\_sla\_domain|The ID of the Rubrik SLA Domain.​|
    |effective\_sla\_domain\_name|The name of the Rubrik SLA Domain. See also: \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |host\_id|The ID of the host with which the Rubrik Fileset is associated.​|
    |template\_id|The ID of the Rubrik Fileset Template, where the Rubrik Fileset defines resources from.​|
    |share\_id|The ID of the Rubrik Share owning the Rubrik Fileset.|

    The Dependency Views map shows discovered filesets and the relationships between them.

    ![Rubrik fileset dependency view](../image/Rubrik-fileset-dependency.jpg)

-   **Resources discovered by the Rubrik Fileset Template \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Fileset Template \[cmdb\_ci\_rubrik\_fileset\_template\]|
    |object\_id|The ID of the Rubrik Fileset Template.|
    |name|The name of the Rubrik Fileset Template.|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |share\_count|The count of shares associated with the Rubrik Fileset Template.​|
    |share\_type|The type of shares associated with the Rubrik Fileset Template.|
    |host\_count|The host count associated with the Rubrik Fileset Template.|
    |os\_type|The operating system type associated with the Rubrik Fileset Template.|

    The Dependency Views map shows discovered fileset templates and the relationships between them.

    ![Rubrik fileset template dependency view](../image/Rubrik-fileset-template-dependency.jpg)

-   **Resources discovered by the Rubrik Hyper-V Instance \(LP\) pattern**

    **Note:** Discovery of Hyper-V instances only updates existing CIs. This is due to a limitation in the Rubrik REST API not returning the GUID \(object\_id\) of the Hyper-V instance. If there is no match between the data from the REST API and the CMDB, no CIs are updated. In addition, when there is no match, the Rubrik Hyper-V Instance \(LP\) pattern completes in an ‘Error’ state, which is expected behavior.

    |Field|Description|
    |-----|-----------|
    |Rubrik Hyper-V Instance \[cmdb\_ci\_hyper\_v\_instance\]|
    |name|The name of the Hyper-V instance.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |effective\_sla\_domain|The ID of the Rubrik SLA Domain.​|
    |effective\_sla\_domain\_name|The name of the Rubrik SLA Domain. See also: \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |host\_id|The ID of the host to which the Hyper-V instance is associated.​|

    The Dependency Views map shows discovered Hyper-V instances and the relationships between them.

    ![Rubrik Hyper-V dependency view](../image/Rubrik-hyperV-dependency.jpg)

-   **Resources discovered by the Rubrik Linux Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Linux Host \[cmdb\_ci\_linux\_server\]|
    |name|The name of the host.|
    |host\_name|The host name of the host.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |os|The operating system type configured on the host.​|
    |os\_version|The operating system version, edition or distribution configured on the host.|
    |operational\_status|The current operational status of the host.​|

    The Dependency Views map shows discovered hosts and the relationships between them.

    ![Rubrik Linux Host dependency view](../image/rubrik-linux-host-dependency.jpg)

-   **Resources discovered by the Rubrik Managed Volume \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Managed Volume \[cmdb\_ci\_storage\_volume\]|
    |object\_id|The ID of the managed storage volume.|
    |volume\_id|The volume ID of the managed storage volume.|
    |name|The name of the managed storage volume.|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |effective\_sla\_domain|The ID of the Rubrik SLA Domain.​|
    |effective\_sla\_domain\_name|The name of the Rubrik SLA Domain. See also: \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |size\_bytes|The total capacity size in bytes of the storage volume.​|
    |used\_size\_bytes|The total used capacity size in bytes.|
    |snapshot\_count|The snapshot count of the managed storage volume.​|
    |share\_type|The shared type of the managed storage volume.|
    |state|The state of the managed storage volume.|

    The Dependency Views map shows discovered managed storage instances and the relationships between them.

    ![Rubrik managed volume dependency view](../image/Rubrik-managed-volume-dependency.jpg)

-   **Resources discovered by the Rubrik MS SQL DB \(LP\) pattern**

    **Note:** Relationships between MS SQL instances hosted on Windows clusters and the associated MS SQL databases are not supported from the 1.0.79 release onwards of the Discovery and Service Mapping Patterns application. This is due to insufficient information returned from the Rubrik REST API for Windows clusters. The MS SQL Instances and MS SQL databases associated to Windows clusters are filtered out from the Rubrik discovery associated patterns.

    |Field|Description|
    |-----|-----------|
    |Rubrik MS SQL DB \[cmdb\_ci\_db\_mssql\_database\]|
    |database|The ID of the MS SQL database.|
    |name|The name of the MS SQL database.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |effective\_sla\_domain|The ID of the Rubrik SLA Domain.​|
    |effective\_sla\_domain\_name|The name of the Rubrik SLA Domain. See also: \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |host\_id|The ID of the host where the MS SQL database is running.|
    |instance\_id|The ID of the database instance, to which the MS SQL database is associated.​|
    |state|The state of the MS SQL database.​|
    |recovery\_model|The recovery model type of the MS SQL database.|
    |last\_snapshot|The last snapshot of the MS SQL database, in the format YY-MM-DD HH-MM-SS.|
    |missed\_snapshot\_count|The missed snapshot count of the MS SQL database.​ ​ ​|

    The Dependency Views map shows discovered MS SQL DBs and the relationships between them.

    ![Rubrik MS SQL dependency view](../image/Rubrik-mssql-db-dependency.jpg)

-   **Resources discovered by the Rubrik MS SQL Instance \(LP\) pattern**

    **Note:** Relationships between MS SQL instances hosted on Windows clusters and the associated MS SQL databases are not supported from the 1.0.79 release onwards of the Discovery and Service Mapping Patterns application. This is due to insufficient information returned from the Rubrik REST API for Windows clusters. The MS SQL Instances and MS SQL databases associated to Windows clusters are filtered out from the Rubrik discovery associated patterns.

    |Field|Description|
    |-----|-----------|
    |Rubrik MS SQL Instance \[cmdb\_ci\_db\_mssql\_instance\]|
    |instance\_name|The ID of the MS SQL instance.​|
    |name|The name of the MS SQL instance.|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |host\_id|The ID of the host with which the MS SQL instance is associated.​|
    |version|The version of the MS SQL instance.|

    The Dependency Views map shows discovered MS SQL instances and the relationships between them.

    ![Rubrik MS SQL instances dependency view](../image/Rubrik-mssql-instance-dependency.jpg)

-   **Resources discovered by the Rubrik NAS Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik NAS Host \[cmdb\_ci\_nas\_storage\]|
    |name|The name of the host.|
    |host\_name|The host name of the host.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |short\_description|The vendor type of the NAS storage.​|
    |operational\_status|The current operational status of the host.​|

    The Dependency Views map shows discovered hosts and the relationships between them.

    ![Rubrik host dependency view](../image/rubrik-nas-dependency.png)

-   **Resources discovered by the Rubrik Node \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Node \[cmdb\_ci\_rubrik\_node\]|
    |brik\_id|The Chassis ID of the Rubrik node.|
    |name|The unique name of the Rubrik node, serving as the ID of the Rubrik node.|
    |cluster\_id|The ID of the Rubrik cluster.|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |unavailable\_disks|True / False. Indicates any unavailable disks on the Rubrik node,|
    |ip\_address|The IP address of the Rubrik node associated with the Rubrik cluster.|
    |tunnel\_enabled|True / False. Indicates if tunneling is enabled for the Rubrik node.|
    |cpu\_core\_count|The CPU cores count of the Rubrik node.|
    |ram|The amount of RAM memory \(in MB\) allocated for the Rubrik node.|
    |\[cmdb\_ci\_rubrik\_node\_disk\]|
    |node\_name|The name of the Rubrik node to which the disk is associated.|
    |device\_id|The ID of the Rubrik node disk, concatenated with the Rubrik node name in the format `ID@NODE_NAME`.|
    |name|The name of the disk associated with the Rubrik node. The name includes the concatenation of the Rubrik node name, the ID of the disk and the type of the disk, in the format `NODE_NAME@DISK_ID@DISK_TYPE`.|
    |size\_bytes|The total capacity size in bytes.​|
    |unallocated\_size\_bytes|The total unallocated capacity size in bytes.​|
    |usable\_size\_bytes|The total available capacity size in bytes.|
    |storage\_type|The type of the storage disk: SSD or HDD.|
    |storage\_path|The location path of the storage disk.​|
    |operational\_status|The operational status of the storage disk.​|

    The Dependency Views map shows discovered nodes and node disks, and the relationships between them.

    ![Rubrik node dependency view](../image/rubrik-node-dependency.jpg)

    ![Rubrik node disk dependency view](../image/rubrik-node-disk-dependency.jpg)

-   **Resources discovered by the Rubrik Nutanix Instance \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Nutanix Instance \[cmdb\_ci\_nutanix\_vm\_instance\]|
    |object\_id|The ID of the Nutanix VM instance.|
    |vm\_inst\_id|The ID of the Nutanix VM instance.|
    |name|The name of the Nutanix VM instance.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |effective\_sla\_domain|The ID of the Rubrik SLA Domain.​|
    |effective\_sla\_domain\_name|The name of the Rubrik SLA Domain. See also: \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |vm\_cluster\_id|The cluster ID to which the Nutanix VM instance belongs.|
    |vm\_cluster\_name|The cluster name to which the Nutanix VM instance belongs.|
    |os\_type|The operating system type configured on the Nutanix VM instance.​ ​|

    The Dependency Views map shows discovered Nutanix instances and the relationships between them.

    ![Rubrik Nutanix dependency view](../image/Rubrik-nutanix-dependency.jpg)

-   **Resources discovered by the Rubrik Oracle DB \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Oracle DB \[cmdb\_ci\_db\_ora\_instance\]|
    |sid|The Oracle system ID of the database.​|
    |name|The ID of the Oracle database in the Rubrik context.|
    |database\_name|The name of the Oracle database.|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |effective\_sla\_domain|The ID of the Rubrik SLA Domain.​|
    |effective\_sla\_domain\_name|The name of the Rubrik SLA Domain. See also: \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |rac\_id|The ID of the Oracle RAC \(Real Application Cluster\), to which the database is part of.​|
    |host\_id|The ID of the host, where the Oracle database is running.​|
    |instance|The Oracle instance ID managing the database associated data.|
    |Instance\_count|The Oracle instances count managing the database associated data.​|
    |last\_snapshot|The last snapshot of the Oracle database, in the format YY-MM-DD HH-MM-SS.|
    |missed\_snapshot\_count|The missed snapshot count of the Oracle database.​|
    |tablespaces\_count|The count of the logical storage units associated with the Oracle database.|

    The Dependency Views map shows discovered Oracle DBs and the relationships between them.

    ![Rubrik Oracle DB dependency view](../image/Rubrik-oracle-db-dependency.jpg)

-   **Resources discovered by the Rubrik Oracle RAC \(Real Application Cluster\) \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Oracle RAC \[cmdb\_ci\_rubrik\_db\_ora\_rac\]|
    |object\_id|The ID of the Rubrik Oracle RAC.​|
    |name|The name of the Rubrik Oracle RAC.|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |db\_count|The count of databases associated with the Rubrik Oracle RAC.|
    |node\_count|The count of the nodes participating in the Rubrik Oracle RAC.|
    |state|The state of the Rubrik Oracle RAC.​|

    The Dependency Views map shows discovered Oracle RACs and the relationships between them.

    ![Rubrik Oracle RAC dependency view](../image/Rubrik-oracle-rac-dependency.jpg)

-   **Resources discovered by the Rubrik Share \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Share \[cmdb\_ci\_storage\_fileshare\]|
    |name|The ID of the host share.|
    |path|The export point of the host share.|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |host\_id|The ID of the host with which the host share is associated.​|
    |share\_type|The share type of the host share.​|
    |vendor\_type|The vendor type of the host share.​|
    |status|The current state of the host share.​|

    The Dependency Views map shows discovered host shares and the relationships between them.

    ![Rubrik host share dependency view](../image/Rubrik-share-view-dependency.jpg)

-   **Resources discovered by the Rubrik SLA Domain \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik SLA Domain \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |object\_id|The ID of the Rubrik SLA domain policy.​|
    |name|The name of the Rubrik SLA domain policy.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |max\_local\_retention\_limit|The maximum local retention limit of the SLA domain policy.​|

    The Dependency Views map shows discovered SLA domains and the relationships between them.

    ![Rubrik SLA domain dependency view](../image/Rubrik-sla-domain-dependency.jpg)

-   **Resources discovered by the Rubrik Solaris Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Solaris Host \[cmdb\_ci\_solaris\_server\]|
    |name|The name of the host.|
    |host\_name|The host name of the host.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |os|The operating system type configured on the host.​|
    |os\_version|The operating system version, edition or distribution configured on the host.|
    |operational\_status|The current operational status of the host.​|

-   **Resources discovered by the Rubrik VMware Instance \(LP\) pattern**

    **Note:** Discovery of VMware instances only updates existing CIs. This is because the regular vCenter discovery does not use the IRE \(Identification and Reconciliation Engine\) and the Rubrik VMware pattern will create duplicates. If there is no match between the data from the REST API and the CMDB, no CIs are updated. In addition, when there is no match, the Rubrik VMware Instance \(LP\) pattern completes in an ‘Error’ state, which is expected behavior.

    |Field|Description|
    |-----|-----------|
    |Rubrik VMware Instance \[cmdb\_ci\_vmware\_instance\]|
    |object\_id|The ID of the VMware instance.|
    |name|The name of the VMware instance.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |effective\_sla\_domain|The ID of the Rubrik SLA Domain.​|
    |effective\_sla\_domain\_name|The name of the Rubrik SLA Domain. See also: \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |host\_id|The ID of the VMware host.​|
    |host\_name|The name of the VMware host.​|
    |vm\_cluster\_name|The cluster name to which the virtual machine instance belongs.​|
    |ip\_address|The IP address of the VMware instance, if assigned.​|
    |guest\_os\_fullname|The guest operating system type.​|
    |state|The state of the VMware instance.​|

    The Dependency Views map shows discovered VMware instances and the relationships between them.

    ![Rubrik VMware instances dependency view](../image/Rubrik-vmware-dependency.jpg)

-   **Resources discovered by the Rubrik Volume Group \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Volume Group \[cmdb\_ci\_rubrik\_volume\_group\]|
    |object\_id|The ID of the volume group.|
    |volume\_id|The volume ID of the volume group.​|
    |name|The name of the volume group.|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |effective\_sla\_domain|The ID of the Rubrik SLA Domain.​|
    |effective\_sla\_domain\_name|The name of the Rubrik SLA Domain. See also: \[cmdb\_ci\_rubrik\_sla\_domain\]|
    |host\_id|The ID of the host with which the volume group is associated.​|

    The Dependency Views map shows discovered volume groups and the relationships between them.

    ![Rubrik volume group dependency view](../image/Rubrik-volume-group-dependency.jpg)

-   **Resources discovered by the Rubrik Windows Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Rubrik Windows Host \[cmdb\_ci\_win\_server\]|
    |name|The name of the host.|
    |host\_name|The host name of the host.​|
    |cluster\_id|The ID of the Rubrik cluster.​|
    |cluster\_name|The name of the Rubrik cluster. See also: \[cmdb\_ci\_rubrik\_cluster\]|
    |os|The operating system type configured on the host.​|
    |os\_version|The operating system version, edition or distribution configured on the host.|
    |operational\_status|The current operational status of the host.​|

    The Dependency Views map shows discovered hosts and the relationships between them.

    ![Rubrik Windows Host dependency view](../image/rubrik-windows-host-dependency.jpg)


## CI relationships

-   **Relationships discovered using the Rubrik AIX Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_aix\_server|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|

-   **Relationships discovered using the Rubrik EC2 Instance \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_rubrik\_vm\_instance|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_rubrik\_vm\_instance|Protected by::Protects|cmdb\_ci\_rubrik\_sla\_domain|

-   **Relationships discovered using the Rubrik Fileset \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_server|Owns::Owned by|cmdb\_ci\_rubrik\_fileset|
    |cmdb\_ci\_storage\_fileshare|Owns::Owned by|cmdb\_ci\_rubrik\_fileset|
    |cmdb\_ci\_rubrik\_fileset\_template|Defines resources for::Gets resources from|cmdb\_ci\_rubrik\_fileset|
    |cmdb\_ci\_rubrik\_fileset|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_rubrik\_fileset|Protected by::Protects|cmdb\_ci\_rubrik\_sla\_domain|
    |cmdb\_ci\_nas\_storage|Owns::Owned by|cmdb\_ci\_rubrik\_fileset|

-   **Relationships discovered using the Rubrik Fileset Template \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_rubrik\_fileset\_template|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|

-   **Relationships discovered using the Rubrik Hyper-V Instance \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_hyper\_v\_instance|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_hyper\_v\_instance|Protected by::Protects|cmdb\_ci\_rubrik\_sla\_domain|

-   **Relationships discovered using the Rubrik Linux Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_linux\_server|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|

-   **Relationships discovered using the Rubrik Managed Volume \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_storage\_volume|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_storage\_volume|Protected by::Protects|cmdb\_ci\_rubrik\_sla\_domain|

-   **Relationships discovered using the Rubrik MS SQL DB \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_db\_mssql\_database|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_db\_mssql\_database|Protected by::Protects|cmdb\_ci\_rubrik\_sla\_domain|
    |cmdb\_ci\_db\_mssql\_instance|Contains::Contained by|cmdb\_ci\_db\_mssql\_database|

-   **Relationships discovered using the Rubrik MS SQL Instance \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_db\_mssql\_instance|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_db\_mssql\_instance|Runs on::Runs|cmdb\_ci\_server|

-   **Relationships discovered using the Rubrik NAS Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_nas\_storage|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|

-   **Relationships discovered using the Rubrik Node \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_rubrik\_node|Cluster of::Cluster|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_rubrik\_node|Uses::Used by|cmdb\_ci\_rubrik\_node\_disk|

-   **Relationships discovered using the Rubrik Nutanix Instance \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_nutanix\_vm\_instance|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_nutanix\_vm\_instance|Protected by::Protects|cmdb\_ci\_rubrik\_sla\_domain|

-   **Relationships discovered using the Rubrik Oracle DB \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_db\_ora\_instance|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_db\_ora\_instance|Protected by::Protects|cmdb\_ci\_rubrik\_sla\_domain|
    |cmdb\_ci\_db\_ora\_instance|Runs on::Runs|cmdb\_ci\_server|
    |cmdb\_ci\_db\_ora\_instance|Cluster of::Cluster|cmdb\_ci\_rubrik\_db\_ora\_rac|

-   **Relationships discovered using the Rubrik Oracle RAC \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_rubrik\_db\_ora\_rac|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|

-   **Relationships discovered using the Rubrik Share \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_storage\_fileshare|Managed by::Manages|cmdb\_ci\_nas\_storage|
    |cmdb\_ci\_storage\_fileshare|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|

-   **Relationships discovered using the Rubrik SLA Domain \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_rubrik\_sla\_domain|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|

-   **Relationships discovered using the Rubrik Solaris Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_solaris\_server|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|

-   **Relationships discovered using the Rubrik VMware Instance \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_vmware\_instance|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_vmware\_instance|Protected by::Protects|cmdb\_ci\_rubrik\_sla\_domain|

-   **Relationships discovered using the Rubrik Volume Group \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_rubrik\_volume\_group|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|
    |cmdb\_ci\_rubrik\_volume\_group|Protected by::Protects|cmdb\_ci\_rubrik\_sla\_domain|
    |cmdb\_ci\_server|Owns::Owned by|cmdb\_ci\_rubrik\_volume\_group|

-   **Relationships discovered using the Rubrik Windows Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_win\_server|Managed by::Manages|cmdb\_ci\_rubrik\_cluster|


**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

