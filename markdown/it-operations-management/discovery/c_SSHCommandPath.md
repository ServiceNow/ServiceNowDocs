---
title: SSHCommand path
description: The SSHCommand probe computes the default path from the following sources.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SSHCommand probe, List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# SSHCommand path

The SSHCommand probe computes the default path from the following sources.

-   MID Server parameter: mid.ssh.path\_override
-   SSH Command probe parameter: path\_override
-   User's default path: Shell configuration file

If you set the MID Server path override parameter, Discovery appends this path to the default path. If you set the probe path parameter, Discovery uses this path instead of the default path. Discovery always appends a user's default execution path to the MID Server and probe parameter paths.

## Default Path

By default, the MID Server searches for SSH commands in the following paths:

-   /usr/sbin
-   /usr/bin
-   /bin
-   /sbin

**Parent Topic:**[SSHCommand probe](c_SSHCommandProbe.md)

