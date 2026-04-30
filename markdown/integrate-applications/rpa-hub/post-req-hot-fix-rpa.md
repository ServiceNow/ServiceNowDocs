---
title: Post requisites after installing a hot fix
description: Perform these tasks after installing a hot fix for either Universal App Connector \(UAC\) or Chromium connector on your instance to verify the hot fix is accurately downloaded.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Building automations, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
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

        ![Chrome and MS Edge exe files.](../image/chrome-exe-hotfix-rpa-studio.jpeg "Ending Chrome and MS Edge exe files")

        ![Native Messaging Chrome and MS Edge exe files.](../image/native-messaging-exe-rpa-studio.jpeg "Ending Chrome and MS Edge Native Messaging exe files")

    -   Use the following commands with elevated access to terminate all dependent tasks.
        -   taskkill /f /im msedge.exe
        -   taskkill /f /im msedgewebview2.exe
        -   taskkill /f /im UTL.RPA.EdgeNativeMessaging.exe
        -   taskkill /f /im chrome.exe
        -   taskkill /f /im UTL.RPA.ChromeNativeMessaging.exe
3.  Verify that the browser tabs or the mentioned executable files aren’t running.

4.  Launch either RPA Desktop Design Studio, Unattended Robot, or Attended Robot and proceed.


**Parent Topic:**[Building automations](../concept/rpa-studio-build.md)

**Related topics**  


[Universal app connector](../concept/universal-app-connector.md)

[Chromium connector](../concept/chrome-connector.md)

[Configuring RPA Desktop Design Studio](../concept/rpa-studio-configure.md)

