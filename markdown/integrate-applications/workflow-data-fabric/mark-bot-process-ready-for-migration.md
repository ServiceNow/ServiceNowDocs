---
title: Mark the bot process as ready for migration in RPA Hub
description: Mark the bot process as ready for migration in RPA Hub so that the bot process configuration and associated assets can be migrated to another environment. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/mark-bot-process-ready-for-migration.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migrating the bot process configuration, Migrate data, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Mark the bot process as ready for migration in RPA Hub

Mark the bot process as ready for migration in RPA Hub so that the bot process configuration and associated assets can be migrated to another environment. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.

## Before you begin

Familiarize yourself with the bot process migration concept. For more information, see [Migrating the bot process configuration in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/bot-process-migration.md).

Verify that you’ve completed the tasks that are related to setting up the target environment. For more information, see [Set up the ServiceNow Remote Instance spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-rem-instance.md).

Verify that the life-cycle stage status of the bot process in the source environment is set to **Published**. For more information, see [Life-cycle stage statuses \(LLCS\) of a bot process in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/lifecycle-stages-botprocess.md).

Verify that the Robotic Process Automation \(RPA\) developer \(sn\_rpa\_fdn.rpa\_developer\) is in the Managed by Group list of the bot process.

Role required: sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Select the bot process that you want to mark as ready for migration.

5.  In the form header, select **Ready for Migration**.

    You can't see the **Ready for Migration** button when the bot process migration is in progress.


**Parent Topic:**[Migrating the bot process configuration in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/bot-process-migration.md)

