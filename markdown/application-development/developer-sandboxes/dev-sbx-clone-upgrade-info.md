---
title: Cloning and upgrading considerations for Developer Sandboxes
description: You should understand how plugins and sandboxes work before you clone or upgrade an instance with Developer Sandboxes. Always back up your work in a sandbox before any clone or upgrade, either by exporting the update sets or committing to source control.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/developer-sandboxes/dev-sbx-clone-upgrade-info.html
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 2
breadcrumb: [Installing, Developer Sandboxes, Developing your application, Building applications]
---

# Cloning and upgrading considerations for Developer Sandboxes

You should understand how plugins and sandboxes work before you clone or upgrade an instance with Developer Sandboxes. Always back up your work in a sandbox before any clone or upgrade, either by exporting the update sets or committing to source control.

**Warning:** Because sandboxes are retired automatically after an upgrade or clone, ensure any work that you want to keep is preserved before upgrading or cloning.

-   For upgrades, you can restore work from the remote update sets that Developer Sandboxes automatically created from prior sandboxes.
-   For clones, you must manually save and restore all work in sandboxes.
-   Any custom table configuration changes or fixes must be reapplied after an upgrade. Contact Now Support to open a case.

## Upgrading instances with Developer Sandboxes

Family, patch, and security upgrades automatically retire all existing sandboxes. Sandboxes are recreated, but any changes from pre-existing sandboxes must be manually restored from the automatic backup created. After an upgrade, you can immediately begin creating new sandboxes without contacting Support.

Developer Sandboxes automatically backs up any update sets from the sandboxes and exports them to the base instance. The following rules apply:

-   The update set must contain at least one change since the sandbox was created for it to be backed up.
-   Incomplete update sets are backed up as long as there's at least one change.

**Note:** When using sandboxes, make sure to save or backup work consistently. Automatic backups are available only for instances on Australia Patch 3 and higher.

Backups are found in the retrieved update sets table, identified by the name of the sandbox they were backed up from. For example, "DSB \[sandboxname\] \(backup date\): \[Original update set name\]". For more information, see [Preview a remote update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_PreviewARemoteUpdateSet.md) and [Commit an update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_CommitAnUpdateSet.md).

Review the update sets, then preview and commit them in each sandbox as needed.

**Note:** If you're using source control, you should restore your work to the sandbox from there. For more information, see [Source control and Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/developer-sandboxes/dev-sandboxes-source-control.md).

## Cloning instances with Developer Sandboxes

**Note:** Sandboxes are not automatically recreated after a clone. You should save your work from a sandbox before the clone so you can recreate it.

Install the Dev Sandboxes CC \(com.glide.dsb.cc\) plugin on the production instance to enable clone preservers that protect Developer Sandboxes feature enablement on your target instance. For more information on clone preservers, see [Create a clone preserver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/create-new-clone-preserver.md). For details on the plugin, see [Plugin information for all Australia features and products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/rn-summary-plugin-info.md).

