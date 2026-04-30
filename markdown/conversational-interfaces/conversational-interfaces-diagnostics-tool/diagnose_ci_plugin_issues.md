---
title: Diagnose Microsoft Teams configuration issues
description: Use the Conversational Interfaces Diagnostic Tool to identify and help solve Microsoft Teams configuration issues before reaching out to Now Support.
locale: en-US
release: xanadu
product: Conversational Interfaces Diagnostics Tool
classification: conversational-interfaces-diagnostics-tool
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using the Conversational Interfaces Diagnostic Tool, Conversational Interfaces Diagnostic Tool, Additional resources for Conversational Interfaces, Conversational Interfaces]
---

# Diagnose Microsoft Teams configuration issues

Use the Conversational Interfaces Diagnostic Tool to identify and help solve Microsoft Teams configuration issues before reaching out to Now Support.

## Before you begin

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Start a conversation with the Virtual Agent chatbot.

2.  At the greeting message, type `diagnostic pre chat`.

3.  Describe the issue that you want to solve.

    For example, if the Microsoft Teams application isn't responding, you can type `no response`.

    The tool displays a list of solutions.

    ![Virtual Agent chat window displaying solutions for Microsoft Teams not responding and Microsoft Teams performance. There is also an option for "Not matching."](../image/ci-dt-microsoft-choices.png "Example solutions for "no response"")

4.  Select the solution that you want to use.

    The Diagnostic Tool asks if you want to proceed with the diagnosis.

    ![Virtual Agent chat window displaying question to user in Microsoft Teams asking to proceed with the diagnosis.](../image/ci-dt-microsoft-proceed-choices.png "Proceed or search again chat response")

5.  Select **Yes** to continue.

    Lists of Health Check Parameters and MS Teams Tenant Configurations display.

    ![Health check parameters include online status, plugin status, and user role. Tenant configurations include the tenant ID and authentication status.](../image/ci-dt-health-check-parameters.png "Health check parameters and tenant configuration status")

6.  Review the values for any parameters that are set incorrectly.

    For example, if a value is set to **False** when it should be set to **True**.

    When the diagnosis is complete, the Diagnostic Tool displays a recommended solution.

    ![Virtual Agent chat window displaying recommended solution.](../image/ci-dt-recommended-solution.png "Issue recommendation")

    ![Virtual Agent chat window displaying confirmation to proceed with workflow.](../image/ci-dt-proceed-with-topic-flow.png "Issue confirmation")

7.  Select **Yes** to confirm, or select **No** to end the workflow.

    The Diagnostic Tool guides you through the relevant workflow. The options and prompts you see depend on the issue you want to solve. Reply to the prompts, as applicable. You may also see a link to the relevant Knowledge Base \(KB\) article where you can find more information. For example, you may see a link to the [Master KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1064282) for common and known issues with Microsoft Teams.

8.  Provide feedback.

    When asked whether the solution was helpful, select one of the following:

    -   Select **Yes**, if the solution wasn't helpful.

        You are asked to provide additional information that helps fine-tune the solution. For example, you may be asked to provide the MS Teams Bot tenant ID, or asked if the instance has been cloned from another instance.

        The prompts you see vary by the issue that you want to solve.

    -   Select **No** to confirm that the solution was helpful and to exit the workflow.
    -   You may see a link that you can use to download support data.
    ![A link to download support data displays at the end of the workflow.](../image/ci-dt-download-support-data.png "Prompt to download support data")

9.  Click the link to download support data.


**Parent Topic:**[Using the Conversational Interfaces Diagnostic Tool](../concept/using-ci-diagnostics-tool.md)

