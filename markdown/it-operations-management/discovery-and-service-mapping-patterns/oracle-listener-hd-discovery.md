---
title: Oracle Listener HD discovery
description: ServiceNow Discovery uses the Oracle Listener HD pattern to find and map Oracle real application cluster components. To discover these resources, install the CMDB CI Class Models and the Discovery and Service Mapping Patterns from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle Listener HD discovery

ServiceNow Discovery uses the Oracle Listener HD pattern to find and map Oracle real application cluster components. To discover these resources, install the CMDB CI Class Models and the Discovery and Service Mapping Patterns from the ServiceNow Store.

Oracle RAC enables you to cluster an Oracle database. Oracle RAC uses Oracle Clusterware for the infrastructure to bind multiple servers so they operate as a single system. Oracle Clusterware enables you to create a clustered pool of storage that can be used by any combination of non-cluster and Oracle RAC databases. Discovery uses Oracle Listener HD patterns to discover information about the Oracle Database Listener and the components in the Oracle RAC infrastructure, when such a setup is configured.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Ensure that the following plugins are installed:
    -   CMDB CI Class Models plugin \(Version 1.29.0 or later\). ​
    -   Discovery and Service Mapping Patterns plugin \(Version 1.0.82 or later\).​
-   Ensure that the Discovery User is in the Oracle DBA group or has the correct Permissions.
-   Ensure that the MID Server has access to the target device.
-   Ensure that the Oracle Clusterware/Grid infrastructure is installed and the Oracle RAC Database is configured. If there is an Oracle Clusterware setup.
-   Ensure that the Oracle Listener process is running on a UNIX OS host.​
-   Use Oracle Clusterware minimum version 12.2.X.X \(Oracle Database 12c Release 2\) or higher, If there is an Oracle Clusterware setup​.

    **Note:** This pattern is supported from the Paris release on. More UNIX OS types \(AIX, Solaris, HP-UX\) are supported from version 1.0.87 of the Discovery and Service Mapping Patterns plugins.

    The following commands are executed during the pattern execution. Executing the commands enables the pattern to populate allthe relevant CMDB classes with the necessary information:

    -   **export TNS\_ADMIN=&lt;oracle\_home\_directory&gt;/network/admin**: Sets the ORACLE\_HOME to the TNS\_ADMIN environment variable.

    -   **export ORACLE\_BASE==&lt;oracle\_home\_directory&gt;**: Sets the ORACLE\_HOME to the ORACLE\_BASE environment variable.

    -   **lsnrctl status LISTENER\_NAME**: Checks the Database Listener status​.

    -   **ps -ef \| grep 'd.bin’**: Searches for the GRID\_HOME path​.

    -   **crsctl query cluster site** **-all**: Lists the nodes and disks that the sites contain​.

    -   **lsnrctl services LISTENER\_NAME**: Lists the services that the listener identifies.

    -   **crsctl stat res -f -w '\(\(TYPE = ora.database.type\)\)’**: Lists the database name, associated node, type, and active status.​

        **Note:** If no output is obtained from the **lsnrctl status LISTENER\_NAME**, then the **Oracle Listener HD** pattern is terminated.


## Limitations

The Oracle Clusterware setup is only supported for the UNIX Operating Systems. The base system **SSH Command-Oracle - Listener Details classifier probe** is inactive \(Active is set to False\), when installing the CMDB CI Class Models version 1.29.0 or higher.

![Classifier Probes.](../image/classifierprobenew.png "Classifier Probes- Oracle Listener Details")

The **Oracle Listener process classification** triggers the Oracle Listener HD pattern.

![Classifier Probes.](../image/classifier_probes_horizontal.png "Classifier Probes- Horizontal Pattern")

## Data collected by Discovery during horizontal discovery

The Oracle Listener HD pattern populates the following CIs:

|Field|Description|
|-----|-----------|
|name|The name of the Oracle Database Listener.|
|oracle\_home|The Oracle home directory where software is installed.|
|configuration|The listener.ora network configuration file.|
|scan\_listener\_name|The name of the SCAN LISTENER.|
|version|The version of the Oracle product.|
|tcp\_port|The listening port for Oracle client connections.|

![Oracle Database Listener Form​.](../image/oracledatabaselistenerform.png "Oracle Database Listener Form​")

![Oracle Database Listener view map​.](../image/oracledatabaseviewmap.png "Oracle Database Listener View Map​")

<table id="table_hc5_jsp_nqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sid

</td><td>

The specific name that specifically identifies the instance.​

</td></tr><tr><td>

name

</td><td>

The name of the Oracle instance combination of SID@HOST\_NAME​

</td></tr></tbody>
</table>![Oracle Instance Form.](../image/oracleinstanceform.png "Oracle Instance Form")

![Oracle Instance View Map.](../image/oracleinstanceviewmap.png "Oracle Instance View Map")

|Field|Description|
|-----|-----------|
|name|The Oracle database unique name.|
|type|The Oracle database type.|
|operational\_status|The active status of the Oracle database.|
|node|The host name of the node hosting the Oracle database.|

![Oracle Database Form.](../image/oracledatabaseform.png "Oracle Database Form")

![Oracle Database View Map.](../image/oracledatabaseviewmap.png "Oracle Database View Map")

|Field|Description|
|-----|-----------|
|name|The name of the Oracle database cluster.|
|cluster\_id|The GUID of the Oracle database cluster.|
|cluster\_status|The active state of the Oracle database cluster.|
|ip\_address|The IP addresses of the nodes participating in the cluster.|

​

![Oracle Cluster Form.](../image/oracleclusterform.png "Oracle Cluster Form")

![Oracle Cluster View Map.](../image/oracledatabaseviewmap.png "Oracle Cluster View Map")

|Field|Description|
|-----|-----------|
|name|The hostname of the cluster node combination of HOSTNAME@CLUSTER\_NAME.​|
|ip\_address|The IP address of the cluster node, if resolvable by DNS.​|
|server|The hostname of the host hosting the cluster node.​|
|cluster|The name of the cluster to which the cluster node is associated.|

![Oracle Cluster Node Form​.](../image/oracleclusterform.png "Oracle Cluster Node Form​")

![Oracle Cluster Node View Map​.](../image/oracleclusternodeviewmap.png "Oracle Cluster Node View Map​")

|Field|Description|
|-----|-----------|
|name|The hostname of the Linux server that is hosting the Oracle Listener process.|

![Linux Server Form.](../image/linuxserverform.png "Linux Server Form")

![Linux Server View Map​.](../image/linkviewmap.png "Linux Server View Map​")

|Field|Description|
|-----|-----------|
|name|The hostname of the AIX server that is hosting the Oracle Listener process.|

|Field|Description|
|-----|-----------|
|name|The hostname of the HP-UX server that is hosting the Oracle Listener process.|

|Field|Description|
|-----|-----------|
|name|The hostname of the Solaris server that is hosting the Oracle Listener process.|

|Field|Description|
|-----|-----------|
|name|The name of the service.|
|tcp\_port|The port of the service.|
|listener\_name|The name of the Listener managing the service.|
|version|The version of the service.|

## CI Relationships

## Relationships created by the Oracle Listener HD Pattern

<table id="id_wxw_5d5_3qb"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

cmdb\_ci\_oracle\_cluster

</td><td>

“Cluster of :: Cluster”

</td><td>

cmdb\_ci\_oracle\_cluster\_node

</td></tr><tr><td>

cmdb\_ci\_oracle\_cluster\_node

</td><td>

“Hosted on :: Hosts”

</td><td>

cmdb\_ci\_linux\_server

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_instance

</td><td>

“Runs on :: Runs”

</td><td>

cmdb\_ci\_linux\_server

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_listener

</td><td>

“Depends on :: Used by”

</td><td>

cmdb\_ci\_db\_ora\_instance

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_instance

</td><td>

“Uses :: Used by”

</td><td>

cmdb\_ci\_db\_oracle\_database​

</td></tr><tr><td>

cmdb\_ci\_oracle\_database

</td><td>

"Hosted on :: Hosts”

</td><td>

cmdb\_ci\_oracle\_cluster\_node

</td></tr><tr><td>

cmdb\_ci\_oracle\_cluster\_node

</td><td>

“Hosted on :: Hosts”

</td><td>

cmdb\_ci\_aix\_server

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_instance

</td><td>

Runs on :: Runs”

</td><td>

cmdb\_ci\_aix\_server

</td></tr><tr><td>

cmdb\_ci\_oracle\_cluster\_node

</td><td>

“Hosted on :: Hosts”

</td><td>

cmdb\_ci\_solaris\_server

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_instance

</td><td>

Runs on :: Runs”

</td><td>

cmdb\_ci\_solaris\_server

</td></tr><tr><td>

cmdb\_ci\_oracle\_cluster\_node

</td><td>

“Hosted on :: Hosts”

</td><td>

cmdb\_ci\_hpux\_server

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_instance

</td><td>

Runs on :: Runs”

</td><td>

cmdb\_ci\_hpux\_server

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_service

</td><td>

Managed by::Manages

</td><td>

cmdb\_ci\_db\_ora\_listener

</td></tr><tr><td>

cmdb\_ci\_db\_ora\_instance

</td><td>

Uses::Used by

</td><td>

cmdb\_ci\_db\_ora\_service

</td></tr></tbody>
</table>**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

