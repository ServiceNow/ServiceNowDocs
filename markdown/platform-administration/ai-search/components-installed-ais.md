---
title: Components installed with AI Search
description: Several types of components are installed with activation of the AI Search plugin, including scheduled jobs, tables, and user roles.Manage configuration settings for the AI Search application.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Components installed with AI Search

Several types of components are installed with activation of the AI Search plugin, including scheduled jobs, tables, and user roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](../../subscription-management/concept/managing-user-subscriptions-v2.md) and contact your account representative.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](../../plugins/task/find-components.md).

## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Aggregate Health Data for AIS Partition|Collects health check data for AI Search query nodes connected to your instance.|
|AI Search Expire Rules|Marks result improvement rules as expired when their end date is in the past.|
|AI Search Relevancy Data Processor|Processes search signal data as part of search profile relevancy model tuning by the machine learning relevancy feature.|
|AIS Collect Ingestion Stats|Collects ingestion history statistics for indexed sources.|
|AIS Derived Dictionary Auto Refresh|Refreshes derived typo handling dictionaries when their refresh interval has elapsed.|
|AIS Index Event Processor|Processes indexing events for indexed sources.|
|AIS Index Event Queue Size Monitor|Monitors the size of the indexing queue during indexing of source records.|
|AIS Index Purge Stale Document|Optimizes the search index by deleting stale documents.|
|AIS Validate Publish ID and Auto Publish|Publishes search profiles and typo handling, stop word, and synonym dictionaries.|
|ML Trigger for AIS Search Relevancy|Triggers automatic tuning of search profile relevancy models by the machine learning relevancy feature.|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search ACL Overrides \[ais\_acl\_overrides\]

</td><td>

List of rules used by content security.

</td></tr><tr><td>

AI Search Active Table Ingestion Tracker \[ais\_active\_table\_ingestion\_tracker\]

</td><td>

List of active content ingestion events for indexed source tables.

</td></tr><tr><td>

AI Search Child Table \[ais\_child\_table\]

</td><td>

List of child tables defined for indexed sources.

</td></tr><tr><td>

AI Search Configuration Attribute \[ais\_configuration\_attribute\]

</td><td>

List of indexed source attributes available for use in indexed sources.

</td></tr><tr><td>

AI Search Connection \[ais\_connection\]

</td><td>

List of AI Search query nodes connected to your instance.

</td></tr><tr><td>

AI Search Dictionary \[ais\_dictionary\]

</td><td>

List of typo handling, stop word, and synonym dictionaries.

</td></tr><tr><td>

AI Search Dictionary Term \[ais\_dictionary\_term\]

</td><td>

List of terms defined in typo handling, stop word, and synonym dictionaries.

</td></tr><tr><td>

AI Search External Content User Mapping Base \[ais\_external\_search\_user\_mapping\]

</td><td>

Empty list of external content user mappings. All custom external content user mapping tables extend this table.**Note:** This table is only installed after activation of the External Content for AI Search plugin \(com.glide.ais.external\_content\).

</td></tr><tr><td>

AI Search External Content User Mapping History Record \[ais\_external\_content\_user\_mapping\_history\]

</td><td>

List of import history events for external content user mapping tables.**Note:** This table is only installed after activation of the External Content for AI Search plugin \(com.glide.ais.external\_content\).

</td></tr><tr><td>

AI Search External Content User Mapping Table Data Source Relationship \[ais\_external\_search\_user\_mapping\_data\_source\_m2m\]

</td><td>

List of mappings between external content user mapping tables and indexed sources.**Note:** This table is only installed after activation of the External Content for AI Search plugin \(com.glide.ais.external\_content\).

</td></tr><tr><td>

AI Search Genius Result Configuration \[ais\_genius\_result\_configuration\]

</td><td>

List of Genius Result configurations.

</td></tr><tr><td>

AI Search Genius Result Configuration NLU Model Mapping \[ais\_genius\_result\_configuration\_sys\_nlu\_model\_m2m\]

</td><td>

List of mappings between NLU models and Genius Result configurations.

</td></tr><tr><td>

AI Search Index Events stats \[ais\_index\_queue\_stats\]

</td><td>

List of statistics entries for indexing events.

</td></tr><tr><td>

AI Search Indexed Batch History \[ais\_ingest\_batch\_stats\]

</td><td>

List of ingestion history events for indexing batches.

</td></tr><tr><td>

AI Search Indexed Event History \[ais\_ingest\_event\_stats\]

</td><td>

List of ingestion history events for indexer events

</td></tr><tr><td>

AI Search Indexed Retry History \[ais\_ingest\_retry\_stats\]

</td><td>

List of ingestion history events produced when retrying indexing for a source table record.

</td></tr><tr><td>

AI Search Indexed Source \[ais\_datasource\]

</td><td>

List of indexed sources.

</td></tr><tr><td>

AI Search Indexed Source Attribute \[ais\_datasource\_attribute\]

</td><td>

List of indexed source attributes configured for indexed sources.

</td></tr><tr><td>

AI Search Indexed Source Field Attribute \[ais\_datasource\_field\_attribute\]

</td><td>

List of field settings configured for indexed sources.

</td></tr><tr><td>

AI Search Indexed Source History \[ais\_ingest\_datasource\_stats\]

</td><td>

List of ingestion history events for indexed sources.

</td></tr><tr><td>

AI Search Indexed Source Statistics \[ais\_datasource\_stats\]

</td><td>

List of entries showing indexed record counts for indexed sources. For more information on these entries, see [Review record counts for indexed sources](../task/record-counts-indexed-sources-ais.md).

</td></tr><tr><td>

AI Search Indexed Table History \[ais\_ingest\_table\_stats\]

</td><td>

List of ingestion history events for individual source tables defined in indexed sources.

</td></tr><tr><td>

AI Search Ingestion Trigger Checkin \[ais\_ingestion\_trigger\_checkin\]

</td><td>

List of ingestion trigger check-in times for AI Search nodes.

</td></tr><tr><td>

AI Search Partition Health \[ais\_partition\_health\]

</td><td>

List of health check events for AI Search query nodes connected to your instance.

</td></tr><tr><td>

AI Search Partition Health Response \[ais\_partition\_health\_response\]

</td><td>

List of health check response events for AI Search query nodes connected to your instance.

</td></tr><tr><td>

AI Search Publish History \[ais\_publish\_history\]

</td><td>

List of publication history events for search profiles and typo handling, stop word, and synonym dictionaries.

</td></tr><tr><td>

AI Search Relevancy Auto Train Solution \[ais\_relevancy\_autotrain\_solution\]

</td><td>

List of relevancy model tuning records used by machine learning relevancy.

</td></tr><tr><td>

AI Search Relevancy Solution Definition \[ais\_relevancy\_solution\_definition\]

</td><td>

List of search profiles with relevancy models tuned by machine learning relevancy.

</td></tr><tr><td>

AI Search Relevancy Training Execution \[ais\_relevancy\_training\_execution\]

</td><td>

List of relevancy model tuning tasks performed by machine learning relevancy.

</td></tr><tr><td>

AI Search Relevancy Training Staging \[ais\_relevancy\_training\_staging\]

</td><td>

List of relevancy model staging tasks performed by machine learning relevancy.

</td></tr><tr><td>

AI Search Results Improvement Rule \[ais\_rule\]

</td><td>

List of result improvement rules.

</td></tr><tr><td>

AI Search Results Improvement Rule Action \[ais\_rule\_action\]

</td><td>

List of actions defined for use in result improvement rules.

</td></tr><tr><td>

AI Search Results Improvement Rule Condition Builder Values \[v\_ais\_result\_improvement\_rule\_condition\_builder\_values\]

</td><td>

List of static values defined for use in result improvement rule actions.

</td></tr><tr><td>

AI Search Retention Policy \[ais\_retention\_policy\]

</td><td>

List of retention policies available for use in indexed sources.

</td></tr><tr><td>

AI Search Search Profile \[ais\_search\_profile\]

</td><td>

List of search profiles.

</td></tr><tr><td>

AI Search Search Profile Dictionary Mapping \[ais\_search\_profile\_ais\_dictionary\_m2m\]

</td><td>

List of mappings between search profiles and typo handling, stop word, and synonym dictionaries.

</td></tr><tr><td>

AI Search Search Profile Genius Result Configuration Mapping \[ais\_search\_profile\_ais\_genius\_result\_configuration\_m2m\]

</td><td>

List of mappings between search profiles and Genius Result configurations.

</td></tr><tr><td>

AI Search Search Profile Relevancy Model \[ais\_search\_profile\_relevancy\_model\]

</td><td>

List of relevancy models created by machine learning relevancy.

</td></tr><tr><td>

AI Search Search Profile Search Source Mapping \[ais\_search\_profile\_ais\_search\_source\_m2m\]

</td><td>

List of mappings between search profiles and search sources.

</td></tr><tr><td>

AI Search Search Source \[ais\_search\_source\]

</td><td>

List of search sources.

</td></tr><tr><td>

AI Search Updatable Field Event \[ais\_updatable\_field\_event\]

</td><td>

List of events for updatable fields on indexed records.

</td></tr><tr><td>

Raw User Mapping for External Content \[ais\_external\_content\_raw\_external\_user\_mapping\]

</td><td>

List of imported user mapping table entries.**Note:** This table is only installed after activation of the External Content for AI Search plugin \(com.glide.ais.external\_content\).

</td></tr></tbody>
</table>## Roles installed

AI Search includes the following roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](../../subscription-management/concept/managing-user-subscriptions-v2.md) and contact your account representative.

**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

## AI Search administrator \[ais\_admin\]

Manage configuration settings for the AI Search application.

-   Creates, reads, updates, and deletes indexed sources
-   Creates, reads, updates, and deletes search sources
-   Creates and deletes mappings between search sources and search profiles
-   Creates, reads, updates, and deletes search profiles
-   Creates, reads, updates, and deletes synonym and stop word dictionaries
-   Creates and deletes mappings between dictionaries and search profiles
-   Reads and updates typo handling auto-correction dictionaries linked to search profiles
-   Creates, reads, updates, and deletes Genius Result configurations
-   Creates and deletes mappings between Genius Result configurations and search profiles
-   Creates, reads, updates, and deletes result improvement rules
-   Creates and deletes mappings between result improvement rules and search profiles

### Contains roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

