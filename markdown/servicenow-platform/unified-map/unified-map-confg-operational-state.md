---
title: Configure CIs to appear based on life cycle stage value
description: By default, only CIs for which Life cycle stage is Operational or empty appear on maps. You can configure the map to display CIs with other Life cycle stage values. These are general settings that only sn\_cmdb\_admin can configure.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure CIs to appear based on life cycle stage value

By default, only CIs for which **Life cycle stage** is **Operational** or empty appear on maps. You can configure the map to display CIs with other **Life cycle stage** values. These are general settings that only sn\_cmdb\_admin can configure.

## Before you begin

Set the application scope in your instance to **CMDB Workspace**.

Role required: sn\_cmdb\_admin

## About this task

-   By default, non-operational CIs are filtered out and do not appear on maps.
-   Search results don't include CIs that are filtered out based on operational state.
-   The **Open Map** button \(for viewing details\) on the CI form isn't available for CIs that are filtered out based on operational state.

These workspace-specific configuration settings affect all users of the CMDB Unified Map page. The settings do not affect other copies of the Unified Map template. Non-admin users can customize some aspects of their personal experience with Unified Map, but can't configure instance-wide workspace-specific settings.

## Procedure

1.  Navigate to **All** and then, in the **Filter** box in the main navigation bar, enter `sn_cmdb_ws_operational_lifecycle_for_unified_map.list` to open the **Operational life cycle modes** table.

2.  Select the list of selected live cycle stage values.

    For Unified Map, the default list of selected live cycle stage values is named **CMDB Workspace Unified Map View**.

    1.  Unlock the **Life cycle list** field and then select the Edit multiple icon ![](../image/icon-edit-multiple.png).

    2.  In the Edit Members pop-up, move the life cycle stage values for CIs that should appear on maps into the **Selected life cycle stages** list and then select **Save**.

    3.  On the record form, select **Update** or **Save**.

    -   The updated settings appear in the appropriate related list on the Configuration identifier form, as described in [Configuring Unified Map — admin settings](../concept/administer-unified-map.md). The updated list of life cycle stage values is added to the **CMDB Workspace Unified Map View** life cycle mode on the **Operational life cycle modes** related list for the affected configuration identifier.
    -   You can also perform this operation from the **Operational life cycle modes** related list.

**Parent Topic:**[Configuring Unified Map — admin settings](../concept/administer-unified-map.md)

