---
title: Automatically map AI search results with guidance inputs in Recommended Actions
description: Automatically create AI search results for a search configuration application in Recommended Actions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring AI search, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Automatically map AI search results with guidance inputs in Recommended Actions

Automatically create AI search results for a search configuration application in Recommended Actions.

Search application configuration records specify the search engine and settings to use for search in Recommended Actions. When you choose AI search as an application's search engine, you can configure the search results and map them to specific actions.

Starting with the Yokohama release, the Recommended Actions application automatically creates the mapping between search results and actions.

When an admin creates or updates the search application configuration for a context record, the system automatically creates search result mapping records for each of the search sources in that configuration.

-   If a search source does not have an existing mapping to an action, the system maps the search source to the [Default guidance for search results](ra-csm-guidances-default-guidance-search.md) guidance.
-   If a search source has an existing mapping to a specific action, the system keeps that mapping and does not overwrite it with the default guidance.

Mapping records are stored in the Search result recommended action mapping table \(sn\_nb\_action\_search\_result\_ra\_mapping\) and are displayed in the Search result mapping related list on the context record.

When a context record is saved or updated and search result mappings are created, the system displays a message: "Based on the selected Search Application Configuration the Search Result Mapping list has been updated. Please review!"

## Adding new search sources

Admins can add search sources to the search profile of a search application configuration. If a new search source is added to the configuration selected for a context record, the system does the following:

-   Creates a new record in the Search result to recommended action mapping table \(sn\_nb\_action\_search\_result\_ra\_mapping\) for the added search source.
-   Maps the search source to the Default guidance for search results.

When a search source is deleted from the search profile, the system removes the corresponding record from the Search result to recommended action mapping table \(sn\_nb\_action\_search\_result\_ra\_mapping\).

## Refreshing the Search result mapping related list

The system stores search result mapping records in the Search result to recommended action mapping table and displays them in the Search Result Mapping related list on the context record.

The Search Result Mapping related list includes a **Refresh** button that admins can use to create search result mapping records for the search sources within a selected search application configuration in a context record. Selecting **Refresh** generates mapping records for any missing search result mappings in the search application configuration and associates them with the Default guidance for search results guidance.

**Note:** Refreshing the Search Result Mapping list does not override existing customer-defined mappings.

Newly created mapping records are active by default. Admins can control which search sources are displayed to agents by enabling or disabling the **Active** field on the mapping records.

## Search result recommended action mapping table

The Search result recommended action mapping table \(sn\_nb\_action\_search\_result\_ra\_mapping\) stores the mapping between search sources and actions. Records in this table include an **Active** field which the admin can use to manage the activation state of search result mappings. When a new record is created in this table, the **Active** field is set to true by default.

When an agent performs a search in the Recommended Actions search component in CSM Configurable Workspace, the system displays the search sources that are marked as active in the search result mapping configuration. Inactive search sources are excluded from the search results.

Changes in the search result mapping, such as activating or deactivating a search source, are automatically reflected in the search results.

When the **Active** field is disabled for a search source, an admin can create a new mapping for that source. A search source can have multiple search result mapping records, but only one can be active at a time.

## Conditional UI display for search result mapping

The Recommended Actions context record includes the **Search application configuration** field. When an admin selects a configuration in this field, the search result mapping records for the configuration are displayed in the Search result mapping related list. If the **Search application configuration** field is empty, the Search result mapping related list does not appear on the context record.

