---
title: Configure related list background loading
description: Configure large selections of records added to a related list to load in the background for your entire workspace experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Lists, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure related list background loading

Configure large selections of records added to a related list to load in the background for your entire workspace experience.

## Before you begin

Role required: admin

## About this task

When you select a large number of records to add to a related list, you can focus on other tasks while the records are added in the background.

If background loading isn’t required for all modals, configure individual modals to load related list records in the background using declarative actions. For instructions, see [Configure background loading for a modal](set-up-asychronous-record-addition-declarative-actions.md).

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Add the **glide.ui.mra.async** system property.

    For more information on adding system property, see Add a system property.

    1.  Set the Value to **true**.

    2.  Select **Submit**.

3.  Add the **glide.ui.mra.threshold** system property.

    For more information on adding system property, see Add a system property.

    1.  Specify how many records can be added before asynchronous record addition occurs.

        The default is 100 records.

    2.  Select **Submit**.


## Result

When you select any number of records beyond the threshold, a notification informs you that the records will load in the background.

![MRA notification 1](../image/y-mra-notification-1.png)

When you add the selected records, the modal closes, and a notification confirms that the records are loading in the background.

![MRA notification 2](../image/y-mra-notification-2.png)

After the records are added, a notification informs you that the records were added successfully.

![MRA notification 3](../image/y-mra-notification-3.png)

