---
title: Download Oracle Global License Advisory Services \(GLAS\) data
description: Download Oracle GLAS data in CSV format to get detailed information on patterns and configuration items. You can also download reports for Oracle Database, Middleware, Oracle Java, VM, and vCenter hardware information.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-01-14"
reading_time_minutes: 4
breadcrumb: [Oracle GLAS data collection, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Download Oracle Global License Advisory Services \(GLAS\) data

Download Oracle GLAS data in CSV format to get detailed information on patterns and configuration items. You can also download reports for Oracle Database, Middleware, Oracle Java, VM, and vCenter hardware information.

## Before you begin

To download Oracle GLAS Java report for versions earlier than Washington DC Patch 9 and Xanadu Patch 3, see [KB1704359](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704359).

Role required: admin or glas\_admin

## About this task

ServiceNow maintains regular verification with Oracle GLAS to provide you with insights on licensing data for your Oracle estate. The following Oracle GLAS reporting versions are currently verified:

-   Database: 25.2
-   Middleware: 23.2
-   Java: 24.4

## Procedure

1.  Navigate to **All** &gt; **Oracle GLAS Data Collection** &gt; **Download GLAS Data Collection**.![Oracle GLAS download page](../image/oracle-glas-download.png)

2.  Download the following reports for Oracle GLAS data:

    -   For downloading Oracle Database, Middleware, and Java reports, navigate to **Step 1: Download GLAS Data Collection** and select your data collection options.
    -   For downloading vCenter hardware information based on your environment setup, navigate to **Step 2: Download vCenter Hardware Information**.
    -   For downloading VM information, navigate to **Step 3: Download VM Information**.
3.  Select the download icon \(![Download icon](../image/download-icon.png)\).

4.  In the Enter email address dialog box, enter the email address where you want to receive a notification when the report is ready.

5.  Select **OK**.

    After the report creation status message appears, you can check the status of the download job by selecting the link provided in the message.

    ![Message for report creation status](../image/report-creation-msg.png)

    The Oracle GLAS Report Job Log \[sn\_itom\_oracleglas\_job\_log\] table opens in a new window. After your report is successfully created, the status of the report changes to Complete in the Oracle GLAS Report Job Logs table.

6.  Select a job log record to view its details including the unique number, name, status, description, and the date and time when the job log is created and updated.

7.  On the Oracle GLAS Report Job Log form that opens, download your report by navigating to **Manage Attachments** and selecting **download**.

    -   Depending on your selection in **Step 1: Download GLAS Data Collection**, the following folders are downloaded:

        -   **Oracle Database**
            -   DB folder – contains the following CSV files:
                -   `ORCL_V$SESSION.csv`
                -   `ORCL_OPTIONS.csv`
                -   `ORCL_DBA_USERS.csv`
                -   `ORCL_DETAIL.csv`
                -   `ORCL_V$LICENSE.csv`
                -   `ORCL_OVERVIEW.csv`
            -   CPUQ folder – contains CPUQ files, vCenter Hardware, and VM information
        -   **Oracle Middleware**

            The following files are exported, where the file name reflects your server name and Oracle product:

            -   ORCL\_OVERVIEW.csv
            -   `Collection-<Server Name>_<Oracle Product>.tar.bz` with the files and directories of the format FMW/u01/app/oracle/config/domains/soa\_domain/config/config.xml in it
        -   **Oracle Java**
            -   Java folder – contains Java installation information

                **Note:** The report that you download for Oracle Java GLAS includes only Java deployments from the Oracle publisher. Java deployments from non‑Oracle publishers are excluded from the report.

            -   CPUQ folder – contains CPUQ files, vCenter Hardware, and VM information
    -   If you selected **Step 2: Download vCenter Hardware Information**, one hardware inventory CSV file is downloaded per vCenter in your environment.
    -   If you selected **Step 3: Download VM Information**, one VM information CSV file is downloaded per vCenter in your environment.
    **Note:** You can also download the CSV files for Oracle Database by navigating to **Oracle GLAS Data Collection** &gt; **Oracle GLAS Data**. From the list that opens, select the table that you want to download and then select **Download GLAS Report**.


## Result

The downloaded files appear in the location that you select.

If the files are empty or contain an error message, check their sizes to verify that they haven't exceeded the limits set in the following properties. Navigate to **All** &gt; **System Properties** &gt; **All Properties** to find the following properties.

**Important:** Consult with ServiceNow support before changing these properties.

<table id="table_w1f_cgc_ddc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.discovery.file\_tracking.max\_file\_size**

</td><td>

The maximum file size for tracked configuration file content.

 Type: integer

 Default value: 500000

</td></tr><tr><td>

**glide.discovery.file\_tracking.max\_files\_per\_ci**

</td><td>

The maximum number of tracked configuration files per CI.

 Type: integer

 Default value: 50

</td></tr><tr><td>

**glide.discovery.file\_tracking.change\_limit\_count**

</td><td>

Number of changes permitted on a tracked configuration file in the defined time window.

 Type: integer

 Default value: 4

</td></tr><tr><td>

**glide.discovery.file\_tracking.change\_limit\_days**

</td><td>

Time window \(in days\) that limits the number of changes on a tracked configuration file.

 Type: integer

 Default value: 7

</td></tr></tbody>
</table>If you receive an error `Error: Skipped sensor for Horizontal Pattern because of error in payload: Payload length 5056040 exceeded the limit of 300000`, verify that the payload hasn't exceeded the system limit. Navigate to **All** &gt; **MID Server** &gt; **Properties** to find the following properties.

<table id="table_ls3_2gc_ddc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**mid.discovery.max\_payload\_size**

</td><td>

Defines the maximum overall payload size for the payload of results that come from patterns.

 Type: integer \(bytes\)

 Default value: 300000

</td></tr></tbody>
</table>If you receive an SSH timeout error, you must create and set the following properties. See "Create a MID Server property" in [MID Server Properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for details.

<table id="table_x43_2gc_ddc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**mid.ssh.command\_timeout\_ms**

</td><td>

Number of milliseconds an SSH command is permitted to run before timing out \(default is configurable per MID Server\).

 Type: integer

</td></tr><tr><td>

**mid.sa.ssh.timeout**

</td><td>

The SSH timeout in milliseconds.

 Type: integer

</td></tr><tr><td>

**channel\_timeout\_ms**

</td><td>

The amount of time, in milliseconds, that a MID Server waits for activity when processing an SSH command. If the MID Server doesn’t detect activity within the specified window, the system terminates the command.

 Type: integer

</td></tr></tbody>
</table>**Parent Topic:**[Oracle Global License Advisory Services \(GLAS\) data collection using patterns](../reference/oracle-glas-discovery.md)

