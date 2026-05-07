---
title: Microsoft SQL Server and Cluster discovery
description: The Discovery and Service Mapping Patterns application uses the MSSql DB On Windows pattern to find Microsoft SQL DB servers and clusters on your infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [Pattern, WMI, SQL instance, SQL DB On Windows, SQL Cluster]
breadcrumb: [Database discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Microsoft SQL Server and Cluster discovery

The Discovery and Service Mapping Patterns application uses the MSSql DB On Windows pattern to find Microsoft SQL DB servers and clusters on your infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

For detailed information on SQL Server supported versions see: [Detailed information on products discovered by ITOM Visibility](../../service-mapping/reference/r_SupportedApplications.md)

## Prerequisites

-   **Verify that the following applications are up to date**
    -   Discovery and Service Mapping Patterns starting with version 1.7.0 \(August 2023\)
    -   Visibility Content starting with version 6.12.1 \(August 2023\)
-   **Create Windows credentials**

    After verifying that the MID Server is connected to the target Windows server, create Windows credentials on the ServiceNow AI Platform. For more information, see [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **Create applicative credentials when using SQL authentication**

    For more information, see [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **Verify the configuration of the MID Server**

    Verify that the MID Server has the necessary permissions to read the Windows Registry on a remote mode. The MSSql DB On Windows pattern uses registry values to discover SQL cluster details.

-   **Verify SQL Server discovery report is active**

    Verify that the SQL Server discovery report is active on your server. Discovery uses the SQL Server discovery report to discover Microsoft SQL Server components.

-   **Verify the permissions to run WMI queries**

    Verify remote read-only access to the following WMI namespaces:

    -   `Root\CIMv2`
    -   `Root\Microsoft\SqlServer\ComputerManagement*`
-   **Verify the SQL Server table permissions**

    The MSSql DB On Windows pattern requires read-only permissions to read the following tables:

    -   `@@version`
    -   `sys.configurations`
    -   `sys.dm_exec_sessions`
    -   `sys.dm_os_schedulers`
    -   `SERVERPROPERTY`
-   **Verify availability group table permissions**

    Verify the following table permissions to discover Microsoft SQL Server Always On availability groups:

    -   **VIEW SERVER STATE** access to the `sys.dm_hadr_availability_group_states` table
    -   Read access permission to the following tables:
        -   `sys.availability_groups`
        -   `sys.availability_group_listeners`
        -   `sys.availability_group_listener_ip_addresses`

## SQL failover cluster instance \(FCI\)

Updating the version 1.6.1 set of Patterns available from the ServiceNow® Store starting August 2023 enables an appropriate discovery of the Always On availability group details and the SQL Failover Clusters. When the failover scenario is occurring, the MSSql DB On Windows pattern discovers the failover cluster \(Node 2\). Then a new MSFT SQL instance and databases are created.

![Node 2 is a duplicate of Node 1](../image/sql_cluster_discovery.png)

The following procedure enables appropriate visibility of the SQL clusters.

1.  Set the **sn\_itom\_pattern.discover\_mssql\_cluster.load\_cluster\_name\_from\_registry=true** MID Server property to **true** to enable the **Collect MSSQL Cluster info- MSSQL Cluster** extension section.
2.  Ensure that an `sqlservr.exe` process to trigger the MSSql DB On Windows pattern is running on the server.
3.  Run a CI discovery.

    For more information, see [Running discoveries in your network](../concept/running-discoveries.md).

4.  Either keep duplicate instances and databases or delete them.
    -   To keep the duplicate instances and databases, keep the default configuration.
        -   The install status of the nodes of the passive cluster changes to **Absent**.
        -   The install status of the nodes of the active cluster changes to **Installed**.
    -   To delete the passive instances and databases, set the **discovery.mssql.cluster.instance.postsensor.delete** system property to **True**.

## Microsoft SQL Server Always On availability groups support

Starting from Discovery and Service Mapping Patterns version 1.27.0, the MSSql DB On Windows pattern extension **Collect MSSQL HADR - Availability Group Info** supports the discovery of Microsoft SQL Server Always On availability groups.

The Collect MSSQL HADR - Availability Group Info pattern extension introduces the following CI classes that extend existing CMDB classes:

|CI class|Extends from|
|--------|------------|
|MSSQL Availability Group \[cmdb\_ci\_mssql\_ag\]|Cluster \[cmdb\_ci\_cluster\]|
|MSSQL Availability Group Listener \[cmdb\_ci\_mssql\_ag\_listener\]|Endpoint \[cmdb\_ci\_endpoint\]|
|MSSQL Availability Group Replica \[cmdb\_ci\_mssql\_ag\_replica\]|MSSQL Cluster Node \[cmdb\_ci\_mssql\_cluster\_node\]|

![Collect MSSQL HADR - Availability Group Info pattern extension relationships](../../service-mapping/image/mssql-ag-pattern-model.png "Data model of Collect MSSQL HADR - Availability Group Info")

-   **Prerequisites**

    [Verify availability group table permissions](mssql-data-collected-pattern.md#verify-availability-group-permissions)

-   **Discovered resources**

    [Resources discovered by the pattern extension: Collect MSSQL HADR - Availability Group Info](mssql-data-collected-pattern.md#resources-discovered-mssql-availability-group-pattern)

-   **Discovered relationships**

    [Relationships discovered by the pattern extension: Collect MSSQL HADR - Availability Group Info](mssql-data-collected-pattern.md#table_er3_qss_p2c)


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the MSSql DB On Windows pattern.

-   **MSFT SQL instance \[cmdb\_ci\_db\_mssql\_instance\]**

    The data collected for the running processes of the database \(the actual SQL server\) is referred to as the database instance

<table id="table_MSSQLServerDictionaryEntries"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The field name.

 For example: MSSQLSERVER@windows\_server\_name

</td></tr><tr><td>

Instance Name \[instance\_name\]

</td><td>

The SQL server instance name.

 For example: MSSQLSERVER

</td></tr><tr><td>

Is clustered \[is\_clustered\]

</td><td>

Indicates the type of installation:-   If this value is set to **true**,the SQL server is a part of a cluster, and the failover mechanism is enabled.
-   If this value is set to **false**, the SQL server is a standalone deployment and the failover mechanism is disabled.


</td></tr><tr><td>

Comments \[comments\]

</td><td>

The type of instance: -   standalone\_instance
-   failover\_cluster
-   always\_on


</td></tr><tr><td>

Version \[version\]

</td><td>

The SQL server version number. For example: 16.0.1000.6

</td></tr><tr><td>

Version Name \[version\_name\]

</td><td>

The SQL server version by release dates. For example: The value **2022** represents version **16.0.1000.6**

</td></tr><tr><td>

Service Pack \[service\_pack\]

</td><td>

The service pack version. For example: SP2.

</td></tr><tr><td>

Edition \[edition\]

</td><td>

The type of the edition. For example: Enterprise Edition.

</td></tr><tr><td>

TCP Port \[tcp\_port\]

</td><td>

The TCP port that the MSSQL instance uses to accept connections.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

The install status of the instance:**Installed**- The instance is currently running.

**Absent**- The instance isn’t running and it’s the backup instance for a failover scenario.

</td></tr></tbody>
</table>-   **MSSQL database \[cmdb\_ci\_db\_mssql\_database\]**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the database. For example: msdb.|
    |Install Status \[install\_status\]|The install status of the database.|
    |Instance name \[instance\_name\]|References the MSFT SQL instance​ \[cmdb\_ci\_db\_mssql\_instance\] table.|

-   **MSSQL Cluster Node \[cmdb\_ci\_mssql\_cluster\_node\]**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The server host name|
    |IP Address \[ip\_address\]|The hosting Windows server's IP address|
    |Cluster \[cluster\]|Reference to the SQL cluster record.|
    |Server \[server\]|Reference to the hosting Windows server record.|

-   **MSSQL Cluster \[cmdb\_ci\_mssql\_cluster\]**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The SQL cluster network name​|
    |IP Address \[ip\_address\]|The SQL cluster's virtual IP address.​|

-   **MSSQL Service Info \[mssql\_sqlservice\_info\]**

<table id="table_vj5_1tk_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description \[description\]

</td><td>

Describes the MSSQL service. For example: "Provides storage, processing, and controlled access of data and rapid transaction processing."

</td></tr><tr><td>

Service Name \[service\_name\]

</td><td>

The MSSQL service name as presented on the server. For example: MSSQL$NAMEDMSSQL2016

</td></tr><tr><td>

Binary Path \[binary\_path\]

</td><td>

The file path of the service. For example: `C:\Program Files\Microsoft SQL Server\MSSQL13.NAMEDMSSQL2016\MSSQL\Binn\sqlservr.exe`

</td></tr><tr><td>

CI \[ci\]

</td><td>

Reference the MSFT SQL instance \[cmdb\_ci\_db\_mssql\_instance\] table.

</td></tr><tr><td>

Installed On \[installed\_on\]

</td><td>

Reference to the Windows server record \[cmdb\_ci\_win\_server\]**Note:** This field isn’t populated for standalone deployments.

</td></tr></tbody>
</table>-   **MSSQL Components Info \[mssql\_components\_info\]**

<table id="table_o3b_lwk_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Install Path \[install\_path\]

</td><td>

The install path of the component service. Foe example: `C:\Program Files\Microsoft SQL Server\MSSQL16.SQLEXPRESS\MSSQL`

</td></tr><tr><td>

Service Name \[service\_name\]

</td><td>

The components service type of the server. For example: **Database Engine Services**

</td></tr><tr><td>

SKU Name \[sku\_name\]

</td><td>

The MSSQL version of the component service. For example: **Express Edition \(64-bit\)**

</td></tr><tr><td>

Version \[version\]

</td><td>

The MSSQL version number of the component service

</td></tr><tr><td>

CI \[ci\]

</td><td>

Reference the MSFT SQL instance \[cmdb\_ci\_db\_mssql\_instance\] table.

</td></tr><tr><td>

Installed On \[installed\_on\]

</td><td>

Reference to the Windows server record \[cmdb\_ci\_win\_server\].**Note:** This field is populated only for SQL Clusters and not for standalone deployments.

</td></tr></tbody>
</table>-   **MSSql DB On Windows pattern extension: Collect MSSQL HADR - Availability Group Info**

    |Field|Description|
    |-----|-----------|
    |Cluster ID \[cluster\_id\]|Globally unique identifier \(GUID\) of the availability group.|
    |Name \[name\]|Cluster name.|
    |IP Address \[ip\_address\]|IP address of the cluster.|

<table id="table_k2p_v4s_p2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Replica ID \[replica\_id\]

</td><td>

Unique ID of the replica.

</td></tr><tr><td>

Role \[role\]

</td><td>

Role of the replica.Possible values are:

-   Primary
-   Secondary
-   Resolving


</td></tr><tr><td>

Availability Mode \[availability\_mode\]

</td><td>

Availability mode of the replica. Possible values are:

-   Asynchronous Commit
-   Synchronous Commit
-   Configuration Only


</td></tr><tr><td>

Failover Mode \[failover\_mode\]

</td><td>

Failover mode of the availability replica. Possible values are:

-   Automatic
-   Manual


</td></tr><tr><td>

Readable Secondary \[readable\_secondary\]

</td><td>

Whether an availability replica that’s performing the secondary role can accept connections from clients. Possible values are:

-   true
-   false


</td></tr><tr><td>

Availability Group \[availability\_group\]

</td><td>

References the MSSQL Availability Group \[cmdb\_ci\_mssql\_ag\] table.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the replica server.

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Unique ID of the replica.

</td></tr><tr><td>

State \[state\]

</td><td>

Failover state.Possible values:

-   Pending
-   Online
-   Offline
-   Failed
-   Failed No Quorum


</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the availability group listener.|
    |Listener ID \[listener\_id\]|Resource globally unique identifier \(GUID\) from Windows Server Failover Clustering \(WSFC\) cluster.|
    |IP Subnet Mask \[ip\_subnet\_mask\]|IP subnet mark for the IPv4 address, if any, that’s configured for the availability group listener.|
    |Availability Group \[availability\_group\]|References the MSSQL Availability Group \[cmdb\_ci\_mssql\_ag\] table.|


## CI relationships

The MSSql DB On Windows pattern creates the following relationships and references to support Microsoft SQL Server and Cluster discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Windows Server \[cmdb\_ci\_win\_server\]|Runs::Runs on|MSSQL Cluster \[cmdb\_ci\_mssql\_cluster\]|
|MSFT SQL instance​ \[cmdb\_ci\_db\_mssql\_instance\]​|Runs::Runs on|MSSQL Cluster \[cmdb\_ci\_mssql\_cluster\]​|
|MSSQL Cluster Node​ \[cmdb\_ci\_mssql\_cluster\_node\]​|Cluster::Cluster of​|MSSQL Cluster \[cmdb\_ci\_mssql\_cluster\]​|
|MSSQL Cluster Node​ \[cmdb\_ci\_mssql\_cluster\_node\]​|Hosted on::Hosts|Windows Server​ \[cmdb\_ci\_win\_server\]​|
|MSFT SQL instance​ \[cmdb\_ci\_db\_mssql\_instance\]|Runs on::Runs|Windows Server​ \[cmdb\_ci\_win\_server\]​|
|MSFT SQL instance​ \[cmdb\_ci\_db\_mssql\_instance\]|Runs on::Runs|MSSQL Cluster Node​ \[cmdb\_ci\_mssql\_cluster\_node\]​|
|MSFT SQL instance​ \[cmdb\_ci\_db\_mssql\_instance\]|Contains::Contained by​|MS SQL Database​ \[cmdb\_ci\_db\_mssql\_database\]​|

|CI|Field|Referenced CI|
|---|-----|-------------|
|MSSQL Cluster Node​ \[cmdb\_ci\_mssql\_cluster\_node\]​|Cluster \[cluster\]|MSSQL Cluster \[cmdb\_ci\_mssql\_cluster\]​|
|MSSQL Cluster Node​ \[cmdb\_ci\_mssql\_cluster\_node\]​|Server \[server\]|Windows Server​ \[cmdb\_ci\_win\_server\]​|
|MSSQL Service Info \[mssql\_sqlservice\_info\]\*|CI \[ci\]|MSFT SQL instance​ \[cmdb\_ci\_db\_mssql\_instance\]|
|MSSQL Components Info \[mssql\_components\_info\]|CI \[ci\]|MSFT SQL instance​ \[cmdb\_ci\_db\_mssql\_instance\]|
|MS SQL Database​ \[cmdb\_ci\_db\_mssql\_database\]​|Instance name \[instance\_name\]|MSFT SQL instance​ \[cmdb\_ci\_db\_mssql\_instance\]|

\*This reference is created only when the pattern uses the WMI queries.

The MSSql DB On Windows pattern creates the following relationships and references using the **Collect MSSQL HADR - Availability Group Info** pattern extension. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|MSFT SQL instance \[cmdb\_ci\_db\_mssql\_instance\]​|Member of::Members|MSSQL Availability Group Replica \[cmdb\_ci\_mssql\_ag\_replica\]|
|MSSQL Availability Group Listener \[cmdb\_ci\_mssql\_ag\_listener\]|Used by::Uses|MSSQL Availability Group \[cmdb\_ci\_mssql\_ag\]|
|MSSQL Availability Group Replica \[cmdb\_ci\_mssql\_ag\_replica\]|Contains::Contained by|MS SQL Database \[cmdb\_ci\_db\_mssql\_database\]|
|MSSQL Availability Group Replica \[cmdb\_ci\_mssql\_ag\_replica\]|Cluster of::Cluster|MSSQL Availability Group \[cmdb\_ci\_mssql\_ag\]|
|MSSQL Availability Group Replica \[cmdb\_ci\_mssql\_ag\_replica\]|Hosted on::Hosts|Windows Server \[cmdb\_ci\_win\_server\]​|

|CI|Field|Referenced CI|
|---|-----|-------------|
|MSSQL Availability Group Listener \[cmdb\_ci\_mssql\_ag\_listener\]|Availability Group \[availability\_group\]|MSSQL Availability Group \[cmdb\_ci\_mssql\_ag\]|
|MSSQL Availability Group Replica \[cmdb\_ci\_mssql\_ag\_replica\]|Availability Group \[availability\_group\]|MSSQL Availability Group \[cmdb\_ci\_mssql\_ag\]|

**Parent Topic:**[Database discovery](../concept/database-discovery.md)

**Related topics**  


[Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#)

[Horizontal Pattern probe](r-HorizontalPatternProbe.md)

[Database Administrator \(DBA\) report discovery](../concept/dba-report-discovery-pattern.md)

