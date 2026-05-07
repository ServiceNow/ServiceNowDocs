---
title: Deploy a MID Server
description: Deploying a MID Server allows ServiceNow to securely communicate with systems inside a private network by installing and validating a trusted runtime that performs discovery, integrations, and automation tasks without requiring inbound network access.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 1
keywords: [ITOM, user roles, Now Assist]
breadcrumb: [ITOM Configuration Console for Discovery, Now Assist for Setup \(ITOM Visibility\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Deploy a MID Server

Deploying a MID Server allows ServiceNow to securely communicate with systems inside a private network by installing and validating a trusted runtime that performs discovery, integrations, and automation tasks without requiring inbound network access.

## Before you begin

Verify the following:

-   You have installed the ITOM Visibility plugin. For more information, see [Install ITOM Visibility using Now Assist for Setup](install-nowassist-setup-itom-visibility.md).
-   You have installed the Now Assist for IT Operations Management plugin. For more information, see [Install Now Assist for IT Operations Management](install-now-assist-itom.md).
-   You're on the Configure IT Operations Management page of the Configuration Console. For more information, see [Access the ITOM Configuration Console](access-itom-config-console-disco.md).

Role required: admin

## About this task

Discovery requires a MID Server to securely detect and collect data from systems in your private network, enabling accurate identification of infrastructure and dependencies without exposing internal resources to the internet.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Discovery** &gt; **Platform foundations**.

2.  Select **Deploy MID server**.

3.  Select the Application manager icon \(![](../image/application-manager-icon.png)\).

    The ITOM Infra Services Workspace displays.

4.  Download the MID Server for the appropriate operating system.

    For more information, see [Install a MID Server on Linux](https://www.servicenow.com/docs/access?context=t_InstallAMIDServerOnLinux&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [Install a MID Server on Windows](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

5.  Select **X** to close the window and return to the Configuration Console.

6.  To complete the setup, select **Mark as configured**.


