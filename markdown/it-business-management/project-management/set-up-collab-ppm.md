---
title: Setting up PPM collaboration for Slack
description: Integrate your ServiceNow instance with your organization's Slack to enable collaboration of your projects in Slack.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [PPM Collaboration, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Setting up PPM collaboration for Slack

Integrate your ServiceNow instance with your organization's Slack to enable collaboration of your projects in Slack.

PPM Collaboration uses the Slack spoke actions such as creating a channel for your project, adding or removing your project team members, archiving the channel when the project is closed, posting a message when a record is updated, and so on. To enable these spoke actions, you must integrate your ServiceNow instance with Slack to authenticate ServiceNow requests. For more information, see [Set up Slack spoke](https://www.servicenow.com/docs/access?context=set-up-slack&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

**Important:** When you activate Slack spoke, a [Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for Slack is created by default with the ID **sn\_slack\_ah\_v2.Slack**. The connection that is active \(the Active field is set to **true**\) in Connections related list of this alias uses this default ID to connect your ServiceNow instance to Slack. Therefore, you can have multiple connections associated with this alias but ensure that only one connection is active at any given time.

**Parent Topic:**[Using Project Management](../../project-management/concept/using-project-management.md)

**Related topics**  


[Slack spoke v2](https://www.servicenow.com/docs/access?context=slack-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)

