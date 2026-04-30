---
title: Create a shared parameter in RPA Hub
description: Create a shared parameter so that you can store the global variables or configurable items in one place. These variables are used across bot processes.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Create a shared parameter in RPA Hub

Create a shared parameter so that you can store the global variables or configurable items in one place. These variables are used across bot processes.

## Before you begin

\(Optional\) Configure the system properties related to **Activity Stream**, to add or remove the fields. The changes to these fields are captured in the work notes. For more information, see [Configure the system properties for an activity stream in RPA Hub](configure-sys-properties-activity.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

Instead of hard-coding these values directly into each individual bot process, the shared parameters are stored in a central location, making it easier to update them universally and avoid duplication.

You cannot delete a shared parameter that is associated to a published bot process.

Shared parameters offer numerous benefits such as consistency, centralized management that contributes to efficient and maintainable development practices.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Shared Parameters**.

4.  Select **New**.

5.  On the form, fill in the fields.

6.  Select **Submit**.

7.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.

8.  To delete a shared parameter, select the three-dot icon next to the **Save** button and select **Delete**.

    **Note:** Verify that the shared parameter is not associated to any bot process. You can delete a shared parameter which is associated to a retired bot process.


**Related topics**  


[Process parameter form in RPA Hub](../reference/process-parameter-form.md)

[Assign a bot process to a shared parameter](assign-botprocess-shared-parameter.md)

[Unassign a bot process from a shared parameter](unassign-botprocess-shared-parameter.md)

[View Audit History](https://www.servicenow.com/docs/access?context=c_HistorySets&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

