---
title: Enable intent to action workflow from triggers
description: Enable and configure intent to action workflow to invoke this agentic workflow from triggers.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 1
breadcrumb: [Configure email agentic workflows, Use agentic workflows in emails, Now Assist in Notifications, Configure core features, Administer]
---

# Enable intent to action workflow from triggers

Enable and configure intent to action workflow to invoke this agentic workflow from triggers.

## Before you begin

Role required: sn\_notif\_agents.notification\_ai\_admin

**Important:** If intent to action has been enabled from Inbound email actions then do not enable intent to action from triggers.

## Procedure

1.  Navigate to **All**, in the search filter, enter `sys_flow_email_trigger`.

2.  Select the filter icon to search based on **Sys ID**.

3.  Enter `e856ae0bff24f210359bffffffffff07` as the Sys ID and select the **Run** button.

4.  Open the record, select the **Active** check box to activate.

    **Note:** In the Email Triggers table, for **Stop condition evaluation** when the trigger is set to **true**, it prevents the system from evaluating trigger conditions after this one. If you want trigger conditions after this, select **true** and set it to **false**.

5.  Run the flow on an incoming email.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Select the **Flows** data pill filter

    3.  Search and open the **Trigger Intent to Action** flow.

    4.  Select the **Edit** button to edit the trigger.

    5.  Select **Inbound Email** trigger and set the desired email conditions that need to be met to run the flow.

    6.  Select **Activate**.

        For more information, see [Edit a flow](https://www.servicenow.com/docs/access?context=flow-edit&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US), [Test a flow](https://www.servicenow.com/docs/access?context=flow-test&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US), and [Activate a flow](https://www.servicenow.com/docs/access?context=flow-activate&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


## What to do next

[Create email intents](create-email-intent.md)

**Parent Topic:**[Configure email agentic workflows in Notifications](../reference/configuring-agentic-workflows-in-notifications.md)

