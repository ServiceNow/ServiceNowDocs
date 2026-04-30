---
title: Open a cloud automation project in RPA Desktop Design Studio
description: Open an automation project remotely from RPA Hub in RPA Desktop Design Studio, so that you can debug, build, or modify the automation.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Build, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Open a cloud automation project in RPA Desktop Design Studio

Open an automation project remotely from RPA Hub in RPA Desktop Design Studio, so that you can debug, build, or modify the automation.

## Before you begin

Make sure that the package \(automation project\) that you’re trying to open is published on RPA Hub. For more information, see [Publish an automation project in RPA Desktop Design Studio](publish-automation-project.md).

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_support\_user, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  In the RPA Desktop Design Studio, navigate to **Home** &gt; **Automation projects**.

2.  Select **Open cloud project**.

    If the selected ServiceNow instance session has expired, add the ServiceNow instance details. For more information, see [Set up RPA Desktop Design Studio](set-up-rpa-studio.md).

3.  In the Open Project dialog box, select a package name and a version.

4.  Select **Open**.

5.  Save the ServiceNow project in the default location by selecting **Save**.

6.  If the plugin versions that are used in the project aren’t found in the local framework, go to the Choose Plugin Version dialog box, select the plugin versions to be used, and select **OK**.

    **Important:** When you open an older automation project in the latest version of [Set up RPA Desktop Design Studio](set-up-rpa-studio.md), the Upgrade Plugin Version dialog box is displayed. If you proceed to upgrade the plugin version and any automation components are unavailable after the upgrade, then these components are marked as Unknown in the automation project.


**Parent Topic:**[Building automations](../concept/rpa-studio-build.md)

