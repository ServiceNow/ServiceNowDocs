---
title: Knowledge article sync via FDS
description: Foundation Data Sync \(FDS\) assigns synced knowledge articles to knowledge bases and creates knowledge bases automatically when the source instance does not specify one. FDS also supports syncing of knowledge data from one instance to another instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/knowledge-base-assignment.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [knowledge base, article sync, knowledge management, instance synchronization]
breadcrumb: [Foundation data sync, Explore, Service Exchange]
---

# Knowledge article sync via FDS

Foundation Data Sync \(FDS\) assigns synced knowledge articles to knowledge bases and creates knowledge bases automatically when the source instance does not specify one. FDS also supports syncing of knowledge data from one instance to another instance.

FDS applies default configurations to knowledge Offering Items and governs article ownership, edit behavior, and knowledge base assignment on target instances. Target instances create company knowledge bases automatically when source instances don't specify one. These configurations verify articles sync and display correctly while preventing conflicting edits or sync failures.

## Offering Item configuration for knowledge articles

When you select Knowledge \[kb\_knowledge\] or an extension table on an FDS Offering Item form, the system applies default configurations automatically. A message displays on the form to confirm that these defaults have been applied.

You can add fields or conditions beyond these defaults. However, the required fields are protected. If you remove a required field and save, the system restores it automatically. This maintains the minimum configuration required for knowledge articles to sync and display correctly.

The system checks the configuration each time you save an Offering Item with Knowledge \[kb\_knowledge\] or an extension table as the table and restores missing required elements.

The following configurations are applied automatically:

-   A filter of **Workflow State** = `Published` is prepended to the conditions on the Offering Item. This filter cannot be removed. Drafts, articles under review, and retired articles on the source are never included in the sync.
-   The Coalesce Fields value is automatically set to Article ID.
-   The **Maintain Sys ID** option is hidden for Knowledge \[kb\_knowledge\]. The system handles sys\_id preservation for knowledge articles automatically.
-   A warning banner displays on the Offering Item form to confirm that sys\_id management is handled by the system.

When FDS syncs a knowledge article to a receiving instance, that article is owned by the Service Exchange connection that delivered it. The source instance is the authority for that article. To enforce this, three standard article actions \(**Checkout**, **Retire**, and **Delete**\) behave differently for FDS-synced articles compared to articles created locally. Only articles created by the FDS sync process are affected. Articles created manually on the same instance behave normally.

|Action|Locally created article|FDS-owned article|
|------|-----------------------|-----------------|
|Checkout|Checkout proceeds|Blocked. Alert displays;checkout does not proceed.|
|Retire|Article is retired|Blocked. Alert displays; article is not retired.|
|Delete|Standard platform confirmation displays|Confirmation required. Custom warning displays; delete proceeds only on explicit confirmation.|
|Edit / Update|Changes are saved|Changes are saved but may be overwritten on the next sync.|

When a knowledge article syncs from a source instance to a target instance, the target instance checks whether the incoming article has a knowledge base assigned. The following outcomes can occur:

-   If the source does not send a knowledge base, the article is assigned to a knowledge base and named named after the sending company. The target instance creates this knowledge base automatically if it does not already exist.
-   If the source sends a knowledge base name that does not exist on the target instance, the article is assigned to the company knowledge base. This assignment prevents sync failure.
-   If the source sends a knowledge base name that exists on the target instance, the article is assigned to that knowledge base. No company knowledge base is created.

**Note:** If a target article already has a knowledge base assigned, this behavior does not overwrite it.

**Related topics**  


[Hide a synced knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/hide-synced-knowledge-article.md)

