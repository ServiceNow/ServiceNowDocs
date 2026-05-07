---
title: Oracle GoldenGate discovery
description: The ServiceNow Discovery and Service Mapping applications find Oracle GoldenGate version 12c components using the Oracle Golden Gate pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle GoldenGate discovery

The ServiceNow Discovery and Service Mapping applications find Oracle GoldenGate version 12c components using the Oracle Golden Gate pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses the Oracle Golden Gate pattern to perform horizontal discovery to collect data into the `$report_file` file. Service Mapping performs top-down discovery on the `$report_file` file to find outgoing Oracle Golden Gate connections.

The Oracle Golden Gate pattern supports the following platforms: AIX, Linux Hewlett Packard, and Solaris.

You can use this pattern on the ServiceNow AI Platform using Kingston, London, or Madrid.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Oracle Golden Gate data model

The Oracle Golden Gate pattern introduces the following CI classes that extend an existing CMDB class.

|CI class|Extends from|
|--------|------------|
|Oracle Golden Gate \[cmdb\_ci\_appl\_oracle\_golden\_gate\]|Application \[cmdb\_ci\_appl\]|
|Oracle Golden Gate Replicat Process \[cmdb\_ci\_appl\_ora\_gg\_replicat\]|Application \[cmdb\_ci\_appl\]|
|Oracle Golden Gate Extract Process \[cmdb\_ci\_appl\_ora\_gg\_extract\]|Application \[cmdb\_ci\_appl\]|

## Prerequisites

-   **Credentials**

    Configure the SSH credentials, for the operating system of the server that hosts the Oracle Golden Gate Server.

-   **User access**

    Give the UNIX OS user permissions to read the `$report_file`. The `$report_file` is the report file that is extracted from the Oracle Golden Gate `manager/replicat/extract` process, with the extension `.rpt`. For example:

    Configuration file:

    ```
    /base/ggs_beta/oracle/bt01pims/ggs/dirprm/mgr.prm REPORTFILE 
    ```

    Report file:

    ```
    /base/ggs_beta/oracle/bt01pims/ggs/dirrpt/MGR.rpt PROCESSID MGR
    ```

-   **Permissions to run commands**

    The OS user must have permissions to run the relevant OS commands for each supported platform.

    Give the UNIX OS user permissions to run the following commands against the Oracle Golden Gate Server:

<table id="table_pw3_lgn_zfb"><thead><tr><th>

Command

</th><th>

Mandatory/Optional

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`$sudo + " ls -d " + $rpt_base_dir + "*.rpt | sort "`

</td><td>

Mandatory

</td><td>

List all report files under the Oracle Golden Gate report base directory.

</td></tr><tr><td>

`$sudo + " ls -d " + $prm_base_dir + "*.prm| sort "`

</td><td>

Mandatory

</td><td>

List all parameter files under the Oracle Golden Gate parameter base directory.

</td></tr></tbody>
</table>-   **Retrieve data**

    Retrieve data by parsing:

    -   The Oracle Golden Gate manager report file \(report\_file\) to retrieve related configuration item \(CI\) names and counter information.
    -   Variables in the process command line to retrieve the install folder, manager process name, configuration file, and parameters file.
    -   Variables in the Oracle Golden Gate installation folder to retrieve a list of parameter and configuration files.
-   **EVAL closure functions**

    Use the following EVAL closure functions to remove duplicate entries from the extract process and the replicat process.

    -   var tableWithoutDuplicates = '';tableWithoutDuplicates = DuplicateRemover.removeDuplicates\($\{extracts\},\["name"\]\);CTX.setAttribute\("extracts", tableWithoutDuplicates\);
    -   var tableWithoutDuplicates = '';tableWithoutDuplicates = DuplicateRemover.removeDuplicates\($\{replicats\},\["name"\]\);CTX.setAttribute\("replicats", tableWithoutDuplicates\);
    Use the following EVAL closure functions to count the number of extract processes and replicat processes.

    ```
    return ${cmdb_ci_appl_ora_gg_replicat[*].config_file}.size()
    return ${cmdb_ci_appl_ora_gg_extract[*].config_file}.size()
    ```

    Use the following EVAL closure function to return the privileged command.

    ```
    return ${ctx}.getDiscoveryProvider(com.snc.sw.dto.ProviderType.SSH).getPrivilegedCommand();
    ```

    Use the following EVAL closure function to return the discovery type.

    ```
    ctx.getWork().getDiscoveryType();
    ```

    Use the following EVAL closure function to extract the version from the installation directory path if it is empty.

    ```
    inst_dir = ${install_directory}if(inst_dir.isEmpty()){return ${version}}if(inst_dir.startsWith('/')){return inst_dir.replaceAll('/.*/','')}if(!inst_dir.startsWith('/') && !inst_dir.isEmpty()){return inst_dir.replaceAll('.*\\\\','')}
    ```


-   **Applicative credentials**
    1.  Navigate to **Discovery** &gt; **Credentials**.
    2.  Click **New**.
    3.  Click **Applicative Credentials**.
    4.  On the form, fill in the fields.

<table id="table_vkj_ft3_hhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Credential name. An example is oracle\_db\_user.

</td></tr><tr><td>

Active

</td><td>

Option for enabling this credential for discovery. Select this check box to enable discovery.

</td></tr><tr><td>

Applies to

</td><td>

Credentials that you may or may not want to apply to **All MID servers** in your network, or to one or more **Specific MID servers**. Select **Specific MID servers**.

</td></tr><tr><td>

MID Servers

</td><td>

MID Servers that the credentials apply to. Select the required MID Server. This field appears when **Specific MID servers** is selected from the **Applies to** field.

</td></tr><tr><td>

Order

</td><td>

Order in which the platform tries this credential as it attempts to log on to devices. A smaller number indicates that the credential appears higher in the list. Establish the credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number, or none, the instance tries the credentials in a random order. The default value is **100**.

</td></tr><tr><td>

User name

</td><td>

Name of the user of this applicative credential. An example is oracle\_db\_user. You can use any user for the credential for this pattern, because the information is extracted from a local cache.

</td></tr><tr><td>

Password

</td><td>

Not required. You can leave this field blank or enter any value.

</td></tr><tr><td>

CI type

</td><td>

CI type for which this credential is used: Storage Server \[cmdb\_ci\_storage\_server\]. **Note:** ServiceNow applications refer to devices and applications that comprise a service instance as configuration items \(CIs\).

</td></tr></tbody>
</table>    5.  Click **Submit**.
-   **Entry point**

    For top-down discovery, use the Oracle Golden Gate IP address and specify the MID Server.


## Data collected by Discovery during horizontal discovery

Discovery uses the Oracle Golden Gate pattern to collect the data described in the following tables.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the CI in the CMDB \(&lt;process name&gt;@&lt;source db&gt;\).|
|Version \[version\]|Version of the Oracle Golden Gate installation.|
|Source DB SID \[source\_db\]|Manager process source database system identifier \(SID\).|
|Counter for replicat processes \[count\_replicat\]|Counter of replicat processes that are managed by the Oracle Golden Gate manager instance.|
|Counter for extract processes \[count\_extract\]|Counter of extract processes that are managed by the Oracle Golden Gate manager instance.|
|Configuration file \[config\_file\]|Parameter file of the Oracle Golden Gate process. Specify the path to the configuration file and the file name, &lt;name&gt;.prm|
|Replicat File \[report\_file\]|Report file of the Oracle Golden Gate process. Specify the path to the report file and the file name, &lt;name&gt;.rpt|
|Type \[type\]|Type of the Oracle Golden Gate installation. Specify the Oracle Golden Gate for Oracle technologies.|
|Installation directory \[install\_directory\]|Folder that contains all the Oracle Golden Gate setup, configuration, libraries, and executable files.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the CI in the CMDB \(&lt;process name&gt;@&lt;source db&gt;\).|
|Replicat File \[report\_file\]|Replicat process report file. Specify the path to the report file and the file name &lt;name&gt;.rpt|
|Configuration file \[config\_file\]|Parameter file of the replicat process. Specify the path to the configuration file and the file name &lt;name&gt;.prm|
|Installation directory \[install\_directory\]|Folder that contains all the Oracle Golden Gate setup, configuration, libraries, and executable files.|
|Version \[version\]|Version of the Oracle Golden Gate installation.|
|Source DB SID \[source\_db\]|Manager process source database SID.|
|Operational status \[operational\_status\]|Operational status of the CI. Select **Operational**.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the CI in the CMDB \(&lt;process name&gt;@&lt;source db&gt;\).|
|Replicat File \[report\_file\]|Report file of the extract process. Specify the path to the report file and the file name &lt;name&gt;.rpt|
|Configuration file \[config\_file\]|Parameter file of the extract process.|
|Version \[version\]|Version of the Oracle Golden Gate installation.|
|Installation directory \[install\_directory\]|Folder that contains all the Oracle Golden Gate setup, configuration, libraries, and executable files.|
|Source DB SID \[source\_db\]|Manager process source database SID.|
|Operational status \[operational\_status\]|Operational status of the CI. Select **Operational**.|

The Dependency Views map shows discovered load balancer CIs and the relationships between them.

![CIs and connections on a Dependency Views map](../image/GoldenGateRelations.png)

## CI relationships

The Oracle Golden Gate pattern creates the following relationships to support Oracle Golden Gate discovery.

|CI|Relationship|CI|
|---|------------|---|
|Oracle Golden Gate \[cmdb\_ci\_appl\_oracle\_golden\_gate\]|Managed by::Manages|Oracle Golden Gate Replicat Process \[cmdb\_ci\_appl\_ora\_gg\_replicat\]|
|Oracle Golden Gate \[cmdb\_ci\_appl\_oracle\_golden\_gate\]|Managed by::Manages|Oracle Golden Gate Extract Process \[cmdb\_ci\_appl\_ora\_gg\_extract\]|
|Oracle Golden Gate \[cmdb\_ci\_appl\_oracle\_golden\_gate\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|
|Oracle Golden Gate Replicat Process \[cmdb\_ci\_appl\_ora\_gg\_replicat\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|
|Oracle Golden Gate Extract Process \[cmdb\_ci\_appl\_ora\_gg\_extract\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|

## Data collected by Service Mapping during top-down discovery

To discover the Oracle Golden Gate process, use the TCP entry point with the proper host and port of the Oracle Golden Gate process.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the CI in the CMDB \(&lt;process name&gt;@&lt;source db&gt;\).|
|Version \[version\]|Version of the Oracle Golden Gate installation.|
|Installation directory \[install\_directory\]|Folder that contains all the Oracle Golden Gate setup, configuration, libraries, and executable files.|
|Configuration file \[config\_file\]|Parameter file of the Oracle Golden Gate process.|
|Replicat File \[report\_file\]|Report file of the Oracle Golden Gate replicat process.|
|Source DB SID \[source\_db\]|Manager process source database SID.|
|Counter for extract processes \[count\_extract\]|Counter of extract processes that are managed by the Oracle Golden Gate manager instance.|
|Counter for replicat processes \[count\_replicat\]|Counter of replicat processes that are managed by the Oracle Golden Gate manager instance.|

**Parent Topic:**[Available on-premise discovery patterns](available-patterns.md)

