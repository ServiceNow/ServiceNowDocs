---
title: Example Asset Refresh Virtual Agent conversation with notifications
description: Virtual Agent can automate many workflows, and a number of common solutions are available when you install Virtual Agent and related plugins, such as ITSM Virtual Agent Conversations.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Example Asset Refresh Virtual Agent conversation with notifications

Virtual Agent can automate many workflows, and a number of common solutions are available when you install Virtual Agent and related plugins, such as ITSM Virtual Agent Conversations.

For an overview of the Asset Refresh workflow from the user perspective, watch this video.

Automate workflows with Virtual Agent. In this example, a user is notified that it's time to get a new tablet. The Virtual Agent workflow helps him order a replacement.

## Pre-built components in Virtual Agent

Virtual Agent comes with a basic configuration that includes common greetings, NLU intents, reusable logic, and pre-built conversations. Using these building blocks, you can quickly put together workflows to handle some of the most common organizational needs, including the following:

-   [Resetting a password](https://www.servicenow.com/docs/access?context=itsm-password-management&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)
-   [IT Self-Service](https://www.servicenow.com/docs/access?context=itsm-va-self-service-topics&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)
-   [IT troubleshooting](https://www.servicenow.com/docs/access?context=itsm-va-it-issues-generic&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)
-   [HR queries and employee profile updates](https://www.servicenow.com/docs/access?context=hr-virtual-agent-conversations&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)
-   [Customer Service queries and requests](https://www.servicenow.com/docs/access?context=csm-virtual-agent-chatbot&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)

To help you understand the possibilities, the Asset Refresh example uses pre-built topic blocks that are included in the [ITSM Virtual Agent Conversations](https://www.servicenow.com/docs/access?context=itsm-virtual-agent&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) plugin. These topic blocks do most of the "heavy lifting" in the topic.

## Asset Refresh workflow

The purpose of the Asset Refresh topic is to automate hardware upgrades for your employees. If your organization's policy is to replace computers or tablets every two years, then you can create a business rule that says when a user has had an asset for two years, the asset should move to the **In maintenance** state. You can create a notification that is triggered by this change of state in the Hardware table. In our example, the asset owner receives the notification and is instructed to upgrade their asset.

The Asset Refresh Virtual Agent topic provides the action for the notification. When the user selects the link in the notification, they proceed to the workflow in Virtual Agent. This example topic contains the primary flow \(helping the user upgrade their hardware\) and two secondary flows that ensure that the user's needs are met.

![The conversation workflow includes the primary path for upgrading the asset, as well as workflows for creating an Incident or helping the customer to understand the organization's upgrade policy first.](../images/crawl-ex-workflow-graphic.png)

After a greeting message, Virtual Agent asks the user if they want to upgrade now or get more information. If they choose to upgrade now, they are directed through the primary flow. Virtual Agent uses the Lookup utility to find the expiring asset that is assigned to the user. Then Virtual Agent makes sure the user still has the asset. If they do not, Virtual Agent uses the Create Incident topic block to open an Incident to resolve the problem. If the user still has the asset, Virtual Agent uses the Search Catalog Item topic block to find a replacement. The Request Catalog Item topic block is used to request it. The request is sent to the user, and the workflow ends.

If the user chooses to get more information, the AI Search topic block returns one or more specific KB articles that explain the organization's policy. Once the user has viewed these, they are given the option to upgrade now or later. If they choose to upgrade now, they are redirected through the primary workflow; otherwise, the conversation ends.

## Creating the Asset Refresh example workflow

The following topics describe how to use Virtual Agent Designer and actionable notifications to create the Asset Refresh workflow. Follow these steps in order.

1.  [Create the Asset Refresh topic in Virtual Agent Designer](../task/create-example-conv-asset-refresh.md).
2.  [Create the Open Incident workflow in the Asset Refresh topic](../task/create-example-asset-refresh-flow2.md).
3.  [Create the More Information workflow in the Asset Refresh topic](../task/create-example-asset-refresh-flow3.md).
4.  [Create the notification for the Asset Refresh topic](../task/create-example-asset-refresh-notification.md).
5.  [Associate content with the Asset Refresh notification](../task/associate-content-example-notification.md).

