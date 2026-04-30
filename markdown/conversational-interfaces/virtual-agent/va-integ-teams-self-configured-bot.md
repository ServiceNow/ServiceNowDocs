---
title: Integrating Virtual Agent with Microsoft Teams using the self-configured bot
description: You can integrate Virtual Agent with Microsoft Teams by configuring your own bots. The self-configured method provides another way for customers to enable the integration without installing the default Now Virtual Agent app that is published on the Microsoft Store. Unlike the pre-published app, the self-configured bot bypasses the collaboration proxy architecture.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with Microsoft Teams using the self-configured bot

You can integrate Virtual Agent with Microsoft Teams by configuring your own bots. The self-configured method provides another way for customers to enable the integration without installing the default Now Virtual Agent app that is published on the Microsoft Store. Unlike the pre-published app, the self-configured bot bypasses the collaboration proxy architecture.

The self-configured method offers a solution for the following cases:

-   Commercial customers with a ServiceNow instance running far away from the United States who may be having issues using the collaboration proxy.
-   ServiceNow Government Community Cloud \(GCC\) customers.

    **Note:** Microsoft Azure supports the bot framework in GCCHIGH and DOD \(US Department of Defense\). For more information about the bot framework support, see [Integrating Virtual Agent with Microsoft Teams for GCC-H or DoD](va-integ-msteams-gcch.md).


If you are a commercial customer who has already installed a pre-published bot but would like to integrate with multiple ServiceNow instances within a single Microsoft Teams tenant, see [Integrate your Self-configured bot with single Microsoft Teams tenant](../task/teams-install-custom-app.md).

## Prerequisites

Before integrating Virtual Agent with your Microsoft Teams tenant, ensure that the following prerequisites are met:

-   Verify that your ServiceNow instances have been upgraded to the San Diego release.
-   If you are a commercial user, verify that your Microsoft 365 is on the commercial environment. If you are a regulated market user, verify that your Microsoft 365 is on the GCC environment.
-   You have not attempted previous installations of the Conversational Integration with Microsoft Teams in your instances.

    If you previously tried to install the integration in Quebec and the above releases, refer to this [Knowledge Base](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1116195) article to remove the residual installation items.

    If you previously tried to install the integration in a release prior to Quebec, contact Customer Service and Support for help with cleaning up your instance manually.

-   Verify that you have the admin permissions on ServiceNow and Microsoft Azure instances.

## What to do next

1.  [Plugins for Conversational Integration with Microsoft Teams](../reference/addtional-plugins-msteams.md)
2.  [Create a Bot in Microsoft Teams](../task/create-bot-msteams.md)
3.  [Integrate your Self-configured bot with Microsoft Teams for GCC](../task/resgiter-bot-on-snow.md).
4.  [Auto-generate the manifest file for uploading on Microsoft Teams](../task/generate-manifest-file-msteams.md)
5.  [Upload the manifest package file to publish your bot](../task/upload-package-file-msteams.md)

