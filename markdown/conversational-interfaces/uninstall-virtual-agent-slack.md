---
title: Remove Virtual Agent integration with Slack
description: Remove the Virtual Agent integration from your ServiceNow instance to disassociate the Slack app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/uninstall-virtual-agent-slack.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Virtual Agent, integration, Slack]
breadcrumb: [Integrate Virtual Agent with Slack, Slack, Integrate VA with messaging apps, Conversational Integration apps for Virtual Agent, Conversational Interfaces]
---

# Remove Virtual Agent integration with Slack

Remove the Virtual Agent integration from your ServiceNow instance to disassociate the Slack app.

## Before you begin

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, select **View All**.

3.  On the Channels and integration page, in the Slack tile, select **Manage**.

4.  In the Manage Slack channel page, find the Virtual Agent integration to remove from your ServiceNow instance, and then select the manage bot icon \[Omitted image "manage-bot-icon.png"\].

5.  Select **Remove integration**.

    \[Omitted image "remove-snva-integration.png"\] Alt text: Remove integration option with Now Virtual Agent.

6.  When prompted to confirm your choice, select **Remove**.

    The Slack app directory displays.

7.  Navigate to the **Configuration** tab, and then select **See All** against **1 authorized member**.

8.  Select **Revoke** in the 1 Authorized member pop-up.

9.  Select **Revoke** in the confirmation message.\[Omitted image "revoke-slack-snow-integ.png"\] Alt text: Revoke ServiceNow Virtual Agent integration with Slack.

    A message displays that says: **You have successfully removed an authorization for Now Virtual Agent**

    Virtual Agent integration with Slack is removed from your ServiceNow instance.


**Parent Topic:**[Integrating Virtual Agent with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-integ-slack.md)

