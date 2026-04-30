---
title: Email notification layout for Universal Task notifications
description: Use the email notification layout and template shipped with the Universal Task application \(sn\_uni\_task\) to deliver email notifications. Apply the layout to email notifications to elevate their look and feel and to deliver branded notifications.
locale: en-US
release: xanadu
product: Universal Task
classification: universal-task
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Email notification layout for Universal Task notifications

Use the email notification layout and template shipped with the Universal Task application \(sn\_uni\_task\) to deliver email notifications. Apply the layout to email notifications to elevate their look and feel and to deliver branded notifications.

The following table lists the email notifications shipped with Universal Task. You can choose to modify the email body or keep the default versions.

|Notification name|Used for|Fields where recipients are identified|
|-----------------|--------|--------------------------------------|
|Universal Child Tasks Closed|Sends an email notification when all child Universal Tasks of the parent are closed.|Assigned to field of the parent|
|Universal Task Assignment For Assigned To|Sends an email notification when the task is assigned and either the assignee changes or the state changes to Work In Progress.|Assigned to, Watch list|
|Universal Task Assignment For Group|Sends an email notification when the task is assigned to a group and either the group changes, or the state changes to Work In Progress.|Assignment group, Watch list|
|Universal Task Cancelled|Sends an email notification when the task is cancelled.|Opened by, Assigned to field of the parent|
|Universal Task Cancelled For Assigned To|Assigned to, Watch list|
|Universal Task Cancelled For Group|Assignment group, Watch list|
|Universal Task Changed For Assigned To|Sends an email notification when the task type, short description, or description is updated.|Assigned to, Watch list|
|Universal Task Changed For Group|Assignment group, Watch list|
|Universal Task Commented For Assigned To|Sends an email notification when there is a new additional comment on the task.|Assigned to, Watch list, Opened by, Assigned to field of the parent|
|Universal Task Commented For Group|Assignment group, Watch list, Opened by, Assigned to field of the parent|
|Universal Task Completed|Sends an email notification when the task is complete.|Opened by, Assigned to field of the parent|
|Universal Task Completed For Assigned To|Assigned to, Watch list|
|Universal Task Completed For Group|Assignment group, Watch list|

**Important:** These email notifications are automatically set up for a new user of Universal Task.

If you are an existing user of Universal Task on a release prior to San Diego, upgrade to Employee Center or Employee Center Pro or install the Employee Experience Foundation plugin from ServiceNow Store to start using these email notifications.

**Parent Topic:**[Setting up and configuring Universal Task](set-up-universal-task.md)

