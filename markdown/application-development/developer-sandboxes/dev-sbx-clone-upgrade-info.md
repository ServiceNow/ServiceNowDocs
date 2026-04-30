---
title: Cloning and upgrading considerations for Developer Sandboxes
description: You should understand how plugins and sandboxes work before you clone or upgrade an instance with Developer Sandboxes.
locale: en-US
release: zurich
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2025-10-21"
reading_time_minutes: 1
breadcrumb: [Installing, Developer Sandboxes, Developing your application, Building applications]
---

# Cloning and upgrading considerations for Developer Sandboxes

You should understand how plugins and sandboxes work before you clone or upgrade an instance with Developer Sandboxes.

Because sandboxes are retired automatically after an upgrade or clone, you should ensure any work that you want to keep is preserved before upgrading.

## Upgrading instances with Developer Sandboxes

Family, patch, and security upgrades retire all existing sandboxes from an instance. After an upgrade, you can immediately begin creating sandboxes without contacting Support.

As of Zurich Patch 5, Developer Sandboxes will back up any update sets from the sandboxes and export them to the main instance. The following rules apply:

-   The update set must contain at least one change since the sandbox was created for it to be backed up.
-   Incomplete update sets are backed up as long as there's at least one change.
-   If you install Developer Sandboxes on an instance after Zurich Patch 5, update sets are automatically backed up.
-   If you install Developer Sandboxes on an instance before Zurich Patch 5, you must add the `export_state` column to the sys\_dsb table:

    ```
    <element name="export_state" label="Export State" type="choice" default="not_exported">
        <choice>
           <element label="Not Exported" sequence="-1" value="not_exported"/>
           <element label="Requested" sequence="0" value="requested"/>
           <element label="Scheduled" sequence="1" value="scheduled"/>
           <element label="In Progress" sequence="2" value="in_progress"/>
           <element label="Completed" sequence="3" value="completed"/>
        </choice>
    </element>
    ```


## Cloning instances with Developer Sandboxes

When you clone an instance, the sandboxes on the target instance are deleted and thus not available. You must open a support case to re-enable sandboxes after a clone.

**Note:** You must always save your work in a sandbox before the clone.

