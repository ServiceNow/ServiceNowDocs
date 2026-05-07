---
title: Create a success play
description: Use this option to create a success play to create automated actions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Basic setup, Customer success, Customer Success Management, Customer Success Management]
---

# Create a success play

Use this option to create a success play to create automated actions.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

## About this task

With success plays, you can use Flow Designer and playbooks to quickly create actions that need to be executed during the engagement lifecycle. These actions can be manual or completely automated. This section describes how to create a success play from the engagement record page. You can also launch the success play workflow from any of the following pages:

-   Success initiative
-   Success objective
-   Touchpoints
-   Success case
-   Internal play
-   Risk signal

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  On the Success landing page, select **View engagement** and then select **Create success play**.

3.  Select a category that aligns with your goal.

    The sub categories displayed are filtered based on the category that you select here.

4.  Select a sub category from the list and select the activity that must be completed to achieve your goal.

5.  Select **Next** to continue.

    Based on your previous selections, you’re prompted for additional details in the next page.

6.  Select **Finish**.

    You’ll see a notification indicating that the success play has been created. When the tasks are completed, the work notes are updated indicating that it’s complete.

    **Note:** When you start creating a success play, a success launcher notifier record is created to track the status of the success play. To view this record, navigate to the **All** menu and enter `sn_acct_lc_success_notifier_launcher.list` in the Search filter. You can view the status in the Success Launcher Notifiers page.


-   **[Define subflows for success plays](account-lifecycle-config-subflow.md)**  
Before you create a success play, you must define a subflow and add it to the Definition Records table.

**Parent Topic:**[Basic customer success setup](../concept/account-lifecycle-basic-config.md)

