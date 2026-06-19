---
title: Open Service and Runtime logs
description: Logs record events that occur during the execution of an automation process. These logs are crucial for debugging and monitoring the performance of the robots.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/open-logs-rpa-studio.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Build, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Open Service and Runtime logs

Logs record events that occur during the execution of an automation process. These logs are crucial for debugging and monitoring the performance of the robots.

## Before you begin

Close the existing Unattended Robot or Attended Robot window.

Role required: none

## About this task

Logs provide detailed information about the actions performed by the robot, including any errors or exceptions that occur. These logs help developers understand the robot's behavior and identify areas for improvement.

There are types of logs - service logs and runtime logs. Service Logs has the windows service-related operation logs. Runtime Logs has the automation-related logs.

Unattended Robot has a windows service for the core operations such as invoking an automation, updating the robot status, creating process jobs. This windows service runs in a system context. All the logs that are captured in that context are saved in a program data location. Verify to unhide the Program Data folder in your Windows machine.

Each log has a naming convention. If it’s a runtime-related log, the log name starts with Runtime. If it’s a RPA Desktop Design Studio related log, the log name starts with Studio.

## Procedure

1.  In the notification area \(system tray\) in the taskbar, select and hold \(or right-click\) the Unattended Robot icon \(\[Omitted image "rpa-robot-runtime-desktop-icon.png"\] Alt text: Unattended Robot icon in the notification area.\).

2.  Select **View Logs** and select either **Service Logs** or **Runtime Logs**, to view the related logs.


**Parent Topic:**[Building automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/rpa-studio-build.md)

