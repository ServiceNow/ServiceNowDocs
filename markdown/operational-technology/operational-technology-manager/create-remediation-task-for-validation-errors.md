---
title: Create a remediation task for invalid staging records
description: After running validations for the Operational Technology \(OT\) device data imported with the Service Graph Connector for Microsoft Excel, optionally create a remediation task to resolve invalid staging records.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-06-23"
reading_time_minutes: 1
breadcrumb: [Using the Service Graph Connector for Microsoft Excel through import tasks, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Create a remediation task for invalid staging records

After running validations for the Operational Technology \(OT\) device data imported with the Service Graph Connector for Microsoft Excel, optionally create a remediation task to resolve invalid staging records.

## Before you begin

Role required: ot\_excel\_import\_user

## About this task

You can optionally create remediation tasks to resolve invalid staging records. For more information about the validation errors that can occur for your staging records, see [Managing Validations](../concept/managing-validations.md).

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Select the **List** \(![List icon](../../../common/image/icon-list.png)\) icon.

3.  Under the OT Excel SGC - Import Task module, select one of the available lists.

4.  Select the Import Task record that you want to create remediation tasks for.

5.  Ensure that you are assigned to the import task so that you can see the **Create Remediation Tasks** UI action.

    If you are not in the **Assigned to** field of the import task, click the **Assign to me** UI action before proceeding with the next step.

6.  Click the **Create Remediation Tasks** UI action.


## Result

Remediation tasks are created for the invalid staging records. To access the remediation tasks in the Import Task record, select the **Remediation Tasks** list.

**Note:** One remediation task is created for all invalid staging records that belong to the same site.

When you view the remediation task record, you can also view the staging records associated with it by selecting the **Staging Records** tab.

**Parent Topic:**[Using the Service Graph Connector for Microsoft Excel through import tasks](../concept/use-excel-sgc-through-import-tasks.md)

