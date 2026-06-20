---
title: Set up Slack spoke
description: Integrate the ServiceNow instance and your Slack account by creating a custom OAuth application in Slack to authenticate ServiceNow requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/integrate-applications/integration-hub/set-up-slack.html
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-02-11"
reading_time_minutes: 1
breadcrumb: [Slack Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up Slack spoke

Integrate the ServiceNow instance and your Slack account by creating a custom OAuth application in Slack to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Slack spoke.
-   Slack account.
-   Add Slack users to the User \[sys\_user\] table of your ServiceNow instance, with **Email** being the unique identifier.
-   Role required: admin

## About this task

The spoke set up procedure outlined here requires bot user tokens only. You can't use the Create User and Deactivate User actions while using the bot token scopes. To use these actions, you must obtain user token from your Slack account.

Perform these steps to set up the Slack spoke.

1.  [Configure Slack app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/integration-hub/configure-slack-workspace.md).
2.  [Add Slack connection in ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/integration-hub/setup-slackspoke-fd.md).
3.  [Provide Signing Key in ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/integration-hub/provide-signingkey-slack.md).
4.  [Configure outbound configurations in ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown).
5.  [Configure inbound decisions in ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/integration-hub/conf-inbound-slack.md).

