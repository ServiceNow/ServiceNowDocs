---
title: Supported ServiceNow AI Platform features in Developer Sandboxes
description: Developer Sandboxes supports almost all development-related ServiceNow AI Platform features.
locale: en-US
release: zurich
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2025-11-21"
reading_time_minutes: 1
breadcrumb: [Explore, Developer Sandboxes, Developing your application, Building applications]
---

# Supported ServiceNow AI Platform features in Developer Sandboxes

Developer Sandboxes supports almost all development-related ServiceNow AI Platform features.

## Development features and apps

Supported features include the following:

-   Metadata updates
-   System Update Sets
-   Legacy source control

    **Note:** Each sandbox can connect to source control with its own git branch. For more information, see [Source control and Developer Sandboxes](dev-sandboxes-source-control.md).

-   ServiceNow IDE
-   Workflow Studio
-   App and plugin installation

    **Note:** Apps and plugins can be installed and upgraded in a sandbox independently.

-   Outgoing integrations

    **Note:** Incoming integrations must be manually updated by customers to support the unique URLs of sandboxes.


## Sandbox limitations

Sandboxes are deleted when the instance is upgraded or cloned, though after the upgrade users can start creating sandboxes immediately, without additional configuration. For more information, see [Cloning and upgrading considerations for Developer Sandboxes](dev-sbx-clone-upgrade-info.md).

You can have up to 30 sandboxes per instance.

Developer Sandboxes does not support self-hosted instances by default, though you can set up your own networking and routing changes to support sandboxes.

