---
title: Oracle database discovery
description: Discovery can identify an Oracle database instance that is running on UNIX or Windows operating systems. It can also find Oracle clusterware, which runs Real Application Clusters \(RAC\).
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Database discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Oracle database discovery

Discovery can identify an Oracle database instance that is running on UNIX or Windows operating systems. It can also find Oracle clusterware, which runs Real Application Clusters \(RAC\).

Patterns perform the discovery of Oracle installations. These patterns replace several probes for new instances. If you want to continue to use probes, you can deactivate the Horizontal discovery probe, which launches the pattern, and then activate the necessary probes.

**Note:** Oracle DB on Unix and Oracle DB on Windows do not support RAC single-node discovery.

The Oracle DB on Unix and Oracle DB on Windows patterns discover Oracle catalog objects through the pattern extension Get Catalog info. For more information, see [Oracle Catalog discovery](../../service-mapping/reference/oracle-catalog-discovery.md). For general information about database catalog discovery, see [database catalogs](c_DatabaseCatalogs.md).

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Credentials

Configure these credentials:

<table id="table_gmd_2kx_jz"><thead><tr><th>

Credential type

</th><th>

Additional information

</th></tr></thead><tbody><tr><td>

[Applicative credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/applicative-creds.md)

</td><td>

Applicative credentials are mandatory for two use cases:

-   Executing SQL queries against the remote Oracle DB Instance
-   Creating connections to database links
-   Software Asset Management activated

You must add the database user you configured during Oracle database installation. Specify `Oracle instance [cmdb_ci_db_ora_instance]` as the CI type. The user must also have access to the **tnsnames.ora** parameters file. Make sure that the tnsnames.ora is configured correctly and exists in the Oracle path on the target Windows host. Also, verify that the utilized Discovery Credentials can read tnsnames.ora file.

The user needs permissions for the SQL\*Plus command line tool and permissions to execute SELECT queries against the following tables:

-   PRODUCT\_COMPONENT\_VERSION
-   V$VERSION
-   V$DATABASE
-   V$PARAMETER

</td></tr><tr><td>

[Windows credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_WindowsCredentialsForm.md)

</td><td rowspan="2">

You can also use Windows and SSH credentials in addition to applicative credentials. For Windows credentials, the user must have read permissions to the `tnsnames.ora` file. SSH credentials, must allow read permission to the `oratab` file and read permission to the System Parameter file.For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

</td></tr><tr><td>

[SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md)

</td></tr></tbody>
</table>## Additional requirements

Discovery identifies a running instance of an Oracle database on UNIX from the process that starts with `ora_pmon_`. Ensure this process is running in the IP range you designate for Discovery. Discovery identifies a running instance of an Oracle database on Windows from the `oracle.exe` process. Ensure this process is running in the IP range you designate.

For Oracle clusterware, you also need permissions to read [the `/etc/hosts/` file](https://docs.oracle.com/cd/E37670_01/E41138/html/ch11s02s01.html), which associates host names with IP addresses.

The following commands are run for Oracle clusterware:

<table id="table_nfs_4tn_ndb"><thead><tr><th>

Command

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`ps -ef | grep 'crsd.bin' |grep -v grep`

</td><td>

Verifies if Oracle CRS process is running.

</td></tr><tr><td>

`ps -ef |grep LISTENER | grep -v $$ | head -1 | awk '{print $8}'`

</td><td>

Gets Oracle home from the listener process path. Used when the ORACLE\_HOME environment variable is unavailable.

</td></tr><tr><td>

`ps -ef | grep 'd.bin' | grep -v grep | grep -v bash | awk '{print $8}'`

</td><td>

Gets Oracle Grid home from the CRS daemon process path.

</td></tr><tr><td>

`/u01/app/12.1.0.2/grid/bin/olsnodes -c | egrep -v 'error|return code'`

</td><td>

Gets Oracle CRS cluster name.

</td></tr><tr><td>

`sudo /u01/app/12.1.0.2/grid/bin/ocrcheck | egrep -v 'error|return code'`

</td><td>

Gets Oracle CRS cluster ID.

</td></tr><tr><td>

`/u01/app/12.1.0.2/grid/bin/crsctl query crs softwareversion| egrep -v 'error|return code'`

</td><td>

Gets Oracle CRS version.

</td></tr><tr><td>

`/u01/app/12.1.0.2/grid/bin/olsnodes | egrep -v 'error|return code'`

</td><td>

Gets Oracle CRS nodes.

</td></tr><tr><td>

`/u01/app/12.1.0.2/grid/bin/crsctl status server | egrep -v 'error|return code'`

</td><td>

Gets Oracle CRS node status.

</td></tr><tr><td>

`/u01/app/12.1.0.2/grid/bin/crsctl stat res -f | tr '\n' '#'`

</td><td>

Gets Oracle CRS resources.

</td></tr><tr><td>

`/u01/app/12.1.0.2/grid/bin/crsctl stat res -p | grep -v CHECK_R |grep -v error |grep -v failed`

</td><td>

Gets Oracle CRS VIP resources.

</td></tr><tr><td>

`/u01/app/12.1.0.2/grid/bin/srvctl config scan | tr '\n' ‘ '`

</td><td>

Gets Oracle RAC SCAN VIP configurations.

</td></tr><tr><td>

`/u01/app/12.1.0.2/grid/bin/srvctl config vip -node ol7-121-rac1| egrep ' Name' | awk '{print $3}'`

</td><td>

Gets Oracle CRS VIPs name.

</td></tr><tr><td>

`/u01/app/12.1.0.2/grid/bin/srvctl config vip -node ol7-121-rac1| grep ' IPv4 Address:' | awk '{print $4}'`

</td><td>

Get Oracle CRS VIPs ip\_address.

</td></tr></tbody>
</table>**Important:** Sudo permission are required to run `sudo /u01/app/12.1.0.2/grid/bin/ocrcheck | egrep -v 'error|return code'`.

## Classifiers, patterns, and probes

Discovery uses these classifiers, probes, and patterns for Oracle database discovery:

<table id="table_fzd_2yv_jz"><thead><tr><th>

Classifier

</th><th>

Trigger probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

Oracle Instance

</td><td>

-   Horizontal discovery probe: launches patterns
-   Powershell-Oracle - Instance PFile \(for Windows\)**\***
-   Powershell-Oracle - Instance Version \(for Windows\)**\***
-   SSHCommand-Oracle - Instance Details \(for Linux\)**\***

</td><td>

Application patterns:

-   Oracle DB On Windows Pattern
-   Oracle DB on UNIX Pattern

 This shared library pattern used by the [Linux Server](../reference/r_DataCollDiscoLinuxComputers.md) pattern:

 UNIX Cluster - ORACLE Clusterware

**Note:** This shared library pattern is triggered if the `crsd.bin` process is running on the Oracle database server.

</td></tr><tr><td>

Oracle Listener

</td><td>

SSHCommand-Oracle - Listener Details

</td><td>

none

</td></tr></tbody>
</table>**\***Probes inactive for new instances.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected

The following data is collected on the Oracle Instances \[cmdb\_ci\_db\_ora\_instance\] table for both UNIX and Windows:

<table id="table_ewc_k1w_jz"><thead><tr><th>

Label

</th><th>

Field name

</th><th>

Additional information

</th></tr></thead><tbody><tr><td>

SID

</td><td>

sid

</td><td>

Obtained from the name of the process that starts with `ora_pmon_`

</td></tr><tr><td>

Install directory

</td><td>

install\_directory

</td><td>

Obtained from the path of `ORA_HOME`

</td></tr><tr><td>

Version

</td><td>

version

</td><td>

Obtained in this order:-   From the output of the `ORA_HOME/bin/sqlplus /NOLOG` command
-   From the output of the `ORA_HOME/bin/lsnrctl` status command
-   From the path of `ORA_HOME`

</td></tr><tr><td>

Parameter file

</td><td>

pfile

</td><td>

The following locations are explored for the location of the System Parameter File. If this file does not exist in one of the explored locations, Discovery does not find the file and reports an error. -   *oracle\_home*/dbs/spfile*SID*.ora
-   *oracle\_home*/dbs/spfile.ora
-   *oracle\_home*/dbs/init*SID*.ora

</td></tr><tr><td>

Oracle Home

</td><td>

oracle\_home

</td><td>

Obtained from the *ORATAB* file.

</td></tr><tr><td>

Edition

</td><td>

edition

</td><td>

Obtained from the `context.xml` file.

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

Combination of SID name Host name in the format `SID@HOST_NAME`.

</td></tr><tr><td>

TCP port\(s\)

</td><td>

tcp\_port

</td><td>

Obtained from the `tnsnames.ora` file, or `lsnrctl` status command. If no valid information is retrieved, the default port 1521 is assigned.

</td></tr></tbody>
</table>**Note:** See [Oracle options](c_OracleDatabaseDiscovery.md#section_lvy_czw_xz) for pattern extensions and additional information collected.

<table id="table_tc2_qbw_jz"><thead><tr><th>

Label

</th><th>

Field name

</th><th>

Additional information

</th></tr></thead><tbody><tr><td>

SID

</td><td>

sid

</td><td>

Obtained from the process parameter that is passed to the `oracle.exe` process.

</td></tr><tr><td>

Install directory

</td><td>

install\_directory

</td><td>

 

</td></tr><tr><td>

Version

</td><td>

version

</td><td>

Obtained from the output of the `ORA_HOME/bin/sqlplus.exe -V` command.

</td></tr><tr><td>

Parameter file

</td><td>

pfile

</td><td>

The following locations are explored for the location of the System Parameter File. If this file does not exist in one of the explored locations, Discovery does not find the file and reports an error. -   *oracle\_home*\\database\\spfile*SID*.ora
-   *oracle\_home*\\database\\spfile.ora
-   *oracle\_home*\\database\\init*SID*.ora

</td></tr><tr><td>

Oracle Home

</td><td>

oracle\_home

</td><td>

Parsed from the path of `oracle.exe`

</td></tr><tr><td>

Edition

</td><td>

edition

</td><td>

 

</td></tr></tbody>
</table>**Note:** See [Oracle options](c_OracleDatabaseDiscovery.md#section_lvy_czw_xz) for pattern extensions and additional information collected.

## Oracle options

For general information on Oracle options, see [https://docs.oracle.com/en/](https://docs.oracle.com/en/).

Discovery can also find the Oracle options that you enable on the instance using the legacy pattern extension, Oracle option extension for Windows/Unix. Note that to discover Oracle options, the Software Asset Management Professional for Oracle \(com.snc.samp.oracle\) plugin is required.

|Label|Field name|
|-----|----------|
|Instance|instance|
|Option|option|
|Licensable|licensable|
|Currently used|currently\_used|
|First usage date|first\_usage|
|Last usage date|last\_usage|
|Last sample date|last\_sample|
|Detected usage|detected\_usage|
|Sample interval|sample\_interval|

<table id="table_qb1_nn5_ymb"><thead><tr><th>

Table privileges needed

</th><th>

Additional information

</th></tr></thead><tbody><tr><td>

The following tables are accessed as part of the Oracle option extension for UNIX and Windows:-   DBA\_FEATURE\_USAGE\_STATISTICS
-   CDB\_FEATURE\_USAGE\_STATISTICS
-   V$DATABASE
-   V$VERSION
-   GV$PARAMETER
-   V$CONTAINERS
-   V$INSTANCE

</td><td>

The following pattern extensions use the Oracle script: options\_packs\_usage\_statistics.sql. This sql script is for DB Server version 11.2 and later. You need the **Select any dictionary** privilege to execute the script. See the support document ID13172651.1 on [https://support.oracle.com/portal/](https://support.oracle.com/portal/) for more information about usage scripts. -   Oracle option extensions for UNIX
-   Oracle option extensions for Windows

</td></tr></tbody>
</table><table id="table_rvs_gjl_mdb"><thead><tr><th>

Table

</th><th>

Labels and field names

</th></tr></thead><tbody><tr><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td><td>

Name \[name\]

 Cluster status \[cluster\_status\]

 Cluster type \[cluster\_type\]

 IP address \[ip\_address\]

 Short description \[short\_description\]

 Cluster ID \[cluster\_id\]

 Cluster version \[cluster\_version\]

</td></tr><tr><td>

cmdb\_ci\_unix\_cluster\_node

</td><td>

Name \[name\]

 Node state \[node\_state\]

 IP address \[ip\_address\]

 Node status \[node\_status\]

</td></tr><tr><td>

cmdb\_ci\_unix\_cluster\_resource

</td><td>

Name \[name\]

 Resource type \[resource\_type\]

 Resource status \[resource\_status\]

 Properties \[properties\]

</td></tr><tr><td>

cmdb\_ci\_cluster\_vip

</td><td>

Name \[name\]

 IP address \[ip\_address\]

 Cluster name \[cluster\_name\]

 Cluster ID \[cluster\_id\]

</td></tr></tbody>
</table>On the dependency view, a **+1** on an Oracle database server signifies that it is part of a cluster.

## Extend Oracle instance extension

**Note:** Discovery can also find additional attributes for the instance using the Extend Oracle instance extension. See the Oracle website for more information on options [https://docs.oracle.com/en/](https://docs.oracle.com/en/). Discovery saves these attributes to the Oracle Instances \[cmdb\_ci\_db\_ora\_instance\] table.

|Label|Field name|
|-----|----------|
|Instance|instance|
|Host Name|host\_name|
|IS\_CDB|cdb\_yn|
|DB Unique Name|db\_unique\_name|
|DB Name|database\_name|
|Replication Enabled|replication\_enabled|

<table id="table_hdn_tkn_pnb"><thead><tr><th>

Table privileges needed

</th><th>

Additional information

</th></tr></thead><tbody><tr><td>

The following tables are accessed as part of the Extend Oracle Instance extension for UNIX and Windows:-   V$DATABASE
-   V$INSTANCE

</td><td>

The Extend Oracle Instance extension needs to be installed. This extension is included in the Discovery and Service Mapping Patterns application, version 1.0.72 or higher, which can be downloaded from the ServiceNow Store.

</td></tr></tbody>
</table>## Oracle instances on virtual machines

When Oracle instances are hosted on virtual machines, the system creates relationships between CIs.

<table id="table_eh4_pjv_xz"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Oracle instance

</td><td>

Hosted on

</td><td>

Computer \[cmdb\_ci\_computer\] or Server \[cmdb\_ci\_server\]**Note:** This is a virtual machine. The **Is virtual** field is **true**.

</td></tr><tr><td>

Computer \[cmdb\_ci\_computer\] or Server \[cmdb\_ci\_server\]**Note:** This is a virtual machine. The **Is virtual** field is **true**.

</td><td>

Virtualized by

</td><td>

Computer \[cmdb\_ci\_computer\] or Server \[cmdb\_ci\_server\]**Note:** This is not a virtual machine.

</td></tr></tbody>
</table>## Oracle instances on virtual machines that are hosted on AWS or Azure clouds

<table id="table_ffp_vmv_xz"><thead><tr><th>

Base class

</th><th>

Relationship

</th><th>

Dependent class

</th></tr></thead><tbody><tr><td>

Oracle instance

</td><td>

Hosted on

</td><td>

Computer \[cmdb\_ci\_computer\]**Note:** This is a virtual machine. The **Is virtual** field is **true**.

</td></tr><tr><td>

Computer \[cmdb\_ci\_computer\]**Note:** This is a virtual machine. The **Is virtual** field is **true**.

</td><td>

Virtualized by

</td><td>

Computer \[cmdb\_ci\_computer\]**Note:** This is not a virtual machine.

</td></tr><tr><td>

Computer \[cmdb\_ci\_computer\]**Note:** This is a virtual machine. The **Is virtual** field is **true**.

</td><td>

Virtualized by

</td><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]**Note:** The vCPU count is populated in this table.

</td></tr><tr><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Hosted on

</td><td>

AWS Datacenter \[cmdb\_ci\_aws\_datacenter\] or Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]

</td></tr></tbody>
</table>## Relationships for clusterware

<table id="table_bbb_zkg_ndb"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td><td>

Virtualizes::Virtualized by

</td><td>

Cluster Virtual IP \[cmdb\_ci\_cluster\_vip\]

</td></tr><tr><td>

Unix Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]

</td><td>

Defines resources for::Gets resources from

</td><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td></tr><tr><td>

Cluster Virtual IP \[cmdb\_ci\_cluster\_vip\]

</td><td>

Uses::Used by

</td><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td></tr><tr><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td><td>

Cluster of::Cluster

</td><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td></tr><tr><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td><td>

Hosted on:Hosts

</td><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td></tr><tr><td>

Unix Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]

</td><td>

Defines resources for::Gets resources from

</td><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td></tr><tr><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td><td>

Hosts::Hosted on

</td><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td></tr><tr><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td><td>

Hosted on::Hosts

</td><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td></tr></tbody>
</table>**Parent Topic:**[Database discovery](database-discovery.md)

**Related topics**  


[Add the Horizontal Pattern probe to a classifier](c-UsingPatternsForHorizontalDiscovery.md#)

[Horizontal Pattern probe](../reference/r-HorizontalPatternProbe.md)

[Database Administrator \(DBA\) report discovery](dba-report-discovery-pattern.md)

[Oracle Catalog discovery](../../service-mapping/reference/oracle-catalog-discovery.md)

[Oracle pluggable database and container database discovery](../../service-mapping/reference/oracle-cdb-pdb-discovery.md)

[Oracle Global License Advisory Services \(GLAS\) data collection using patterns](../../service-mapping/reference/oracle-glas-discovery.md)

