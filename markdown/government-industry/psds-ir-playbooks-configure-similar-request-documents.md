---
title: Configure Similar Request Documents UI in Information Request Playbook
description: The Similar Request Documents Activity UI uses the name and description of existing information request cases to display a list of documents associated with the current case, providing helpful information the documents used to resolve similar information requests in Information Request Playbook.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Information Request Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Similar Request Documents UI in Information Request Playbook

The Similar Request Documents Activity UI uses the name and description of existing information request cases to display a list of documents associated with the current case, providing helpful information the documents used to resolve similar information requests in Information Request Playbook.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Information Request**.

3.  Under Intake, select **Add Activity**.

4.  Select**Playbooks for Customer Service Management** &gt; **Similar Documents**.

5.  Select the edit button, and rename **Similar Documents** to **Similar Request Documents**.

6.  Under When to Start, select **Immediately**.

7.  Select **View All Properties** to set the trigger and edit other configurations.

8.  In the top right corner of the screen, select the Advanced button to toggle it on.

    The Experience tab should now display.

9.  Select **Automation**.

10. Under Record, select **Trigger- Information Request** &gt; **Information Request Record**.

11. Under Conditions, select **State Is New**.

12. Select the Experience tab.

13. Under Associated table, select **Information Request**, and under Associated Record, select **Trigger- Information Request** &gt; **Information Request Record**.

14. Under Related Record Encoded Query, enter**state=3**.

15. Under Title, select **This Activity** &gt; **Label**.

16. Select **Done**, then **Activate**.


## Result

The Similar Documents UI activity is now configured, and the modal should now display when you open a new or existing Information Request Playbook.

