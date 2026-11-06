---
title: Supported ServiceNow AI Platform features in Developer Sandboxes
description: Developer Sandboxes supports almost all development-related ServiceNow AI Platform features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/developer-sandboxes/dev-sbx-supported-features.html
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-10-15"
reading_time_minutes: 1
breadcrumb: [Explore, Developer Sandboxes, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Supported ServiceNow AI Platform features in Developer Sandboxes

Developer Sandboxes supports almost all development-related ServiceNow AI Platform features.

## Development features and apps

Supported features include the following:

-   Metadata updates
-   System Update Sets
-   Legacy source control

    **Note:** Each sandbox can connect to source control with its own git branch. For more information, see [Source control and Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sandboxes-source-control.md).

-   ServiceNow IDE
-   Workflow Studio
-   App and plugin installation

    **Note:** Apps and plugins can be installed and upgraded in a sandbox independently.

-   Outgoing integrations

    **Note:** You must manually update incoming integrations to support the unique URLs of sandboxes.


## Sandbox considerations and limitations

Upgrading an instance automatically backs up update sets to the base instance and recreates the sandboxes on that instance. Sandboxes are recreated in a base state, so you must restore backed up update sets. For details, see [Cloning and upgrading considerations for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-clone-upgrade-info.md).

**Note:** Sandboxes are not automatically recreated after a clone. You should save your work from a sandbox before the clone so you can recreate it.

You can have up to 30 sandboxes per instance.

Developer Sandboxes is supported on on-premises instances. For setup steps, see the Knowledge Base article on [Developer Sandboxes on-premises architecture](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2670540). You're responsible for networking setup, adding the required nodes to the instance, and enabling sandboxes. License management isn't supported on on-premises instances.

**Note:** Developer Sandboxes are not supported on UI/Worker node instances.

**Parent Topic:**[Exploring Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/exploring-sandboxes.md)

