---
title: Jenkins log levels and Log Recorders
description: Set log levels in the Jenkins plugin for ServiceNow DevOps based on the extent of log detail you need for debugging.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Jenkins log levels and Log Recorders

Set log levels in the Jenkins plugin for ServiceNow DevOps based on the extent of log detail you need for debugging.

## Base system Log Recorder in Jenkins logs

You can set the level of detail that your log messages capture. In previous versions of the plugin, you could only enable or disable the **Debug** mode, which meant that you could either enable or disable all Jenkins logs without the ability to select the level of information or detail you want to save in your logs. Often, this leads to excessive information in your logs, used up more disk space, and collected information that might not always be relevant or useful.

The flexibility to set log levels allows you to select the right log level information that is appropriate for your organizational needs. You can select custom log levels based on the log levels or categories that Jenkins currently supports.

The log level is turned off by default for first-time DevOps installations. Consider the following items after successfully upgrading:

-   if the **Debug** check box was previously selected, the log level is enabled and set to **Info** by default.
-   If the **Debug** check box was cleared previously, by default, log levels are tuned off.

**Note:**

The Jenkins log does not record log messages at a level lower than **Info**. The base system ServiceNow DevOps log recorders are used to record this message.

You can select a custom level from the Jenkins plugin- ServiceNow DevOps Configuration form &gt; Log level list. A base system ServiceNow DevOps log recorder is created in the Jenkins Log Recorders list. For more information, see [Jenkins documentation on viewing logs](https://www.jenkins.io/doc/book/system-administration/viewing-logs/).

**Note:** Do not modify the log recorder from the Jenkins &gt; Log Recorders &gt; Configure log recorders. Editing the log recorder from Jenkins creates a duplicate entry for any changes to the log levels that you make. Please use the list of log levels in the ServiceNow DevOps Configuration form, to modify the log levels.

