---
title: Oracle Listener HD discovery
description: ServiceNow Discovery uses the Oracle Listener HD pattern to find and map Oracle real application cluster components. To discover these resources, install the CMDB CI Class Models and the Discovery and Service Mapping Patterns from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
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

Discovery populates the data in the CMDB when running the Oracle Listener HD pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the Oracle Database Listener.|
|Oracle Home \[oracle\_home\]|The Oracle home directory where software is installed.|
|Configuration \[configuration\]|The listener.ora network configuration file.|
|Scan Listener Name \[scan\_listener\_name\]|The name of the SCAN LISTENER.|
|Version \[version\]|The version of the Oracle product.|
|TCP port\(s\) \[tcp\_port\]|The listening port for Oracle client connections.|

|Field|Description|
|-----|-----------|
|SID \[sid\]|The specific name that specifically identifies the instance.​|
|Name \[name\]|The name of the Oracle instance combination of SID@HOST\_NAME​.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The Oracle database unique name.|
|Type \[type\]|The Oracle database type.|
|Operational status \[operational\_status\]|The active status of the Oracle database.|
|Node \[node\]|The host name of the node hosting the Oracle database.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the Oracle database cluster.|
|Cluster ID \[cluster\_id\]|The GUID of the Oracle database cluster.|
|Cluster Status \[cluster\_status\]|The active state of the Oracle database cluster.|
|IP Address \[ip\_address\]|The IP addresses of the nodes participating in the cluster.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The hostname of the cluster node combination of HOSTNAME@CLUSTER\_NAME.​|
|IP Address \[ip\_address\]|The IP address of the cluster node, if resolvable by DNS.​|
|Server \[server\]|The hostname of the host hosting the cluster node.​|
|Cluster \[cluster\]|The name of the cluster to which the cluster node is associated.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the service.|
|TCP port\(s\) \[tcp\_port\]|The port of the service.|
|Listener name \[listener\_name\]|The name of the Listener managing the service.|
|Version \[version\]|The version of the service.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The hostname of the Linux server that is hosting the Oracle Listener process.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The hostname of the AIX server that is hosting the Oracle Listener process.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The hostname of the HP-UX server that is hosting the Oracle Listener process.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The hostname of the Solaris server that is hosting the Oracle Listener process.|

## Dependency Views map

The following dependency views display the relationships between Oracle Listener resources.

![Oracle Database Listener view map​.](../image/oraclelistenerviewmap.png "Oracle Database Listener View Map​")

![Oracle Instance View Map.](../image/oracleinstanceviewmap.png "Oracle Instance View Map")

![Oracle Database View Map.](../image/oracledatabaseviewmap.png "Oracle Database View Map")

![Oracle Cluster View Map.](../image/oracleclusterviewmap.png "Oracle Cluster View Map")

![Oracle Cluster Node View Map​.](../image/oracleclusternodeviewmap.png "Oracle Cluster Node View Map​")

![Linux Server View Map​.](../image/linkviewmap.png "Linux Server View Map​")

## CI relationships

The Listener HD pattern creates the following relationships to support Oracle Listener discovery.

|CI|Relationship|CI|
|---|------------|---|
|Oracle Cluster \[cmdb\_ci\_oracle\_cluster\]|Cluster of::Cluster|Oracle Cluster Node \[cmdb\_ci\_oracle\_cluster\_node\]|
|Oracle Cluster Node \[cmdb\_ci\_oracle\_cluster\_node\]|Hosted on::Hosts|Linux Server \[cmdb\_ci\_linux\_server​\]|
|Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|Runs on::Runs|Linux Server \[cmdb\_ci\_linux\_server​\]|
|Oracle Database Listener \[cmdb\_ci\_db\_ora\_listener\]|Depends on::Used by|Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|
|Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|Uses::Used by|Oracle Database \[cmdb\_ci\_db\_oracle\_database\]​|
|Oracle Database \[cmdb\_ci\_db\_oracle\_database\]​|Hosted on::Hosts|Oracle Cluster Node \[cmdb\_ci\_oracle\_cluster\_node\]|
|Oracle Cluster Node \[cmdb\_ci\_oracle\_cluster\_node\]|Hosted on::Hosts|AIX Server \[cmdb\_ci\_aix\_server\]|
|Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|Runs on::Runs|AIX Server \[cmdb\_ci\_aix\_server\]|
|Oracle Cluster Node \[cmdb\_ci\_oracle\_cluster\_node\]|Hosted on::Hosts|Solaris Server \[cmdb\_ci\_solaris\_server\]|
|Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|Runs on::Runs|Solaris Server \[cmdb\_ci\_solaris\_server\]|
|Oracle Cluster Node \[cmdb\_ci\_oracle\_cluster\_node\]|Hosted on::Hosts|HPUX Server \[cmdb\_ci\_hpux\_server\]|
|Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|Runs on::Runs|HPUX Server \[cmdb\_ci\_hpux\_server\]|
|Oracle DB Service \[cmdb\_ci\_db\_ora\_service\]|Managed by::Manages|Oracle Database Listener \[cmdb\_ci\_db\_ora\_listener\]|
|Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|Uses::Used by|Oracle DB Service \[cmdb\_ci\_db\_ora\_service\]|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

