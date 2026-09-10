---
title: Data Collection for Oracle Global Licensing and Advisory Services release notes
description: Version history for the Data Collection for Oracle Global Licensing and Advisory Services on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-data-collection-oracle-global.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - ITOM Visibility version history release notes, ServiceNow Store - IT Operations Management version history release notes, ServiceNow Store version history release notes]
---

# Data Collection for Oracle Global Licensing and Advisory Services release notes

Version history for the Data Collection for Oracle Global Licensing and Advisory Services on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.13.0 - September 2026**
    -   New: Discover Oracle Databases on Windows using Oracle Wallet instead of storing applicative credentials in the ServiceNow instance.
    -   Fixed:
        -   The Data Collection for Oracle Global Licensing and Advisory Services plugin doesn't include a plugin.properties file, which affects plugin identification and packaging. \(PRB2070400\)
        -   When top-down Discovery runs the "Oracle DB On Unix" pattern, an extension section intended only for Horizontal Discovery also executes. This can overwrite Oracle database instance CI records, and subsequent IRE processing fails when required attributes such as SID and TCP port are missing from the payload. \(PRB2026132\)
        -   The access control for the Oracle GLAS Linux server export processor report attachment doesn't work correctly. \(PRB2068165\)
        -   Oracle database instances can be related to Oracle options belonging to a different instance, and options can be reported as In Use when they are not, resulting in incorrect license calculations. \(PRB1872945\)
        -   Security fixes. \(PRB2033903, PRB2023675, PRB2023674, PRB2023673\)
        -   Top-down discovery of an Oracle database fails when the connection originates from J2EE EAR connectivity. \(PRB2025288\)
        -   Files uploaded for script execution don't honor the MID Server property mid.powershell.target\_base\_dir and aren't written to the configured directory. \(PRB2058696\)
        -   Oracle GLAS data collection causes replication lag, slow Oracle Instance CI form loading, and query timeouts due to large data volumes. \(PRB1786627\)
        -   The WebLogic discovery pattern doesn't load in Pattern Designer. \(PRB2076886\)
        -   OpenJDK installation paths aren't classified as open source, causing Java installations using OpenJDK to be reported as licensable. \(PRB2028988\)
        -   The OPTION\_QUERY field is stored with a null value in the Oracle GLAS Database Audit Data \[sn\_itom\_oracleglas\_glas\_data\_for\_database\] table, resulting in incomplete option usage data. \(PRB2030384\)
        -   Oracle GLAS V1 and V2 data collection doesn't run in Windows environments. \(PRB2061491\)
        -   Oracle GLAS data collection doesn't create the Windows hardware script output file in the directory defined by the MID Server property mid.powershell.target\_base\_dir. \(PRB2067798\)
        -   During Oracle GLAS discovery on Windows, the connection identifier isn't set, and the GLAS output folder is assigned an incorrect temporary path, causing data collection to fail. \(PRB2054115\)
-   **Version 1.12.0 - June 2026**
    -   New:
        -   Scale Oracle GLAS data collection in large environments with Oracle GLAS V2, which collects all database data into a single table \[sn\_itom\_oracleglas\_glas\_data\_for\_database\].
        -   Discover Oracle Databases on UNIX using Oracle Wallet instead of storing applicative credentials in the ServiceNow instance.
    -   Fixed:
        -   The Oracle GLAS Java report correctly deduplicates entries when Java audit records are missing host information. \(PRB1983591\)
        -   Oracle GLAS no longer counts the Oracle OLAP option as a separately licensed component for Oracle Database starting with 19c. \(PRB2011315\)
        -   The "Java Installation" pattern no longer crashes when executing jinfo and java.exe commands, preventing JVM crash log files \(hs\_err\_pid\) from filling up the file system. \(PRB1995020\)
-   **Version 1.11.1 - March 2026**
    -   Fixed:
        -   The Data Collection for Oracle Global Licensing and Advisory Services app installation no longer generates errors related to the file "sys\_report\_users\_groups\_56d8afcb1b1001109451eb15624bcb63.xml." \(PRB1959057\)
        -   The "Java Installation" pattern now updates the Last scanned \[last\_scanned\] and Updated \[sys\_updated\_on\] fields in the Software Installation \[cmdb\_sam\_sw\_install\] table on each discovery run. \(PRB1971286\)
-   **Version 1.11.0 - December 2025**
    -   Fixed:
        -   The "Oracle DB On Unix" and “Oracle DB On Windows” extension sections create CSV files with data for Oracle Pluggable Database \(PDB\) \(PRB1936680\).
        -   Oracle GLAS Data Collection deletes the directory and CSV files that were created on the target server after discovery is successfully finished \(PRB1934167\).
        -   The downloaded Oracle Java GLAS Data zip folder can be opened using the built-in Windows zip application \(PRB1920590\).
        -   Removed the underscore from the label in Oracle GLAS Data navigation menu to support internationalization \(i18n\). For example: ORCL\_DETAIL is now ORCL DETAIL \(PRB1908120\).
        -   The Oracle GLAS report doesn’t fail when there are multiple Java Audit \[ora\_java\_audit\] records with the same Host CI names \(PRB1927138\).
        -   The Oracle GLAS Data Collection terminates for non-SQL extension if the middleware components are not running \(PRB1909285\).
        -   The Java Audit \[ora\_java\_audit\] and Software Installation \[cmdb\_sam\_sw\_install\] tables are automatically cleaned up \(PRB1902045\).
-   **Version 1.10.2 - August 2025**
    -   Fixed:
        -   Refined the JOB level logging for "SAM - Evaluate database option usage from Oracle GLAS data" so that it improves performance \(PRB1879145\).
        -   The "Oracle Instance" class is fixed not to create Orphan records \(PRB1889319\).
        -   The "Oracle GLAS - Collect Middleware Data for Tuxedo" is fixed, a Library on Library Reference step can now be added \(PRB1894357\).
        -   The Oracle GLAS discovery is now creating a folder under the absolute path \(PRB1887847\).
        -   The Oracle Options table now shows the correct value in the "Currently Used" field \(Oracle Cloud Management Pack for Oracle Database, Oracle Data Masking and Sub-setting Pack, and Oracle Database Lifecycle Management Pack for Oracle Database\) \(PRB1905211\).
    -   Changed:
        -   The MID Server property to disable Oracle GLAS Data Collection has been renamed from "sn\_itom\_pattern.disable\_glas\_data\_collection" to correct store app prefix value "sn\_itom\_oracleglas.disable\_glas\_data\_collection" \(PRB1885418\).
-   **Version 1.10.0 - May 2025**
    -   New: As part of Oracle GLAS DB 25.2 requirements, we updated reporting for changed records:
        -   Rowcount has been added at the end of the VMware files.
        -   New columns for VMCreateDate and VMPowerState have been added to the VM HW file.
    -   Fixed:
        -   The Discovery property "glide.discovery.enable\_file\_tracking" is now honored by Oracle GLAS Data Collection. By default, glide.discovery.enable\_file\_tracking" property is set to true \(PRB1849553\).
        -   The Oracle GLAS Data Collection for Non-SQL extension now does not leave behind the hostname-info.txt and hostname-opmn\_output.txt files in the /temp folder when executing the "Linux Server" pattern \(PRB1854870\).
-   **Version 1.8.5 - February 2025**
    -   Fixed:
        -   The "Download GLAS Data Collection" UI page for the Oracle Java report is fixed \(PRB1815267\).
        -   The "Oracle DB on Unix" deletion strategy has been improved to include a new MID Server property "sn\_itom\_pattern.disable\_glas\_data\_collection". This ensures the deletion strategy does not execute for Oracle options if they were not collected \(PRB1755961\).
-   **Version 1.8.4 - November 2024**
    -   New:
        -   New feature: Oracle Java process and data collection \(for both software installation and hardware reporting details\).
            -   You can perform the discovery using either the Java installation pattern \(IP-based\) or Agent Client Collector.
            -   Tables included:
                -   Java Audit \[ora\_java\_audit\]
                -   Java Evidence \[ora\_java\_evidence\]
            -   If you are on an earlier family release, before Yokohama, you must download the update set from [KB1705854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705845)
    -   Fixed: The Oracle GLAS Data Collection pattern is fixed to address the discrepancy between the value of the "DB\_NAME" field in "cmdb\_ci\_orcl\_option" and the DB containing that option \(PRB1790036\).
-   **Version 1.8.0 - August 2024**
    -   Fixed:
        -   Oracle GLAS Middleware components "\*.info.txt" file content contains all process information
        -   Discovery is attempting to use "sudo" when the MID Server is configured to use "pbrun" or "dzdo"
-   **Version 1.7.11 - May 2024**
    -   Fixed:
        -   Oracle GLAS - collect middleware data for the extension of the WebLogic pattern and Oracle GLAS data for the non-SQL extension of the Linux Server pattern.
            -   Collects the below-mentioned middleware product missing files and creates tracked configuration files \(cmdb\_ci\_config\_file\_tracked\)
                -   WebLogic 11g and 12
                -   BIEE 11g and 12c
                -   SOA 11 and 12
                -   WebCenter Content
                -   WebCenter Portal
                -   WebCenter Sites
        -   The name of the Fusion Middleware output folder utilizes a capital letter for the initial character
        -   The Oracle GLAS Data Collection extension, Oracle DB on Windows and Oracle DB on Unix patterns collect Oracle option data for Pluggable Database \(PDB\)
    -   Removed:
        -   Tracked file definitions within the WebLogic patterns
            -   inventory\_folder
            -   config\_directory
            -   domain\_registry\_folder
            -   server\_xml\_folder
            -   domain\_directory
            -   soa\_comps\_xml\_folder
            -   weblogic\_comps\_xml\_folder
-   **Version 1.7.9 - November 2023**
    -   Fixed:
        -   "SAM - Evaluate database option usage from Oracle GLAS data" job was failing.
        -   Export Utility - Masking of data is done for username, IP, Port even if the masking system property is set to False
-   **Version 1.7.7 - August 2023**

    Fixed:

    -   ""Oracle GLAS Data Collection"" pattern had performance issues on the instance
    -   Oracle per Processor Licensing calculations issue with retired servers
    -   ""Data Collection for Oracle Global Licensing and Advisory Services' plugin upgrade to V 1.7.5 skipped the cmdb\_metadata\_containment\_adf1382fdbfaf30003a05561ca961947' record, an OOTB record
    -   ""Oracle GLAS Data Collection"" pattern extension identification errors
    -   Oracle GLAS data was populated for multiple databases
    -   Oracle GLAS Session wasn't populated
    -   GLAS data was discovered for both CDB and PDB from the server
-   **Version 1.7.5 - February 2023**
    -   Fixed:
        -   Oracle GLAS Collection Pattern extension exists if PDBs are not discovered for Oracle 11
        -   report\_view ACLs for platform tables.
-   **Version 1.7.3 - October 2022**

    Fixed: Oracle Glass Data pattern error "ORA-12504: TNS:listener was not given the SERVICE\_NAME in CONNECT\_DATA" even though the service name is provided

-   **Version 1.7.1 - June 2022**
    -   New: Oracle MiddleWare information collection
    -   Fixed:
        -   GLAS Oracle LMS script execution step is fails in RAC environment where host is not primaryhost
        -   Discovery users are unable to access "HMC server" records after installing Store Application "Data Collection for Oracle Global Licensing and Advisory Services" plugin due an ACL
-   **Version 1.7.0 - May 2022**
    -   New: Usage of Oracle Option collected by GLAS App for SAM Licensing.
    -   Fixed:
        -   Incorrect value in runtime\_access\_tracking in sys\_app xml.
        -   Feature string "Application Continuity" for RAC option is not evaluated as 'In use'.
        -   \[Perf Scale\] cache\_flush \| Patterns Category is using one or more plugins that clear caches on upgrade.
-   **Version 1.4.3 - July 2021**

    Fixed: Not all of the "in-use" options are populated in the "orcl\_options" table.

-   **Version 1.4.2 - June 2021**
    -   Fixed:

        -   Discovery created unexpected formatted records in the cmdb\_ci\_orcl\_options table.
        -   For Oracle LMS, the Options data table was not updated and cleaned up. LMS Data was creating duplicates.
        -   GLAS Store app certification issues.
-   **Version 1.4.0 - March 2021**
    -   New:
        -   Oracle Pattern extension support to collect GLAS/LMS data.
        -   ServiceNow navigation menu to access GLAS data.
        -   CSV export utility.

**Parent Topic:**[ServiceNow Store - ITOM Visibility version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-visibility-landing.md)

