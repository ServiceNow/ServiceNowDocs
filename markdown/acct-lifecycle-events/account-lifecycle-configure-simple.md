---
title: Configure simple Customer Success Management playbook tasks
description: You can configure simple playbook tasks using the Playbooks.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the account onboarding playbook using Playbooks, Configuring account onboarding, Account onboarding, Customer Success Management]
---

# Configure simple Customer Success Management playbook tasks

You can configure simple playbook tasks using the Playbooks.

## Before you begin

Role required:

-   sn\_acct\_lc.agent
-   One or more Playbooks roles. See [Playbooks roles](https://www.servicenow.com/docs/access?context=process-automation-designer-roles&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for details.

## About this task

You can add, modify, and delete any tasks for the Customer Success Management playbook using the Process Automation Designer. For example, if you want to configure one of the tasks in the Development &amp; Automation lane, perform the following steps.

## Procedure

1.  Navigate to **All** &gt; **Process Automation Designer**.

2.  Select the **Account lifecycle onboarding process**.

3.  Navigate to the Development &amp; Automation lane and select the Setup Account Relationships activity.

4.  In the Activity properties window, select **View all properties** and select **Advanced**.

5.  In the General tab, enter the label name and description.

6.  In the When to start field, select **With Previous**.

    This option enables you to execute all activities in the task in parallel.

7.  Select the Automation tab and select **Accounts Lifecycle Task** table.

8.  Add all required fields and any other fields that must be populated for this task in the Customer Success Management playbook.

9.  Select **Done** and then **Activate**.


