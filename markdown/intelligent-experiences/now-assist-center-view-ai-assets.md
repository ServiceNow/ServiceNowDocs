---
title: View your AI assets in the asset inventory
description: Use the asset library to view the AI assets in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-center-view-ai-assets.html
release: australia
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 4
keywords: [Now Assist, Now Assist Center, Gen AI, Generative AI]
breadcrumb: [Using the asset inventory, Use, Now Assist Center, Enable AI experiences]
---

# View your AI assets in the asset inventory

Use the asset library to view the AI assets in your instance.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to view the AI assets on your instance. AI assets include agents, agentic workflows, skills, subflows, actions, virtual assistants, and topics.They also include datasets, knowledge graphs, and catalog items.

For more information, see [Now Assist AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-assets-section.md).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Center** or **Workspaces** &gt; **Now Assist Center**.

2.  Select **Asset inventory** \(\[Omitted image "icon-now-assist-center-nav-assets.png"\] Alt text: Asset inventory icon.\) in the side navigation bar.

    The Asset inventory tab opens showing tabs for the various asset types.

    \[Omitted image "now-assist-center-asset-inventory-overview-2.png"\] Alt text: Asset inventory in Now Assist Center.

3.  Select the tab to view your AI assets for that type.

    Select **More** to view and select additional tabs.

    The asset inventory contains the following tabs.

<table id="table_v4m_pyd_53c"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

Displays the total number of each asset type and a full list of all assets in your instance.

 Select the **Recently created** or **New from ServiceNow** filters in the Discover assets section to see new AI assets.

</td></tr><tr><td>

Agents

</td><td>

Displays a list of all AI agents.

 An AI agent is an autonomous digital worker that uses LLMs, tools, and workflows to complete tasks on behalf of users. They can reason, plan, and act independently or collaboratively.

</td></tr><tr><td>

Agentic workflows

</td><td>

Displays a list of all agentic workflows.

 An agentic workflow is a structured sequence of tasks executed by one or more AI agents with minimal human intervention to fulfill a business objective.

</td></tr><tr><td>

Skills

</td><td>

Displays a list of all Now Assist skills.

 A Now Assist skill is a capability that uses generative AI to perform tasks such as generating summaries, resolution notes, and so on. You can have base system skills or custom skills created in Now Assist Skill Kit.

</td></tr><tr><td>

Subflows

</td><td>

Displays a list of all subflows.

 A subflow is an automated process that is part of a larger automated process. It consists of reusable actions and flow logic, data inputs, and outputs.

</td></tr><tr><td>

Actions

</td><td>

Displays a list of all actions.

 An action is a single step or task performed by a an AI agent, a workflow, or a subflow.

</td></tr><tr><td>

Virtual assistants

</td><td>

Displays a list of all virtual assistants.

 A virtual assistant is the container for the end-to-end administrative configuration for a chat or voice conversation.

</td></tr><tr><td>

Topics

</td><td>

Displays a list of all topics.

 A conversational topic is used to structure back-and-forth conversations between the virtual agent and the end user.

</td></tr><tr><td>

Data assets

</td><td>

Displays a list of all datasets.

 A custom dataset and data collection in Now Assist Data Kit is used for evaluations in Now Assist Skill Kit.

</td></tr><tr><td>

Catalog items

</td><td>

Displays a list of all catalog items.

 A catalog item is used to publish a service to users in the Service Catalog.

</td></tr><tr><td>

Knowledge graphs

</td><td>

Displays a list of all knowledge graphs.

 A knowledge graph is a graphical representation of real-world entities \(tables\) and their relationships. It is used add context and meaning to information to enable intelligent search, insights, and AI-driven experiences.

</td></tr></tbody>
</table>4.  Select a combination of sort and filter options to refine the list.

    The filters vary depending on the asset tab selected.

    \[Omitted image "now-assist-center-asset-inventory-filters.png"\] Alt text: Filter and sorting controls for the asset list.

    -   Select the **Sort by** button \(\[Omitted image "icon-now-assist-center-sort.png"\] Alt text: Sort by icon.\) and select a sorting order.
    -   Select a filter button.
    -   Select an option from a filter menu.
    -   Type in the search box and select the **Submit search** icon \(\[Omitted image "icon-now-assist-center-search.png"\] Alt text: Submit search icon.\) to filter by search criteria.
5.  Change the columns that appear in the list table.

    1.  Select the **Personalize columns** button \(\[Omitted image "icon-now-assist-center-personalize.png"\] Alt text: Personalize columns button.\).

        The **Select columns to display** box opens.

        \[Omitted image "now-assist-center-asset-inventory-select-columns.png"\] Alt text: Select columns to display box with options for adding, removing, and reordering table columns.

    2.  Customize the columns as needed.

        -   Select an option in the **Available columns** panel to add the column to your list. Deselect an option to remove it.
        -   Select the **Remove items** icon \(\[Omitted image "icon-now-assist-center-remove.png"\] Alt text: Remove items icon.\) on an item in the **Selected columns** panel to remove it from your list.
        -   Drag one or more columns to a different location in the **Selected columns** panel to change the order in which they appear in your list.

            Columns ordered from top to bottom in the panel appear from left to right in the list table.

        -   Select **Reset to defaults** to restore the column configuration before your changes.
    3.  Select **Apply**.

6.  In the Overview tab, use theAvailable assets section to find the new AI assets on your instance.

    -   Select the **Recently created** filter to see all AI assets you created in the last 30 days.
    -   Select the **New from ServiceNow** filter to see all base system assets provided by ServiceNow within the last 90 days.
7.  Select the asset name in the list to view the asset details.

    The asset details page may open on a separate workspace tab if the selected asset is managed using an application that is fully integrated in Now Assist Center. If it is managed in another application, the application opens to the asset details page.


**Parent Topic:**[Using the asset inventory in Now Assist Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-center-using-asset-inventory.md)

**Related topics**  


[Create an AI asset in the asset inventory]()

