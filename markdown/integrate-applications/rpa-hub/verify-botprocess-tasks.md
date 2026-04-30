---
title: Verify the associated schedules, parameters, packages, and queues in RPA Hub
description: Verify that the bot process has the associated schedule, process parameters, shared parameters, package, package version, and work queues in RPA Hub. You do this task when you’re migrating your data from a lower \(non-production\) environment to a higher \(production\) environment.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Verify the associated schedules, parameters, packages, and queues in RPA Hub

Verify that the bot process has the associated schedule, process parameters, shared parameters, package, package version, and work queues in RPA Hub. You do this task when you’re migrating your data from a lower \(non-production\) environment to a higher \(production\) environment.

## Before you begin

Role required: sn\_rpa\_fdn.rpa\_release\_manager or admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process that you want to verify and select one or more of the following options.

    |Option|Action|
    |------|------|
    |**To verify schedules**|On the **Schedules** tab, verify the schedules.|
    |**To verify process parameters**|On the **Process Parameters** tab, verify the process parameters.|
    |**To verify the package and package version**|On the **Details** tab, verify the package and package versions.|

5.  To verify the queues, do the following actions:

    1.  On the **Lists** tab, under **Build**, select **Queues**.

    2.  Open the queue that you want to verify.

    3.  On the **Bot Process Configuration** tab, verify the association.

6.  To verify the shared parameters, do the following actions:

    1.  On the **Lists** tab, under **Build**, select **Shared Parameters**.

    2.  Open the shared parameter that you want to verify.

    3.  On the **Bot Process Configuration** tab, verify the association.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[Create a package to assign to a bot process](create-package.md)

[Create a schedule within a bot process in RPA Hub](create-schedule-botprocess.md)

[Create a process parameter within a bot process in RPA Hub](create-process-parameter-botprocess.md)

[Create a shared parameter in RPA Hub](create-shared-parameter.md)

[Create a queue in RPA Hub](create-queue.md)

[Assign a bot process to a queue from Queues menu in RPA Hub](assign-botprocess-queue.md)

[Assign a bot process to a shared parameter in RPA Hub](assign-botprocess-shared-parameter.md)

[Schedule form in RPA Hub](../reference/schedule-rpa-form.md)

[Process parameter form in RPA Hub](../reference/process-parameter-form.md)

