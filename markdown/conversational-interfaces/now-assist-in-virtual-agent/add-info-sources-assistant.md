---
title: Assign search sources to a chat assistant
description: Assign search sources to a chat assistant. Search sources are used to determine what the assistant looks at to answer user queries.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Assign search sources to a chat assistant

Assign search sources to a chat assistant. Search sources are used to determine what the assistant looks at to answer user queries.

## Before you begin

See [Use agentic support for a chat assistant](use-agentic-support.md).

Role required: virtual\_agent\_admin or admin

## About this task

Each assistant has its own search configuration. If you have configured AI Search on any existing portal or mobile app, you can copy the existing configuration to your assistant’s search configuration. You can also add external or internal search sources to the assistant.

**Note:** Search configuration isn't applicable to Now Assist panel - Developer assistant.

## Procedure

1.  Assign search sources to your chat assistant.

    ![View of the information sources.](../image/NAinVA-search-sources-122025.png "Search sources in the default search profile")

    When a chat assistant is created, a search profile for that assistant gets created. All search sources associated with the profile are listed. The default search sources are:

    -   Now Assist Multi-Turn Catalog Ordering \(catalog search sources\)
    -   Now Assist Q&amp;A \(knowledge base search sources\)
2.  Select the ellipsis if you want to edit the conditions of each skill.

3.  Select **Copy existing configuration** if you have already configured AI Search for your portal, mobile app, or platform search, and you want the assistant to have those same search configurations.

    Copying an existing configuration imports an existing search configuration to the assistant's search profile and search configuration.

    Using existing search application configurations saves time building assistant search configurations. In addition, for the display experience that uses enhanced chat, the assistant search configuration takes over the portal, mobile app, and the platform search experience to ensure that search and the assistant always provide consistent answers.

4.  Select a search application configuration from the **Copy configuration** drop-down list.

    The **Copy configuration** list includes all portal search configurations, mobile search configurations, platform search configurations, and the default assistant search configuration from the AI Search Admin console.

    For the Now Assist panel - Platform \(default\) assistant, copy the Global Search application configuration if you want the answers from the assistant and the platform Global Search to be consistent. The name of the default Global Search app is \[AIS\] Next Experience Search Configuration. However, AI Search admins can change which search app is configured for the Global Search.

    When a user starts a chat with the Now Assist - Platform \(default\) assistant from the sparkle icon, search typeahead or the \(+\) button, the Now Assist - Platform \(default\) assistant search application configuration is used for both Virtual Agent and platform searches.

    When a user selects **Ask a follow up** or requests a catalog item from the search results page of a specific workspace, the specific workspace search application configuration is used for both Virtual Agent and search.

    The associated search profile is also shown.

    ![Drop-down list with search configurations.](../image/NAinVA-copy-config-052025.png "Select a search configuration to copy")

5.  Select **Copy**.

    After copying an existing configuration, the existing configuration for your portal, mobile app, or platform search overwrites your assistant's search application configuration. The latest configuration and the search sources are shown.

    **Note:** All search sources are copied into the assistant search profile. However, only knowledge base, conversational catalog items, and external content are used for the LLM-generated conversational responses. Other search sources are used for the query-based search results, and when the user selects **View more search results**, Virtual Agent responses are seamless with the portal or mobile app search results page.

6.  Select the ellipsis at the end of each table row to edit conditions or add a new condition set.

    The **Edit conditions** pop-up window appears.

    ![Table view for editing conditions.](../image/NAinVA-edit-conditions4NOV.png "Edit conditions")

7.  Select **Apply** after you have edited the conditions or added a new condition set.

8.  Select the **External Content Connectors** link to create or configure additional search sources.

    **Note:** If you have any external search sources created on your instance, the external search sources are shown in the **Add search sources** drop-down list.

    The External Content Connectors application adds support for indexing content and metadata from documents in external repositories to make those documents searchable in AI Search applications. The External Content Connectors application ships with a default search source for each connector. Connector admins can link the default search source for a connector to a search profile as part of the connector creation process, or after the connector is created. For more information, see [Create a GitHub Enterprise Cloud external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-github-enterprise-cloud&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Connect an external content connector to a search profile](https://www.servicenow.com/docs/access?context=connect-external-content-connector-search-profile&version=australia&pubname=australia-platform-administration&ft:locale=en-US). For information about creating search sources and linking them to search profiles, see [Search sources in AI Search](https://www.servicenow.com/docs/access?context=search-sources-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

9.  Select the **Add search sources** drop-down list to select or deselect search sources and save them into the assistant search profile.

    -   An internal search source refers to all knowledge base search sources on the instance and all catalog search sources on the instance.
    -   An external search source refers to all external content search sources on an instance. Examples of external search sources include Microsoft SharePoint or Confluence. For a complete list of external search sources, see [Exploring External Content Connectors](https://www.servicenow.com/docs/access?context=exploring-ext-cont-connectors&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    Search sources that aren't a knowledge base, external content, or catalog won't be used for the LLM-generated responses, but they are used for query-based search results shown in the assistant. Tool tips are shown for non-LLM eligible search sources.

10. Select **Restore default search sources** if you want to revert to the default search sources of Now Assist Multi-Turn Catalog Ordering and Now Assist Q&amp;A.

    ![Select the Restore default search sources to revert to the default sources.](../image/NAinVA-search-sources-restore-default-122025.png "Restore default search sources")

11. Select **Manage search profile** if you have not yet configured AI Search for your portal or mobile app and want to start building the search configuration for your assistant from scratch, or edit advanced settings such as dictionaries, improvement rules, and stop words.

    A new browser tab opens with your assistant's search profile page from the AI Search Admin console page.

    You must first complete the build of your search profile in the AI Search Admin console, and then publish your profile for it to be saved. For more information, see [Configure and manage AI Search in search applications](https://www.servicenow.com/docs/access?context=ais-admin-console-setup-manage-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

    ![Review and publish profile in AI Search Admin console](../image/NAinVA-publish-profile.png "Publish profile in AI Search Admin console")

    When navigating back to your assistant admin configuration in Assistant Designer, refresh your browser page to reflect published updates from the AI Search Admin console. For more information about the AI Search Admin console, see [Using AI Search Admin console](https://www.servicenow.com/docs/access?context=using-ais-admin-console&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

    **Note:** If you rename an assistant, the assistant's search profile name is automatically renamed to match the latest assistant's name.

12. Select the ellipsis if you want to remove a search source or edit the conditions, and then save the change.

13. Select **Save and continue**.

    The assistant search profile needs to have at least one KB or external content search source in order to be saved.


## What to do next

See [Brand an assistant](brand-assistant.md).

