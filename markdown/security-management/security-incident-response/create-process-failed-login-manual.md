---
title: Create processes for Failed Login Manual in PAD
description: Use these steps to create processes for Failed Login Manual in the Process Automation Designer \(PAD\).
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Playbook for Failed Login Manual, Process-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create processes for Failed Login Manual in PAD

Use these steps to create processes for Failed Login Manual in the Process Automation Designer \(PAD\).

## Before you begin

Role required: sn\_si.admin or sn\_si.manager

## Procedure

1.  Select **All** &gt; **Process Automation Designer** &gt; **** &gt; **New** and select **Playbook**.

    For example, Failed Login Manual Playbook Template V1.

2.  Enter a name for the process, the description, and the application for which the process is being created.

3.  Select **Select a trigger**.

4.  Select **Define your own conditions for when your process runs**, and select the trigger condition for when your process must run.

5.  Select **Set your trigger conditions**.

6.  Choose the conditions to define when your process must run by selecting a table and filling in the conditions.

    For example, the trigger condition is when a security incident of category Phishing is created.

7.  Select **Go to Designer**.

    The Process Automation Designer page opens.

8.  To start designing your automated process, select **Add a new stage**.

    The stage properties pane opens on the right side of the UI.

9.  In the stage properties pane, enter the following details: **Name**, **Description**, **Run condition**, and **Indicate when to start**.

    The **Run condition** and **Indicate when to start** fields imply when the stage would run.

10. Select **Save and close**.

11. To add another stage, select **Add another stage**.

    Similarly, you can create as many stages as you want. In this example, you can create a stage for Analysis, Contain, Eradicate, and Review respectively. In the following example, **Analysis** stage starts immediately and has no run condition. **Contain** stage start after the previous stage is completed and has a run condition that is based on the outcome of an activity in the previous stage.

    After adding the stages, you need to add process activities for each stage.

12. Select **Add another process activity** under a particular stage \(For example, Analysis stage\).

    The Add activity pop-up opens.

    1.  In the Add activity pop-up, select the required activity definition.

13. Select **Create a new activity**.

    After an activity definition is added, it can be further configured similar to stages. Similarly, you can create other process activities under each stage.

14. In the Activity properties pane, add a run condition and indicate when to start the process activity.

15. Add a run condition and indicate when to start.

    All the input required for this activity \(Includes inputs in the automation plan that are configured\) will be shown. You can override the values or use the preconfigured values.

16. Select **View all properties** and enable the **Advanced properties** toggle to display all the activity experience fields from the activity definition.


**Parent Topic:**[Playbook for Failed Login Manual](../concept/playbook-failed-login.md)

