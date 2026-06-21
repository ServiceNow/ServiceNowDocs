---
title: Shell script options
description: The SSHCommand probe supports the following scripting options in the ECC queue name field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-operations-management/discovery/r\_ShellScriptOptions.html
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SSHCommand probe, List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# Shell script options

The SSHCommand probe supports the following scripting options in the ECC queue name field.

|Summary|Syntax|Description|
|-------|------|-----------|
|Variable|$\{variable\}|Replaces the token with the value of the variable. For example, $\{catalina\_home\} specifies the installation location of a Tomcat server.|
|Include File|$\{File:file\_name.sh\}|Treats the contents of the specified file as a shell script. For example, $\{File:findcat.sh\} runs the findcat shell script.|

**Parent Topic:**[SSHCommand probe](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/discovery/c_SSHCommandProbe.md)

