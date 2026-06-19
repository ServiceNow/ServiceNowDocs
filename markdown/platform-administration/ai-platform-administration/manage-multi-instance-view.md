---
title: Manage Multi-Instance View
description: Manage a consolidated view of clones across all your instances and clone statusFilter and sort the instance list to find specific instances and customize the display format.Manage Instance Clone operations across multiple linked instances.Remove a connected instance from Multi-Instance View
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/manage-multi-instance-view.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2026-04-08"
reading_time_minutes: 2
breadcrumb: [Manage, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Manage Multi-Instance View

Manage a consolidated view of clones across all your instances and clone status

## Before you begin

Role required: clone\_admin. [Multi-Instance view is enabled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/setup-multi-instance-view.md).

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.


## Result

The Clone Activity section displays all instances in your Multi-Instance View configuration.

## Filter and sort instances

Filter and sort the instance list to find specific instances and customize the display format.

### Before you begin

Role required: clone\_admin. [Multi-Instance view is enabled.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/setup-multi-instance-view.md)

### Procedure

1.  Filter instances by source using the **Origin Instance** list.

    Use the **Origin Instance** drop-down to view instances by their clone source.

2.  Filter instances by status using the filter icon.

    Use the **filter** icon to view instances by their status.

3.  Sort the instance list by selecting any column header.

    Default sort is Most Recent to show most recently cloned instances first.

4.  Change the instance display format using the view icons.

    -   Select the **grid** icon to view the instance list as a grid.
    -   Select the **list** icon to view the instance list as a list. The list view allows customizing the columns displayed. Select the **gear** icon to configure the columns.

### Result

The Instance List shows each instance with the following information:

|Column|Description|
|------|-----------|
|CHG Number|Change request associated with the clone request|
|Source Instance|Which instance serves as source for the clone operation|
|Target Instance|Which instance is cloned to|
|State|The current status of the clone activity|
|Scheduled Date/Time|The scheduled timestamp of the clone activity|
|Clone start time|The starting timestamp of the clone activity|
|Estimated End Time|The estimated end timestamp for completing the clone activity|
|Duration \(for completed actions\)|The duration taken for the clone activity|

## Add an instance to Multi-Instance View

Manage Instance Clone operations across multiple linked instances.

### Before you begin

Role required: clone\_admin

### Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home** &gt; **Configuration**.

2.  Select **Multi-Instance View** link.

3.  Select **Add Instance** in the Instances list.

4.  Select the instance from the drop-down of available instances linked to your account.

5.  Select **Add**.

    The instance is now included in your centralized view. It will appear on your Clone Homepage with its status.

6.  Select **Set Up Trust** to set up a trusted relationship between the instances.

7.  Select **Done** to complete adding the instance.


### Result

The instance is now included in your centralized view. It will appear on your Clone Homepage with its status.

## Remove a connected instance from Multi-Instance View

Remove a connected instance from Multi-Instance View

### Before you begin

Role required: clone\_admin

### Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home** &gt; **Configuration**.

2.  Select **Multi-Instance View** link.

3.  In the **Connected Instances** section, click **Remove Trust** from the instance you want to remove from Multi-Instance View.


### Result

The instance is removed from your centralized view. This does not delete the instance itself; you can add it back later if needed.

