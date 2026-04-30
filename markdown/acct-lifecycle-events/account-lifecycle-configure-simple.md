---
title: Configure simple Account Lifecycle Events playbook tasks
description: You can configure simple playbook tasks using the Playbooks.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure the account onboarding playbook using Process Automation Designer, Configuring account onboarding, Account onboarding, Account Lifecycle Events]
---

# Configure simple Account Lifecycle Events playbook tasks

You can configure simple playbook tasks using the Playbooks.

## Before you begin

Role required:

-   sn\_acct\_lc.agent
-   One or more Playbooks roles. See [Playbooks roles](https://www.servicenow.com/docs/access?context=process-automation-designer-roles&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) for details.

## About this task

You can add, modify, and delete any tasks for the Account Lifecycle Events playbook using the Process Automation Designer. For example, if you want to configure one of the tasks in the Development &amp; Automation lane, perform the following steps.

## Procedure

1.  Navigate to **All** &gt; **Process Automation Designer**.

2.  Select the **Account lifecycle onboarding process**.

3.  Navigate to the Development &amp; Automation lane and select the Setup Account Relationships activity.

4.  In the Activity properties window, select **View all properties** and select **Advanced**.

5.  In the General tab, enter the label name and description.

6.  In the When to start field, select **With Previous**.

    This option enables you to execute all activities in the task in parallel.

7.  Select the Automation tab and select **Accounts Lifecycle Task** table.

8.  Add all required fields and any other fields that must be populated for this task in the Account Lifecycle Events playbook.

9.  Select **Done** and then **Activate**.


