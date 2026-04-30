---
title: Manage plugins in RPA Desktop Design Studio
description: Install, update, or remove plugins to design automations while you're creating unattended and attended automation projects in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Building automations, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Manage plugins in RPA Desktop Design Studio

Install, update, or remove plugins to design automations while you're creating unattended and attended automation projects in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

An RPA plugin is a bundle of Windows library files that are consumed by the RPA Desktop Design Studio application. These plugins extend the capability of the Robotic Process Automation \(RPA\) product. For instance, the Universal App Connector plugin enables the RPA application to automate tasks on a Google Chrome browser.

Internet Explorer, Essential Connectors, Essential Toolkit, and Universal App Connector plugins are available in the RPA Desktop Design Studio project by default.

Install, update, or remove all plugins from a RPA Desktop Design Studio project from the **Plugin manager** under the **View** tab or the **Plugins** node under **Project Explorer** in the RPA Desktop Design Studio.

The following table lists the RPA plugins and their descriptions.

<table id="table_ljz_ttx_fgc"><thead><tr><th>

Plugin Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Internet Explorer

</td><td>

A connector that enables automating web applications inside Microsoft Internet Explorer.For more information about the IE connector, see [IE connector](../concept/internet-explorer-connector.md).

</td></tr><tr><td>

SSH

</td><td>

Connector for interacting with server via Secure Shell \(SSH\).For more information about the SSH connector, see [Secure Shell \(SSH\) connector](../concept/ssh-connector.md).

</td></tr><tr><td>

Essential Toolkit

</td><td>

An essential toolkit for developing unattended and attended projects.

</td></tr><tr><td>

FTP

</td><td>

Connector to transfer files between a client and server on a network.For more information about the FTP connector, see [FTP](../concept/ftp-connector.md).

</td></tr><tr><td>

Windows

</td><td>

Enables automation of Windows desktop applications.For more information about the Windows connector, see [Windows connector](../concept/windows-connector.md).

</td></tr><tr><td>

Barcode Reader

</td><td>

Provides barcode or QR code reading components.For more information about the Barcode connector, see [Use the ReadBarcode component](use-utilities-barcode-readbarcode.md).

</td></tr><tr><td>

Universal App Connector

</td><td>

Connector for interacting with Google Chrome, Edge, Java, and Windows based applications.For more information about the Universal App connector, see [Universal app connector](../concept/universal-app-connector.md).

</td></tr><tr><td>

Java

</td><td>

Connector for interacting with Java based applications.For more information about the Java connector, see [Configure the Java connector](configure-java-connector.md).

</td></tr><tr><td>

Essential Connectors

</td><td>

An essential set of connectors for developing unattended and attended projects.

</td></tr><tr><td>

Scripting

</td><td>

A connector that enables developers to code in Python, VB.NET, C\#, and Javascript languages.For more information about the C\#, VB.NET, and Javascript connectors, see [Configure the Python connector](configure-python-connector.md), [Configure the C\#.Net connector](configure-C-net-connector.md), [Configure the JavaScript connector](configure-javascript-connector.md), and [Configure the VB.Net connector](configure-vbnet-connector.md).

</td></tr><tr><td>

Terminal \(Mainframe\)

</td><td>

Connector that interacts with Mainframe applications through IBM Personal Communications \(PCOMM\) and Rocket BlueZone emulators.For more information about the Terminal connector, see [Configure the Terminal connector](../concept/configure-terminal-connector.md).

</td></tr><tr><td>

Chromium

</td><td>

A connector that enables automating web applications inside Google Chrome or Microsoft Edge.For more information about the Chromium connector, see [Chromium connector](../concept/chrome-connector.md).

</td></tr><tr><td>

SAP

</td><td>

Connector for interacting with SAP applications.For more information about the SAP connector, see [Configure the SAP connector](configure-the-sap-connector.md).

</td></tr></tbody>
</table>## Procedure

1.  To navigate to the Plugins Manager window to the RPA Desktop Design Studio project, do either of the steps.

    -   Navigate to **View** &gt; **Plugin manager**.
    -   Right-click **Plugins** in the **Project Explorer** pane and select **Add Plugin**.
    The **Available** tab shows the plugins that you can install and the **Installed** tab shows the plugins that are available to the current RPA Desktop Design Studio project.

2.  To add a plugin, on the Plugins Manager window, select the **Available** tab.

3.  Select the plugin you want to add.

    **Tip:** To find the plugin, enter the name of the plugin in the Filter field.

4.  Select **ADD**.

    By default, the RPA Desktop Design Studio displays the latest version of the plugin. To view the previous versions, select the drop-down.

    The plugin is added to the current RPA Desktop Design Studio project and appears under the **INSTALLED** tab of the Plugins Manager window.

5.  Select **OK**.

6.  To add more plugins, repeat the procedure.

7.  Perform the following steps for more plugin options.

<table id="choicetable_sx3_1wd_b2c"><thead><tr><th align="left" id="d376981e570">

Action

</th><th align="left" id="d376981e573">

Steps

</th></tr></thead><tbody><tr><td id="d376981e579">

**Update a plugin version**

</td><td>

1.  Open the Plugins Manager window.
2.  Select the **AVAILABLE** or **INSTALLED** tab.
3.  Select the plugin.
4.  Select **UPDATE**.
5.  Select **OK**.
6.  Save, close and reopen the project to load the updated plugins to the current project.


</td></tr><tr><td id="d376981e622">

**Remove a plugin**

</td><td>

1.  Open the Plugins Manager window.
2.  Select the **AVAILABLE** or **INSTALLED** tab.
3.  Select the plugin and select **REMOVE**.
4.  Select **Yes**.
5.  Select **OK**.
 The plugin is no longer available to the current RPA Desktop Design Studio project and removed from the **INSTALLED** tab.

</td></tr></tbody>
</table>
**Parent Topic:**[Building automations](../concept/rpa-studio-build.md)

