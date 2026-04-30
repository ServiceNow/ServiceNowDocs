---
title: Connect SPW to Jira
description: Connect Strategic Planning Workspace to Jira to enable the integration between the applications.
locale: en-US
release: yokohama
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Configure, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Connect SPW to Jira

Connect Strategic Planning Workspace to Jira to enable the integration between the applications.

## Before you begin

Role required: sn\_jira\_int.user

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Jira Integration** &gt; **Jira Instances**.

2.  Select your Jira instance.

3.  Click **Get Webhook Callback URL**.

4.  Set up a webhook using this URL in Jira Administration.

    This action is done outside your ServiceNow instance.

    [Registering a webhook via the Jira administration console](https://developer.atlassian.com/server/jira/platform/webhooks/#registering-a-webhook-via-the-jira-administration-console)

5.  On the Jira instance form, select **Connect**.


## Result

If the connection is successful, the **State** field on your Jira instance record shows **Connected**. A webhook is now registered in Jira to receive update events.

## What to do next

[Import Jira projects to SPW](imports-jira-projects-to-spw.md).

