---
title: Copy subflow template for callback routing
description: Create a copy of External Callback Operations Template in Workflow Studio Subflows and make the necessary modifications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/omnichannel-callback/configure-callback-route-copy-subflow-template.html
release: zurich
product: Omnichannel Callback
classification: omnichannel-callback
topic_type: task
last_updated: "2026-01-16"
reading_time_minutes: 1
breadcrumb: [Configuring Omnichannel Callback, Omnichannel Callback, Manage people and work, Conversational Interfaces]
---

# Copy subflow template for callback routing

Create a copy of External Callback Operations Template in Workflow Studio Subflows and make the necessary modifications.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **Subflows**.

3.  Search for **External Callback Operations Template** and open it.

4.  Select the \[Omitted image "icon-ellipses.png"\] Alt text: More actions menu more actions icon, and select **Copy subflow**.

    To learn more, see .

5.  Activate or open the copied subflow.

    -   Make sure that the subflow is available and activated on the base system.
    -   Activate the copied subflow after making the required changes.
6.  Use the **Inputs &amp; Outputs** in the subflow to define the payload for external routing.

    The input and output parameters are automatically copied to the subflow template.

7.  Create a Workflow Studio Subflow action to make third-party API calls and publish the subflow.

    To learn more, see .

    You have successfully copied and executed the subflow.


## What to do next

[Configure callback routing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/omnichannel-callback/configure-callback-route-ccaas-api.md).

