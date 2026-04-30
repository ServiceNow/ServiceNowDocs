---
title: Delete an exporter
description: Delete an exporter to ensure that users cannot use it to generate config data.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Export a snapshot, Use, DevOps Config, IT Service Management]
---

# Delete an exporter

Delete an exporter to ensure that users cannot use it to generate config data.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: cdm\_exporter\_editor or cdm\_editor or cdm\_admin

## About this task

-   You cannot delete, modify, or activate exporters that are included in the CDM content pack. Exporters in the content pack have a **Source** value of **ServiceNow**.
-   If an exporter has performed a standard execution, you cannot delete it. This ensures a complete and accurate audit trail. You can archive an exporter that has performed a standard execution. See [Archive an exporter](cdm-exporter-archive.md).
-   If an exporter does not have a standard execution, then you can delete all draft versions and published versions by deleting the exporter.
-   You can delete any draft version of an exporter.

**Tip:** You cannot generate a draft version of a content pack exporter, but you can duplicate one and edit draft versions of the duplicate. Editing a duplicate of a content pack exporter is a good way to create a custom exporter. See [Create a custom exporter](cdm-exporter-create-custom.md).

## Procedure

1.  Use either of the following methods to delete all versions of an exporter: While working on an exporter on the **Exporter builder** tab or viewing a list of exporters, select the exporter and then select **Delete**.

    -   While working on an exporter on the **Exporter builder** tab, select **Delete**.
    -   While viewing a list of exporters, select the exporter and then select **Delete**.
    All versions of the exporter are deleted and the exporter is no longer listed on the **Versions** tab.

2.  To delete only a particular draft version of an exporter, select the version, select **Delete draft**, and then confirm the action.


