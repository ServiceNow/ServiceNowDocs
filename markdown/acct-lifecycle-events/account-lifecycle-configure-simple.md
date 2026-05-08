---
title: Configure onboarding tasks in playbook
description: You can configure customer success onboarding tasks in a playbook using the Process Automation Designer.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure playbook activities, Account onboarding, Customer Success Management, Customer Success Management]
---

# Configure onboarding tasks in playbook

You can configure customer success onboarding tasks in a playbook using the Process Automation Designer.

## Before you begin

Role required:

-   sn\_acct\_lc.agent
-   One or more Playbooks roles. See Playbooks roles for details.

## About this task

You can add, modify, and delete any tasks for the Customer success onboarding tasks in a playbook using the Process Automation Designer. For example, if you want to configure one of the tasks in the Development &amp; Automation lane, perform the following steps.

## Procedure

1.  Navigate to **All** &gt; **Process Automation Designer** &gt; **Playbook Designer**.

2.  Select the **Account lifecycle onboarding process**.

3.  Navigate to the Development &amp; Automation lane and select the Setup Account Relationships activity.

4.  In the Activity properties window, select **View all properties** and select **Advanced**.

5.  In the General tab, enter the label name and description.

6.  In the When to start field, select **With Previous**.

    This option enables you to execute all activities in the task in parallel.

7.  Select the Automation tab and select **Onboarding Task** table.

8.  Add all required fields and any other fields that must be populated for this task in the Customer success onboarding in the onboarding playbook.

9.  Select **Done** and then **Activate**.


**Parent Topic:**[Configure the onboarding playbook activities](../concept/account-lifecycle-pad.md)

