---
title: Migrating non-reference fields to reference fields
description: Manually preserve sys\_ids in reference fields instead of storing the display name as a string.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Archiving records, Manage data growth, Data Management, Tables and data, Configure core features, Administer]
---

# Migrating non-reference fields to reference fields

Manually preserve sys\_ids in reference fields instead of storing the display name as a string.

## Determining tables to migrate

To begin the data migration process, run the following background script. This script creates migration records for both direct table extensions and related archived records in the Archive Rule Reference Migration \[sys\_archive\_ref\_migration\] table, ensuring that only valid tables are processed.

```javascript
var tables = GlideDBObjectManager.get().getAllExtensions(current.table);
    for (i = 0; i < tables.size(); i++) {
        var gr = new GlideRecord('sys_archive_ref_migration');
        gr.addQuery('table', 'ar_' + tables.get(i));
        gr.query();
        if (!gr.next()) {
            if (GlideTableDescriptor.isValid('ar_' + tables.get(i))) {
                var gr2 = new GlideRecord("sys_archive_ref_migration");
                gr2.initialize();
                gr2.setValue('rule', current.sys_id);
                gr2.setValue('table', 'ar_' + tables.get(i));
                gr2.setValue('reference_migration_progress', 'waiting');
                gr2.insert();
            }
        }
    }
    //Also get insert related records tables as well
    var map = new GlideRecord('sys_archive');
    map.addQuery('table', current.table);
    map.query();
    if (map.next()) {
        var id = map.getValue('sys_id');
        if (!(id === undefined)) {
            var related = new GlideRecord('sys_archive_related');
            related.addQuery('archive_map', id);
            related.addQuery('action', 'archive');
            related.query();
            while (related.next()) {
                if (!GlideTableDescriptor.isValid('ar_' + related.getValue('table'))) {
                    gs.log('Related Record table: ' + related.getValue('table') + ' not created yet');
                    continue;
                }
 
                var gr3 = new GlideRecord("sys_archive_ref_migration");
                gr3.initialize();
                gr3.setValue('rule', current.sys_id);
                gr3.setValue('table', 'ar_' + related.getValue('table'));
                gr3.setValue('reference_migration_progress', 'waiting');
                gr3.insert();
            }
        }
    }
```

## Copying archive references

For each table that goes through the migration process, the Archive Reference Copy \(RefCopyJob\) job identifies the sys\_id of the reference fields and updates the display value to be the correct sys\_id. The job configures 10k records at a time unless there are more than 10k records with the same timestamp. The migration progress relies on the archived timestamp.

## Changing field types from string to reference

After the tables associated with an archive rule completely migrate, the ArchiveRefJob job executes. This job changes the sys\_dictionary types of the archive table from string to reference.

## Fixing node failures for RefCopyJob and ArchiveRefJob

If node failure occurs while these jobs are running, it leaves the status of the data migration in an improper state. If the **RefCopyJob** fails, it can leave a table in a migrating status. You can verify this condition by checking if rows in the sys\_archive\_ref\_migration are stuck in **migrating** status for an extraordinary amount of time. Update the specific row status from **migrating** to **waiting** and the **RefCopyJob** continues the data migration on the table when the job runs again.

The node can also fail when the **ArchiveRefJob** terminates prematurely. Check if tables have fields that are reference fields and some that are still string type fields. The job might have stopped in the middle of changing the field types. You can resolve this condition by setting up a trigger job to execute in a background script, which starts the process over again:

```javascript
GlideRecord trigger = new GlideRecord('sys_trigger');
trigger.initialize();
trigger.setValue('state', 0);
trigger.setValue('trigger_type', 0);
trigger.setValue('next_action', new GlideDateTime());
trigger.setValue('job_context', 'fcRuleId=' + ruleId);
trigger.setValue('name', 'Job Reference Migration' + ' Node - ' + new GlideClusterSynchronizer().getSystemID());
trigger.setValue('trigger_class', 'com.glide.db.auxiliary.job.ArchiveRefJob');
trigger.insert();
```

**Parent Topic:**[Archiving records](../../managing-data/concept/archiving-older-records.md)

