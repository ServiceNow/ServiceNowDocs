---
title: Oracle Global License Advisory Services \(GLAS\) data collection using patterns
description: The ServiceNow Discovery application uses the Oracle verified GLAS Data Collection pattern to discover Oracle GLAS data. This data includes discovered Oracle Database, Middleware, and Java configuration items.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-25"
reading_time_minutes: 8
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle Global License Advisory Services \(GLAS\) data collection using patterns

The ServiceNow Discovery application uses the Oracle verified GLAS Data Collection pattern to discover Oracle GLAS data. This data includes discovered Oracle Database, Middleware, and Java configuration items.

The Oracle GLAS Data Collection pattern is an extension of the following patterns:

-   Oracle Database on UNIX and Windows patterns
-   Oracle Middleware on Linux for the following patterns:
    -   Oracle Tuxedo
    -   WebLogic
    -   Linux
-   Oracle Java on Java installation pattern

The Oracle Database and Middleware patterns execute the pattern extensions, and the data collected is stored in the ServiceNow tables for GLAS data. The Oracle GLAS Data Collection Database pattern can be used on the ServiceNow AI Platform beginning with the Paris release. The Oracle GLAS Data Collection Middleware pattern can be used on the ServiceNow AI Platform beginning with the Rome release. The Oracle Java pattern can be used on the ServiceNow AI Platform beginning with the Washington DC release.

For details on how to view and download the collected Oracle GLAS data, see [Download Oracle Global License Advisory Services \(GLAS\) data](../task/download-oracle-glas-data.md).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To learn about the supported versions of Oracle, refer to [Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md).

## Prerequisites

-   **Install the Data Collection for Oracle Global Licensing and Advisory Services store app**

    Navigate to **System Definition** &gt; **Plugins** and install the Data Collection for Oracle Global Licensing and Advisory Services app.

    -   The minimum version for Database collection is 1.4.0
    -   The minimum version for Middleware collection is 1.7.1
    -   The minimum version for Java collection is 1.8.4
    **Note:** The Data Collection for Oracle Global Licensing and Advisory Services app requires the Discovery \(com.snc.discovery\) plugin to work correctly.

-   **Verify the following applications are installed**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
-   **Verify operating system privileges**

    Verify that your Windows or UNIX user can write temporary files under `/tmp`.

    Verify that you can run the following operating system commands:

    -   ls
    -   cat
    -   ps
-   **Create operating system credentials**

    Verify that you have the following credentials for your operating system, and then create credentials for them on the ServiceNow AI Platform:

    -   UNIX credentials using SSH. For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
    -   Windows credentials using PowerShell/WMI. For more information, see [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

        **Note:** PowerShell and WMI credentials are required only for Database collection.

-   **Verify the following Oracle privileges**

    Verify that you have applicative credentials for the Oracle instance \(cmdb\_ci\_db\_ora\_instance\) that have the following privileges:

    -   Read permissions on the `tnsnames.ora` file.
    -   Permissions to execute the `sqlplus` command.
    -   \(For middleware collection\) Sudo permissions to run the following command: `sudo su - oracle -c "$ORACLE_INSTANCE/bin/opmnctl status"`
    Verify you have the user name and password for the relevant Oracle Database, with read permissions on the following tables:

<table id="table_ixr_1rz_5tb"><tbody><tr><td>

DBA\_ADVISOR\_TASKS

</td><td>

DBA\_USERS

</td><td>

SYS.MODEL$

</td></tr><tr><td>

DBA\_CPU\_USAGE\_STATISTICS

</td><td>

DMSYS.DM$MODEL

</td><td>

SYS.REGISTRY$HISTORY

</td></tr><tr><td>

DBA\_ENCRYPTED\_COLUMNS

</td><td>

DMSYS.DM$OBJECT

</td><td>

SYSMAN.MGMT\_INV\_CONTAINER

</td></tr><tr><td>

DBA\_FEATURE\_USAGE\_STATISTICS

</td><td>

DMSYS.DM$P\_MODEL

</td><td>

SYSMAN.MGMT\_LICENSES

</td></tr><tr><td>

DBA\_FLASHBACK\_ARCHIVE\_TABLES

</td><td>

DVSYS.DBA\_DV\_REALM

</td><td>

SYSMAN.MGMT\_LICENSE\_DEFINITIONS

</td></tr><tr><td>

DBA\_INDEXES

</td><td>

GV$IM\_SEGMENTS

</td><td>

SYSMAN.MGMT\_TARGETS

</td></tr><tr><td>

DBA\_LOBS

</td><td>

GV$INSTANCE

</td><td>

SYSMAN.MGMT\_VERSIONS

</td></tr><tr><td>

DBA\_LOB\_PARTITIONS

</td><td>

GV$PARAMETER

</td><td>

V$ARCHIVE\_DEST\_STATUS

</td></tr><tr><td>

DBA\_LOB\_SUBPARTITIONS

</td><td>

MDSYS.SDO\_FEATURE\_USAGE

</td><td>

V$BLOCK\_CHANGE\_TRACKING

</td></tr><tr><td>

DBA\_OBJECTS

</td><td>

MDSYS.SDO\_GEOM\_METADATA\_TABLE

</td><td>

V$CONTAINERS

</td></tr><tr><td>

DBA\_RECYCLEBIN

</td><td>

MGMT$TARGET

</td><td>

V$DATABASE

</td></tr><tr><td>

DBA\_REGISTRY

</td><td>

ODM.ODM\_MINING\_MODEL

</td><td>

V$DATAGUARD\_CONFIG

</td></tr><tr><td>

DBA\_SQLSET

</td><td>

ODM\_DOCUMENT

</td><td>

V$LICENSE

</td></tr><tr><td>

DBA\_SQLSET\_REFERENCES

</td><td>

ODM\_RECORD

</td><td>

V$OPTION

</td></tr><tr><td>

DBA\_SQL\_PROFILES

</td><td>

REDACTION\_POLICIES

</td><td>

V$PARAMETER

</td></tr><tr><td>

DBA\_TABLES

</td><td>

SCHEMA\_VERSION\_REGISTRY

</td><td>

V$SESSION

</td></tr><tr><td>

DBA\_TABLESPACES

</td><td>

SYS.CDC\_CHANGE\_SETS$

</td><td>

V$VERSION

</td></tr><tr><td>

DBA\_TAB\_PARTITIONS

</td><td>

SYS.CDC\_CHANGE\_TABLES$

</td><td>

dba\_aws

</td></tr><tr><td>

DBA\_TAB\_SUBPARTITIONS

</td><td>

SYS.DBA\_MINING\_MODELS

</td><td>

 

</td></tr></tbody>
</table>-   **Create applicative credentials for Oracle Instance**

    Create applicative credentials on the ServiceNow AI Platform. For more information, see [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

-   **For virtual machines: Verify virtual machine credentials**

    For virtual machines, verify you have the relevant credentials to collect hardware data for machines hosted on the following virtual providers:

    -   VMware
    -   Nutanix
    -   IBM
    -   Hyper-V

## Database CI relationships

|CI|Relationship/Reference|CI|
|---|----------------------|---|
|cmdb\_ci\_orcl\_vsession|Contains::Contained By|cmdb\_ci\_db\_ora\_instance|
|cmdb\_ci\_ora\_lms\_detail|Contains::Contained By|cmdb\_ci\_db\_ora\_instance|
|cmdb\_ci\_ora\_lms\_overview|Contains::Contained By|cmdb\_ci\_db\_ora\_instance|
|cmdb\_ci\_orcl\_options|Contains::Contained By|cmdb\_ci\_db\_ora\_instance|
|cmdb\_ci\_orcl\_dba\_users|Contains::Contained By|cmdb\_ci\_db\_ora\_instance|
|cmdb\_ci\_orcl\_vlicense|Contains::Contained By|cmdb\_ci\_db\_ora\_instance|

## Tuxedo middleware extension

Tuxedo license configuration and log files collected:

-   \*\_InstallLog.log
-   \*ubbc\*
-   bdmconfig\*
-   comps.xml
-   dmconfig\*
-   JSconfig.xml
-   lic.txt
-   registry.xml
-   tuxconfig\*
-   tuxwsvr.ini

**Note:** The asterisk represents one or more characters in the file name.

Processes collected:

-   BBL
-   DBBL
-   GWWS
-   JSH
-   JSL
-   TMJAVASVR
-   TMMETADATA

## WebLogic middleware extension

Files collected:

-   beahomelist
-   biee-domain.xml
-   cluster.properties
-   comps.xml
-   config.xml
-   domain-registry.xml
-   opmn.xml
-   portalconfig.xml
-   pthome.xml
-   registry.xml
-   server.xml
-   sessions.xml
-   setupinfo.txt

WebLogic processes and files collected for the following middleware products:

-   WebLogic
-   OAS
-   SOA
-   OBI
-   WebCenter
-   FormsReports

|WebLogic|OAS|OBI|
|--------|---|---|
|startWebLogic|httpd|f90|iooomgrrmi|r30rbe32|rwrqm60|nqsserver|
|java|apache|frmweb|javaw|r30rqm32|rwrqm|sawserver|
|startWLS|java|ifbld60|java|r30run32|rwrun60|coreapplication\_obijh1|
|nodemanager|opmn|ifbld90|jre|r30sxc32|rwserver|nqscheduler|
|beasvc|dis3|ifcgi60|oad|r30sxu32|rwsxc60|nqsclustercontroller|
|beasvc64|dis4|ifcmp60|odisrv|rwbld60|rwsxu60|essbase|
|beasvcX64|dis51pr|ifcmp90|ofcguard|rwbuilder|vdeserver|essvr|
|oraclesvc|dis51ws|ifctrl60|oidrepld|rwcgi60|webcachea|essbasestudio|
|opmn|dis51|ifdbg60|oidmon|rwcli60|webcached|hyperion|
|wlsvc|dwfde61|ifrun60|oidldapd|rwcon60|webcache| |
|wlsvc64|f45des|ifsrv60|opmn|rwconverter| | |
|wlsvcX64|f45run|ifwdb60|r30cli32|rwisv60| | |
|jmc|f50dbg32|ifweb60|r30con32|rwmts60| | |
|httpd|f50run32|ifweb90|r30isv32|rwqmu60| | |
|jrmc|f60|imapds|r30qmu32|rwrbe60| | |

## Middleware CI relationships

|CI|Relationship/Reference|CI|
|---|----------------------|---|
|cmdb\_ci\_ora\_lms\_overview|Contains::Contained by|cmdb\_ci\_linux\_server|
|cmdb\_ci\_config\_file\_tracked|Contains::Contained by|cmdb\_ci\_linux\_server|

These relationships are created by a containment rule that describes the valid objects that the Linux CIs can contain.

## Properties installed with the Middleware data collection application

To access the installed application properties, navigate to **All** &gt; **System Properties** &gt; **All Properties**. You must have the admin role to modify these properties.

|System property|Default value|Description|
|---------------|-------------|-----------|
|**sn\_itom\_oracleglas.isMaskingIp**|true|Determines whether to mask the IP Address in Oracle middleware tracked files by replacing the value with "text\_removed."|
|**sn\_itom\_oracleglas.isMaskingUserName**|true|Determines whether to mask the user name in Oracle middleware tracked files by replacing the value with "text\_removed."|
|**sn\_itom\_oracleglas.isMaskingPort**|true|Determines whether to mask the port in Oracle middleware tracked files by replacing the value with "text\_removed."|

## Control GLAS data collection

The following MID Server property controls the GLAS data collection: **sn\_itom\_oracleglas.disable\_glas\_data\_collection**

The property is set to **False** by default.

**Note:** In Data Collection for Oracle Global Licensing and Advisory Services versions earlier than 1.10.2, the property name is **sn\_itom\_pattern.disable\_glas\_data\_collection**.

## Oracle Java process discovery

ITOM Visibility can discover Java-running processes in your infrastructure, allowing you to comply with Oracle licensing agreements and prepare for GLAS Audits. You can perform the discovery using the Java Installation pattern \(IP-based\), Agent Client Collector with application patterns, or Agent Client Collector with file-based discovery.

In the pattern flow, the Java processes are discovered by Application Dependency Mapping \(ADM\). When the processes are discovered, the Java Installation pattern triggers and collects the data.

For information about privileged user access, see [KB1705845](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705845).

For more information about Agent Client Collector with patterns, see [Application patterns for the Agent Client Collector](../../agent-client-collector/concept/application-patterns-acc.md).

For more information about Agent Client Collector with file-based discovery, see [Discover java installation data using Agent Client Collector for Visibility - Content file-based discovery](../../agent-client-collector/task/acc-file-based-discovery.md).

-   **Data collected**

    |Field|Description|
    |-----|-----------|
    |Name|Name of the record. For example: Java@hostname|
    |Physical Machine Name|Name of the host CI|
    |Machine Type|Either Server\(S\) or Desktop\(D\)|
    |Java Publisher/Runtime Vendor|Java Vendor name|
    |Operating System|Operating system in which the java is run|
    |Environment Type|Production or Development or QA environment|
    |Java Release/Version/Build|Java Version|
    |Installation Path|Absolute installation path of the java binary|
    |Installation Date \(DateTime\)|The date and time of the java binary file created on the filesystem|
    |Release File \(Y / N\)|Indicates if a *release.md* file exists in the installation|
    |Processor Make/Model|Processor model name|
    |Sockets \(Integer\)|Number of CPU sockets|
    |Cores \(Integer\)|Number of CPU cores|
    |V6 and earlier|Indicates if you have a 6 or earlier java version|
    |Open Source|Indicates if you have an open-source java installation|
    |Unlock Commercial features|Indicates if you have the commercial features \(like JFR\) enabled|
    |Mission Control|Indicates if the mission control plugin is enabled|
    |AMC Agent|Indicates if the AMC agent plugin is enabled|
    |Usage Tracker|Indicates if the Usage Tracker feature is enabled|
    |Virtual Machine Object ID|Object ID of the Virtual machine instance|
    |PID|Running process PID|
    |IP Address|IP address of the host/VM|
    |First Discovered|The date of the first discovery|
    |Most recent discovery|The date of the most recent discovery|
    |Discovery Source|The discovery method.|
    |Application|Reference to the \[cmdb\_ci\_appl\] table|
    |Software installation|Reference to the \[cmdb\_sam\_sw\_install\] table|
    |Java evidence|Reference to the \[cmdb\_ora\_java\_evidence\] table|
    |Host|Reference to the \[cmdb\_ci\] table|

-   **Java Evidence \[ora\_java\_evidence\]**

    |Field|Description|
    |-----|-----------|
    |Running process|Reference to the \[cmdb\_running\_process\] table|
    |Host CI|Reference to the \[cmdb\_ci\_computer\] table|
    |File information|Provides a reference to the \[cmdb\_file\_information\] table. Relevant only for file-based discovery \(FBD\); in pattern-based discovery, this field remains empty.|


Download the Oracle GLAS report in the Discovery Admin Workspace. For more information, see [Download Oracle Global License Advisory Services \(GLAS\) data](../task/download-oracle-glas-data.md).

## Oracle GLAS Data Collection

After Discovery finishes discovering the components of your database or middleware deployment, you can view the relevant statistics in the Oracle GLAS Data Collection.

After upgrading to Discovery Admin Workspace version 1.3.1 \(August 2024 Store\), you can navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** to view and access the Oracle GLAS Data Collection.

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

