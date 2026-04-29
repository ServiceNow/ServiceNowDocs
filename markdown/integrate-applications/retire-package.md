---
title: Retire a package in RPA Hub
description: Retire a package to turn it off. It is one of the life-cycle stages of a package. After you retire a package, it cannot be used further.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Package and package version, Use, RPA Hub, Workflow Data Fabric]
---

# Retire a package in RPA Hub

Retire a package to turn it off. It is one of the life-cycle stages of a package. After you retire a package, it cannot be used further.

## Before you begin

Create a package. For more information, see [Create a package to assign to a bot process](create-package.md#).

Verify that the package and associated package versions are not assigned to any other bot process.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

**Warning:** When you retire a package, all the associated package versions are also retired automatically.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Packages**.

4.  Open the package that you want to retire.

5.  In the form header, select **Retire**.

6.  In the Confirmation dialog box, select **Retire**.


**Parent Topic:**[Package and package version in RPA Hub](../concept/package-version-rpa-hub.md)

**Related topics**  


[Retire a package version in RPA Hub](retire-package-version.md)

