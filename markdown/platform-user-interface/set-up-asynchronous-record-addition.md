---
title: Enable asynchronous record addition for the multi-record associator
description: Enable large selections of records added to a related list by the multi-record associator to load in the background.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Enable asynchronous record addition for the multi-record associator

Enable large selections of records added to a related list by the multi-record associator to load in the background.

## Before you begin

Role required: admin

## About this task

When you add a large number of records to a related list, you can focus on other tasks while the record addition loads in the background.

If asynchronous record addition isn't required for all multi-record associator modals, use declarative actions to enable asynchronous record addition for select modals. For instructions, see [Set up asynchronous record addition for select modals](set-up-asychronous-record-addition-declarative-actions.md).

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Add the **glide.ui.mra.async** system property.

    For more information on adding system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

    1.  Select **New**.

    2.  Add a system property named **glide.ui.mra.async**.

    3.  Set the Value to **true**.

    4.  Select **Submit**.

3.  Add the **glide.ui.mra.threshold** system property.

    1.  Select **New**.

    2.  Add a system property named **glide.ui.mra.threshold**.

    3.  Specify how many records can be added before asynchronous record addition occurs.

        The default is 100 records.

    4.  Select **Submit**.


## Result

When you select any number of records beyond the threshold, a notification informs you that the records will load in the background.

![MRA notification 1](../image/y-mra-notification-1.png)

When you add the selected records, the modal closes, and a notification confirms that the records are loading in the background.

![MRA notification 2](../image/y-mra-notification-2.png)

After the records are added, a notification informs you that the records were added successfully.

![MRA notification 3](../image/y-mra-notification-3.png)

