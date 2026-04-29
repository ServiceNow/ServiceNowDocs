---
title: Published TRM catalog experience
description: When you publish a Technology Reference Model \(TRM\) catalog from the Publishing Center, the system generates a Knowledge Base catalog that presents approved technology standards in a consumable, read‑only format.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with the publishing center, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Published TRM catalog experience

When you publish a Technology Reference Model \(TRM\) catalog from the Publishing Center, the system generates a Knowledge Base catalog that presents approved technology standards in a consumable, read‑only format.

## What you can see after publishing

After a TRM catalog is published, you can access it as Knowledge Base content:

-   A TRM catalog appears in the Knowledge Base with categories that help you browse and filter products.
-   Each TRM product is published as an individual Knowledge Base article.
-   Each product article displays product metadata based on the publishing configuration, including only the fields selected by the administrator.
-   The order of fields in the article reflects the order configured in the Publishing Center.
-   TRM product lifecycle information is displayed as a table within the article. As an Administrator user you can control:
    -   Which lifecycle records are included
    -   Which columns are displayed
    -   The order of lifecycle columns

This structure ensures that you can see consistent, curated technology standards without accessing the Enterprise Architecture Workspace.

## Access type and visibility

When creating a publishing configuration, as an administrator user you can select an access type that determines who can view the published catalog:

-   **Internal**: Only authenticated users with access to the Knowledge Base can view the catalog.
-   **Public**: The catalog can be made available to guest users, depending on portal configuration.

**Note:** For public catalogs, the associated portal pages must be configured to allow guest access. Portal configuration determines, where and how the catalog is exposed.

## Where the catalog can be accessed

Because the output is Knowledge Base content, the published TRM catalog can be surfaced in multiple portals, such as:

-   Service Portal
-   Employee Portal
-   Other custom portals built on ServiceNow

Portal visibility is managed by associating the knowledge base with one or more portals in the Publishing Center.

## How published content stays up to date

After publishing, the system keeps the Knowledge Base articles synchronized with TRM data:

-   Updates to TRM product fields and lifecycle data are reflected automatically in the published articles.
-   Date‑driven lifecycle phase changes are updated automatically as phases transition.

This synchronization ensures that published technology standards remain current without requiring repeated publishing for routine data updates.

**Note:** Some structural changes, such as renaming TRM phases or categories, require the catalog to be republished to apply the updates consistently across all articles.

**Parent Topic:**[Working with the publishing center](../../concept/eaw-concept/working-with-publishing-center.md)

**Related topics**  


[Create a new configuration to publish TRM data](../../task/eaw-task/config-trm-data-to-publish.md)

[Publish a TRM catalog to the knowledge base](../../task/eaw-task/publish-trm-cat-to-kb.md)

[View publishing status and run log](../../task/eaw-task/view-run-log.md)

[Access the published TRM catalog knowledge base](../../task/eaw-task/access-the-published-kb.md)

[Understanding the publishing results and knowledge base output](understand-publishing-output.md)

