---
title: Using AI Search with CSM Configurable Workspace
description: Use the ServiceNow AI Search application with CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Using AI Search with CSM Configurable Workspace

Use the ServiceNow® AI Search application with CSM Configurable Workspace.

Starting with the Utah release, the [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US) application replaces the Zing search application for CSM Configurable Workspace. To support this feature, the Zing search configurations have been migrated to AI Search.

Use the Unified Navigation search field in CSM Configurable Workspace to search for information. You can switch between global search results and results from the **CSM/FSM Configurable Workspace** workspace application. The different search configurations are based on different tables.

For more information about using AI Search with CSM Configurable Workspace, see [AI Search for Next Experience](https://www.servicenow.com/docs/access?context=ais-next-experience-app&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Search application configurations

A search application configuration specifies the search engine and the settings to use for search in a ServiceNow AI Platform application. The **\[CSM AIS\] Configurable Workspace Search Config** search application configuration is provided with the CSM Configurable Workspace store app.

To access this configuration, navigate to **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

## AI Search indexed sources

Indexed sources reflect what content users are able to search on. The CSM Configurable Workspace store app adds AI Search indexed sources for the following tables:

-   Account \[customer\_account\]
-   Case \[sn\_customerservice\_case\]
-   Consumer \[csm\_consumer\]
-   Contact \[customer\_contact\]
-   Order Line Item \[csm\_order\_line\_item\]
-   Order \[csm\_order\]
-   Catalog item \[sc\_cat\_item\]

## Navigation tabs

Navigation tabs appear at the top of the search results page and are static filter options that you can use to filter the results by indexed source. The **\[CSM AIS\] Configurable Workspace Search Config** search application configuration includes the following navigation tabs:

-   All
-   Cases
-   Accounts
-   Contacts
-   Consumers
-   Orders
-   Order Line Items
-   Locations

For information about creating navigation tabs, see [Configure navigation tabs in an AI Search application configuration](https://www.servicenow.com/docs/access?context=config-nav-tabs-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Facets

Facets are dynamic filter options that you can use to refine the search results by field value. The **\[CSM AIS\] Configurable Workspace Search Config** search application configuration includes the following facets:

-   State
-   Priority
-   Assignment Group
-   Product
-   Account
-   Contact
-   Consumer
-   Needs Attention
-   Action Status
-   Channel
-   Active Escalation

For information about creating facets, see [Create a facet in an AI Search application configuration](https://www.servicenow.com/docs/access?context=create-facet-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Guided setup

Guided setup provides a sequence of tasks that helps you configure search application settings. To access guided setup, navigate to **All** &gt; **AI Search** &gt; **AI Search for Next Experience** &gt; **Guided Setup for Zing to AI Search Migration**.

This guided setup tool assists with the migration of Next Experience applications from Zing to AI Search. For more information about using guided setup, see [Configuring AI Search for Next Experience](https://www.servicenow.com/docs/access?context=configuring-ais-next-experience&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Depending on your release, you may need to perform only some of the tasks within the guided setup to use AI Search with CSM Configurable Workspace. For Utah zBoot instances, AI Search is the default search application for global search and the CSM Configurable Workspace application.

## Migrating Zing search configurations

If you have added, modified, or deleted any search configurations provided out of box, you may need to migrate existing Zing search configurations to AI Search configurations.

-   If you have added or modified any search sources in **Agent Workspace Search Config**, you need to migrate these sources to AI Search.
-   If you have deleted any search sources from **Agent Workspace Search Config**, you need to manually delete them from **\[Migrated\] Agent Workspace Search Config**

## Enable fuzzy matching in AI search

Fuzzy matching enables agents to search for records using partial record IDs or incomplete record details and retrieve relevant results. Fuzzy matching identifies similar but not identical elements in data table sets.

AI search in CSM Configurable Workspace supports fuzzy matching with a script. Activating the Customer Service plugin \(com.sn\_customerservice\) automatically runs the script and enables fuzzy match search in both the CSM Configurable Workspace global search and the Recommended Actions AI search component.

When fuzzy matching is enabled:

-   AI search returns results based on approximate matching, including partial text or slightly mistyped record IDs.
-   The system ranks the search results in order of relevance, prioritizing exact matches but including close matches.

After fuzzy matching is enabled, the system adminisrator needs to re-index the tables used in AI search:

1.  Make sure that fuzzy matching is enabled by running this command as a background script:

    **gs.info\(new sn\_ais.AisUtil\(\).isFuzzyNumberMatchEnabled\(\)\);**

    The result should be 'true'.

2.  Make sure that AI search is enabled.
3.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.
4.  Select the table to re-index.
5.  Select **Index All Tables**.
6.  Go to the homepage and enter a search query in the global search field.

    You should see fuzzy matching results for the tables that were re-indexed.


**Note:** If a table is not present in the AI Search Index Sources list, you can add the table by selecting **New** on this list.

**Related topics**  


[Exploring AI Search](https://www.servicenow.com/docs/access?context=explore-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

[Configuring AI Search](https://www.servicenow.com/docs/access?context=configuring-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

