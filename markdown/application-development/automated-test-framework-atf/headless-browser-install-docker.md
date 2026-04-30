---
title: Install Docker for Headless Browser setup for Microsoft Windows
description: Step 1 in the Windows setup for the ServiceNow Headless Browser for Automated Test Framework: Install Docker.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Headless Browser setup for Microsoft Windows, Headless Browser, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Install Docker for Headless Browser setup for Microsoft Windows

Step 1 in the Windows setup for the ServiceNow® Headless Browser for Automated Test Framework: Install Docker.

## Before you begin

Role required: admin

-   See Prerequisites in the [Headless Browser setup for Microsoft Windows](../concept/headless-browser-procedure-windows.md) topic.
-   **Tip:** To make remembering these easier, set the following environment variables:

-   set PASSWORD=&lt;password&gt;
-   set SERVERIP=&lt;server ip&gt;
-   set HOSTNAME=&lt;hostname&gt;

**Warning:** The only supported version of Microsoft Windows as a host is Windows Server 2019 v10.0.17763.737. No other versions are supported. If you are unable to meet these requirements, a Linux host is recommended.

## Procedure

1.  Open an elevated PowerShell session and install the Docker-Microsoft PackageManagement Provider from the [PowerShell Gallery](https://www.powershellgallery.com/packages/DockerMsftProvider).

    PowerShell

    `Install-Module -Name DockerMsftProvider -Repository PSGallery -Force`

    If you're prompted to install the NuGet provider, type `Y` to install it as well.

2.  Use the PackageManagement PowerShell module to install the latest version of Docker.

    PowerShell

    `Install-Package -Name docker -ProviderName DockerMsftProvider`

    When PowerShell asks you whether to trust the package source 'DockerDefault', type `A` to continue the installation.

3.  After the installation completes, restart the computer.

    PowerShell

    `Restart-Computer -Force`


**Parent Topic:**[Headless Browser setup for Microsoft Windows](../concept/headless-browser-procedure-windows.md)

**Previous topic:**[Headless Browser setup for Microsoft Windows](../concept/headless-browser-procedure-windows.md)

**Next topic:**[Generate certificates for Headless Browser setup for Microsoft Windows](headless-browser-certificates-windows.md)

