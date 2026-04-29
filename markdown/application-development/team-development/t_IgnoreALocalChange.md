---
title: Ignore a local change
description: Ignoring a local change prevents updates to a record from generating new versions in the Local Changes list.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Team Development, Planning your application, Building applications]
---

# Ignore a local change

Ignoring a local change prevents updates to a record from generating new versions in the Local Changes list.

## Before you begin

Role required: none.

## About this task

An ignored local change always points to the current version for the record. You cannot push ignored records to another instance.

|Action|Result|
|------|------|
|Ignore a record that has a version queued for push|The queued change is deleted|
|Ignore a record that has a version queued for code review|The queued change is deleted|
|Pull changes for an ignored record|Collision|
|Resolve a collision by taking the parent version|There is no longer a local change to ignore|
|Resolve a collision by keeping the local version|The ignored change remains on the local instance|

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  Filter the Local Changes list to show only the changes that you want to ignore.

    For example, filter the list to show all changes in the Default Update Set.

    ![Ignore changes default](../image/IgnoreChangesDefault.png)

3.  Click **Ignore All**.

4.  Review the Ignored list to ensure that the correct changes are ignored.

    This step is a recommended best practice.

<table id="choicetable_nvm_53c_bq"><tbody><tr><td id="d225985e201">

**To stop ignoring changes**

</td><td>

Select the check boxes beside the rows and select **Do Not Ignore** from the Actions choice list.

</td></tr><tr><td id="d225985e216">

**To stop ignoring changes and add them to the queue instead**

</td><td>

Select the check boxes beside the rows and select **Queue for Push** from the Actions choice list.

</td></tr></tbody>
</table>    ![The Ignored tab](../image/Ignored.png)


