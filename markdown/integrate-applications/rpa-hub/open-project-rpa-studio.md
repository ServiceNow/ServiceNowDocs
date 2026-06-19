---
title: Open a local automation project in RPA Desktop Design Studio
description: Open an automation project from the local file system in RPA Desktop Design Studio, so that you can debug, build, or modify the automation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/open-project-rpa-studio.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Build, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Open a local automation project in RPA Desktop Design Studio

Open an automation project from the local file system in RPA Desktop Design Studio, so that you can debug, build, or modify the automation.

## Before you begin

Create an automation project. For more information, see [Create an automation project manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-automation-project.md) or [Create an automation with Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-automation-now-assist.md).

Download the automation package file by accessing the associated package file in RPA Hub. For more information, see [Download a package version in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/download-package-version.md).

Role required: none

## Procedure

1.  In the RPA Desktop Design Studio, navigate to **Home** &gt; **Automation projects**.

2.  Select **Open local project**.

3.  In the Open ServiceNow Automation Project dialog box, select a project.

4.  Select **Open**.

5.  If the plugin versions that are used in the project aren’t found in the local framework, go to the Choose Plugin Version dialog box, select the plugin versions to be used, and select **OK**.

    **Important:** When you open an older automation project in the latest version of [Set up RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/set-up-rpa-studio.md), the Upgrade Plugin Version dialog box is displayed. If you proceed to upgrade the plugin version and any automation components are unavailable after the upgrade, then these components are marked as **Unknown** in the automation project.


**Parent Topic:**[Building automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/rpa-studio-build.md)

