---
title: Version control for AI agents and agentic workflows
description: Version control enables you to track changes made to instructions sent to the LLM for AI agents and agentic workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Now Assist AI agents, Enable AI experiences]
---

# Version control for AI agents and agentic workflows

Version control enables you to track changes made to instructions sent to the LLM for AI agents and agentic workflows.

## Version control overview

When creating an AI agent or agentic workflow, the **List of steps** field is important because it provides the context necessary for the large language model \(LLM\) to accomplish tasks. You can use version control to create multiple versions of the **List of steps** field in the guided setup. Tracking your changes with version control helps enable you to experiment and test new instructions. You can create versions, edit and refine versions, and revert to previous versions as needed.

![Version control modal from the guided setup of an AI agent with multiple versions showing](../image/version-modal.png "Version control modal")

## Creating versions

You can create a version by selecting **View versions** &gt; **New version** in the guided setup of an AI agent or agentic workflow. Doing so brings up the **Create a new version** modal where you can name the version and make changes. Naming your version enables you to identify what changes were made to make it easier to track.

You can choose to make the new version active immediately by selecting the **Set as active** toggle.

For more information about writing effective descriptions and instructions, see [General guidelines for creating AI agents and agentic workflows](gg-creating-aia.md).

When creating a new version, you also have the option to use Now Assist to refine your current **List of steps**. You must already have an active version for this option to be available. Selecting **View versions** &gt; **Refine version** brings up the modal where Now Assist generates and displays a new **List of steps** for you to review. You can change any of the generated text, or you can use it as it was generated. Select **Create** to use the new, refined version.

![Create a new version modal](../image/version-create.png "Create a new version modal")

## Changing between versions

When you have multiple versions of the same **List of steps** field, you can switch which one is active at any time. Choosing to make a new version active enables you to test it and evaluate its effectiveness.

If you’re updating an agentic workflow, you can [execute an agentic evaluation run](../task/execute-aia-eval.md) to measure performance.

You can decide which version is active by selecting **View versions** in the guided setup. Toggle the **Set as active** field and save your changes to make the new version active.

## Testing different versions

You can test different versions of an agentic workflow or AI agent from the AI Agent Studio **Testing** page. The **Version** selector dropdown displays both active and inactive versions with the currently active version marked as **\(Active\)**. You can also start evaluation runs for specific versions by selecting **Set up evaluation run**.

![Testing page in AI Agent Studio with a workflow and a version selected](../image/version-test.png "Version selector in the AI Agent Studio Testing page")

## Version logs

The AI Agent Studio **Activity** page enables you to track AI agent and agentic workflow executions by version. When in the guided setup, you can select **View version logs** in the **View all versions** modal. Choosing to view the version logs opens the **Activity** tab in a new window with the list filtered for the version you selected.

When viewing the **Activity** tab at any time, you can choose to filter by version. The more specific your version names, the easier it is to identify those changes in the list.

![Activity page of AI Agent Studio with the versions column highlighted](../image/ais-activity-versions.png "Example execution logs")

