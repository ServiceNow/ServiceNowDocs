---
title: Upload the rctrlx.exe file to MID Servers
description: Upload the rctrlx.exe file to MID Servers to enable running discovery commands on Microsoft Exchange 2007 and 2010, and Citrix XenApp.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Upload the rctrlx.exe file to MID Servers

Upload the rctrlx.exe file to MID Servers to enable running discovery commands on Microsoft Exchange 2007 and 2010, and Citrix XenApp.

## Before you begin

Role required: admin or service\_mapping\_admin

## About this task

During the discovery process, the MID Server runs Service Mapping and Discovery patterns on applications and devices located inside the organization network. A pattern is a sequence of commands designed to detect attributes of a CI and its outbound connections. To execute commands over PowerShell correctly, MID Server runs patterns as services using the rctrlx.exe file. The rctrlx.exe file is part of the open source ManagePC utility and is available for downloading from the Internet.

Upload an `rctrlx.exe` file for every MID Server in your deployment.

## Procedure

1.  Download the `rctrlx.exe` file onto your computer from the Internet.

    For example, [https://github.com/leonsodhi/rctrlx/releases](https://github.com/leonsodhi/rctrlx/releases) offers the latest versions of the `rctrlx.exe` file:

2.  Place the rctrlx.exe file into the folder for Windows 32-bit servers:

    `<MID Server installation directory>\agent\bin\sw_wmi\bin\32`

    For example, C:\\SN\_MID\\SN\_MID\_Dev\\agent\\bin\\sw\_wmi\\bin\\32.

3.  Place the rctrlx.exe file into the folder for Windows 64-bit servers:

    `<MID Server installation directory>\agent\bin\sw_wmi\bin\64`

    For example, C:\\SN\_MID\\SN\_MID\_Dev\\agent\\bin\\sw\_wmi\\bin\\64.


**Related topics**  


[Pattern-based discovery in Service Mapping](../concept/pattern-based-discovery.md)

[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

