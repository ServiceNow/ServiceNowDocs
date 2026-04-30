---
title: Highlights
description: Learn how Workspace highlights function with Configurable Workspace.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Highlights

Learn how Workspace highlights function with Configurable Workspace.

Highlights provide background color that visually expresses the status of a highlighted value. The status you choose determines the color highlight.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_highlighted\_value|sys\_highlighted\_value sys\_ux\_highlighted\_value\_config sys\_ux\_m2m\_highlighted\_value\_config|

To migrate your highlights, add an extra step in the custom highlighted values to Configurable Workspace.

An additional highlighted value configuration is provided out of box, CSM/FSM Configurable Workspace Highlighted Value Config.

-   Legacy highlighted values in form headers work without modification, but may affect the functionality of Configurable Workspace.
-   Highlighted values must be added to a highlighted value configuration to appear in Configurable Workspace.

For more information, see [Set up a highlighted value](../task/config-csm-config-ws-highlight-value.md).

