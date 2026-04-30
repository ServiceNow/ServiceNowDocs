---
title: Handling a large amount of in-progress update sets
description: You can batch a large group of update sets in the Clone Admin Console.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Manage, Instance Clone, Configure core features, Administer]
---

# Handling a large amount of in-progress update sets

You can batch a large group of update sets in the Clone Admin Console.

## Before you begin

Role required: clone\_admin

## Procedure

1.  On your target instance, which has the work in progress \(WIP\) update sets, filter to obtain a list view with all your WIP update sets.

2.  In a separate window/tab, create an update set.

3.  How to mass-update: Hold down the shift key + selecting the whole column with your mouse device.

4.  Double select any of the fields in the selected column and enter the desired value to update all of them to that value.

5.  Set the parent field on your list of WIP update sets to the new batch update set.

6.  Update the parent update set to "Completed" and give it an identifiable name, such as `"CLNREQ_DATE"`.

7.  Export the parent update set.

8.  On your source instance, retrieve the update set.

    **Important:** \(Important: Don’t commit!\)

    The parent update set is added to the retrieved update sets on your source instance.

9.  Wait 24 hours until your update set is captured by the daily backup.

    You can also select an on-demand backup on the Clone Admin Console.

10. Perform the clone as usual from your source instance to target instance.

    Because your parent update set has been retrieved in the backup. Your target instance will have your parent update set along with your dev work that is in flight after the clone.

11. On the target instance, set the parent update set back to work in progress, and un-parent it.

    Removing the parent update set enables you to continue only importing and exporting your in-progress work.

12. On the source instance, the retrieved parent update set can be cleaned up or deleted.


**Parent Topic:**[Managing Instance Clone](using-instance-clone.md)

