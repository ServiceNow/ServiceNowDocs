---
title: Create a backup for the Console
description: You can create a full or partial backup of the Discovery Console for OT data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/create-console-backup-concept.html
release: australia
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 2
breadcrumb: [Settings page, Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Create a backup for the Console

You can create a full or partial backup of the Discovery Console for OT data.

## Creating a Console backup

To create a backup for the Console, you must have **admin** access.

To support disaster recovery, the Discovery Console for OT generates backup files containing restore data, configuration, and logs. Console administrators can initiate backups and restore the Discovery Console for OT, the Discovery Sensor for OT, and the OT Discovery Collector to their previous states when needed. This enhancement provides reliable disaster recovery capabilities across all system components.

To create a backup of the Discovery Console for OT:

1.  Navigate to **Settings &gt; Export** tab.
2.  Use the **Database** section to create a backup of the Console MongoDB.

    \[Omitted image "image.database-backup"\] Alt text: Database section

3.  Select the **Backup Type** and select from the drop-down menu.
    -   A **Full** back up includes:
        -   entire WebConsole database
        -   all images
    -   A **Partial** backup only includes the collections defined in the `PartialIncludeCollections` setting in `appsettings.json`.
4.  If you select a **Partial**, the downloaded ZIP file, by default, includes only the following collections:

    -   AssetAutoScans
    -   AssetDeviceMessages
    -   AssetDeviceStatistics
    -   AssetDevices
    -   AssetProperties
    -   AssetRevisions
    -   AssetScanResults
    -   AssetScanResultsArchive
    -   AssetScans
    -   AssetSites
    -   Assets
    -   CyberDashboards
    -   DetectionRules
    -   DetectionScoreDetails
    -   Detections
    -   DeviceErrors
    -   DevicePolicyStatus
    -   DeviceScoreDetails
    -   DeviceWhitelistApplicationPermissions
    -   Devices
    -   EthernetVendorOrganizations
    -   EthernetVendorRanges
    -   EthernetVendors
    -   ExternalAssets
    -   NetworkZones
    -   Settings
    -   UnsafePorts
    Image files are not included in a Partial backup.

5.  Archive data can be included or excluded based on the system configuration.
6.  You can set system configurations during the Console installation process.
7.  The backup behavior for archived query results is controlled by the following Backup configuration settings in the `appsettings.json` file.
    -   If `ExcludeArchiveFromFull` is set to **true**, archived scan results are excluded from the Full backup.
    -   If `ExcludeArchiveFromFull` is set to **false**, archived scan results are included in the Full backup.
    -   If `ExcludeArchiveFromPartial` is set to **true**, archived scan results are excluded from the Partial backup.
    -   If `ExcludeArchiveFromPartial` is set to **false**, archived scan results are included in the Partial backup, provided that `AssetScanResultsArchive` is listed in `PartialIncludeCollections`.
    -   **Full backup**:
        -   If `ExcludeArchiveFromFull = true` Archive **NOT included**
        -   If `ExcludeArchiveFromFull = false` Archive **INCLUDED**
    -   **Partial backup**

        Even though `AssetScanResultsArchive` is in your list for backup in configuration:

        -   If `ExcludeArchiveFromPartial = true` Archive **NOT included**
        -   If `ExcludeArchiveFromPartial = false` Archive **INCLUDED**
8.  After deciding the **Backup Type**, select the **Backup Database** button.

    \[Omitted image "image.backup-database-button"\] Alt text: Backup Database button

9.  When the backup is finished, the screen displays "Database backup completed successfully."
10. A backup ZIP file is available to download.

    \[Omitted image "image.ZIP-name"\] Alt text: Zip file

11. Select the **Download** button and the ZIP is downloaded to your local system.
12. Once the file is downloaded, select the delete icon \(\[Omitted image "image.trashcan"\] Alt text:\) to remove the archive and free up disk space on the Console.

