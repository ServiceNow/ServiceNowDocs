---
title: Sync definitions
description: Enable definition synchronization and push new, customized, or overridden definitions from a development instance to production.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/sync-new-customized-overridden-defs.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Definitions integration, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Sync definitions

Enable definition synchronization and push new, customized, or overridden definitions from a development instance to production.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## Procedure

1.  Enable definition synchronization
2.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

3.  On the **Definitions** properties tab, ensure **Enable definition synchronization** is active.

4.  Sync a definition
5.  Navigate to **ALL** &gt; **Impact** &gt; **Definitions** and open the definition to sync.

6.  Select the appropriate sync action.

    |Action|Result|
    |------|------|
    |**Sync Definition**|Syncs the definition with a sync note.|
    |**Delete and Sync**|Deletes the definition on the target instance and propagates the current version.|


## Result

The definition is pushed to the production instance.

To bulk sync multiple definitions, select the checkbox for each definition in the Definitions list view, then select **Sync Definition** or **Delete and Sync** from the actions menu.

**Parent Topic:**[Definitions integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/definitions-integrations.md)

