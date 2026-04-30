---
title: Migrating the bot process configuration in RPA Hub
description: In RPA Hub, you can migrate the bot process configuration and associated assets for an attended or unattended bot process from one environment to another environment. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Migrating the bot process configuration in RPA Hub

In RPA Hub, you can migrate the bot process configuration and associated assets for an attended or unattended bot process from one environment to another environment. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.

## Bot process migration overview

You can migrate the bot processes from any environment to any environment. For example, when a bot process is ready to be migrated from a developer’s environment to a UAT environment, an RPA developer or RPA administrator can select the **Ready for Migration** button on a published bot process. This action enables the **Migrate** button to appear. This button is only visible when the bot process migration isn’t in progress. Then, an RPA release manager or RPA administrator can initiate the migration process by selecting the **Migrate** button. After the bot process and associated assets are migrated, a release manager can make any necessary changes \(such as creating more process parameters, shared parameters, or credential mapping\), create and associate credentials, create an associated bot process record, and publish the bot process on the UAT \(target\) environment.

## What's migrated with the bot process

In an unattended bot process migration, the following records and associated assets are also migrated:

-   Bot process configuration
-   Packages
-   Package versions with attachments
-   Process parameters
-   Shared process parameters, if assigned to the bot process
-   Schedules
-   Queues
-   Associated skills

In an attended bot process migration, the following records and associated assets are also migrated:

-   Bot process configuration
-   Packages
-   Package versions with attachments
-   Process parameters
-   Shared process parameters, if assigned to the bot process
-   Process field parameters, if Embedded Task Automation \(ETA\) is enabled
-   Attended configurations, if ETA is enabled
-   Queues
-   Associated skills

## What's not migrated with the bot process

The robot credentials, application credentials, and credential group that are associated with the bot process configuration aren't migrated. After the bot process configuration is migrated, the credentials must be created or updated in the target environment.

If any shared parameters or process parameters are marked as sensitive in the bot process, the sensitive values that are stored in these parameters aren't migrated and the parameter values are empty in the target environment.

Only the default field values are migrated. The custom field values aren't migrated.

## Restructured RPA Hub tables \(Tokyo and earlier releases\)

For Tokyo and earlier releases, you must restructure the RPA Hub tables before migration. For more information, see [Restructuring RPA Hub tables](restructured-rpa-hub-tables-utah.md).

**Related topics**  


[Mark the bot process as ready for migration](../task/mark-bot-process-ready-for-migration.md)

[Migrate the bot process configuration to another environment](../task/migrate-bot-process.md)

