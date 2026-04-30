---
title: Mark the bot process as ready for migration
description: Mark the bot process as ready for migration in RPA Hub so that the bot process configuration and associated assets can be migrated to another environment. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Mark the bot process as ready for migration

Mark the bot process as ready for migration in RPA Hub so that the bot process configuration and associated assets can be migrated to another environment. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.

## Before you begin

Familiarize yourself with the bot process migration concept. For more information, see [Migrating the bot process configuration in RPA Hub](../concept/bot-process-migration.md).

Verify that you’ve completed the tasks that are related to setting up the target environment. For more information, see [Set up the ServiceNow Remote Instance spoke](../../../administer/integrationhub-store-spokes/task/setup-rem-instance.md#).

Verify that the life-cycle stage status of the bot process in the source environment is set to **Published**. For more information, see [Life-cycle stage statuses of a bot process in RPA Hub](../reference/lifecycle-stages-botprocess.md).

Verify that the Robotic Process Automation \(RPA\) developer \(sn\_rpa\_fdn.rpa\_developer\) is in the Managed by Group list of the bot process.

Role required: sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Select the bot process that you want to mark as ready for migration.

5.  In the form header, select **Ready for Migration**.

    You can't see the **Ready for Migration** button when the bot process migration is in progress.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

