---
title: Overwrite customizations during an upgrade
description: Specify which customized objects you want to replace during the next upgrade. By default, the upgrade process skips changes to customized objects.
locale: en-US
release: xanadu
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Update set administration, System update sets, Deploying applications, Building applications]
---

# Overwrite customizations during an upgrade

Specify which customized objects you want to replace during the next upgrade. By default, the upgrade process skips changes to customized objects.

## About this task

The systems tracks the configuration changes you make such as modifying the dictionary record for a table or field. Each configuration change you make has a corresponding record in the Customer Update `[sys_update_xml]` table where the **Replace on upgrade** field is set to false. You may want to overwrite your customizations with the next software version. For example, you may change a script to implement a temporary workaround for a problem that is fixed in the next version. You would want to overwrite your workaround when upgrading to the next version to ensure that you receive any future enhancements to the script.

## Procedure

1.  Open the customized object \(for example, the ArrayUtil script include\).

2.  Right-click the header and select **Show Latest Update**.

3.  Configure the form to add the **Replace on upgrade** field, if necessary.

4.  Select the **Replace on upgrade** check box and click **Update**.

    The customized object will be replaced on the next upgrade.


