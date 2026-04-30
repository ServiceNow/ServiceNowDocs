---
title: Configure the Manage documents activity UI in Information Request Playbook
description: Configure the Manage Documents activity UI in Information Request Playbook to allow agents to view, link, or unlink documents to an information request case.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Information Request Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure the Manage documents activity UI in Information Request Playbook

Configure the Manage Documents activity UI in Information Request Playbook to allow agents to view, link, or unlink documents to an information request case.

## Before you begin

This task requires the Document Management \[com.snc.platform\_document\_management\] plugin to be active on your instance. If Document Management \[com.snc.platform\_document\_management\] is not active on your instance, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for instructions.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Information Request**.

3.  Under Intake, select **Add Activity**.

4.  Select **Playbooks for Customer Service Management** &gt; **Manage Documents List**.

5.  Select the edit button, and rename the action to **Manage Documents**.

6.  Under When to Start, select **Immediately**.

7.  Select **View All Properties** to set the trigger and edit other configurations.

8.  In the top right corner of the screen, select the Advanced button to toggle it on.

    The Experience tab should now display.

9.  Select **Automation**.

10. Under Record, select **Trigger- Information Request** &gt; **Information Request Record**.

11. Under Conditions, select **State Is New**, then select Done.

12. Select Experience.

13. Under Associated table, select **Information Request**, and under Associated Record, select **Trigger- Information Request** &gt; **Information Request Record**.

14. Under Title, select **This Activity** &gt; **Label**.

15. Select **Done**, then **Activate**.


## Result

The Manage Documents UI activity is now configured, and the modal should now display when you open a new or existing Information Request Playbook.

