---
title: Now Assist for Hardware Asset Management \(HAM\) AI agent collection Help repair hardware assets agentic workflow
description: Use the Help repair hardware assets agentic workflow, driven by AI agents, to handle the repair requests of defective and out-of-warranty hardware assets automatically. These AI agents validate the repair tasks, provide detailed troubleshooting and repair steps, and finally close the relevant tasks after receiving user confirmation.
locale: en-US
release: australia
product: Now Assist for Hardware Asset Management
classification: now-assist-for-hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [AI Agents, agentic AI]
breadcrumb: [Use agentic workflows, Now Assist for Hardware Asset Management \(HAM\), Hardware Asset Management, IT Asset Management]
---

# Now Assist for Hardware Asset Management \(HAM\) AI agent collection Help repair hardware assets agentic workflow

Use the Help repair hardware assets agentic workflow, driven by AI agents, to handle the repair requests of defective and out-of-warranty hardware assets automatically. These AI agents validate the repair tasks, provide detailed troubleshooting and repair steps, and finally close the relevant tasks after receiving user confirmation.

## Help repair hardware assets agentic workflow overview

**Important:** This agentic workflow is turned on by default. For more information, see Now Assist skills, agents, and agentic workflows on by default.

The AI agents in the Help repair hardware assets agentic workflow offers these benefits:

-   AI-guided troubleshooting and repair steps help improve accuracy and consistency
-   End-to-end task automation helps reduce delays in resolving hardware issues

-   **Prerequisites to use the Help repair hardware assets agentic workflow**
    -   Your organization must have an IT asset management system integrated with AI-driven repair workflows.
    -   AI agents must have access to repair order records and the web.
    -   Repair task numbers are required to initiate requests.
    -   Users must have the inventory\_user role.
-   **Actors in the Help repair hardware assets agentic workflow**
    -   Asset manager: Reports hardware issues by submitting repair requests.
    -   Inventory user: Works on assigned troubleshooting and repair tasks.
    -   AI agents: Provide detailed troubleshooting and repair steps through web-based search and complete the relevant tasks.
-   **Stages in the agentic workflow**

    The repair of defective or out-of-warranty hardware assets through the agentic workflow includes the following stages:

    1.  Repair order creation by an Asset manager
        1.  Initiates the repair process for defective or out-of-warranty hardware assets in the stockroom by creating a repair order.
        2.  Adds one or more repair order lines to the repair order, depending on the number of assets that must be fixed, and saves the repair order.

            Result: A Troubleshoot task is created for each repair order line.

        3.  Assigns a technician for the troubleshooting task, automatically triggering the Help repair hardware assets agentic workflow.

            **Note:** The assigned technician with the inventory\_user role can log in and view the active conversation with the AI agents in the Now Assist panel in the Hardware Asset Workspace by selecting the sparkle icon ![](../../../common/image/icon-ai-sparkle.png).

            To access the Now Assist panel after it has been activated, you should have the now\_assist\_panel\_user role.

    2.  Repair order task validation by the AI agent
        1.  The Asset next best action AI agent retrieves the task details and validates them.
        2.  Based on the validation result, one of the following events occurs:
            -   If the task number is invalid or the task isn't active, the agentic workflow ends.
            -   If the task is valid, the AI agent checks whether it's a troubleshooting task, or a repair task and triggers the appropriate AI agent to handle it.
    3.  Processing of tasks by AI agents
        -   **Handling of the troubleshooting task by the Evaluate asset AI agent**

            The Evaluate asset AI agent manages the troubleshooting task as follows:

            1.  Searches the web to find a detailed evaluation guide that matches the model and manufacturer of the asset.

                If the model or manufacturer details aren't present on the asset record, the agentic workflow stops.

                **Important:** Web searches using third-party large language models \(LLMs\) like Gemini won't be supported for Federal customers.

            2.  Displays the evaluation guide in the Now Assist panel, to help the technician to identify the issue with the asset.
            3.  Checks with the technician to confirm whether the troubleshooting steps were helpful.
                -   If the technician confirms that the troubleshooting steps helped, the AI agent performs these steps:
                    1.  Asks the technician to confirm the troubleshoot result \(**Repairable**, **Unrepairable**, or **Redeployable**\) and provide the issue details.
                    2.  Updates the task with the details provided by the technician and closes the task.
                -   If the technician confirms that the troubleshooting steps didn't help, the AI agent performs these steps:
                    1.  Requests more details about the issue to refine the web search.
                    2.  Searches the web again to find a detailed evaluation guide that matches with the details provided.
                    3.  Displays the evaluation guide in the Now Assist panel, to assist the technician in identifying the issue.
                    4.  Checks with the technician to confirm whether the new troubleshooting steps were helpful.
                        -   If the technician confirms that the new troubleshooting steps were helpful, the AI agent updates the task with the troubleshooting result and the issue details provided by the technician, and then closes the task.
                        -   If the technician confirms that the new troubleshooting steps weren't helpful, the agentic workflow stops.
            When a troubleshoot asset task is marked as Repairable and closed, the following events occur:

            1.  A repair task is automatically generated and assigned to the technician who handled the troubleshoot task. This action also initiates the Help repair hardware assets agentic workflow.
            2.  The Asset next best action AI agent fetches the details of the repair task and performs a validation check.
            3.  Depending on the validation result, one of these events occurs:
                -   If the task number is invalid or the task isn't active, the agentic workflow ends.
                -   If the task is valid, the AI agent confirms the task type and triggers the Repair asset AI agent to manage the repair process.
        -   **Handling of the repair task by the Repair asset AI agent**

            The Repair asset AI agent checks if the issue is identified and present on the repair task.

            -   If the issue is present on the repair task, the AI agent performs the following actions:
                1.  Searches the web to find detailed repair steps to resolve the issue identified on the asset.

                    **Note:** If the model or manufacturer details aren't present on the asset record, the agentic workflow stops.

                2.  Displays the repair instructions in the Now Assist panel, to help the technician to fix the asset issue.
                3.  Checks with the technician to confirm whether the repair steps were helpful.
                    -   If the technician confirms that the repair steps were helpful, the AI agent performs these steps:
                        1.  Asks the technician to confirm the repair result \(**Repaired**, **Unrepairable**, or **Redeployable**\) and provide the issue details.
                        2.  Updates the repair task with the repair result and the issue details provided by the technician, and closes the task.
                    -   If the technician confirms that the repair steps weren't helpful, the AI agent performs these steps:
                        1.  Requests more details about the issue to refine the web search.
                        2.  Searches the web again to find repair steps that match with the details provided.
                        3.  Displays the repair steps in the Now Assist panel, to assist the technician in resolving the issue.
                        4.  Checks with the technician to confirm whether the new repair steps were helpful.
                            -   If the technician confirms that the new repair steps were helpful, the AI agent updates the task with the details provided by the technician and closes the task.
                            -   If the technician confirms that the new repair steps were not helpful, the agentic workflow stops.
            -   If the issue isn't present on the repair task, the AI agent performs the following actions:
                1.  Requests more details about the issue to refine the web search.
                2.  Searches the web again to find repair steps that match with the details provided.
                3.  Displays the repair steps in the Now Assist panel, to assist the technician in resolving the issue.
                4.  Checks with the technician to confirm whether the new repair steps were helpful.
                    -   If the technician confirms that the new repair steps were helpful, the AI agent updates the task with the details provided by the technician, and then closes the task.
                    -   If the technician confirms that the new repair steps weren't helpful, the agentic workflow stops.

## Role masking

Roles required:

Agentic workflows and their AI agents use role masking to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

## AI agents used in the Help repair hardware assets agentic workflow

The Help repair hardware assets agentic workflow uses specific AI agents to validate repair tasks, handle troubleshooting and repair tasks, and complete the tasks autonomously.

|AI agent|AI agent role|
|--------|-------------|
|Asset next best action AI agent|Validates the repair tasks, checks the task type, and triggers the Evaluate asset AI agent to manage the troubleshooting task or the Repair asset AI agent to manage the repair task.|
|Evaluate asset AI agent|Performs a web search and provides a detailed evaluation guide to help the technician identify the issue on the asset. Updates the troubleshooting task with the details received from the technician and then closes the task.|
|Repair asset AI agent|Performs a web search and provides detailed repair steps to help the technician resolve the issue identified on the asset. Updates the repair task with the details received from the technician and then closes the task.|

