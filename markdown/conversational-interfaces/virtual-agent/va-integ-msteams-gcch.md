---
title: Integrating Virtual Agent with Microsoft Teams for GCC-H or DoD
description: You can integrate Virtual Agent with Microsoft Teams for GCC-H \(Government Community Cloud - High\) or DoD \(Department of Defense\) customers by configuring your own bots. The self-configured method provides another way for customers to enable the integration without installing the default Now Virtual Agent app that is published on the Microsoft Store. The self-configured bot bypasses the collaboration proxy architecture.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with Microsoft Teams for GCC-Hor DoD

You can integrate Virtual Agent with Microsoft Teams for GCC-H \(Government Community Cloud - High\) or DoD \(Department of Defense\)customers by configuring your own bots. The self-configured method provides another way for customers to enable the integration without installing the default Now Virtual Agent app that is published on the Microsoft Store. The self-configured bot bypasses the collaboration proxy architecture.

If you are a commercial customer who has already installed a pre-published bot but would like to integrate with multiple ServiceNow instances within a single Microsoft Teams tenant, see [Integrate your Self-configured bot with single Microsoft Teams tenant](../task/teams-install-custom-app.md).

If you are aMicrosoft GCC \(GovtCommunityCloud\) customer, do not follow this step. Instead, refer to [Integrating Virtual Agent with Microsoft Teams using the self-configured bot](va-integ-teams-self-configured-bot.md).

## Prerequisites

Before integrating Virtual Agent with your Microsoft Teams tenant, ensure that the following prerequisites are met:

-   Verify that your ServiceNow instances have been upgraded to the San Diego release.
-   Verify that you have not previously attempted installing the Conversational Integration with Microsoft Teams app on your instances.

    If you previously tried to install the integration in Quebec and the above releases, refer to this [Knowledge Base](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1116195) article to remove the residual installation items.

    If you previously tried to install the integration in a release prior to Quebec, contact Customer Service and Support for help with cleaning up your instance manually.

-   Verify that you have the admin permissions on ServiceNow and Microsoft Azure instances.

## What to do next

1.  [Plugins for Conversational Integration with Microsoft Teams](../reference/addtional-plugins-msteams.md).
2.  [Create a bot in Microsoft Teams for GCC-H or DoD](../task/create-msteams-bot-gcch.md).
3.  [Integrate your Self-configured bot with Microsoft Teams for GCC-H or DoD](../task/link-msteams-bot-snow.md).
4.  [Auto-generate the manifest file and upload it into Microsoft Teams for GCC-H or DoD](../task/upload-app-package-msteams.md).

