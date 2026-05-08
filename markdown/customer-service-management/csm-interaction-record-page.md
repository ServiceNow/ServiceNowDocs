---
title: CSM Interaction record page
description: The CSM Interaction record page provides CSM interaction management features and functionality and enables agents to accept and respond to live chats, calls, email and SMS messages.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Record pages, Record pages and page templates, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Interaction record page

The CSM Interaction record page provides CSM interaction management features and functionality and enables agents to accept and respond to live chats, calls, email and SMS messages.

The CSM Interaction record page provides the basic structure for an interaction record, including interaction information and related search results.

![The CSM Interaction record page provides agents with the active chat panel, interaction details, and the ability to look up and verify a contact or consumer.](../image/csm-Interaction-record-template.png "CSM Interaction record page")

The CSM Interaction record page is included with the CSM/FSM Configurable Workspace experience.

## Record presence feature

The CSM default record page and the CSM Interaction record page include the record presence feature. This feature allows agents to see other users who are viewing the same record and enables easy collaboration.

The user presence component displays an icon in the form header that shows the user who is currently viewing the record. For three or more users, the component displays two icons plus a number that represents additional users.

-   Hover over an icon to see more information about a user.
-   Click the number icon to see more information about the additional users.

For more information about this feature, see User presence.

## Thin compose modeless dialogs

[Thin compose modeless dialogs](csm-front-line-case-page-modeless-dialogs.md#section_nws_1rs_rfc) enable agents to initiate a work note or email from the activity stream in a modeless dialog.

**Note:** For the CSM Interaction record page, the thin compose modeless dialogs feature is hidden by default and can be enabled by the admin.

## Recommended Actions feature

The Recommended Actions tab is now available as the first tab in the contextual side panel and is enabled for Pro customers. It includes a set of base system recommendations, such as similar incidents and similar open incidents.

The Recommended Actions tab includes [AI search](ra-csm-ai-search.md) functionality and Suggested Actions for the chat, video, email, and walk-up channels on the CSM Interaction record page.

-   AI search tab: Agents can use AI search to find relevant resources or resolutions for customer issues. The search feature displays an initial set of search results based on the text in the interaction short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search. From the list of search results, agents can select a source to see search results of that type.

    For the Knowledge source type, agents can do the following:

    -   Share an article link in chat and email.
    -   Copy a link to an article.
    -   Read an article.
    -   Flag an article.
    -   Mark an article as helpful.
    For all the other source types, default guidance is supported. The default guidance for search results is a guidance that can be used for any search sources that don't have mapped guidances. For more information on default guidance, see [Default guidance for search results](ra-csm-guidances-default-guidance-search.md).

    For more information on how to avail the AI search feature in Recommended Actions, see [Enable AI search in Recommended Actions](../task/migrate-ra-agent-assist.md).

    For more information, see [Use AI search in Recommended Actions to resolve cases](../task/nba-use-ai-search.md).

    **Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

-   Suggested Actions tab: This tab displays relevant actions to agents based on a context of a record or recommend a value for a field. For more information on how to configure contexts so that relevant actions are displayed for the agents, see [Recommended Actions](configure-nba.md).

## Editable record header field

Agents can edit the short description of a record directly from the record header field. For more information, see [Editable record headers](../reference/csm-workspace-agent-actions.md#section_hhb_1tj_23c).

## Collaborate component

The Collaborate component enables agents to communicate with stakeholders and other users and gather information for case resolution. This component is available on the CSM default record page n the contextual side panel. For more information, see [Collaborate component](csm-config-ws-collaborate-component.md).

**Related topics**  


[CSM voice interaction record page](csm-native-voice-record-page.md)

