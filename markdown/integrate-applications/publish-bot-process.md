---
title: Publish a bot process in RPA Hub
description: Publish a bot process so that you can get it ready to execute a process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring a bot process record, Use, RPA Hub, Workflow Data Fabric]
---

# Publish a bot process in RPA Hub

Publish a bot process so that you can get it ready to execute a process.

## Before you begin

Ensure that the associated package version complies with the code quality check system property **sn\_rpa\_fdn.restrict\_package\_by\_severity**, to verify if the code quality check is enabled in the RPA Hub instance. For more information about the system property, see [Configure RPA Hub properties](../reference/rpahub-sys-properties.md). For more information about the compliance rules, see [Code quality check compliance for RPA Hub](../reference/cqc-publish-rpa-hub.md).

Ensure that you complete the following tasks to publish an unattended bot process in the order that they’re presented.

1.  Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).
2.  Associate a credential group. For more information, see [Associate a credential group to a bot process in RPA Hub](map-credential-groups-to-bot-process.md).
3.  Assign a robot to a bot process. For more information, see [Assign a robot to a bot process in RPA Hub](assign-robots.md).
4.  Assign a process robot credential within a bot process. For more information, see [Assign a process robot credential within a bot process in RPA Hub](assign-process-robot-cred-botprocess.md).
5.  Verify that all the assigned robots are mapped to a credential group.

Ensure that you complete the following tasks to publish an attended bot process in the order that they’re presented.

1.  Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).
2.  Assign an attended user or group to an attended bot process. For more information, see [Assign an attended user or group to an attended bot process](assign-rda-users-botprocess.md).

If you are publishing an unattended bot process that is assigned to a robot pool, then ensure that the following conditions are met:

-   Associate a queue to the bot process. For more information, see [c to the bot process from the related list](associate-queue-botprocess.md).
-   The queue is not associated to another bot process.
-   The bot process is not associated with multiple queues.
-   Assign a process robot credential to each robots of the robot pool within a bot process. For more information, see [Assign a process robot credential within a bot process in RPA Hub](assign-process-robot-cred-botprocess.md).

If you are publishing a bot process that is enabled with external credential, then ensure that the associated external credential vault is active. This scenario is valid if one or more Robot Credentials, Application Credentials, or TOTP Authenticators are associated with inactive External Credential Vault record. For more information about the external credential settings in Robot Credentials, Application Credentials, and TOTP Authenticators, see [Create a robot credential in RPA Hub](create-credential-set-botprocess.md), [Create an application credential in RPA Hub](create-application-credential.md), and [Create a TOTP authenticator in RPA Hub](map-totp-credential-set-rpa.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_support\_user, or sn\_rpa\_fdn.rpa\_admin

## About this task

Publishing a bot process is one of the life-cycle stages of a bot process. For more information, see [Life-cycle stage statuses \(LLCS\) of a bot process in RPA Hub](../reference/lifecycle-stages-botprocess.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open a bot process that you want to publish.

    **Tip:** To modify the details of a bot process, change the life cycle stage of the bot process to **In-maintenance**. For more information, see [Edit a bot process in RPA Hub](edit-botprocess.md).

5.  In the form header, select **Publish**.

    **Warning:** After you publish a bot process, you can't change or delete the entries in the bot process form, associated business applications, robots, process credential mappings, process robot credential sets, and schedules.


## Result

After you publish a bot process, the added schedule \(if any\) takes effect.

If there is no schedule, the published bot process is ready to be triggered by the API.

**Parent Topic:**[Configuring a bot process record in RPA Hub](../concept/create-botprocess.md)

