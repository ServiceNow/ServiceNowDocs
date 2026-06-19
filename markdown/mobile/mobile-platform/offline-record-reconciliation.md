---
title: Offline record reconciliation
description: Configure offline mode to include associated records in the offline cache when users perform an action in online mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/offline-record-reconciliation.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Action items/action steps, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Offline record reconciliation

Configure offline mode to include associated records in the offline cache when users perform an action in online mode.

An offline step may create a record locally on the device. When connectivity is restored, the online step runs and creates the corresponding record on the instance. Use the `addRecordForSync()` method in the online step to register the server-side record so that the mobile platform can reconcile it with the record created locally on the device. This method verifies that the locally created record and the server record represent the same entity after synchronization.

## How record IDs are handled in offline mode

When a record is created offline, it is stored in the device's local database and assigned a temporary `sys_id`, as the record does not yet exist on the instance. The record is marked with a yellow indicator to distinguish it from records that have been synced to the instance. The temporary `sys_id` allows the mobile app to reference and update the record while the device remains offline.

When the device reconnects and synchronization occurs, the following process takes place:

1.  The record is stored in the device's local database is sent to the instance.
2.  The instance creates the corresponding record.
3.  The instance assigns the permanent `sys_id` for that record.
4.  The permanent `sys_id` replaces the temporary `sys_id` in the device's local database during synchronization.

After synchronization completes, the record on the device and the record on the instance share the same `sys_id`. This process verifies that the record is no longer treated as a temporary or locally created record.

If the user loses connectivity again before the offline cache is refreshed, the record on the device already contains the permanent `sys_id` from the instance and is treated as a regular synchronized record rather than a temporary offline record. This prevents duplicate records from being created and confirms that any further updates continue to reference the correct instance record.

When write-back actions create records during offline execution, the `addRecordForSync()` method verifies that the record created on the instance during the online step is properly associated with the record created locally on the device. During synchronization, the platform updates the local record with the permanent `sys_id` and reconciles the two records so that they represent the same entity.

-   **[Register associated records in the offline cache](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/register-assoc-records-offline-cache.md)**  
Configure a write-back action step by adding an execution script that registers newly created instance records for synchronization. Local and server-side records are then reconciled when connectivity is restored, preventing duplicate records.

**Parent Topic:**[Using action items and action item steps in ofﬂine mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-action-item-steps.md)

