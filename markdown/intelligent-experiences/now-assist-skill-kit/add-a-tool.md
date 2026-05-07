---
title: Add a tool
description: Add and configure tools in the Now Assist Skill Kit tool canvas to gather data and context before a prompt runs. Tools can be chained sequentially, run in parallel, or branched conditionally using decision nodes.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-04-23"
reading_time_minutes: 5
keywords: [tool, tool node, decision node, Now Assist Skill Kit]
breadcrumb: [Create a prompt, Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Add a tool

Add and configure tools in the Now Assist Skill Kit tool canvas to gather data and context before a prompt runs. Tools can be chained sequentially, run in parallel, or branched conditionally using decision nodes.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

A tools are utilities that run before the skill prompt executes. They gather data, call services, or run scripts. Their outputs can be referenced in the prompt template as context. The input for a tool can be a skill input or the output of a previous tool in the canvas.

The **Add tools** tab displays a visual canvas showing the execution flow of your skill: from **Start**, through any tool and decision nodes you add, to the skill prompt, and then to **End**. You add nodes to the flow by selecting the **\(+\)** icon on a connector between existing nodes.

Two types of nodes are available:

-   **Tool Nodes**

    Tool nodes run a single tool such as a script, flow action, retriever, or web search. Tool nodes execute sequentially by default. When adding a tool node, you can select **Add as parallel node** to place it alongside an existing node at the same level in the flow, so both tools run simultaneously and their outputs are both available downstream.

-   **Decision nodes**

    Decision nodes route execution to one of several downstream tool nodes based on conditions. Branches are evaluated in order. The first fulfilled condition runs and the rest are skipped. A default branch runs if no conditions are met.


**Important:** Decision nodes require all destination tool nodes to already exist on the canvas. Create all tool nodes that the decision will route to before adding the decision node.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to add a tool to.

3.  Select the **2. Add tools** tab.

4.  Select the **\(+\)** icon on the connector where you want to insert a node.

    The **Add node** dialog opens. Select **Tool node** or **Decision node**. Decision node is only selectable after at least one tool node exists on the canvas.

5.  To add a tool node, select **Tool node** and then **Add**.

    1.  In the **Add tool** dialog, select a tool type from the **Tool type** dropdown.

        |Tool type|Description|
        |---------|-----------|
        |Flow Action|Runs a flow action from Workflow Studio as a tool.|
        |Retriever|Retrieves records or data from the platform to use as context in the prompt. See [Add a retriever](../task/add-retriever.md).|
        |Script|Runs a custom server-side script as a tool.|
        |Skill|Calls another published skill as a tool, enabling skill chaining.|
        |Sub Flow|Runs a subflow from Workflow Studio as a tool.|
        |Web Search|Searches the web and returns results to use as context in the prompt. See [Add a web search tool](../task/add-web-search.md).|
        |Predictive Intelligence|Uses a Predictive Intelligence solution to classify or predict values as part of the skill flow. See .|
        |Document Intelligence|Extracts structured data from documents as part of the skill flow. See .|

    2.  If you want this tool to run simultaneously with another tool at the same level in the flow, select **Add as parallel node**.

        When selected, the tool is placed alongside the next node in the flow rather than above it. Both tools run at the same time and their outputs are available to the next step downstream.

    3.  Select **Configure tool**.

    4.  Complete the five-step configuration wizard.

        |Step|Description|
        |----|-----------|
        |1. General info|Enter a name for the tool node. The description and resource fields have defaults based on the tool type selected.|
        |2. Tool inputs|Configure the inputs for the tool. The available fields depend on the tool type. Input values can be set as static values, references to skill inputs, or script-generated values.|
        |3. Tool outputs|Review the outputs the tool produces. Output names and types are fixed by the tool type and cannot be edited. Optionally, select **Truncate** to prevent an output from exceeding token limits. Avoid truncating outputs that are critical to the prompt.|
        |4. Tool conditions \(optional\)|Set conditions that determine whether the tool runs or is skipped during execution. Select **None \(Always run\)** to run the tool unconditionally, or define conditions using **Script** or **Filters**.|
        |5. Summary|Review the tool configuration before adding it to the canvas.|

    5.  Select **Add tool**.

6.  To add a decision node, select **Decision node** and then **Add**.

    **Important:** All tool nodes that the decision will route to must already exist on the canvas before you add the decision node. The **Destination node** dropdown only lists nodes already on the canvas.

    1.  Enter a **Name** for the decision node.

        The **Originating node** field is read-only and is automatically populated with the upstream tool node.

    2.  For each branch, enter a **Branch name** and select a **Destination node**.

    3.  Under **Branch conditions**, select **Filters** or **Script** and define the conditions that must be met for this branch to execute.

        Branches are evaluated in the order they appear. Once a branch condition is fulfilled, all subsequent branches are skipped. Use the arrow controls to reorder branches.

    4.  Select **Add branch** to add additional branches.

    5.  Select **Add**.

        The default branch executes if no other branch conditions are met.

7.  Select **Run tools** to test the tool flow.


## What to do next

After adding and testing your tools, configure the prompt to reference tool outputs using the **+ Inputs and tools** button in the prompt editor. To learn more, see [Create a prompt](../task/create-prompt-template.md).

**Parent Topic:**[Create a prompt](../task/create-prompt-template.md)

