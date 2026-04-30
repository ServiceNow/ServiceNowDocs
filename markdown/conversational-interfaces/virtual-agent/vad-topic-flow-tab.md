---
title: Topic Flow tab
description: Use the topic Flow tab to build the conversation flow. Use the controls for user inputs, bot responses, and utilities to define the flow.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 11
keywords: [Virtual Agent, Designer, Flow tab, Components, Variables, table view, canvas view]
breadcrumb: [Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Topic Flow tab

Use the topic **Flow** tab to build the conversation flow. Use the controls for user inputs, bot responses, and utilities to define the flow.

## Flow tab \(default view\)

![View of Virtual Agent Designer topic Flow tab with 10 callouts highlighted. For the text description, see the table that follows.](../images/DesignerTextNodeCalloutSections-2.png "Example Flow tab in default view") ![View of Virtual Agent Designer topic Flow tab with 10 callouts highlighted. For the text description, see the table that follows.](../images/DesignerTextNodeCalloutSections-2a.png "Example Flow tab in default view")

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](vad-prev-topics-page.md).

<table id="table_njp_rgk_zhb"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Navigation bar

</td><td>

Tabs to navigate between your design and the home pageAsset library. You can open and navigate between multiple topics and the home pageAsset library by selecting **Virtual Agent Designer** or an open topic's tab. Select the close icon ![](../images/delete-icon.png) on a tab to close that topic.

</td></tr><tr><td>

2. Topic header bar

</td><td>

Tabs and design options for your topic: -   Tabs: Each tab provides a different view for working on your conversation.
    -   **Flow**: Displays the canvas for building your conversation flow.
    -   [Topic NLU Intent tab](vad-topic-nlu-intent-tab.md) \(NLU topics only\)
    -   [Topic Properties tab](vad-topic-properties-tab.md)
    -   [Topic Languages tab](vad-topic-languages-tab.md) \(available if multiple languages are configured for Virtual Agent\).

For more information, see [Localizing Virtual Agent conversations](../concept/localize-va-topic.md).

-   **Table View**: Option that displays a table view of the nodes in the conversation flow. You can use this option to switch between table view and diagram view as you design your conversation.
-   **Active/Inactive**: Option that changes the design state so that it's active \(available to users\) or inactive \(in development and not available to users\). Select it to see the following options:
    -   **Included in Topic Discovery**: Option to make the topic discoverable via keywords, NLU, or Now LLM Service. If inactive, the topic is included when performing search fallback.
    -   **Included in List of Topics**: Option to make the topic visible under the “show me everything” list of topics.
-   **Save**: Saves the current design.
-   **Test**: Opens the design in a chat test window so that you can preview and test the conversation. If the Now Assist panel, Microsoft Teams application, or Slack application is configured for your environment, preview options for those channels are displayed in the Test button list. Select **Preview in Now Assist panel** or **Preview in Microsoft Teams** in the list to test your topic in those environments.
-   **Publish**: Activates the design and makes it available to the chat clients. If you're using language-specific NLU models, select **Review and publish** from the Publish list to specify languages.
-   More actions on topics icon ![More actions icon.](../images/kebab-menu.png)
    -   **Duplicate**: Copy the current design to create an unpublished version of the design.
    -   **Delete**: Remove the current and published version of the design.

When updating designs, the header bar displays an `Unpublished Changes` message until you publish the topic.Hover over the message to see a tooltip explaining the unpublished changes. For example, the changes can include your topic's main design or Natural Language Understanding \(NLU\) language mappings.![Flow tab header bar showing Unpublished changes warning message. A tooltip detailing unpublished changes appears when you hover over the message.](../images/vad-flow-tab-unpublished-changes-tooltip.png)

If you close the topic without saving, a **Recover changes** button appears on the header bar. Select this button to recover any unpublished changes that were unsaved before closing. The **Recover changes** button is replaced by the `Unpublished changes` message.![Flow tab header bar showing Recover changes button after reopening an unsaved topic.](../images/vad-flow-tab-recover-changes-button.png)

If you add a node, then close the topic before saving or publishing, the node disappears and the button and message appear when you reopen the topic. Select **Recover changes** to restore the node and remove the button.![Flow tab header bar showing Unpublished changes message and Recover changes button. Both appear after reopening an unsaved topic with a node added.](../images/vad-flow-tab-unpublished-recover-combined.png)

</td></tr><tr><td>

3. Palette

</td><td>

Collapsible sidebar with Components and Variables tabs.The Components tab shows a list of controls that you can drag onto the canvas to build a conversation. The following types of controls are available:

-   [User Input](va-user-inputs.md): Controls used to prompt and capture information from the user in a conversation. When Now Assist is enabled and you're working with a large language model \(LLM\) topic, the LLM User Input section indicates which controls are LLM compatible.
-   [Bot Response](va-bot-responses.md): Controls for showing virtual agent responses in a conversation.
-   [Utilities](va-utilities.md): Controls for performing actions within a topic, such as running a script, adding different conversation paths \(branches\) in a topic, or adding topic blocks.

The Variables tab includes inputs and scripts.![Variables tab showing Input and Scripts in topic being viewed.](../images/variables-tab.png)

-   **Input section**
    -   Live Agent variables specified on the topic **Properties** tab to provide contextual information from the virtual agent session to the live agent.
    -   Input variables defined by User Input controls and Utilities that are added to the flow on the canvas.
    -   "Nodeless" NLU entities added by the topic author that are used as slot-filled input variables for the topic.
-   **Script section**

The Script section includes the scripts found in nodes on the canvas. The topic author can add further script variables to store values outside of control variables. Scripting variables enable more complex scripting scenarios.


</td></tr><tr><td>

4. Canvas

</td><td>

Area that displays the conversation flow graphically. As you drag a control onto the canvas, that control becomes a node in the conversation flow. Includes a related property sheet that opens in the right pane. Each flow has a **Start** and **End** node. When you add or remove controls, the layout of controls on the canvas is adjusted automatically.

</td></tr><tr><td>

5. Node search

</td><td>

Option for quickly finding specific nodes in the conversation flow. Select the node search icon ![Search icon.](../images/icon-search.png) to expand the search field and enter the name of the node that you want to find. When a matching node is found, the node is highlighted in the flow. Use the left or right arrows to search for the previous or next node that matches the search node name. ![Node search, showing highlighted node in flow and highlighted search bar.](../images/expanded-node-search.png "Node search showing highlighted node")

</td></tr><tr><td>

6. Issues warning

</td><td>

Counter showing number of issues needing correction before the topic can be published. For more information, see the Incomplete property warnings section of this documents.

</td></tr><tr><td>

7. Node

</td><td>

Input or output item on the canvas created by dragging a control from the Components or Variables sidebar. All controls in the conversation are represented as individual nodes on the canvas. If a node is incomplete, a counter showing the number of issues in the node appears. For more information, see the Incomplete property warnings section of this documents.

</td></tr><tr><td>

8. Property sheet

</td><td>

Properties specific to the selected node on the canvas. The list of properties changes based on the node you select. Each node has its own set of properties that you can define, which can include scripts that control the behavior or processing that is performed in the node. If NLU is enabled, the property sheets for Input controls contain additional NLU fields. For further information, see [Virtual Agent Designer controls](../concept/virtual-agent-controls.md)

</td></tr><tr><td>

9. Data pill picker

</td><td>

A tool for selecting data pills from input variables or script variables to use in the property field. Select the data pill picker to select from the existing variables accessible in the topic. You can also drag data pills directly into property fields.

</td></tr><tr><td>

10. Script editor

</td><td>

A tool for adding or editing JavaScript scripts used in a property. Provides scripting assistance, including a list of valid elements at the insertion point. Elements include function name, object names, and variable names available for the topic. For more information, see the [JavaScript syntax editor](https://www.servicenow.com/docs/access?context=c_SyntaxEditor&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td></tr><tr><td>

11. Property sheet tab

</td><td>

Opens the property sheet view for the currently selected node on the canvas.

</td></tr><tr><td>

12. Validation Issues tab

</td><td>

Opens the Validation Issues view, showing the number of issues in the topic needing correction before the topic can be published. This tab appears when you try to publish an incomplete topic, and disappears when all issues are resolved. For more information, see [Publish a Virtual Agent topic](../task/publish-virtual-agent-topic.md).

</td></tr><tr><td>

13. Resources tab

</td><td>

Opens the Helpful resources view, containing a link to product documentation. In an LLM topic, further resources appear including Guided tours on the canvas, and links to videos for LLM controls.![Helpful resources tab in an LLM topic, showing guided tour, video, and product documentation links.](../images/vad-llm-resources-tab.png)

</td></tr></tbody>
</table>## Flow tab with Table View enabled

Most of the functionality of the Flow tab is the same in Table View. The following figure and table highlight the differences.

![Table view of Virtual Agent Designer Flow tab with variables, search table, and Table toggle highlighted. For the text description, see the table that follows.](../images/DesignerTableviewCallouts-2a.png "Example Flow tab in Table View")

<table id="table_tkl_txp_ckb"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Palette: Variables sidebar

</td><td>

The Components tab is not shown. Only the Variables sidebar is visible.

</td></tr><tr><td>

Table view

</td><td>

A list of table rows, where each row corresponds to a node in the conversation flow. You can add nodes in this section. When you add or remove nodes, the table rows adjust automatically. A node can be any of the following controls, aside from the **Start** and **End** nodes:-   **User Input**: Controls used to prompt and capture information from the user in a conversation.
-   **Bot Response**: Controls for displaying virtual agent responses in a conversation.
-   **Utilities**: Controls for performing actions within a topic, such as running a script, adding different conversation paths \(branches\) in a topic, or adding topic blocks.

Select **Add new node** to add a node. You can specify the type of control in the dialog box.

</td></tr><tr><td>

Search table

</td><td>

Option for searching nodes in the conversation \(table\).

</td></tr></tbody>
</table>## LLM components guided tour

When you create or open a non-read-only LLM topic, a dialog box appears and displays an option to take a guided tour of the LLM components in Virtual Agent Designer. Select the close icon to close the window or **Start guided tour** to be shown the various components. You can also take a tour by selecting **Guided tour for LLM enabled nodes** in the Helpful resources tab.

To stop seeing the dialog box open each time you open an LLM topic, select **Do not show this again** before closing the dialog box or starting the tour. To restore the dialog box, navigate to **All**, then enter `sys_cb_user_preference_list.do`. On the Designer User Preferences page, find the **LLM\_INTRO\_MODAL\_ENABLED** preference. Open its **Value** field and set it to `true`.

![Introducing LLM components dialog box with the Do not show this again and Start guided tour options.](../images/vad-llm-intro-popup.png "LLM guided tour dialog box")

## Incomplete property warnings

Controls on the canvas have required properties. If required properties are missing, Virtual Agent Designer displays the total number of missing required properties and the controls that are missing them. All incomplete warnings must be addressed to test or publish the topic.

In the following example, the topic is missing two required properties. Two nodes are affected, and each is missing one property. The Text response node is missing the Message response.

![Virtual Agent Designer Flow tab view with incomplete properties. Number of incomplete nodes is shown in the canvas. The sidebar and each node show the number of incomplete entries.](../images/vad-flow-tab-missing-properties-warnings.png "Flow tab with incomplete properties")

Point to the incomplete message to see a tooltip that describes what is missing.

![Virtual Agent Designer properties, with incomplete message selected to show missing items in the node.](../images/vad-flow-tab-missing-properties-tooltip.png "Select the message to get more information")

**Parent Topic:**[Virtual Agent Designer interface reference](../concept/vad-reference.md)

