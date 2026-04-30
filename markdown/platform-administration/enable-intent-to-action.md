---
title: Enable intent to action workflow from inbound actions
description: Enable and configure intent to action workflow to invoke the agentic workflow from inbound actions.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Configure email agentic workflows, Use agentic workflows in emails, Now Assist in Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable intent to action workflow from inbound actions

Enable and configure intent to action workflow to invoke the agentic workflow from inbound actions.

## Before you begin

Role required: sn\_notif\_agents.notification\_ai\_admin

**Important:** If intent to action has been enabled from the Workflow studio flow for Inbound email trigger then do not enable intent to action from inbound actions.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Email** &gt; **Inbound Actions**.

2.  Search for **Trigger Intent to Action**.

3.  Select the **Active** check box to activate the inbound email action.

4.  In the **Order** field, enter the desired order number, the default value mentioned is **999**.

    **Note:** You can modify the order number to determine the point at which the agentic workflow is invoked.

5.  Select **Update**.


## What to do next

[Create email intents](create-email-intent.md)

