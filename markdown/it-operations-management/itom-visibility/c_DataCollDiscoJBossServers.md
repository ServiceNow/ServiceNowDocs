---
title: Red Hat JBoss server discovery
description: Discovery can detect JBoss application servers running on Linux and Windows systems.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Red Hat JBoss server discovery

Discovery can detect JBoss application servers running on Linux and Windows systems.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Requirements

For JBoss application servers running on Linux systems.

-   Set probe permissions to use these Bourne shell commands: find, cat, and dirname.
-   Enable SSH on the JBoss application server. The SSH credential must also have read permissions on the `web.xml` and `jboss-service.xml` files.

For JBoss application servers running on Windows systems, enable [PowerShell](../task/t_SetUpAMIDServerToUsePowerShell.md) on the MID Server.

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

## Credentials

-   [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US)

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

## Classifiers, patterns, and probes

<table id="table_fzd_2yv_jz"><thead><tr><th>

Classifier

</th><th>

Trigger probes

</th><th>

Patterns

</th></tr></thead><tbody><tr><td>

JBoss Server

</td><td>

-   Horizontal Pattern: launches patterns
-   Windows - JBoss Find web.xml List\*
-   Windows - JBoss Get jboss-service.xml\*
-   JBoss - Find web.xml List\*
-   JBoss - Get jboss-service.xml\*

</td><td>

JBoss pattern

</td></tr></tbody>
</table>\*For new instances, these probes are inactive on the classifier. Discovery uses patterns for discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected

Discovery populates the following fields in the JBoss \[cmdb\_ci\_app\_server\_jboss\] table:

|Label|Field name|
|-----|----------|
|Name|name|
|Category|category|
|Version|version|
|TCP port\(s\)|tcp\_port|

Discovery populates the following fields on the Web Service \[cmdb\_ci\_web\_service\] and Web Application \[cmdb\_ci\_web\_application\] servers tables:

|Label|Table name|Field name|Source|
|-----|----------|----------|------|
|Name|cmdb\_ci\_web\_service|name|jboss-service.xml|
|App server|cmdb\_ci\_web\_service|app\_server|Internal reference|
|Description|cmdb\_ci\_web\_application|short\_description|web.xml|
|Name|cmdb\_ci\_web\_application|name|web.xml|
|Document base|cmdb\_ci\_web\_application|document\_base|web.xml|
|App server|cmdb\_ci\_web\_application|app\_server|web.xml|
|Servlet Name\*|cmdb\_ci\_web\_application|servlet\_name|web.xml|
|Servlet Class\*|cmdb\_ci\_web\_application|servlet\_class|web.xml|

\*Windows servers only

## Relationships

|Parent class|Relationship|Child class|
|------------|------------|-----------|
|cmdb\_ci\_web\_service|Runs on::Runs|cmdb\_ci\_windows\_server|
|cmdb\_ci\_app\_server\_jboss|Contains::Contained by|cmdb\_ci\_web\_application|
|cmdb\_ci\_app\_server\_jboss|Runs:Runs on|cmdb\_ci\_web\_application|
|cmdb\_ci\_app\_server\_jboss|Runs:Runs on|cmdb\_ci\_web\_service|

-   **[Legacy: JBoss probes and sensors](../reference/r_JBossProbesAndSensorsForLinux.md)**  
Discovery identifies a Linux JBoss application server using probes and sensors.

**Parent Topic:**[Operating systems discovery](c_Computers.md)

