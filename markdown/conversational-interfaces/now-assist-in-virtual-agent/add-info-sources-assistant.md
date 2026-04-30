---
title: Add information sources to an assistant
description: Select the information that should be available to your assistant.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 8
breadcrumb: [Configuring Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Add information sources to an assistant

Select the information that should be available to your assistant.

## Before you begin

[Display your assistant on a portal or channel](display-assistant-portal-channel.md)

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Select a search source for your search configuration.

    **Note:** Search configuration isn't applicable to Now Assist panel assistant \(Developer\)

    ![View of the information sources.](../image/NAinVA-info-sources-052025.png "Information sources in the default search profile")

    In the Search configuration section, each assistant has its own search configuration. If you have configured AI Search on any existing portal or mobile app, you can copy the existing configuration to your assistant's search configuration or add an external search source. External sources such as Microsoft SharePoint or Confluence can be added for a seamless experience. For a complete list of external search sources, see [Exploring External Content Connectors](https://www.servicenow.com/docs/access?context=exploring-ext-cont-connectors&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    When a Now Assist in Virtual Agent assistant is created, a search profile for that assistant gets created. All search sources associated with the profile are listed. If the Virtual Agent Q&amp;A and the Virtual Agent Multi-Turn Catalog Ordering skills are turned on for the assistant, the default search profile contains the default knowledge articles and catalog items. Select the ellipsis to edit the conditions of each skill.

    If you have configured AI Search for your portal or mobile app, you have the option to **Copy existing configuration**.

    **Note:** Copying an existing configuration doesn't apply to Now Assist panel assistants \(Platform or Developer\).

    Copying an existing configuration imports an existing search configuration to the assistant's search profile and search configuration. Copying a configuration ensures that the portal and assistant have the same search configuration. After copying an existing search configuration, previous configurations for your portal will apply to your assistant's search profile.

    To change the search application, select **Copy existing configuration**.

    1.  Select a search application configuration from the drop-down list.

        The associated search profile is also shown.

        ![Drop-down list with search configurations.](../image/NAinVA-copy-config-052025.png "Select a search configuration to copy")

    2.  Select **Copy**.

        The latest configuration from the search application that was selected in the previous step, and the search sources, are shown.

        ![Edit conditions of search sources.](../image/NAinVA-info-sources-edit-conditions-052025.png "Edit conditions of each source")

        **Note:** If the enhanced chat experience is enabled for any display experience, all of the search sources are copied into the assistant search profile. Search sources, except Knowledge, external content, and catalog items, aren't used for the LLM-generated Virtual Agent responses. The search sources are used for the portal and mobile app's search results to ensure that Virtual Agent responses are seamless with the portal search and the mobile search.

    3.  Select the ellipsis to edit current conditions or add a new condition set, then select **Apply**.

        ![Table view for editing conditions.](../image/NAinVA-edit-conditions4NOV.png "Edit the conditions")

        If you have a Now Assist Multi-Turn Catalog Ordering section, the following conditions appear. To design a topic conversation in Virtual Agent, see Create a Virtual Agent topic.

        ![Table view for editing conditions.](../image/NAinVA-multiturn-conditionsNOV.png "Edit conditions")

    If you have not yet configured AI Search for your portal and want to add search sources to your assistant, or edit advanced settings such as dictionaries, improvement rules, and stop words, select the **Search sources** &gt; assistant name link. The AI Search Admin Console page appears for your assistant's search profile where you can build your search configuration from scratch.

    For example, in the AI Search Admin Search Console **Search Sources** tab, you could link catalog items, change requests, and so on, or add a new search profile to your Virtual Agent search profile. You must first complete the build of your search profile in the AI Search Admin Console, and then publish your profile for it to be saved. For more information, see [Configure and manage AI Search in search applications](https://www.servicenow.com/docs/access?context=ais-admin-console-setup-manage-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    ![Review and publish profile in AI Search Admin console](../image/NAinVA-publish-profile.png "Publish profile in AI Search Admin console")

    When navigating back to your Now Assist in Virtual Agent admin configuration, refresh your page to reflect the search profile that you created or updated in the AI Search Admin Console. Refreshing your page confirms that any changes that were made, and published, within the AI Search Admin console are reflected in your Now Assist in Virtual Agent admin configuration. For more information about the AI Search Admin Console, see [Using the AI Search Admin console](https://www.servicenow.com/docs/access?context=using-ais-admin-console&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    **Note:** If you rename an assistant, the assistant's search profile name is automatically renamed to match the latest assistant's name.

    If you have a Now Assist topics section, see [Create a Virtual Agent topic](../../virtual-agent/task/create-virtual-agent-topic.md) to create or conﬁgure more topics.

    ![Create or configure additional Now Assist topics.](../image/NAinVA-info-sources-NAtopicsNOV.png "Create or configure additional Now Assist topics")

    In **Virtual Agent Designer** &gt; **Basic Properties**, the topic needs to be assigned to the assistant. For more information, see [Create a topic form](../../virtual-agent/reference/vad-topic-creation-form.md).

    **Note:** For Now Assist panel assistants \(Platform and Developer\), contact support to assign Now Assist Topics to the assistants.

    If you have a Conversational subflows and actions section, the following appears.

    ![Create conversational subflows and actions.](../image/NAinVA-subflows-actionsNOV.png "Create conversational subflows and actions")

    Subflows and actions are created and configured in Workflow Studio. Navigate to **Workflow Studio** &gt; **Conversational Settings** to assign subflows and actions to the assistant.

    **Note:** Conversational subflows and actions aren't applicable to Now Assist panel assistant \(Developer\).

    If a custom skill was turned on, the Custom skills section appears. Create custom skills and make them available to the assistant in the Now Assist Skill Kit.

    ![Create custom skills.](../image/NAinVA-info-sources-custom-skills.png "Create custom skills")

    In **Now Assist Skill Kit** &gt; **Deployment Settings**, custom skills are to be assigned to the assistant. For more information, see [Configure skill deployment settings](https://www.servicenow.com/docs/access?context=configure-skill-settings&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

    If an AI agents skill was turned on, an AI agents section appears. Create and manage AI agents in Now Assist AI Agents Studio.

    ![Create and manage AI agent use cases.](../image/NAinVA-info-sources-agent2-052025.png "Create and manage AI agents")

    In **AI Agents Studio** &gt; **Select Display**, workflows are to be assigned to the assistant. For more information, see [Managing AI agents in Virtual Agent Designer](../../virtual-agent/concept/managing-use-cases-ai-agents.md) and [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

    Add other search sources that won't be used for the LLM Virtual Agent generated responses but will be used for the portal and mobile search results.

    ![Card with link to add search results for sources other than Knowledge and Catalog items.](../image/NAinVA-add-more-info-052025.png "Add other search sources")

    **Note:** Knowledge Graph applies to Now Assist in Virtual Agent assistants and not to Now Assist panel assistants \(Platform and Developer\).

    If Knowledge Graph is enabled, select **Manage Knowledge graphs** to configure the Knowledge Graph application, and then select a Knowledge Graph schema from the drop-down list to associate Knowledge Graph with an assistant.

    **Note:** To enable Knowledge Graph for Now Assist in Virtual Agent, set the **sn\_vad\_genai.knowledge\_graph.enabled** and **sn\_ais\_assist.enable\_knowledge\_graph\_nlq** system properties to `true`.

    For more information, see [Leverage Knowledge Graph prebuilt integration with Virtual Agent](https://www.servicenow.com/docs/access?context=example-use-case-for-knowledge-graph&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

    **Note:** Knowledge Graph transforms search into an intelligent, predictive, and efficient experience, reducing friction, increasing accuracy, and improving productivity. By default, search personalization is available with AI Search in the Now Assist in Virtual Agent assistant, and delivers personalized, context-aware search experiences powered by Knowledge Graph. To disable the integration with Knowledge Graph for personalization, open a ServiceNow support ticket.

    ![Drop-down list of Knowledge Graph schemas.](../image/NAinVA-knowledge-graphNOV.png "Select a Knowledge Graph schema")

    The **External Content Connectors** card appears if the Now Assist Q&amp;A skill is active for the assistant. The External Content Connectors application adds support for indexing content and metadata from documents in external repositories to make those documents searchable in AI Search applications. For a complete list of External Content Connectors, see . The Now Assist Q&amp;A skill must be turned on for the assistant to access knowledge articles and external content. Select **Go to External Content Connectors** to create and connect external sources. After creating a connector, create a search source and link it to a search profile. For information about creating search sources and linking them to search profiles, see [Search sources in AI Search](https://www.servicenow.com/docs/access?context=search-sources-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    ![Add an External Content Connector to create and connect external sources](../image/NAinVA-external-connectors2-052025.png "External Content Connectors")

    In the **Add external search sources** drop-down list, select or deselect them and save your external search sources into the assistant search profile.

    **Note:** If you have Now Assist Q&amp;A enabled but you don't have external search sources created on your instance, the external search sources drop-down list is grayed out.

    Select the ellipsis if you want to remove an external search source and then save the change. At least one Now Assist Q&amp;A search source must remain linked to the assistant if the Now Assist Q&amp;A skill is enabled.

    Now Assist Multi-Turn Catalog Ordering search sources don't have the removal option. If the Now Assist Multi-Turn Catalog Ordering skill is turned off in the Now Assist skills section of this admin guided setup, you won't have it as a search source.

    **Note:** If an external search source is already linked to an existing assistant, a warning message appears if you deselect Now Assist Q&amp;A in the Now Assist skills tab before saving the change.

    Now Assist Q&amp;A skill is a prerequisite for both Knowledge and external content. If you deactivate the Now Assist Q&amp;A skill, both Knowledge and external content are removed as search sources for this assistant. The **Add external search sources** drop-down list doesn't appear. If you reactivate Now Assist Q&amp;A, add external content search sources again.

2.  Select **Save and continue**.


## What to do next

[Brand an assistant](brand-assistant.md).

