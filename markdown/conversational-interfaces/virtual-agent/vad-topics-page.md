---
title: Assistant Designer Asset library
description: The Assistant Designer Asset library lists all LLM assets and NLU/Keyword topics available in your instance. You can also create more topics, subflows, actions, custom skills, AI agents, and agentic workflows.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
keywords: [Virtual Agent, Designer, home page, topics, conversational assets, subflows, actions, LLM, NLU, Large langauge model, Natural Language Understanding]
breadcrumb: [Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Assistant Designer Asset library

The Assistant Designer Asset library lists all LLM assets and NLU/Keyword topics available in your instance. You can also create more topics, subflows, actions, custom skills, AI agents, and agentic workflows.

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](vad-prev-topics-page.md).

To navigate to Virtual Agent Designer, select **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

![Assistant Designer Asset library page view with 4 highlighted sections. For more information, see the Options in the Asset library table.](../images/convo-studio-list-view-2.png "Topics page")

<table id="table_vng_lvj_hcc"><thead><tr><th>

Sections

</th><th>

Fields and descriptions

</th></tr></thead><tbody><tr><td>

1. Navigation header bar

</td><td>

Header bar for navigation and Virtual Agent Designer settings.-   **Assistant Designer** tab: Select this tab while viewing a topic in the Virtual Agent Designer canvas to return to the Assistant Designer Asset library page
-   Topic tabs: Shows any open topics as navigation tabs. Hover over a tab to show its topic type and scope. Select a topic's tab to view that topic. Select the close icon ![](../images/gray-x-icon.png) on a tab to close the topic.

**Note:** If you close a topic with unsaved changes, a warning window opens. Select **Cancel** or **Close without saving**.

If you open more tabs than your browser window can display, a drop-down tab holding the overflowing topics appears on the header bar. Select the drop-down tab followed by the topic that you want to view.

-   User preferences: Icon to access preferences and settings. Hover on the icon to see user name and roles. Select the icon to shows Virtual Agent Designer settings for the home page. Toggle **Group tabs by app scope** in the settings window to group or ungroup tabs by their application scope.

**Note:** Each group of tabs has a random color when you group tabs by app scope.

For more information on changing the scope, see [Change the application scope for Virtual Agent Designer topics](../task/change-application-scope-vad.md).


</td></tr><tr><td>

2. Topic list controls

</td><td>

Controls for filtering, managing, testing, creating, and deleting Virtual Agent topics.-   **LLM** or **NLU/keyword** toggle switch: Use this switch to select between LLM or NLU/keyword discovery type topic lists.
    -   LLM controls:
        -   **Select Assistant**: Drop-down menu to filter topics associated with a given LLM assistant.

**Note:** Hover over the tooltip icon \(![](../images/i-tooltip.png)\) to see information about the assistant you have selected from the drop-down menu.

        -   **Test Assistant**: Opens the testing window for the topics that are associated with the assistant you selected.

You can use three testing options: Standard Chat, Enhanced Chat, or Integrated chat.  If you configured either Enhanced Chat or Integrated Chat for your instance, you can use that test option.  If you configured both Enhanced and Integrated chat, you can choose between the two.  If you configured Standard Chat, you can choose from all three options.

**Note:** If you have not filtered topics with **Select assistant**, the option **Test in Now Assist panel** appears in this drop-down menu. For more information on associating an LLM assistant with a topic, see [Create a Virtual Agent topic](../task/create-virtual-agent-topic.md).

        -   **All assets**: Button to view all LLM topics.
        -   **Topics**: Button to view only basic LLM topics.
        -   **Subflows**: Button to view only conversational subflows.
        -   **Actions**: Button to view only conversational actions.
        -   **Custom skills**: Button to view custom skills from Now Assist Skill Kit.
    -   **AI agents**: Button to view list of AI agents. For more information, see [Explore Now Assist AI agents](https://www.servicenow.com/docs/access?context=exploring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
    -   **Agentic workflows**: Button to view list of Agentic workflows. For more information, see [Now Assist agentic workflows](https://www.servicenow.com/docs/access?context=sn-aia-use-cases-list&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
    -   NLU controls:

○ **Test active topics**: Button to test all active NLU/keyword topics.

-   **Create Asset**: Button to create a new Virtual Agent topic. For more information, see [Create a Virtual Agent topic](../task/create-virtual-agent-topic.md).
-   Search icon ![](../images/icon-search.png): Opens a field to enter a string to search for a match in the topic list. When you enter a string, the text is used as a condition in the Filter.
-   Filter icon ![](../images/filter-icon.png): Opens a menu to add filtering conditions that contain a field, operator, and value\(s\). If you define a condition or enter a string using the **Search** button, you can remove it by selecting the delete condition ![](../images/gray-x-icon.png) icon.
-   Refresh list icon ![](../images/refresh-icon-updated.png): Refreshes the currently defined list of topics.
-   Edit columns icon![](../images/edit-columns-icon.png): Opens a menu to reorder or change the columns in the topic records list from their defaults.

</td></tr><tr><td>

3. Topic records list

</td><td>

List of all topics available, filtered by topic list controls. Default columns include the following.-   **Name**: Name given to the topic when created.
-   **Type**: Indicates the topic types.
    -   Topic
    -   Topic block
    -   Small talk
    -   Custom input
    -   Custom output
    -   Action
    -   Subflow
-   **Status**: Indicates the status of the topic:
    -   Draft
    -   Published
    -   Modified
-   **Active**: Indicates whether the topic is **Active** or **Inactive**.
-   **Last modified**: Time and date when the topic was last modified.
-   **Description**: Short description entered when you create the topic. For more information, see [Create a Virtual Agent topic](../task/create-virtual-agent-topic.md).
-   **Promoted in**: Lists the assistants in which the asset is promoted.
-   Show actions for this row ![](../images/kebab-menu.png): Icon to open a menu with the following options.

    -   **Promoted**: Option to toggle the topic's **Promoted** status. For more information, see [Promote or demote LLM conversational subflows, actions, and topics in Virtual Agent Designer](../task/promote-demote-va-topics.md).
    -   **Discoverable**: Option to toggle the topic's **Discoverable** status.
    -   **Visible**: Option to toggle the topic's visibility to users.
    -   **Active**: Option to toggle the topic's **Active** status.
    -   **Conversational Settings**: Option to open a window with information on the asset.

        -   **Name**: Name of the asset.
        -   **Asset type**: Type of the asset.
        -   **Link to asset**: Option to open a tab for the asset in Virtual Agent Asset library.
        -   **Description**: Asset description used for topic discovery. This description is also shown in the asset's **Properties** tab and its **Description** value on the assets table on the Assistant Designer Asset library page.
This option appears if you have selected **LLM** on the **LLM and NLU/Keyword** toggle switch.

For more information, see [Conversational settings for Assets in the Asset library](../concept/asset-lib-conv-settings.md).

    -   **Remove from assistant**: Option to remove asset from an LLM assistant. You must first select an assistant from the **Select assistant** drop-down menu to filter assets. This option appears if you have selected **LLM** on the **LLM and NLU/Keyword** toggle switch.
    -   **Delete**: Option to delete the topic.

**Note:** If you select **Delete**, a dialog box opens. Select **Delete** to continue or **Cancel** to stop.

A check mark appears next to any menu option when it is activated.

**Note:** If the topic is inactive and you try to promote it or make it discoverable or visible, you see a message reading `This asset must be active in order to be promoted, discoverable, or visible`. Set the topic to **Active** under the Show actions for this row ![](../images/kebab-menu.png) to perform those actions.


</td></tr><tr><td>

4. Side panel

</td><td>

Collapsible panel showing recently opened topics and helpful resources. Select the open or close panel icon ![](../images/open-panel-icon.png)/![](../images/close-panel-icon.png) to toggle the panel open or closed. -   Pick up where you left off: List of the last 3 topics you opened and when they were last updated. Select any from the list to open that topic.
-   Latest updates: List of the last 5 users to open a topic, along with the topic name and when it was last updated.
-   Resources: Links and features available for LLM or NLU topics. You can view localization insights, product documentation, and migrate NLU topics to LLM from here.

**Note:** The **Migrate topics to LLM** option appears in the Resources section only if you have activated Now Assist in Virtual Agent.

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent Designer interface reference](../concept/vad-reference.md)

