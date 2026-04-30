---
title: Skipped Records visual task board \(VTB\)
description: View the resolution status of any previous upgrade with skipped records using the visual task board \(VTB\) view. An upgrade history record is created for each upgrade that is run.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reviewing upgrade history, Upgrade History tool in Upgrade Console, Upgrade Console tools, Using Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Skipped Records visual task board \(VTB\)

View the resolution status of any previous upgrade with skipped records using the visual task board \(VTB\) view. An upgrade history record is created for each upgrade that is run.

To view the history report navigate to Upgrade History using one of the following ways.

|Option|Navigation|
|------|----------|
|Using left navigation|Navigate to **All** &gt; **Admin Center** &gt; **Upgrade Management** &gt; **Upgrade History**.|
|Using Admin tab option|Navigate to **Admin** &gt; **Upgrade Management** &gt; **Upgrade History**.|

You can then select an upgrade from the list to view the upgrade history details. Click the **Skipped Record VTB** related link to view and manage the skipped records over VTB.

**Note:** The **Skipped Record VTB** related link shows up only when there are skipped records for the version upgrade.

|Field|Description|
|-----|-----------|
|Not Reviewed|Tasks which have not been reviewed|
|Reviewed|Tasks which have been reviewed|
|Merged|Tasks which have both the old and new changes|
|Retained|Tasks which have retained the updates from the latest upgrade|
|Reverted|Tasks which have reverted its changes to the base system|

The skipped records are prioritized based on the importance of the file types. The prioritization is done as follows:

-   Priority 1 \(highest priority\): UI pages, UI macros, and more
-   Priority 2: Business Rules, Security ACLs, and more
-   Priority 3: Reports and more
-   Priority 4: Form Sections, Choice Sets, and more
-   Priority 5 \(lowest priority\): other

![Image showing the VTB view of skipped records resolution status](../../upgrade-center/image/uc-vtb.png)

-   **[Upgrade History Task form](../reference/um-history-task-form.md)**  
You can update information about a skipped record task using the Upgrade History Task form.
-   **[Previous Resolutions related list](../reference/um-previous-resolutions-rl.md)**  
The Previous Resolutions related list shows the history of the selected skipped record. You can see what resolutions have been done with the selected skipped record in the previous upgrades.
-   **[Update default labels in VTB view](../task/um-label-vtb.md)**  
Filter skipped records in the task board of the VTB with the implementation of color-coded labels. You can filter the skipped records by assigning a color to each of the products.

**Parent Topic:**[Reviewing upgrade history](um-review-history.md)

