---
title: Exploring Agent Client Collector for Visibility
description: Learn how you can use Agent Client Collector for Visibility \(ACC-V\) to discover data on your target hosts.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector for Visibility, Agent Client Collector, IT Operations Management]
---

# Exploring Agent Client Collector for Visibility

Learn how you can use Agent Client Collector for Visibility \(ACC-V\) to discover data on your target hosts.

## Agent Client Collector for Visibility overview

ACC-V is an additional mechanism to perform Discovery. It is an alternative to horizontal IP-based Discovery for OS-related attributes including system information, network interfaces, running process, and so on. ACC-V is suitable for on-prem servers and cloud instances. ACC-V discovers software from different installation sources, such as Chocolatey, Click-to-Run and winget, in addition to traditional msi-based installations.

Agent Client Collector for Visibility supports the following modules:

-   Data Collection
-   Enhanced Inventory
-   Serial Numbers
-   Storage Devices
-   File Systems
-   Network Adapters
-   TCP Connections
-   Running Processes
-   Installed Software
-   Local User
-   Intel vPro® platform

**Note:**

-   Currently, Agent Client Collector for Visibility does not support multi-languages. If values returned are not in English, the returned data cannot be parsed properly and the discovery will fail.
-   Powershell is not being used in any of the ACC-V modules on Microsoft Windows operating systems.

You can register and manage your target systems in the ServiceNow Configuration Management Database \(CMDB\) using the ACC-V pushed-based model. There is no need to provide credentials, configure schedules, or scan IP ranges.

## Agent Client Collector for Visibility workflow

The following illustration describes the high-level architecture of Agent Client Collector for Visibility.

![This block diagram shows the components that work together](../image/acc-v_arch.png "ACC-V architecture")

ACC-V works with the following components:

-   ServiceNow Instance
-   ServiceNow MID Server
-   Target host machines
-   ServiceNow Agent Client Collector which runs on the Target host machines

## Supported operating systems

ACC-V collects the system attributes and related lists normally collected by the OS pattern. ACC-V currently supports the following operating systems on x86\_64 architecture:

-   Linux
    -   Red Hat Enterprise Linux \(RHEL\) and Oracle Linux \(OL\) 7, 8, 9
    -   Centos 7, 8, 9
    -   SLES 12, 15
    -   Ubuntu 18, 20
    -   Amazon Linux 2
    -   Debian 9 and 10
-   Microsoft Windows
    -   Windows Server 2012, 2012r2, 2016, 2019, 2022
    -   Windows 10 Enterprise Edition
    -   Windows 11 Enterprise and Professional Editions
-   macOS \(starting in ACC-V version 1.3.0\)
    -   10.15 - Catalina
    -   11 - Big Sur
    -   Monterey \(x86\)
    -   13 - Ventura
    -   macOS Ventura on ARM64 - Apple Silicon M1/M2
    -   Sonoma

