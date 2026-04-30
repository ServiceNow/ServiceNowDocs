---
title: Virtual Agent Designer home page
description: The Virtual Agent Designer home page lists all conversational assets available in your instance, including subflows, actions, and topics.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-02-04"
reading_time_minutes: 5
keywords: [Virtual Agent, Designer, home page, topics, conversational assets, subflows, actions, LLM, NLU, Large langauge model, Natural Language Understanding]
breadcrumb: [Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent Designer home page

The Virtual Agent Designer home page lists all conversational assets available in your instance, including subflows, actions, and topics.

To navigate to Virtual Agent Designer, select **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

![Virtual Agent Designer Conversational Studio Topics page view with 4 highlighted sections. For more information, see the Filters and options in the topics page table.](../images/convo-studio-list-view.png "Topics page")

<table id="table_vng_lvj_hcc"><thead><tr><th>

Sections

</th><th>

Fields and descriptions

</th></tr></thead><tbody><tr><td>

1. Navigation header bar

</td><td>

Header bar for navigation and Virtual Agent Designer settings.-   Virtual Agent Designer tab: Select this tab to view the Virtual Agent Designer home page.
-   Topic tabs: Shows any open topics as navigation tabs. Hover over a tab to show its topic type and scope. Select a topic's tab to view that topic. Select the close icon ![Close icon.](../images/gray-x-icon.png) on a tab to close the topic.

**Note:** If you close a topic with unsaved changes, a warning window opens. Select **Cancel** or **Close without saving**.

If you open more tabs than your browser window can display, a drop-down tab holding the overflowing topics appears on the header bar. Select the drop-down tab followed by the topic that you want to view.

-   User preferences: Icon to access preferences and settings. Hover on the icon to see user name and roles. Select the icon to shows Virtual Agent Designer settings for the home page. Activate the **Group tabs by app scope** toggle in the settings window to group or ungroup tabs by their application scope.

**Note:** Each group of tabs has a random color when you group tabs by app scope.

For more information on changing the scope, see [Change the application scope in Virtual Agent Designer](../task/change-application-scope-vad.md).


</td></tr><tr><td>

2. Topic list controls

</td><td>

Controls for filtering, managing, testing, creating, and deleting Virtual Agent topics.-   **LLM** or **NLU/keyword** toggle switch: Use this switch to select between LLM or NLU/keyword discovery type topic lists.
-   LLM controls:
    -   **Select Assistant**: Drop-down menu to filter topics associated with a given LLM assistant.
    -   **Test Assistant**: Opens the testing window for the topics that are associated with the assistant you selected.

**Note:** If you have not filtered topics with **Select assistant**, the option **Test in Now Assist panel** appears in this drop-down menu. For more information on associating an LLM assistant with a topic, see [Create a Virtual Agent topic](../task/create-virtual-agent-topic.md).

    -   **All**: Button to view all LLM topics.
    -   **Topics**: Button to view only basic LLM topics.
    -   **Subflows**: Button to view only conversational subflows.
    -   **Actions**: Button to view only conversational actions.
    -   **Custom skills**: Button to view custom skills from Now Assist Skill Kit.
-   NLU controls:

○ **Test active topics**: Button to test all active NLU/keyword topics.

-   **Create**: Button to create a new Virtual Agent topic.
-   Search icon ![Search icon](../images/icon-search.png): Opens a field to enter a string to search for a match in the topic list. When you enter a string, the text is used as a condition in the Filter.
-   Filter icon ![Filter icon.](../images/filter-icon.png): Opens a menu to add filtering conditions that contain a field, operator, and value\(s\). If you define a condition or enter a string using the **Search** button, you can remove it by selecting the delete condition ![Delete condition icon.](../images/gray-x-icon.png) icon.
-   Refresh list icon ![Refresh icon.](../images/refresh-icon-updated.png): Refreshes the currently defined list of topics.
-   Edit columns icon![Edit columns icon.](../images/edit-columns-icon.png): Opens a menu to reorder or change the columns in the topic records list from their defaults.

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
-   **Description**: Short description entered when you create the topic. For more information, see [Create a Virtual Agent topic](../task/create-virtual-agent-topic.md)
-   **Promoted in**: Lists the assistants in which the asset is promoted.
-   Show actions for this row ![KB link](../images/kebab-menu.png): Icon to open a menu with the following options.

    -   **Promoted**: Option to toggle the topic's **Promoted** status. For more information, see [Promote or demote LLM topics in Virtual Agent Designer](../task/promote-demote-va-topics.md).
    -   **Discoverable**: Option to toggle the topic's **Discoverable** status.
    -   **Visible**: Option to toggle the topic's visibility to users.
    -   **Active**: Option to toggle the topic's **Active** status.
    -   **Delete**: Option to delete the topic. For more information, see [Delete a Virtual Agent topic](../task/delete-virtual-agent-topic.md).

**Note:** If you select **Delete**, a warning window opens. Select **Delete** to continue or **Cancel** to stop. For more information, see [Delete a Virtual Agent topic](../task/delete-virtual-agent-topic.md).

**Note:** If the topic is inactive and you try to promote it or make it discoverable or visible, you see a message reading `This asset must be active in order to be promoted, discoverable, or visible`. Toggle the topic to Active to perform those actions.


</td></tr><tr><td>

4. Side panel

</td><td>

Collapsible panel showing recently opened topics and helpful resources. Select the open or close panel icon ![Open panel icon.](../images/open-panel-icon.png)/![Close panel icon.](../images/close-panel-icon.png) to toggle the panel open or closed. -   Pick up where you left off: List of the last 3 topics you opened and when they were last updated. Select any from the list to open that topic.
-   Latest updates: List of the last 5 users to open a topic, along with the topic name and when it was last updated.
-   Resources: Links and features available for LLM or NLU topics. You can view localization insights, product documentation, and migrate NLU topics to LLM from here.

**Note:** The **Migrate topics to LLM** option appears in the Resources section only if you have activated Now Assist in Virtual Agent.

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent Designer interface reference](../concept/vad-reference.md)

