---
title: Run metadata collectors manually
description: Execute a metadata collector on-demand to import metadata immediately.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Running metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Run metadata collectors manually

Execute a metadata collector on-demand to import metadata immediately.

## Before you begin

Role required: connection\_admin

## About this task

Running a collector manually initiates immediate metadata harvesting from the configured source system. Use manual execution to verify new collector configurations, refresh metadata after source system changes, or gather updated information outside the scheduled collection cycle. Collection duration varies based on the volume of metadata in the source system.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub icon in the left sidebar.

3.  Select **Connectors**.

4.  Select **Metadata collector**.

5.  Select the metadata collector you want to run manually.

6.  In the Last run summary section, select **Run now**.![Run a collector manually](../image/dc-mcollector-run.png)


**Parent Topic:**[Running metadata collectors](../concept/run-metadata-collectors-dc.md)

