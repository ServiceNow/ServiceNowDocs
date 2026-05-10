---
title: Domain separation and AI Search
description: Domain separation is unsupported for the AI Search application tables, but user search queries respect domain restrictions from indexed ServiceNow AI Platform table records. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Domain separation and AI Search

Domain separation is unsupported for the AI Search application tables, but user search queries respect domain restrictions from indexed ServiceNow AI Platform® table records. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Note:** Refer to the Overview and following sections for details on how AI Search search queries respect domain settings from indexed records.

## Support level: No support

-   The domain field may exist on data tables but there is no business logic to manage the data.
-   This level is not considered domain-separated.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## AI Search domain separation overview

AI Search enables users to index and search content from records in ServiceNow AI Platform tables. The AI Search application tables and properties don't support domain separation, but user search queries respect domain settings from indexed content as described in the following sections.

## Domain separation in indexed content and search queries

When indexing searchable content from a ServiceNow AI Platform table, AI Search stores the sys\_domain field values for records on the source table and referenced tables.

If domain separation is enabled, AI Search applies a filter for the current session domain to every search query. This filter excludes records that aren't visible in the session domain. Only records visible in the session domain appear as search query results.

For child tables that have the **domain\_master** attribute set, both indexing and search use the appropriate reference field to derive the child record domain from a referenced parent record.

Restrictions apply to referenced records in search queries, as summarized in the following table.

<table id="table_hh3_lyh_3nb"><thead><tr><th>

Condition

</th><th>

Behavior

</th></tr></thead><tbody><tr><td>

Referenced record isn't visible in current session domain

</td><td>

-   Search queries don't match content from the referenced record
-   Filtering on the reference field has no effect on search results
-   Faceting on the reference field has no effect

</td></tr><tr><td>

Referenced record domain differs from parent record domain

</td><td>

Search result records don't display the reference field

</td></tr></tbody>
</table>## Indexing changes to record domains

AI Search automatically updates indexed domains for records in tables configured as indexed sources.

AI Search doesn't automatically update indexed domains for referenced tables. You can update the indexed domain for a referenced table in either of the following ways.

<table id="table_b21_zf3_3nb"><thead><tr><th>

Use case

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Perform a one-time update of domain field values for a referenced table

</td><td>

Perform a full table reindex for the indexed source that includes the affected table. For details on this procedure, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr><tr><td>

Enable automatic updating of domain field values for a referenced table

</td><td>

Create a **dot\_walk\_fields** field setting for the reference field, specifying the `sys_domain,sys_domain_path` domain fields as the attribute value. For full steps for this task, see [Enable automatic domain updates for a referenced table](../task/enable-ref-auto-domain-update-ais.md).

</td></tr></tbody>
</table>-   **[Enable automatic domain updates for a referenced table](../task/enable-ref-auto-domain-update-ais.md)**  
Configure a field setting to automatically index domain field value updates for records from a referenced table.

**Parent Topic:**[Configuring AI Search](configuring-ais.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

