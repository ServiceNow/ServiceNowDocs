---
title: Migrate the collaborate and Microsoft Teams import screens to new Collaboration services screens
description: Map the collaborate and MS Teams import screens to use the new Collaboration services screens in Service Operations Workspace \(SOW\).
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enable collaboration services for configurable workspaces, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Migrate the collaborate and Microsoft Teams import screens to new Collaboration services screens

Map the collaborate and MS Teams import screens to use the new Collaboration services screens in Service Operations Workspace \(SOW\).

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, search and select **sys\_ux\_screen\_type.list**.

2.  Map the **Collaborate** tab to use the UI Components of Collaboration for Configurable Workspaces \(com.snc.uib.collaboration\) plugin.

    1.  Apply the filter and search for **4367156343b62110361dff53e9b8f2de** in Sys ID.

        The Collaborate UX screen collection is displayed.

    2.  Select **Collaborate**.

    3.  In the **UX Screens** tab, under **Active**, set the **Collaborate Tab SNC** value as **false**.

3.  Map the MS Teams Import default - v2 screen to use the UI Components of Collaboration for Configurable Workspaces \(com.snc.uib.collaboration\) plugin.

    1.  Apply the filter and search for **eac6db0d3bb92290305efec5e4e45a8d** in Sys ID.

        The MS Teams Import screen collection is displayed.

    2.  Select **MS Teams Import**.

    3.  In the **UX Screens** tab, under **Active**, set the **MS Teams Import** value as **false**.

4.  Map Start MS Teams Chat screen to use the UI Components of Collaboration for Configurable Workspaces \(com.snc.uib.collaboration\) plugin.

    1.  Apply the filter and search for **c04230e9ff7da210549fffffffffff1d** in Sys ID.

        The Start MS Teams Chat screen collection is displayed.

    2.  Select **Start MS Teams Chat**.

    3.  In the **UX Screens** tab, under **Active**, set the **Start MS Teams Chat** value as **false**.


