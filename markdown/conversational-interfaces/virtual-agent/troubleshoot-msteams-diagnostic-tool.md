---
title: Capture common errors and provide resolution steps for Microsoft Teams using the Conversational Interfaces Diagnostic Tool
description: The Conversational Interfaces Diagnostic Tool runs a health report to define and capture information for different categories of the Conversational Integration with Microsoft Teams app, such as plugin details, configuration settings, system properties, integration failures, and so on, and lets the user validate and review these settings to start a bot-conversation.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Microsoft Teams, MSTeams, Conversational Interfaces, Diagnostic tool, health report]
breadcrumb: [VA feature support in Teams conversations, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Capture common errors and provide resolution steps for Microsoft Teams using the Conversational Interfaces Diagnostic Tool

The Conversational Interfaces Diagnostic Tool runs a health report to define and capture information for different categories of the Conversational Integration with Microsoft Teams app, such as plugin details, configuration settings, system properties, integration failures, and so on, and lets the user validate and review these settings to start a bot-conversation.

When a user runs the health check scan and if there are issues that are shown on the report, then the user can take actions to resolve the issues based on the recommendations that the bot provides through the CI Diagnostic Tool.

## Grouping common errors

To provide a health report of the various aspects of the Conversational Integration with Microsoft Teams application, the most common issues have been grouped into the following categories:

-   Microsoft Teams not responding
-   Notifications
-   Automatic Linking
-   Image/HTML
-   Performance
-   Installation
-   Live Agent

## Resolution

The Conversational Interfaces Diagnostic Tool is used to resolve the errors that users come across with their Microsoft Teams app. Knowledge Base articles are documented with resolutions to the issues and the records for these KB articles are created in the CI Diagnostic Tool.

**Note:** Microsoft Teams requires the CI Diagnostics Tool of version 1.1.0 to make the diagnostic topic available for the user.

Resolving errors using the CI Diagnostic Tool includes the following steps:

1.  Login into the chat widget and start the CI Diagnostic Tool.

    The CI Diagnostic Tool presents the following groups to choose from:

    -   Error Message
    -   System Property Lookup
    -   Plugin/Functionality Issue
    -   General Question
2.  Select **Plugin/Functionality Issue** and type `Conversational Integration with Microsoft Teams` or any related keyword to get the options of available plugins related to your search term.

    The Microsoft Teams application logo appears as a response.

3.  After Microsoft Teams is provided as an input to the CI Diagnostic tool, a basic health check of the app gets executed and a report is generated for the user.

    The health check is run to verify if:

    -   Microsoft Teams app plugin installed
    -   Provider application record verification.
    -   Message auth table has all the records
    -   Dependant plugins are available
    -   OIDC token verification records are available
    -   Provider reference is missing in the \[sys\_cs\_provider\_application\] table
    After successful health check scan, verifications such as recent installation errors, recent syslog errors, and recent HTTP transactions are presented to the user.![Microsoft Teams health check in Now Support using Diagnostic tool.](../images/msteams-health-check-diagnostic-tool.png)

4.  The health check report also provides you with an option to view existing Knowledge Base articles that may be associated with your issue. Enter **Yes** and provide a few words to describe your issue.

    For example, if you enter `image` as your issue description, then the CI Diagnostic tool presents you with the Knowledge Base articles related to images. Select the link to view the Knowledge Base article.

    Select **No** to proceed for additional support.

5.  The CI Diagnostic Tool provides you with an additional support topic available for the Microsoft Teams plugin. Select **Yes** to proceed.

    You are presented with the following issue types to select from.![Virtual Agent chat window showing diagnostic support and issue type selection for the Microsoft Teams plugin.](../images/msteams-troubleshoot-type.png)

    For example, if you select any one of the issue types, the CI Diagnostic Tool provides you with the resolution steps pertaining to that issue type to identify the cause of the issue and to resolve it. You will also be presented with the relevant Knowledge Base articles to get further details about the issue.

    Finally, the CI Diagnostic Tool asks you to check if your issue is resolved. Select **Yes** if the issue is resolved.


**Parent Topic:**[Virtual Agent feature support in Microsoft Teams conversations](va-teams-other-features.md)

