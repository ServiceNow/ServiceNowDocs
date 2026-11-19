---
title: Remove a CI from a map using the map editor
description: You can remove \(hide\) a CI from the map only if you added it during the current editing session. You cannot remove CIs that were on the map when you started the editing session.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/unified-map/unified-map-editor-remove-ci.html
release: yokohama
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Edit a map, UNDER CONSTRUCTION Use, Unified Map, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Remove a CI from a map using the map editor

You can remove \(hide\) a CI from the map only if you added it during the current editing session. You cannot remove CIs that were on the map when you started the editing session.

## Before you begin

Role required: admin

## About this task

The following things happen when you remove \(hide\) a CI from the map:

-   The CI no longer appears on the map, but the CI record isn’t deleted from the CMDB.
-   The records in the \[cmdb\_ci\_rel\] table for all relationships to and from the CI are deleted.

## Procedure

1.  While editing a map, take one of the following actions:

    -   Select the CI and then select **Remove** in the Attributes panel.
    -   Right-click the CI and then select **Remove**.

