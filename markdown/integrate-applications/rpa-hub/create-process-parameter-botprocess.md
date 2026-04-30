---
title: Create a process parameter within a bot process in RPA Hub
description: Create a process parameter to store the variables that are used within a bot process. The process parameter that you just created can only be used by this bot process.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Adding details for your bot process in RPA Hub, Configuring a bot process record in RPA Hub, Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Create a process parameter within a bot process in RPA Hub

Create a process parameter to store the variables that are used within a bot process. The process parameter that you just created can only be used by this bot process.

## Before you begin

Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Before you can access a bot process, ensure that the RPA business user \(sn\_rpa\_fdn.rpa\_business\_user\), RPA developer \(sn\_rpa\_fdn.rpa\_developer\), or the RPA support user \(sn\_rpa\_fdn.rpa\_support\_user\) are in the Managed by Group list.

\(Optional\) Configure the system properties related to **Activity Stream**, to add or remove the fields. The changes to these fields are captured in the work notes. For more information, see [Configure the system properties for an activity stream in RPA Hub](configure-sys-properties-activity.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

You cannot delete a process parameter that is associated to a published bot process.

**Note:** To use a variable in multiple processes, create a shared parameter. For more information, see [Create a shared parameter in RPA Hub](create-shared-parameter.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process that you want to create and associate a process parameter to.

5.  On the **Process Parameters** tab, select **New**.

6.  On the form, fill in the fields.

7.  Select **Save**.

8.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


**Related topics**  


[Process parameter form in RPA Hub](../reference/process-parameter-form.md)

[View Audit History](https://www.servicenow.com/docs/access?context=c_HistorySets&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

