---
title: Database Administrator \(DBA\) report discovery
description: Discovery and Service Mapping uses the Patterns extension sections to provide a Database Administrator report \(DBA report\) for the Apache Cassandra, Microsoft SQL, MySQL, MongoDB, and Oracle databases. The extension sections for each DB pattern populate the related entries tables. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
keywords: [NetApp, Server, Cluster, Patterns]
breadcrumb: [Database discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Database Administrator \(DBA\) report discovery

Discovery and Service Mapping uses the Patterns extension sections to provide a Database Administrator report \(DBA report\) for the Apache Cassandra, Microsoft SQL, MySQL, MongoDB, and Oracle databases. The extension sections for each DB pattern populate the related entries tables. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify the plugins setup**
    -   CMDB CI Class Models 1.49.0 \(September 2023\)
    -   Discovery and Service Mapping Patterns 1.8.0 \(September 2023\)
-   **Verify the system properties are enabled**

    By default, the system properties for DBA reports are set to **false**. To enable the report collection, verify that the system properties value for each pattern is set to **true**.

    |Pattern|System property|
    |-------|---------------|
    |Cassandra|cassandra\_dba\_report\_enabled|
    |MongoDB|mongo\_dba\_report\_enabled|
    |MSSQL DB On Windows|mssql\_dba\_report\_enabled|
    |My SQL server On Windows and Linux|mysql\_dba\_report\_enabled|
    |Oracle DB|oracle\_dba\_report\_enabled|

-   **Verify the configuration of the credentials**

    For more information, see [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

<table id="table_uzm_pxs_lyb"><tbody><tr><td>

MongoDB execute command

</td><td>

Applicative credentials should have read access to run `“getSiblingDB (databaseName)”`

</td></tr><tr><td>

Apache Cassandra execute command

</td><td>

Discovery credentials should have read access to `“nodetool”`

</td></tr><tr><td>

MySQL tables and execute commands

</td><td>

Discovery credentials should have read access to:-   `“information_schema.tables”` table​
-   run `“show databases”`command


</td></tr><tr><td>

Microsoft SQL tables

</td><td>

Discovery credentials should have read access to the following tables:-   **master.sys.databases**
-   **sys.sysprocesses**
-   **sys.dm\_os\_sys\_info**
-   **sys.dm\_os\_ring\_buffers**
-   **msdb.dbo.backupset**
-   **master.dbo.sysdatabases**
-   **master..sysprocesses**
-   **msdb..sysjobactivity**
-   **sys.master\_files**
-   **sys.dm\_tran\_session\_transactions**
-   **sys.dm\_os\_sys\_memory**
-   **sys.database\_files**


</td></tr><tr><td>

Oracle DB tables and execute commands

</td><td>

Discovery credentials should have read access to: -   Run `“lsnrctl services”` and `“sqlplus”` commands
-   **dba\_data\_files** table
-   **dba\_segments** table
-   **v$database** table
-   **gv$instance** table
-   **dba\_hist\_osstat** table
-   **dba\_hist\_snapshot** table
-   **v$asm\_disk** table
-   **v$asm\_diskgroup** table
-   **dba\_audit\_session** table
-   **gv$session\_longops** table
-   **gv$session** table
-   **gv$sqlarea** table
-   **gv$process** table


</td></tr></tbody>
</table>-   **Verify that a Discovery schedule is configured**

    For more information, see [create a discovery schedule](running-discoveries.md)


## Data collected by the extension section of the Apache Cassandra pattern

Discovery populates the following data when running the Apache Cassandra pattern.

**Note:** See the Prerequisites section for important information about enabling the system property.

<table id="simpletable_yg3_m3b_pyb"><thead><tr><th>

Table name

</th><th>

Table label

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

cassandra\_health\_report

</td><td>

Cassandra Health Report

</td><td>

-   database\_host
-   local\_write\_latency
-   read\_latency
-   snapshot\_used\_space
-   space\_used
-   table
-   keyspace
-   ci

</td></tr></tbody>
</table>## Data collected by the extension section of the MongoDB pattern

Discovery populates the following data when running the MongoDB pattern.

**Note:** See the Prerequisites section for important information about enabling the system property.

<table id="table_t3n_wlb_pyb"><thead><tr><th>

Table name

</th><th>

Table label

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

mongo\_db\_statistics

</td><td>

Mongo DB Statistics

</td><td>

-   database\_host
-   database\_name​
-   fs\_total\_size
-   fs\_used\_size
-   scale\_factor
-   index\_size
-   index\_count
-   extents\_count
-   storage\_size
-   data\_size
-   average\_object\_size
-   objects\_count
-   collection\_count
-   view\_count
-   ci

</td></tr></tbody>
</table>## Data collected by the extension section of the MSSQL pattern

Discovery populates the following data when running the MSSQL pattern.

**Note:** See the Prerequisites section for important information about enabling the system property.

<table id="simpletable_syn_kmb_pyb"><thead><tr><th>

Table name

</th><th>

Table label

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

ms\_sql\_db\_blocking\_info

</td><td>

MSSQL DB Blocking Info

</td><td>

-   database\_host
-   database\_instance
-   definition
-   object\_name
-   blocking\_spid
-   spid
-   ci

</td></tr><tr><td>

ms\_sql\_db\_cpu\_util

</td><td>

MSSQL DB CPU Util

</td><td>

-   database\_host
-   database\_instance
-   load\_date
-   other\_process\_cpu\_util
-   other\_process
-   system\_idle\_process
-   sql\_server\_cpu\_util
-   event\_time
-   server\_name
-   ci

</td></tr><tr><td>

ms\_sql\_db\_not\_backup

</td><td>

MSSQL DB Not BackUp

</td><td>

-   database\_host
-   database\_instance
-   last\_backup\_date
-   database\_name
-   ci

</td></tr><tr><td>

ms\_sql\_db\_running\_job

</td><td>

MSSQL DB Running Job

</td><td>

-   database\_host
-   database\_instance
-   login\_name
-   nt\_domain
-   cmd
-   hostname
-   name
-   status
-   open\_tran
-   Spid
-   last\_wait\_type
-   login\_time
-   ci

</td></tr><tr><td>

ms\_sql\_disk\_info

</td><td>

MSSQL DB Disks Info

</td><td>

-   database\_host
-   database\_instance
-   percentage\_free\_space
-   volume\_free\_space
-   volume\_capacity
-   volume\_label
-   volume\_name
-   ci

</td></tr><tr><td>

ms\_sql\_files\_space

</td><td>

MSSQL DB Files Space

</td><td>

-   database\_host
-   database\_instance
-   database\_name
-   free\_space\_mb
-   file\_size\_mb
-   file\_type
-   file\_logic\_name
-   ci

</td></tr><tr><td>

ms\_sql\_fregment\_info

</td><td>

MSSQL DB Fragmentation Info

</td><td>

-   database\_host
-   database\_instance
-   index\_status
-   page\_count
-   avg\_frag
-   index\_name
-   object\_name
-   schema\_name
-   ci

</td></tr><tr><td>

ms\_sql\_last\_restart

</td><td>

MSSQL DB Last Restart

</td><td>

-   database\_host
-   database\_instance
-   uptime\_in\_days
-   current\_date
-   last\_recycle
-   ci

</td></tr><tr><td>

ms\_sql\_long\_trans

</td><td>

MSSQL DB Long Transactions

</td><td>

-   database\_host
-   database\_instance
-   blocked
-   sql
-   cmd
-   program\_name
-   hostname
-   login\_name
-   status
-   last\_batch
-   duration
-   login\_time
-   database\_name
-   user\_tran
-   trans\_id
-   spid
-   ci

</td></tr><tr><td>

ms\_sql\_memory\_info

</td><td>

MSSQL DB Memory Info

</td><td>

-   database\_host
-   database\_instance
-   system\_memory\_state\_desc
-   percentage\_used
-   available\_page\_file\_mb
-   total\_page\_file\_mb
-   available\_physical\_memory\_mb
-   total\_physical\_memory\_mb
-   ci

</td></tr><tr><td>

ms\_sql\_temp\_files\_space

</td><td>

MSSQL DB Temp Files Space

</td><td>

-   database\_host
-   database\_instance
-   percent\_full
-   available\_space\_mb
-   file\_physical\_name
-   file\_logic\_name
-   database\_name
-   ci

</td></tr></tbody>
</table>## Data collected by the extension section of the MySQL pattern

Discovery populates the following data when running the MySQL pattern.

**Note:** See the Prerequisites section for important information about enabling the system property.

<table id="table_k5w_kh1_myb"><thead><tr><th>

Table name

</th><th>

Table label

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

mysql\_table\_schemas

</td><td>

MySql Table Schemas

</td><td>

-   database\_host
-   database\_instance
-   data\_index\_lengh
-   table\_schema
-   ci

</td></tr></tbody>
</table>## Data collected by the extension section of the Oracle DB pattern

Discovery populates the following data when running the Oracle DB pattern.

**Note:** See the Prerequisites section for important information about enabling the system property.

<table id="table_lvg_dj1_myb"><thead><tr><th>

Table name

</th><th>

Table label

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

oracle\_active\_session

</td><td>

Oracle Active Session

</td><td>

-   database\_host
-   database\_instance
-   Key
-   sql\_id
-   program
-   module
-   action
-   status
-   last\_call\_et\_hrs
-   sid
-   spid
-   inst
-   ci

</td></tr><tr><td>

oracle\_asm\_info

</td><td>

Oracle, ASM Disk Info

</td><td>

-   database\_host
-   database\_instance
-   used\_gb
-   free\_gb
-   total\_gb
-   state
-   block\_size
-   asm
-   ci

</td></tr><tr><td>

oracle\_asm\_nodes\_info

</td><td>

Oracle ASM Nodes Disk Info

</td><td>

-   database\_host
-   database\_instance
-   redundancy
-   free\_gb
-   total\_gb
-   state
-   asm\_node
-   ci

</td></tr><tr><td>

oracle\_cpu\_usage

</td><td>

Oracle CPU Usage

</td><td>

-   database\_host
-   database\_instance
-   idle
-   io
-   sys
-   nice
-   user
-   snapid
-   Inst
-   end\_time
-   begin\_time
-   ci

</td></tr><tr><td>

oracle\_inactive\_sessions

</td><td>

Oracle Inactive Sessions

</td><td>

-   database\_host
-   database\_instance
-   key
-   status
-   spid
-   sid
-   program
-   Module
-   last\_call\_et\_hrs
-   inst
-   ci

</td></tr><tr><td>

oracle\_instance\_info

</td><td>

Oracle Instance Info

</td><td>

-   database\_host
-   database\_instance
-   platform\_name
-   current\_scn
-   dbid
-   db\_unique\_name
-   log\_mode
-   db\_name
-   open\_mode
-   ci

</td></tr><tr><td>

oracle\_nodes\_info

</td><td>

Oracle Nodes Info

</td><td>

-   database\_host
-   database\_instance
-   instance\_mode
-   instance\_state
-   instance\_role
-   instance\_status
-   instance\_version
-   hostname
-   instance\_name
-   ci

</td></tr><tr><td>

oracle\_table\_space

</td><td>

Oracle Table Space

</td><td>

-   database\_host
-   database\_instance
-   used\_mb
-   free\_percent
-   free\_mb
-   tablespace
-   total\_mb
-   ci

</td></tr><tr><td>

oracle\_top\_10\_queries

</td><td>

Oracle Top 10 Queries

</td><td>

-   database\_host
-   database\_instance
-   unique
-   status
-   sql\_id
-   spid
-   sid
-   program
-   Module
-   last\_call\_et\_hrs
-   ci

</td></tr></tbody>
</table>**Parent Topic:**[Database discovery](database-discovery.md)

