---
title: Specifying the inbound email processing order
description: You can configure a processing order for inbound email actions and use the order to manage multiple filters in inbound email actions.Configure the processing order for inbound email actions to force them to run in a prescribed order.Use process ordering and the stop\_processing command to manage multiple filters in inbound email actions.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure inbound email actions, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Specifying the inbound email processing order

You can configure a processing order for inbound email actions and use the order to manage multiple filters in inbound email actions.

The Ordered Email Processing \(com.glide.email\_ordered\_processing\) plugin is enabled by default for new instances. Users with the admin role can activate the plugin for upgraded instances. The plugin adds the **Order** column to the Rules \[sysrule\] table, which the instance uses to determine when to process emails. Admins can also add a command to an action script that halts processing after the script runs.

**Parent Topic:**[Configure inbound email actions](../concept/configure-inbound-email.md)

## Configure the processing order

Configure the processing order for inbound email actions to force them to run in a prescribed order.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Email** &gt; **Inbound Actions**.

2.  Open an existing inbound action or create one.

3.  Complete the form and assign an order number to the **Order** field to establish when this inbound rule should run in relation to other rules.

    If you upgraded and activated the plugin, the **Order** field might be named **Execution Order**.

    **Note:** Ensure each inbound action has a unique **Order** value to ensure the system stops processing as expected. If multiple inbound actions have the same **Order** value, the system might evaluate all of the inbound actions, even if one of them contains the `event.state="stop_processing";` script or has the **Stop processing** option selected.

4.  To stop rule processing when an inbound email action runs successfully: add the following line to the bottom of the script:

    -   Select the **Stop processing** check box.
    -   Add the following line to the bottom of the **Actions** script:

        ```
        event.state="stop_processing";
        ```


## Manage multiple filters in an inbound email action

Use process ordering and the stop\_processing command to manage multiple filters in inbound email actions.

### Before you begin

Role required: admin

### About this task

In this example, you can create new problem records when `prb:` appears in the subject line and new change requests when `chg:` appears in the subject line. All other emails are used to create an incident. The actions are set up as follows:

### Procedure

1.  Create an action with a condition of `Subject > starts with > chg:` and the `event.state="stop_processing";` command appended to the script.

2.  Assign this action an Order value of `100`.

3.  Create an action with a condition of `Subject > starts with > prb:` and the `event.state="stop_processing";` command appended to the script.

4.  Assign this action an Order value of `200`.

5.  Create an action for incident with no conditions and an Order value of `300`.

    It is not necessary to add the stop\_processing command to the script for the incident action unless you want processing to stop at this rule to avoid continuing to another action.


### Result

If either a change request or a problem is created, the stop\_processing command stops processing, and no incident record is created. If neither a change request nor a problem is created, the inbound email action for incident creates a record.

