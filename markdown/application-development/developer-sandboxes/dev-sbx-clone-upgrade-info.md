---
title: Cloning and upgrading considerations for Developer Sandboxes
description: You should understand how plugins and sandboxes work before you clone or upgrade an instance with Developer Sandboxes.
locale: en-US
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installing, Developer Sandboxes, Developing your application, Building applications]
---

# Cloning and upgrading considerations for Developer Sandboxes

You should understand how plugins and sandboxes work before you clone or upgrade an instance with Developer Sandboxes.

## Upgrading instances with Developer Sandboxes

Family, patch, and security upgrades automatically recreate all existing sandboxes from an instance. After an upgrade, you can immediately begin creating sandboxes without contacting Support.

Developer Sandboxes automatically backs up any update sets from the sandboxes and exports them to the base instance. The following rules apply:

-   The update set must contain at least one change since the sandbox was created for it to be backed up.
-   Incomplete update sets are backed up as long as there's at least one change.

## Cloning instances with Developer Sandboxes

After a clone, sandboxes on an instance are automatically re-created with the same name, but without the previous work.

**Note:** You must always save your work from a sandbox before the clone.

Install the Dev Sandboxes CC \(com.glide.dsb.cc\) plugin on the production instance to enable clone preservers that protect Developer Sandboxes feature enablement on your target instance. For more information on clone preservers, see [Create a clone preserver](https://www.servicenow.com/docs/access?context=create-new-clone-preserver&version=australia&pubname=australia-platform-administration&ft:locale=en-US). For details on the plugin, see [Plugin information for all Australia features and products](https://www.servicenow.com/docs/access?context=rn-summary-plugin-info&version=australia&pubname=australia-release-notes&ft:locale=en-US).

After you clone an instance, the repository information \(for ServiceNow Studio\) and the workspace \(for ServiceNow IDE\) are automatically saved and restored after the clone. If you're using the ServiceNow IDE, you must manually clone the Git repository again.

