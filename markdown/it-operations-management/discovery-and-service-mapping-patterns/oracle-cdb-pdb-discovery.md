---
title: Oracle pluggable database and container database discovery
description: The ServiceNow Discovery application can discover Oracle pluggable databases \(PDBs\) and container databases \(CDBs\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle pluggable database and container database discovery

The ServiceNow Discovery application can discover Oracle pluggable databases \(PDBs\) and container databases \(CDBs\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

A PDB is a portable collection of schemas, schema objects, and non-schema objects that appear to an Oracle Net client as a separate database. A collection of PDBs is called a container database \(CDB\).

For more information about PDBs and CDBs, see [What are CDBs, PDBs and Containers?](http://www.oracle-wiki.net/premium:startdocsminimulticdbs)

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

Set the user credentials and grant permissions:

-   Configure [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   For Windows, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   For Unix, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   For the Oracle database, configure [Oracle database discovery](../../discovery/concept/c_OracleDatabaseDiscovery.md)
-   Provide a user with permissions to run queries on the following tables:
    -   V$DATAFILE
    -   V$TEMPFILE​
    -   V$LOG
    -   DBA\_FREE\_SPACE
    -   V$DATABASE
    -   V$PDBS
    -   V$PARAMETER

**Note:** Set applicative credentials at the CDB level to discover relationships for PDBs and the CDB size only. Alternatively, set applicative credentials at the CDB/PDB level to discover relationships for PDBs and the CDB/PDB size. If you do not set applicative credentials at the CDB level, no PDB attributes are discovered.

## Data collected during Discovery

Discovery collects the following data:

|Table and field|Description|
|---------------|-----------|
|cmdb\_ci\_db\_ora\_pdb\_instance: Relation Type : Managed By​​|
|sid|Name of the PDB instance​​|
|name|Name of the CI in CMDB. This is a combination of sid and the hostname​.|
|version|Version of the PDB as taken from the CDB instance​​|
|edition|Edition of the PDB as taken from the CDB instance​​|
|install\_directory|Install directory of the PDB as taken from the CDB instance|
|oracle\_home​|Oracle home of the PDB as taken from the CDB instance|
|cdb\_name|Name of the cdb sid that contains the PDB. This refers to the Oracle database instance configuration item \(CI​\)|
|cmdb\_ci\_db\_instance\_size: Relation Type : Contained By​​|
|sid|Name of the Oracle database CDB/PDB instance​​|
|name|Name of the CI in CMDB. This is a combination of the sid and the hostname.|
|db\_size|Total size allocated to the database instance|
|used\_size|Size used by the database instance|
|free\_size|Size of the free space on the database instance|

The following is a dependency view of the relationship between PDBs, CDBs, and containers.

![Dependency view of relationship between PDBs, CDBs, and containers](../image/oracle-pdb-cdb.png)

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

**Related topics**  


[Oracle Catalog discovery](oracle-catalog-discovery.md)

[Oracle Global License Advisory Services \(GLAS\) data collection using patterns](oracle-glas-discovery.md)

