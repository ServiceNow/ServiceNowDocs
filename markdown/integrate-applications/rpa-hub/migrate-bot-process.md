---
title: Migrate the bot process configuration to another environment in RPA Hub
description: Migrate the bot process configuration and associated assets to another environment in RPA Hub. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/migrate-bot-process.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Migrate the bot process configuration to another environment in RPA Hub

Migrate the bot process configuration and associated assets to another environment in RPA Hub. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.

## Before you begin

Familiarize yourself with the bot process migration concept. For more information, see [Migrating the bot process configuration in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/bot-process-migration.md).

Verify that you’ve completed the tasks that are related to setting up the target environment. For more information, see [Set up the ServiceNow Remote Instance spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-rem-instance.md).

The bot process must be marked ready for migration. For more information, see [Mark the bot process as ready for migration in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/mark-bot-process-ready-for-migration.md).

Verify that the life-cycle stage status of the bot process in the source environment is set to **Published**. For more information, see [Life-cycle stage statuses \(LLCS\) of a bot process in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/lifecycle-stages-botprocess.md).

When you re-migrate, verify that the life-cycle stage status of the bot process in the target environment isn’t set to **Published** or **Retired**. If **Published**, the values are overridden in the target environment.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Select the bot process that you want to migrate.

5.  In the form header, select **Migrate**.

    You can't see the **Migrate** button when the bot process migration is in progress.

6.  In the Confirmation dialog box, select **Migrate**.


## Result

After the migration is completed successfully or if an error occurs, an email notification is sent to the user who performs the migration. To receive the email notification, the email address of the user must be added to the user profile.

## What to do next

-   [Associate a bot process to a bot process configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/select-botprocess.md)
-   [Configuring credentials in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configuring-credentials-rpahub.md)
-   [Adding details to your bot process in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/post-req-bot-process-rpa.md)
-   [Publish a bot process in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/publish-bot-process.md)

**Parent Topic:**[Managing RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/managing-rpa-hub.md)

