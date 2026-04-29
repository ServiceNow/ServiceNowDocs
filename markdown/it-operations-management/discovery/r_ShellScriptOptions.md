---
title: Shell script options
description: The SSHCommand probe supports the following scripting options in the ECC queue name field.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SSHCommand probe, List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Shell script options

The SSHCommand probe supports the following scripting options in the ECC queue name field.

|Summary|Syntax|Description|
|-------|------|-----------|
|Variable|$\{variable\}|Replaces the token with the value of the variable. For example, $\{catalina\_home\} specifies the installation location of a Tomcat server.|
|Include File|$\{File:file\_name.sh\}|Treats the contents of the specified file as a shell script. For example, $\{File:findcat.sh\} runs the findcat shell script.|

**Parent Topic:**[SSHCommand probe](../concept/c_SSHCommandProbe.md)

