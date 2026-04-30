---
title: Diagnose Conversational Interfaces errors
description: Use the Conversational Interfaces Diagnostic Tool to resolve issues related to conversational interfaces such as error messages and system property issues before reaching out to Now Support.
locale: en-US
release: yokohama
product: Conversational Interfaces Diagnostics Tool
classification: conversational-interfaces-diagnostics-tool
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using the Conversational Interfaces Diagnostic Tool, Conversational Interfaces Diagnostic Tool, Conversational Interfaces]
---

# Diagnose Conversational Interfaces errors

Use the Conversational Interfaces Diagnostic Tool to resolve issues related to conversational interfaces such as error messages and system property issues before reaching out to Now Support.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Use this task to resolve errors and find and change system property values.

## Procedure

1.  Start a conversation with the Virtual Agent chatbot.

2.  At the greeting message, type `diagnostic pre chat`.

3.  Describe the issue that you want to solve.

    If it is an error message issue, you can copy-and-paste or type the error message into the chatbot conversation.

    For system properties, you don't need to know the exact name of the system property. Type a feature name related to the property to see a list of matching system properties.

    When your input matches an existing system property, but that property isn't in your instance, you see the system property name followed by two dash lines. For example: `some.property.name--`

    Find or create the system property on your instance and make changes, as applicable.

    The tool displays a list of solutions.

4.  Select the solution that you want to use.

    The Diagnostic Tool asks if you want to proceed with the diagnosis.

    ![Virtual Agent chat window in Microsoft Teams, asking if you want to proceed with the diagnosis.](../image/ci-dt-microsoft-proceed-choices.png "Proceed or search again chat response")

5.  Select **Yes** to continue.

    The tool initiates the workflow and leads you through the relevant prompts. The prompts you see depend on the issue you want to diagnose and solve.

6.  Answer the prompts.

    When the diagnosis is complete, the Diagnostic Tool displays a recommended solution.

    ![Virtual Agent chat window displaying a recommended solution: Please ensure that group name is the same as the tenant ID in the message_auth table.](../image/ci-dt-recommended-solution.png "Issue recommendation")

    ![Virtual Agent chat window displaying confirmation to proceed with workflow.](../image/ci-dt-proceed-with-topic-flow.png "Issue confirmation")

7.  Select **Yes** to confirm, or select **No** to end the workflow.

    The Diagnostic Tool guides you through the relevant workflow. The options and prompts you see depend on the issue you want to solve. Reply to the prompts, as applicable. You may also see a link to the relevant Knowledge Base \(KB\) article where you can find more information.

8.  Provide feedback.

    When asked whether the solution was helpful, select one of the following:

    -   Select **Yes**, if the solution wasn't helpful.

        You are asked to provide additional information that helps fine-tune the solution.

        The prompts you see vary by the issue that you want to solve.

    -   Select **No** to confirm that the solution was helpful and to exit the workflow.
    -   You may see a link that you can use to download support data.
    ![A link to download support data displays at the end of the workflow.](../image/ci-dt-download-support-data.png "Prompt to download support data")

9.  Click the link to download support data.


**Parent Topic:**[Using the Conversational Interfaces Diagnostic Tool](../concept/using-ci-diagnostics-tool.md)

