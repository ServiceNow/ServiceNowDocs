---
title: View assistants
description: View and mange all existing chat and voice assistants on your instance.
locale: en-US
release: yokohama
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-09-10"
reading_time_minutes: 6
keywords: [Now Assist, Virtual Agent, LLM, Large language model]
breadcrumb: [Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# View assistants

View and mange all existing chat and voice assistants on your instance.

## Before you begin

See [Configuring assistants overview](configure-now-assist-va.md).

To view the **Assistants** tab in Assistant Designer, verify that the Now Assist for Platform plugin and/or the Now Assist for Creator plugin is installed. The plugins come with Now Assist products such as Now Assist for ITSM, Now Assist for CSM, and others.

**Note:**

-   With the Now Assist for Platform plugin, you can see all Now Assist in Virtual Agent and Now Assist panel assistants.
-   If you only have the Now Assist for Creator plugin installed, only the Now Assist panel - Developer assistant is shown.

|Assistant type|Activate|Deactivate|Edit|Test|Delete|
|--------------|--------|----------|----|----|------|
|Now Assist in Virtual Agent \(default\)|Yes|Yes|Yes|Yes|No|
|Now Assist panel - Platform \(default\)|Yes|Yes|Yes|Yes|No|
|Now Assist - Developer|Yes|Yes|Yes|Yes|No|
|Now Assist Voice Deployment|Yes|Yes|Yes|No|No|

Role required: virtual\_agent\_admin or admin

## About this task

By default, chat assistants and voice assistants are shown as cards. Voice assistants show a voice label and icon on the card. Voice assistants can only be edited. They can’t be tested in Assistant Designer at the moment.

![View chat and voice assistants in card view.](../image/NAinVA-card-view-122025.png "Assistant card view")

Assistants are shown in card view and in map view.

-   If an assistant's name or description is too long, it's truncated to fit the card view.
-   An assistant status shows as active \(in green\) or inactive \(in gray\).
-   Labels show in which display experiences the assistant is deployed, for example, HR portal.
-   Last updated shows the name of the person who created the assistant and the date that the assistant was created.
-   If a card shows **View** and not **Edit**, it means that you don't have the ability to edit the assistant because you only have access to assistants in specific domains.
-   A domain label is displayed on all assistant cards if any assistant has been created outside of the global domain. The label shows the domain that the assistant is in. If assistants are only created within the global domain, the label isn't shown.
    -   In any sub-domain \(e.g., Asia\), the assistants from that domain and the assistants from the global domain are shown on the card.
    -   Assistants created within a non-global domain can be edited, turned on, off, or deleted only within that domain and not from within the global domain.
    -   If you're in a specific domain while opening the edit flow of an assistant created in another domain:
        -   Activate/deactivate is inactive.
        -   Delete is inactive.
        -   Edit triggers the assistant edit flow, but all fields are read-only.
    -   Assistants from the global domain can be edited, activated, deactivated, or deleted as long as you're in the global domain. To switch domains, open a new browser tab and navigate to anywhere that has Unified Navigation and select the globe icon to switch domains. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US). If the domain plugin is installed, these options are available:
        -   **Domain scope: Default** determines the domain that you are in.
        -   **Application scope: Global** determines the store app pr plugin scope that you are in.
        -   **Update set: Default \[Global\]** determines where updates are made on the instance are saved.
    -   For more information on domain separation, see [Exploring domain separation](https://www.servicenow.com/docs/access?context=c_DomainSeparation&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) and [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Select the **View as cards** drop-down menu to toggle to the map view. The linkage between primary and secondary assistants is shown. For general information about primary and secondary assistants, see [LLM assistants](../concept/llm-assistants.md).

-   In the map view, primary assistants on the top row show secondary assistants that are linked to them.
-   Green indicates that the assistant is turned on. Gray indicates that the assistant is turned off.

The side panel shows where you left off, recent activity, and resources. The links that appear within the **Resources** section are hard-coded and can't be changed. If you select the **Manage model provider \(Now LLM\)** link, you will be redirected to Now Assist Admin console. For more information, see [Edit model providers](https://www.servicenow.com/docs/access?context=edit-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

To change the LLM provider for all assistants on the instance, select **Customize** &gt; **Edit provider for a skill group** &gt; **AI agents**.

![Select LLM provider from a drop-down list.](../image/NAinVA-LLM-provider.png "Change LLM provider for an assistant")

## Procedure

1.  To create a new chat or voice assistant, select **Create assistant**.

    The new assistant is a Now Assist in Virtual Agent assistant.

    ![Create a chat or voice assistant.](../image/NAinVA-create-assistant-122025.png "Create an assistant")

    The assistant creation flow launches where you can choose between a chat-based assistant or a voice-based assistant.

    ![Select a chat or voice assistant.](../image/NAinVA-select-assistant-122025.png "Select a chat or voice assistant")

    Follow the procedures to set up your chat assistant or voice assistant.

2.  To set up your chat assistant, see:

3.  1.  [Create a chat assistant](create-assistant.md).
2.  [Use agentic support for a chat assistant](use-agentic-support.md).
3.  [Assign search sources to a chat assistant](add-info-sources-assistant.md).
4.  [Add a Knowledge Graph schema to a chat assistant](add-kg-schema-assistant.md).
5.  [Add assets to a chat assistant](add-assets.md).
6.  [Display your chat assistant on a portal, channel, or mobile app](display-assistant-portal-channel.md).
7.  For Now Assist panel assistants, see [Display your assistant on Platform or ServiceNow Studio](display-nap-assistant.md).
8.  [Brand an assistant](brand-assistant.md).
9.  [Manage an assistant chat experience](manage-assistant-chat-experience.md).
10. [Enable additional chat features](additional-chat-features.md).
11. [Review chat assistant settings](review-assistant-settings.md).
12. [Test a chat assistant](test-assistant.md).
13. [Edit a chat assistant](edit-assistant.md).
4.  To set up your voice assistant, see [Create a voice assistant](configure-voice-assistants.md).

5.  Select the ellipsis to activate, deactivate, or delete an assistant.


## What to do next

For chat assistants, see [Create a chat assistant](create-assistant.md).

For voice assistants, see [Create a voice assistant](configure-voice-assistants.md).

