---
title: Puppet automation software discovery
description: Discovery identifies Puppet Masters running on UNIX servers.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Puppet automation software discovery

Discovery identifies Puppet Masters running on UNIX servers.

Discovery uses secure shell \(SSH\) commands to collect information.

To access Puppet Master records, navigate to **All** &gt; **Configuration** &gt; **Automation Servers** &gt; **Puppet Masters**. You can view the resources in the related list of the Puppet Master record.

## How the Puppet Master probe works

Discovery identifies the Puppet Master using the following process:

1.  The **UNIX - Active Processes** probe detects a running process that matches one of the following criteria:
    -   The name of the process is `pe-httpd`.
    -   The name of the process is `ruby` and the parameters of the process contain **puppet master**.
2.  If there is a match on one of these criteria:
    -   A record is created in the Puppet Master table \[cmdb\_ci\_puppet\_master\] if one does not already exist for that running process.
    -   The **Puppet - Master Info** probe is triggered. The sensor of this probe populates additional information in the Puppet Master \[cmdb\_ci\_puppet\_master\] record.

## Requirements to discover a Puppet master

By default, Discovery identifies Puppet Masters running on UNIX servers. Discovery uses secure shell \(SSH\) commands to collect information.

The credentials used to discover the UNIX server must have privileges to execute the following commands. The use of sudo is supported, but you must add the **must\_sudo** parameter to the probe.

|Probe|Commands|
|-----|--------|
|Puppet – Master Info|puppet, echo, hostname \(within the Borne shell script\)|
|Puppet – Certificate Requests|puppet|
|Puppet – Manifests|echo, sed, find \(within the Bourne shell script\)|
|Puppet – Modules|puppet|

## Data collected

| | | | |
|---|---|---|---|
|Name|Puppet Master \[cmdb\_ci\_puppet\_master\]|name|Puppet - Master Info|
|Configuration directory|Puppet Master \[cmdb\_ci\_puppet\_master\]|config\_directory|Puppet - Master Info|
|Manifest directory|Puppet Master \[cmdb\_ci\_puppet\_master\]|manifestdir|Puppet - Master Info|
|Module path|Puppet Master \[cmdb\_ci\_puppet\_master\]|modulepath|Puppet - Master Info|
|Fully qualified domain name|Puppet Master \[cmdb\_ci\_puppet\_master\]|fqdn|Puppet - Master Info|
|IP Address|Puppet Master \[cmdb\_ci\_puppet\_master\]|ip\_address|Puppet - Master Info|
|Version|Puppet Master \[cmdb\_ci\_puppet\_master\]|version|Puppet - Master Info|

-   **[Add the must\_sudo parameter to the Puppet probe](../task/t_AddMustSudoParameterPuppetProbe.md)**  
To use the Puppet probe with sudo, you must add the **must\_sudo** parameter to each probe that requires it.

**Parent Topic:**[Software discovery](c_Software.md)

