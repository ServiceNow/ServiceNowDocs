---
title: Set up Slack spoke
description: Integrate the ServiceNow instance and your Slack account by creating a custom OAuth application in Slack to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Slack Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Slack spoke

Integrate the ServiceNow instance and your Slack account by creating a custom OAuth application in Slack to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Slack spoke.
-   Slack account.
-   Add Slack users to the User \[sys\_user\] table of your ServiceNow instance, with **Email** being the unique identifier.
-   Role required: admin.

## About this task

The spoke set up procedure outlined here requires bot user tokens only. You can't use the Create User and Deactivate User actions while using the bot token scopes. To use these actions, you must obtain user token from your Slack account.

