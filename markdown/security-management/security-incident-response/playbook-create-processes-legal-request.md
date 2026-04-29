---
title: Create processes for Legal Request playbook
description: Use these steps to create processes for Legal Request playbook in the Process Automation Designer \(PAD\).
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Playbook for Legal Request, MSIM Playbooks, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create processes for Legal Request playbook

Use these steps to create processes for Legal Request playbook in the Process Automation Designer \(PAD\).

## Before you begin

Role required: sn\_msi.workspace\_manager.

## Procedure

1.  Click **ALL** &gt; **Process Automation Designer** &gt; **** &gt; **Create a new process**.

    For example, Legal request Playbook.

2.  Enter a name for the process, the description, and the application for which the process is being created.

3.  Click **Select a trigger**.

4.  Select **Define your own conditions for when your process runs**, and select the trigger condition for when your process must run.

5.  Click **Set your trigger conditions**.

6.  Choose the conditions to define when your process must run by selecting a table and filling in the conditions.

7.  Click **Go to Designer**.

    The Process Automation Designer page opens.

8.  To start designing your automated process, click **Add a new lane**.

    The Lane properties pane opens on the right side of the UI.

9.  In the Lane properties pane, enter the following details: **Name**, **Description**, **Run condition**, and **Indicate when to start**.

    The **Run condition** and **Indicate when to start** fields imply when the lane would run.

10. Click **Save and close**.

11. To add another lane, click **Add another lane**.

    Similarly, you can create as many lanes as you want. In this example, you can create a lane for Analysis, Contain, Eradicate, and Review respectively. In the following example, **Analysis** lane starts immediately and has no run condition. **Contain** lane start after the previous lane is completed and has a run condition that is based on the outcome of an activity in the previous lane.

    After adding the lanes, you need to add process activities for each lane.

12. Click **Add another process activity** under a particular lane \(For example, Analysis lane\).

    The Add activity pop-up opens.

    1.  In the Add activity pop-up, select the required activity definition.

13. Click **Create a new activity**.

    After an activity definition is added, it can be further configured similar to lanes. Similarly, you can create other process activities under each lane.

14. In the Activity properties pane, add a run condition and indicate when to start the process activity.

15. Add a run condition and indicate when to start.

    All the input required for this activity \(Includes inputs in the automation plan that are configured\) will be shown. You can override the values or use the preconfigured values.

16. Click **View all properties** and enable the **Advanced properties** toggle to display all the activity experience fields from the activity definition.


