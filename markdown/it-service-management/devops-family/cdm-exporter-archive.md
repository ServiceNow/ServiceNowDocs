---
title: Archive an exporter
description: Archive an exporter to preserve its record and remove it from the lists that you use in your everyday work.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Export a snapshot, Using DevOps Config, DevOps Config, IT Service Management]
---

# Archive an exporter

Archive an exporter to preserve its record and remove it from the lists that you use in your everyday work.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: cdm\_exporter\_editor, or cdm\_editor, or cdm\_admin

## About this task

-   You can archive only exporters that have standard runs.
-   You can copy and test run an archived exporter. You cannot use the API to run an archived exporter.
-   You cannot perform the export operation using an archived exporter.
-   You cannot delete, modify, publish, or rename an archived exporter or any of its versions.
-   You cannot create new draft of or reuse the name of an archived exporter.
-   To restore an exporter for normal use, set its **State** value to **Active** and publish a version.

## Procedure

1.  While working on an exporter on the **Exporter builder** tab or while viewing a list of exporters, select the exporter and then select **Archive**.

    The **State** value of the exporter is set to **Archived**.


