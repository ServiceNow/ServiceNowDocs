---
title: Issue Auto Resolution diagnostic chat
description: Admin users can initiate a chat conversation to troubleshoot the settings and functionality of Issue Auto Resolution if an issue arises that wasn't addressed as expected.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Issue Auto Resolution, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Issue Auto Resolution diagnostic chat

Admin users can initiate a chat conversation to troubleshoot the settings and functionality of Issue Auto Resolution if an issue arises that wasn't addressed as expected.

## Enabling diagnostic chat

To enable the Issue Auto Resolution diagnostic tool, an admin user must set certain Restricted Caller access records to **Allowed** on the Restricted Caller Access Privileges table.

To identify the records to allow, follow these steps:

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access**.
2.  Filter the records by `Source=76fec17dc0e1d5d0f877e9d0ea777a12` \(Script Include: IARIssueNotAssignedDiagnostic\).
3.  Navigate to each record and change the status to **Allowed**.

    ![Double-click in the Status column, and then choose Allowed from the list. Select the save icon.](../images/iar-diagnostic-12.png)


## Diagnostic conversation flows

The admin user enters `IAR` in the chat window to initiate a conversation about Issue Auto Resolution, and then selects one of two issues:

-   An Incident or case isn’t getting assigned to the Bot user.
-   An Incident or case isn’t going through Issue Auto Resolution.

![When the admin types "IAR," the bot offers these two solutions. Select the one that applies.](../images/iar-diagnostic-1a.png)

## Conversation flow: Incident or HR case is not getting assigned to bot user

1.  Confirm your selection, return to search, or search KB articles.

    ![Bot responses for this flow include Yes, Back to Searched result, Search KB, and Search again.](../images/iar-diagnostic-2a.png)

2.  Select the type of case or Incident with which you need help, or choose to search all Issue Auto Resolution configurations.

    ![You are prompted to select the related table you want to run the health check on. For instance, HR Cases, Incidents, or all configured tables.](../images/iar-diagnostic-3a.png)

3.  The diagnostic tool performs an analysis on Issue Auto Resolution configuration and settings and displays the results. The diagnostic confirms the following conditions:

    -   The prediction server is up.
    -   There are existing Issue Auto Resolution configurations.
    -   The configurations are active.
    A health check for the selected configuration type also runs to determine if the Incident or case is properly configured for Issue Auto Resolution. The diagnostic for an Incident checks the following conditions:

    -   Issue Auto Resolution configuration is active.
    -   Language configuration is active.
    -   There is an active response channel.
    -   There is an active intent topic map for the Incident configuration.
    The diagnostic for a case additionally checks that AI Search has been enabled and doesn’t check for an intent topic map. If all the settings are correct and the issue persists, the user can choose to continue the conversation.

    ![Bot response showing PASSED test results for the conversation.](../images/iar-diagnostic-4a.png)

4.  Enter the Incident or case number and confirm it’s correct.

    ![When you've chose to proceed with the test, enter the Incident or case number in the chat.](../images/iar-diagnostic-6.png)![When you've chose to proceed with the test, enter the Incident or case number in the chat.](../images/iar-diagnostic-6a.png)

    The bot asks you to confirm the number you entered.

5.  The diagnostic tool analyzes the issue to determine if the following conditions are met:

    -   The trigger condition on the configuration matches the Incident or case values.
    -   The business rule order is the highest.
    -   There’s only one trigger business rule for Issue Auto Resolution on the Incident or case table and it’s active.
    If the suggestions don’t resolve the issue, you can choose to run further analysis.


## Conversation flow: An Incident or case is not going through Issue Auto Resolution

1.  Confirm your choice to proceed diagnosing a functionality issue with Issue Auto Resolution.

    ![Confirm your choice to diagnose an Issue Auto Resolution problem in the chat window.](../images/iar-diagnostic-9a.png)

2.  The diagnostic tool checks the following conditions:

    -   The intent prediction was successful \(Incidents only\).
    -   The criticality is correct and AI Search is active \(cases only\).
    -   A notification was sent.
    -   The end user responded to the notification.
    If any of these checks reveal an issue, the diagnostic tool displays a possible solution. Indicate whether these solutions resolved the issue, or choose to perform further analysis.

    ![Select Yes if you found a solution, or select No to continue with further diagnosis.](../images/iar-diagnostic-11a.png)


**Parent Topic:**[Using Issue Auto Resolution](auto-resolution-va.md)

**Related topics**  


[Conversational Interfaces Diagnostic Tool](../../conversational-interfaces/concept/ci-diagnostics-tool-landing.md)

