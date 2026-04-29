---
title: Overwrite customizations during an upgrade
description: Specify which customized objects you want to replace during the next upgrade. By default, the upgrade process skips changes to customized objects.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, System update sets, Deploying applications, Building applications]
---

# Overwrite customizations during an upgrade

Specify which customized objects you want to replace during the next upgrade. By default, the upgrade process skips changes to customized objects.

## Before you begin

Role required: admin

Configuration changes you make such as modifying the dictionary record for a table or field are tracked. Each configuration change has a corresponding record in the customer update table, where **Replace on upgrade** is set to `false`.

## About this task

When updating to the latest software version, you can replace your custom changes. For instance, if you modified a script as a temporary fix, you’ll want to remove that workaround during the upgrade so you can benefit from new improvements and confirm compatibility with future updates.

## Procedure

1.  Navigate to **All** &gt; **System update sets** &gt; **Local update sets**

2.  Select an update set.

3.  Select a customized object in the customer updates list.

4.  Select and hold \(or right-click\) the header and select **Show Latest Update**.

5.  Configure the form to add the **Replace on upgrade** field, if necessary.

    1.  Hold \(or select and hold \(or right-click\)\) the header and select **Configure**.

    2.  Select **Replace on upgrade** from the available list and add it to the form.

    3.  Select **Save**.

6.  Select the **Replace on upgrade** check box and select **Update**.

    The customized object will be replaced on the next upgrade.


**Parent Topic:**[Configuring System Update Sets](../concept/configure-system-update-sets.md)

