---
title: Migrate the bot process configuration to another environment in RPA Hub
description: Migrate the bot process configuration and associated assets to another environment in RPA Hub. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Migrating the bot process configuration, Migrate data, RPA Hub, Workflow Data Fabric]
---

# Migrate the bot process configuration to another environment in RPA Hub

Migrate the bot process configuration and associated assets to another environment in RPA Hub. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.

## Before you begin

Familiarize yourself with the bot process migration concept. For more information, see [Migrating the bot process configuration in RPA Hub](../concept/bot-process-migration.md).

Verify that you’ve completed the tasks that are related to setting up the target environment. For more information, see [Set up the ServiceNow Remote Instance spoke](../../../administer/integrationhub-store-spokes/task/setup-rem-instance.md#).

The bot process must be marked ready for migration. For more information, see [Mark the bot process as ready for migration in RPA Hub](mark-bot-process-ready-for-migration.md).

Verify that the life-cycle stage status of the bot process in the source environment is set to **Published**. For more information, see [Life-cycle stage statuses \(LLCS\) of a bot process in RPA Hub](../reference/lifecycle-stages-botprocess.md).

When you re-migrate, verify that the life-cycle stage status of the bot process in the target environment isn’t set to **Published** or **Retired**. If **Published**, the values are overridden in the target environment.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Select the bot process that you want to migrate.

5.  In the form header, select **Migrate**.

    You can't see the **Migrate** button when the bot process migration is in progress.

6.  In the Confirmation dialog box, select **Migrate**.


## Result

After the migration is completed successfully or if an error occurs, an email notification is sent to the user who performs the migration. To receive the email notification, the email address of the user must be added to the user profile.

## What to do next

-   [Associate a bot process to a bot process configuration record](select-botprocess.md#)
-   [Credential Management in RPA Hub](../concept/credential-management-rpa-hub.md)
-   [Adding details to your bot process in RPA Hub](../concept/post-req-bot-process-rpa.md)
-   [Publish a bot process in RPA Hub](publish-bot-process.md)

**Parent Topic:**[Migrating the bot process configuration in RPA Hub](../concept/bot-process-migration.md)

