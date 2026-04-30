---
title: Create and integrate a self-configured bot for a single tenant page
description: Create a self-configured single tenant bot with Microsoft Teams for integration with Virtual Agent.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Create and integrate a self-configured bot for a single tenant page

Create a self-configured single tenant bot with Microsoft Teams for integration with Virtual Agent.

## Before you begin

Role required: virtual\_agent\_admin or admin and Microsoft Azure admin.

## About this task

Creating and integrating a single tenant bot is similar to creating a GCC-H or DoD bot, with minor adjustments.

## Procedure

1.  Follow the instructions in [Create a bot in Microsoft Teams for GCC-H or DoD](create-msteams-bot-gcch.md), with the following changes.

    1.  Follow steps 1 through 4 as normal.

    2.  In step 5, select **Single tenant**.

    3.  Follow the remaining steps as normal.

2.  Follow the instructions in [Integrate your Self-configured bot with Microsoft Teams for GCC-H or DoD](link-msteams-bot-snow.md), with the following changes.

    1.  Follow steps 1 through 6 as normal.

    2.  In step 7, select **Single tenant**, and add your tenant ID, but keep the `.com` domain, for example: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/token`.

    3.  Follow steps 8 through 10 as normal.


## Result

Your single-tenant bot is ready for use in Virtual Agent.

