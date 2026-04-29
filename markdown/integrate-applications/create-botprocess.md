---
title: Configuring a bot process record in RPA Hub
description: In RPA Hub, you can create a bot process configuration record and assign assets to associate it with a bot process. Or you can just save the bot process configuration record, however it won't be associated to a bot process. It remains orphaned.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [bot process rpa hub, configuring bot process rpa hub, configuring bot process configuration rpa hub, configuring attended bot process rpa hub, configuring unattended bot process rpa hub]
breadcrumb: [Use, RPA Hub, Workflow Data Fabric]
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

-   **[Life-cycle stage statuses \(LLCS\) of a bot process in RPA Hub](../reference/lifecycle-stages-botprocess.md)**  
The State transition of a bot process guides you through the stages of its life cycle.
-   **[Execution priority of bot processes in RPA Hub](bot-process-prioritization-order-rpa-hub.md)**  
Learn how to prioritize bot processes efficiently and avoid triggering multiple automations on the same robot. The bot processes are organized by both robots and Windows user credentials.
-   **[Create a bot process configuration record in RPA Hub](../task/create-botprocess-config.md#)**  
Create a bot process configuration record in RPA Hub so that you can define the preliminary fields for a bot process record.
-   **[Associate a bot process to a bot process configuration record](../task/select-botprocess.md#)**  
Select a bot process configuration record to associate it with a bot process. This action creates a bot process record in RPA Hub.
-   **[Adding details to your bot process in RPA Hub](post-req-bot-process-rpa.md)**  
After you create a bot process in RPA Hub, you can add some details for your bot process, such as information about the credential groups, business applications, and more.
-   **[Publish a bot process in RPA Hub](../task/publish-bot-process.md)**  
Publish a bot process so that you can get it ready to execute a process.
-   **[Edit a bot process in RPA Hub](../task/edit-botprocess.md)**  
Edit an existing bot process in RPA Hub to modify a few details.
-   **[Retire a bot process in RPA Hub](../task/retire-bot-process.md)**  
Retire a bot process to turn it off. It's one of the life-cycle stages of a bot process. After you retire a bot process, you can't use it anymore.

**Parent Topic:**[Using RPA Hub](managing-rpa-hub.md)

