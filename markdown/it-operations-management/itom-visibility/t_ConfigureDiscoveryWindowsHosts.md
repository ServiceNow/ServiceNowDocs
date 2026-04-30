---
title: Configure Discovery for Windows hosts with attached storage
description: Discovery can find information about a Windows host and attached storage.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure discovery of hosts with attached storage, Storage discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Configure Discovery for Windows hosts with attached storage

Discovery can find information about a Windows host and attached storage.

## Before you begin

Role required: discovery\_admin

## Procedure

1.  Follow the steps if you're using the Windows 2008 servers that is attached to storage:

    1.  Download and install the Microsoft Fibre Channel Information Tool from http://www.microsoft.com and search the website for Microsoft Fibre Channel Information Tool.
    2.  Set the environment path for the fcinfo executable and run the `fcinfo.exe` file.
    **Note:** For servers that are using newer operating systems, similar functionality is present with the operating system; this step is not required.

2.  For all Windows hosts including Windows 2008, [add Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) to the Discovery Credentials table.

3.  On the ServiceNow instance, create a Discovery Schedule for each host IP address.

4.  Create a behavior that uses a functionality definition with a wbem port probe to make the initial port-scanning phase \(Shazzam\) more efficient.

5.  Run network discovery.

    **Note:** If the host also connects to a NAS or SAN storage array, set up the [SMI-S Provider](t_ConfigDiscoForStandaloneStorage.md) and [CIM credentials](https://www.servicenow.com/docs/access?context=r_CIMCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).


**Parent Topic:**[Configure discovery of hosts with attached storage](../concept/configure-discovery-of-hosts-with-attached-storage.md)

