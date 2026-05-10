---
title: Exploring the publishing center in Enterprise Architecture Workspace
description: The Publishing Center is a centralized capability in the Enterprise Architecture Workspace. It helps you configure, manage, and track publishing activities from a single location.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Exploring the publishing center in Enterprise Architecture Workspace

The Publishing Center is a centralized capability in the Enterprise Architecture Workspace. It helps you configure, manage, and track publishing activities from a single location.

## Publishing Center Overview

The Publishing Center provides a structured, repeatable way to publish curated EA content to broader audiences.

Use the Publishing Center for:

-   Centralize publishing workflows- instead of managing ad‑hoc or manual publishing processes.
-   Ensure consistency and governance- by controlling what content is published and how.
-   Increase visibility and adoption- following enterprise standards by publishing them to consumable platforms.
-   Track publishing activity and outcomes- through status and historical run logs.

Understanding the terminology used in Publishing Center:

-   Publishing Configuration– defines the information that is published to the knowledge base.
-   Knowledge Base – from where the published catalogs are consumed.

The Publishing Center displays a list of all available publishing configurations. Each row represents a catalog that can be published or republished.

Publishing status and indicators- Each publishing configuration displays a status that reflects its current publishing state. Status values are visually indicated using color‑coded badges. Use the status indicators to quickly understand the publishing state of each catalog. The following are the status indicators:

-   Draft– The configuration is ready to publish or has unpublished changes after edits.
-   Publishing– A publish or republish operation is currently in progress.
-   Published– The catalog has been successfully published to the Knowledge Base.
-   Publishing failed– The publishing operation failed and requires attention.

![Publishing center home page in the Setup section](../../image/eaw-image/pub-center-home.png)

## Required plugin

To use this feature in the Enterprise Architecture Workspace, you must install the Knowledge Management Advanced Installer \[com.snc.knowledge\_advanced.installer\] plugin. For more information, see [Activate the Knowledge Management Advanced plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/activate-knowledge-advanced-plugin.md). Activating this plugin activates the features such as article versioning, article subscriptions, and article templates.

**Note:** Starting with the Xanadu release, the Knowledge Management Advanced plugin is automatically activated for new customers. If you are upgrading from a previous version, you must activate the plugin manually.

## Roles and permissions required for publishing

While many users consume the published content, the ability to publish or republish knowledge base content is controlled to ensure only authorized users can change what is shared organization‑wide. The following are the required roles:

-   Enterprise Architecture Admin \(sn\_apm.apm\_admin\)- to access the Publishing Center page in Enterprise Architecture Workspace
-   Knowledge Base Admin \(knowledge\_admin\)- to publish knowledge base articles
-   Service Portal Admin \(sp\_admin\)- to associate the knowledge base with portals

## Configure publishing workflows

You can create and manage publishing configurations that define:

-   What Enterprise Architecture content is included
-   How the content is structured using AND/OR operators
-   Where the published output is delivered

Each configuration represents a repeatable publishing setup whenever data changes.

## Monitor publishing status

You can track the execution of publishing workflows, including:

-   Whether a publishing job is in progress, completed, or failed
-   The outcome of each publishing run
-   Errors or warnings encountered during publishing

This visibility helps you validate publishing results and quickly identify issues.

## View publishing history

You can view all the publishing activity, including:

-   Historical publishing runs
-   Execution timestamps
-   Status and results for each run

Publishing history provides traceability and operational insight, making it easier to audit changes and understand when published content was last refreshed.

**Parent Topic:**[Exploring Enterprise Architecture Workspace](../explore-eaw.md)

**Related topics**  


[Working with the publishing center](working-with-publishing-center.md)

[Published TRM catalog experience](../../reference/eaw-reference/published-trm-cat-exp.md)

[Access the published TRM catalog knowledge base](../../task/eaw-task/access-the-published-kb.md)

[Understanding the publishing results and knowledge base output](../../reference/eaw-reference/understand-publishing-output.md)

