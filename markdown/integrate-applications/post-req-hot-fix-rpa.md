---
title: Post requisites after installing a hot fix
description: Perform these tasks after installing a hot fix for either Universal App Connector \(UAC\) or Chromium connector on your instance to verify the hot fix is accurately downloaded.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/post-req-hot-fix-rpa.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Build, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Post requisites after installing a hot fix

Perform these tasks after installing a hot fix for either Universal App Connector \(UAC\) or Chromium connector on your instance to verify the hot fix is accurately downloaded.

## Before you begin

Install the hot fix in your RPA Hub instance. An admin access might be required, to do this task.

Take a backup of the iBot project file that you’re trying to open.

Close RPA Desktop Design Studio and any open browser tabs on your machine.

Role required: sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin

## About this task

For example, if you created a project using the UAC plugin version 6.1, and a hot fix is installed on your instance for the same version. In this scenario, the following steps are required only for the first time when you either launch the RPA Desktop Design Studio, Unattended Robot, or Attended Robot after installing a hot fix.

This procedure is applicable if you are using Google Chrome, or Edge applications.

## Procedure

1.  In your Windows machine, navigate to the Task Manager.

2.  Perform any of the following tasks to close the `chrome.exe`, `msedge.exe`, and `msedgewebview2.exe` processes \(dependent tasks\).

    -   Locate the running `chrome.exe`, `msedge.exe`, `msedgewebview2.exe`, `UTL.RPA.ChromeNativeMessaging.exe`, and `UTL.RPA.EdgeNativeMessaging.exe` processes and select and hold \(or right-click\) **End task**.

        \[Omitted image "chrome-exe-hotfix-rpa-studio.jpeg"\] Alt text: Chrome and MS Edge exe files.

        \[Omitted image "native-messaging-exe-rpa-studio.jpeg"\] Alt text: Native Messaging Chrome and MS Edge exe files.

    -   Use the following commands with elevated access to terminate all dependent tasks.
        -   taskkill /f /im msedge.exe
        -   taskkill /f /im msedgewebview2.exe
        -   taskkill /f /im UTL.RPA.EdgeNativeMessaging.exe
        -   taskkill /f /im chrome.exe
        -   taskkill /f /im UTL.RPA.ChromeNativeMessaging.exe
3.  Verify that the browser tabs or the mentioned executable files aren’t running.

4.  Launch either RPA Desktop Design Studio, Unattended Robot, or Attended Robot and proceed.


**Parent Topic:**[Building automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-studio-build.md)

**Related topics**  


[Universal app connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/universal-app-connector.md)

[Chromium connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/chrome-connector.md)

[Configuring RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-studio-configure.md)

