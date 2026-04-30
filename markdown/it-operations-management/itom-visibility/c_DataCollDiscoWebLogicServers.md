---
title: WebLogic application server discovery
description: Discovery creates or updates a CMDB record when it detects an instance of an Oracle or BEA Weblogic application server running on a Windows or Linux system.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# WebLogic application server discovery

Discovery creates or updates a CMDB record when it detects an instance of an Oracle or BEA Weblogic application server running on a Windows or Linux system.

## Requirements

-   **For Windows**
    -   [PowerShell](../task/t_SetUpAMIDServerToUsePowerShell.md) must be enabled on the MID Server.
    -   The WebLogic Administration Server instances that start via WebLogic NodeManager must have the **-Dweblogic.RootDirectory=&lt;path&gt;** parameter defined upon server startup. The Windows credential must also have read permissions on the `config.xml` file.
-   **For Linux**
    -   Discovery requires the use of these Bourne shell commands:
        -   `find`
        -   `cat`
        -   `dirname`
    -   WebLogic administration server instances started via NodeManager must have the **-Dweblogic.RootDirectory=&lt;path&gt;** parameter defined and visible through the Linux ps process stat command \(for each AdminServer\) for the rest of the Linux WebLogic application server and web application information to be populated in the CMDB.
    -   The following configuration must be set on the sudorers file:

        `User ALL=(root) NOPASSWD: /bin/sh *`

        `User` is the user name on the SSH credential that you create for this discovery.

    -   This command must be able to be run:

        `/bin/sh /tmp/snc-*-findcat.sh * *"`

        Do not make any changes to `findcat.sh`.

    -   If you are using probes, not patterns, for Weblogic discovery, the **Linux - Weblogic - Find config.xml** probe must specify this parameter and value: **must\_sudo** `=` **true**

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Credentials

-   [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

## Classifier, pattern, and probes

<table id="table_fzd_2yv_jz"><thead><tr><th>

Classifier

</th><th>

Trigger probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

Weblogic Server

</td><td>

-   Horizontal Pattern: launches patterns
-   Windows - Weblogic - Get web.xml\*
-   Windows - Weblogic - Find config.xml\*
-   Linux - Weblogic - Find config.xml\*

</td><td>

WebLogic

</td></tr></tbody>
</table>\*For new instances, these probes are inactive on the classifier. Discovery uses patterns for discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected on Windows

|Label|Table Name|Field Name|Source|
|-----|----------|----------|------|
|Name|cmdb\_ci\_app\_server\_weblogic|name|running process|
|Version|cmdb\_ci\_app\_server\_weblogic|version|config.xml|
|Weblogic domain|cmdb\_ci\_app\_server\_weblogic|weblogic\_domain|config.xml|
|TCP port\(s\)|cmdb\_ci\_app\_server\_weblogic|tcp\_port|web.xml and running process|
|Name|cmdb\_ci\_web\_application|name|config.xml|
|Document base|cmdb\_ci\_web\_application|document\_base|config.xml|
|Description|cmdb\_ci\_web\_application|description|web.xml|
|Servlet class|cmdb\_ci\_web\_application|servlet\_class|web.xml|
|Servlet name|cmdb\_ci\_web\_application|servlet\_name|web.xml|
|App server|cmdb\_ci\_web\_application|app\_server|config.xml|
|TCP port\(s\)|cmdb\_ci\_web\_application|tcp\_port|web.xml|

## Data collected on Linux

|Table|Field|Source|
|-----|-----|------|
|cmdb\_ci\_app\_server\_weblogic|Name \(name\)|running process|
|cmdb\_ci\_app\_server\_weblogic|TCP port \(tcp\_port\)|running process|
|cmdb\_ci\_app\_server\_weblogic|Version \(version\)|config.xml|
|cmdb\_ci\_app\_server\_weblogic|Weblogic domain \(weblogic\_domain\)|config.xml|
|cmdb\_ci\_web\_application|Name \(name\)|config.xml|
|cmdb\_ci\_web\_application|Context path \(context\_path\)|config.xml|
|cmdb\_ci\_web\_application|App server \(app\_server\)|config.xml|

## Relationship

<table id="table_wnk_3nw_wtb"><thead><tr><th>

Parent class

</th><th>

Relationship type

</th><th>

Child class

</th></tr></thead><tbody><tr><td>

cmdb\_ci\_app\_server\_weblogic

</td><td>

Runs on::Runs

</td><td>

cmdb\_ci\_windows\_server or cmdb\_ci\_linux\_server

</td></tr><tr><td>

cmdb\_ci\_app\_server\_weblogic

</td><td>

Contains::Contained by

</td><td>

cmdb\_ci\_web\_application

</td></tr><tr><td>

cmdb\_ci\_app\_server\_weblogic

</td><td>

Depends on::Used by

</td><td>

cmdb\_ci\_app\_server\_weblogicThis relationship is made between an AdminServer and any managed servers it encapsulates.

</td></tr></tbody>
</table>![Example weblogic relationships](../image/weblogic-relationships.png "Example Weblogic relationships")

-   **[Add sudo access for the Weblogic - Find config.xml probe](../task/t_AddSudoforWeblogic.md)**  
If you are not using the Weblogic pattern, you can add sudo privileges to the Linux, the Weblogic - Find config.xml probe.
-   **[Identifying Windows WebLogic application servers](../reference/r_WeblogicProbesAndSensorsWindows.md)**  
If you are not using the Weblogic pattern, Discovery follows this process when it uses the Windows - Active Processes or Linux - Active Processes probes.

**Parent Topic:**[Software discovery](c_Software.md)

