---
title: Create Snapshots to migrate Indoor Mapping data
description: Create snapshots for taking point-in-time backups of your Indoor Mapping map data and objects and migrate the snapshots to Workplace Service Delivery instances.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-02-12"
reading_time_minutes: 3
breadcrumb: [Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Create Snapshots to migrate Indoor Mapping data

Create snapshots for taking point-in-time backups of your Indoor Mapping map data and objects and migrate the snapshots to Workplace Service Delivery instances.

## Before you begin

**Note:** Users without map admin or map editor roles cannot create, read, download, or apply a snapshot. Users with wsd\_core\_admin roles can create or apply snapshots when the **Snapshot Workplace locations** option is enabled.

Snapshot capability in Indoor Mapping provides the following:

-   Ability to export Indoor mapping data and instance values
-   Ability to import Indoor mapping data and instance values
-   Ability to import and export Workplace Indoor Mapping related objects

Role required: map admin, map editor, wsd\_core\_admin

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Snapshots**.

    The Snapshots page appears and list of existing snapshots, if any, are displayed.

2.  Select **New** to create a new snapshot record.

    Ensure to export/import the update set for Indoor Mapping and other configured applications as well.

3.  Complete the following information:

    -   **Name**: Provide a name for the snapshot.
    -   **Campuses**: Select single or multiple campuses as required. By default all campuses are selected.
    -   **Include workplace locations**: Select it to capture all workplace elements linked to Indoor Mapping.
4.  Click **Submit**.

    The snapshot is created. The status is shown as **In Progress** in the Snapshot page. This process may take some time to complete. Once completed, the state moves to **Created**.

5.  From the Snapshot page, click open the newly created snapshot data.

6.  Select **Download Snapshot** to download or export the snapshot locally.

    Files will be downloaded as XML.

7.  Import the snapshot using update sets on a different instance where you want to apply the snapshot.

8.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieve update sets** to import the XML file.

9.  From the Related Links, select **Import Update Set from XML**.

10. On the Import XML page, click **Choose file** and select the downloaded XML from where you have downloaded the XML file.

11. Select **Upload**.

12. After importing, go to **Indoor Mapping** &gt; **Snapshots** and select the imported snapshot.

13. Click **Apply snapshot** to apply it to an instance where you want to have the snapshot data applied.

    Applying a snapshot overwrites all the records for a selected map object for example, campus,building, floor, or spaces. So having a snapshot in place helps in case a backup data is required.

14. Select **Yes** to apply the snapshot to a selected map object.

15. To delete a snapshot, select the campus from the Campus page and click **Actions** on Selected items drop-down box and select **Delete**.

16. Few workplace tables are impacted during the snapshot process.

    For more information about impacted tables, see [Snapshot Impacted tables](../reference/snapshot-ind-mapping-tables.md).


## What to do next

**Note:** After moving the snapshots, the Space Details table \[sn\_wsd\_spcmgmt\_space\_detail\] in Workplace Space Management doesn't get populated with the snapshots. To get the updated Space details table record, manually run the fix script **Load space details table- current state**. Navigate to **All** &gt; **Fix Scripts** and search for Workplace Space Management **Load space details table- current state** fix script. Select **Run Fix Script** tab to run the script and get latest Space Details table \[sn\_wsd\_spcmgmt\_space\_detail\] record.

**Parent Topic:**[Manage map objects and data](../concept/using-indoor-mapping.md)

**Previous topic:**[Print a map](print-map.md)

**Next topic:**[Keyboard shortcuts](keyboard-shortcuts.md)

