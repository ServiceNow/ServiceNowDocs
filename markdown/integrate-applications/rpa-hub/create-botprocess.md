---
title: Configuring a bot process record in RPA Hub
description: In RPA Hub, you can create a bot process configuration record and assign assets to associate it with a bot process. Or you can just save the bot process configuration record, however it won't be associated to a bot process. It remains orphaned.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [bot process rpa hub, configuring bot process rpa hub, configuring bot process configuration rpa hub, configuring attended bot process rpa hub, configuring unattended bot process rpa hub]
breadcrumb: [Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Configuring a bot process record in RPA Hub

In RPA Hub, you can create a bot process configuration record and assign assets to associate it with a bot process. Or you can just save the bot process configuration record, however it won't be associated to a bot process. It remains orphaned.

## What is a bot process

A bot process is a predefined sequence of actions that a robot follows to accomplish a specific task or achieve a particular goal.

Let's say that you have an Accounting System Update bot process. The associated robot logs in to your company's accounting system, such as SAP. The robot enters the extracted invoice data, which creates the entries for your accounts payable. The robot then attaches the original invoice to the accounting system for reference.

## Benefits of a bot process

A bot process enables you to do the following:

-   streamline operations
-   enhance efficiency
-   improve overall productivity

## What is a bot process configuration

A bot process configuration is a record that contains the bot process settings. The bot process configuration record is mapped to a bot process record. It is a one to one mapping.

You assign a package and schedule the bot process run that will be executed by the robot. You can add other details that pertain to the bot process, such as business applications, credential groups, robots, process robot credentials, process parameters, attended users, or groups. For more information about these terms, see [Robotic Process Automation \(RPA\) Hub glossary](../reference/rpa-hub-glossary.md#).

