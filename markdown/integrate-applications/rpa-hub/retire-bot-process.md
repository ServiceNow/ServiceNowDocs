---
title: Retire an RPA Hub bot process
description: Retire a bot process to turn it off. It's one of the life-cycle stages of a bot process. After you retire a bot process, you can't use it anymore.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Retire an RPA Hub bot process

Retire a bot process to turn it off. It's one of the life-cycle stages of a bot process. After you retire a bot process, you can't use it anymore.

## Before you begin

Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

If you are retiring an attended bot process that is enabled with Embedded Task Automation, then the following configurations are deleted:

-   All the associated attended configurations.
-   Corresponding buttons \(UI actions\) that are associated to the attended configuration on the related forms.

For more information, see [Embedded Task Automation in RPA Hub](../concept/embedded-task-auto-rpa.md).

If you are retire an unattended bot process, the associated credential groups and process robot credential mappings are removed.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process that you want to retire.

5.  In the form header, select **Retire**.

6.  In the Confirmation dialog box, select **Retire**.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[Retire an MFA authenticator in RPA Hub](retire-mfa-authenticator.md)

