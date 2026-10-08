---
title: View your AI assets in the asset library \(Lux UI\)
description: Use the asset library to view and manage the AI assets in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-admin-center-lux-view-ai-assets.html
release: brazil
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 5
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Managing AI assets, Setting up AI capabilities and configurations, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# View your AI assets in the asset library \(Lux UI\)

Use the asset library to view and manage the AI assets in your instance.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to view and manage the AI assets on your instance. AI assets include agents, agentic workflows, skills, subflows, actions, intents, virtual assistants, and topics. They also include datasets, knowledge graphs, and catalog items.

**Note:** This topic describes the AI Admin Center feature based on the Lux user interface \(UI\). If you're using the Next Experience UI for AI Admin Center, see the Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **Asset library** \(\[Omitted image "icon-aiac-lux-nav-inventory.png"\] Alt text: Asset library icon.\) in the side navigation panel.

    The Asset library page opens showing tabs for the various asset types.

    \[Omitted image "ai-admin-center-lux-asset-library.png"\] Alt text: Asset library page showing tabs for asset types.

3.  Select the tab to view your AI assets for that type.

    Select **More** to view and select additional tabs.

    The asset library contains the following tabs.

    |Tab|Description|
    |---|-----------|
    |Overview|Displays the total number of each asset type and a full list of all assets in your instance. Select the **Recently created** or **New from ServiceNow** filters in the **Available assets** section to see new AI assets.|
    |Agents|Displays a list of all AI agents. An AI agent is an autonomous digital worker that uses LLMs, tools, and workflows to complete tasks on behalf of users. They can reason, plan, and act independently or collaboratively.|
    |Agentic workflows|Displays a list of all agentic workflows. An agentic workflow is a structured sequence of tasks executed by one or more AI agents with minimal human intervention to fulfill a business objective.|
    |Skills|Displays a list of all generative AI skills. A generative AI skill is a capability that uses generative AI to perform tasks such as generating summaries and resolution notes. You can have base system skills or custom skills created in AI Skill Kit.|
    |Intents|Displays a list of all intents. An intent is a data record that captures and defines what a user is trying to accomplish in a chat request. Intent records help the system classify, understand, and route user input appropriately.|
    |Virtual assistants|Displays a list of all virtual assistants. A virtual assistant is the container for the end-to-end administrative configuration for a chat or voice conversation.|
    |Subflows|Displays a list of all subflows. A subflow is an automated process that is part of a larger automated process. It consists of reusable actions and flow logic, data inputs, and outputs.|
    |Data assets|Displays a list of all datasets. A custom dataset and data collection in AI Data Kit is used for evaluations in AI Skill Kit.|
    |Actions|Displays a list of all actions. An action is a single step or task performed by an AI agent, a workflow, or a subflow.|
    |Topics|Displays a list of all topics. A conversational topic is used to structure back-and-forth conversations between the virtual agent and the end user.|
    |Catalog items|Displays a list of all catalog items. A catalog item is used to publish a service to users in the Service Catalog.|
    |Knowledge graphs|Displays a list of all knowledge graphs. A knowledge graph is a graphical representation of real-world entities \(tables\) and their relationships. It's used to add context and meaning to information to enable intelligent search, insights, and AI-driven experiences.|

4.  Select a combination of sort and filter options to refine the list.

    The filters vary depending on the asset tab selected.

    \[Omitted image "ai-admin-center-lux-asset-library-filters.png"\] Alt text: Filter options on the Asset library page.

    1.  Select a filter button.

    2.  Select an option from a filter menu.

    3.  Type in the search box and select the **Submit search** icon \(\[Omitted image "icon-now-assist-center-search.png"\] Alt text: Submit search icon.\) to filter by search criteria.

5.  Change the columns that appear in the list table.

    1.  Select the **Personalize columns** button \(\[Omitted image "icon-aiac-lux-personalize.png"\] Alt text: Personalize columns icon.\).

        The **Personalize columns** box opens.

        \[Omitted image "ai-admin-center-lux-asset-library-personalize.png"\] Alt text: Personalize columns box showing column options.

    2.  Customize the columns as needed.

        -   Select an option to add the column to your list. Clear an option to remove it.
        -   Drag one or more columns to a different location to change the order in which they appear in your list. Columns ordered from top to bottom in the panel appear from left to right in the list table.
        -   Select **Reset to default** to restore the column configuration before your changes.
    3.  Select **Apply**.

6.  In the **Overview** tab, use the **Available assets** section to find the new AI assets on your instance.

    -   Select the **Recently created** filter to see all AI assets you created in the last 30 days.
    -   Select the **New from ServiceNow** filter to see all base system assets provided by ServiceNow within the last 90 days.
7.  Select the asset name in the list to view the asset details.

    The asset details page opens in AI Admin Center if the selected asset is managed using an application that is fully integrated. If it is managed in another application, the application opens to the asset details page.


**Parent Topic:**[Managing AI assets in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-using-asset-inventory.md)

**Related topics**  


[View your AI assets in the asset inventory \(Next Experience UI\)]()

[Create an asset in the AI asset inventory \(Next Experience UI\)]()

[Create an asset in AI Admin Center \(Lux UI\)]()

[Create an intent in AI Admin Center \(Lux UI\)]()

[Edit an intent in AI Admin Center \(Lux UI\)]()

[Create a data asset in AI Admin Center \(Lux UI\)]()

