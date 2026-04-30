---
title: Solving errors on dashboards moved with update sets
description: When you move a dashboard with an update set, if errors are shown on the Update Set Preview Problems tab of the Retrieved Update Set page, follow the instructions for each error to solve these problems.When you move a dashboard with an update set, the following error may occur: 'Could not find a record in sys\_grid\_canvas for column canvas\_page referenced in this update'. To solve this error, move the canvas page from the source instance to the target instance.When you attempt to move a dashboard in a scoped app, the move fails when you try to retrieve the update set.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Move a Core UI dashboard with an update set, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Solving errors on dashboards moved with update sets

When you move a dashboard with an update set, if errors are shown on the **Update Set Preview Problems** tab of the Retrieved Update Set page, follow the instructions for each error to solve these problems.

## Could not find a record in sys\_grid\_canvas for column canvas\_page referenced in this update

When you move a dashboard with an update set, the following error may occur: 'Could not find a record in sys\_grid\_canvas for column canvas\_page referenced in this update'. To solve this error, move the canvas page from the source instance to the target instance.

### Before you begin

Role required: admin.

### Procedure

1.  In the **Update Set Preview Problems** related list, click the information icon \(![](../../../common/image/Form_ReferenceLookupIcon.png)\) next to the error.![Update Set Preview Problems tab with two errors.](../image/update-set-preview-problems.png)

2.  In the pa\_tabs record payload, copy the sys\_id associated with the canvas\_page field.

    ![Filter grid canvas on Sys ID](../image/filter-on-sys-id.png)

3.  In the source instance, navigate to sys\_grid\_canvas.list.

4.  Filter the list on the sys\_id copied in step 2.

5.  Right-click on the returned record and select **Unload Canvas Page** to add this record to the current update set.

6.  Transfer the update set to the target instance using standard update set functionality.

    For more information, see [Retrieve an update set](https://www.servicenow.com/docs/access?context=t_RetrieveAnUpdateSet&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

7.  Repeat this task for all update set preview problems that have this error.


### Result

The missing dashboard tab content is moved to the target instance.

## Update set id 'global' is different than update set scope id

When you attempt to move a dashboard in a scoped app, the move fails when you try to retrieve the update set.

### Before you begin

Role required: admin.

### About this task

Dashboards comprise multiple tables. The ServiceNow AI Platform® does not track all of these tables. The untracked tables are always in the global scope. When you are moving a dashboard in the global scope, these tables do not present a problem. However, these tables block the move of dashboards in any other scope, because the scope of all components in an update set must be the same.

### Procedure

1.  Put the global Customer Updates record, sys\_update\_xml, in a global update set.

2.  Commit this update as its own update set, or make it a parent of the original update set and commit both at the same time.

    One update set has all Customer Updates records from the non-global scope, and the other has the sys\_portal Customer Updates records from the Global scope.

3.  Export both, and retrieve them in the target instance at same time.

4.  Preview and commit them in sequence: First commit the update set with non-global customer updates records and then the update set with global customer updates records.


