---
title: Issue Auto Resolution for ITSM Virtual Agent
description: Proactively deflect common ITSM incidents to ITSM Virtual Agent. Initiate a conversation with an end user after they submit an incident through a non-conversational service channel, if an existing ITSM Virtual Agent conversation can resolve the issue.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [ITSM Virtual Agent pre-built actionable notifications, ITSM Virtual Agent, IT Service Management]
---

# Issue Auto Resolution for ITSM Virtual Agent

Proactively deflect common ITSM incidents to ITSM Virtual Agent. Initiate a conversation with an end user after they submit an incident through a non-conversational service channel, if an existing ITSM Virtual Agent conversation can resolve the issue.

## Understanding Issue Auto Resolution

Issue Auto Resolution uses ITSM Virtual Agent to proactively resolve incidents through a conversation on the user's preferred chat channel. The Issue Auto Resolution flow follows these steps:

-   When an end user creates an incident through a non-conversation service channel, such as ServiceNow® Service Portal or email, the Natural Language Understanding \(NLU\) model checks for a matching intent that has Issue Auto Resolution enabled.
-   If a matching intent and topic are found, Issue Auto Resolution sends an actionable notification to the end user on their existing chat channel. The user can accept or decline assistance.
-   If the end user accepts the assistance, Issue Auto Resolution invokes the matched ITSM Virtual Agent conversation to resolve the incident.
-   When the conversation completes, the user can indicate if the conversation resolved the incident and can choose to keep the ticket open or to close it.
-   When there are no matching Issue Auto Resolution intents found, AI Search is enabled as fallback along with added intents. For more information, see [Enabling AI Search in Issue Auto Resolution](enable-ai-search-itsm.md).

## When an incident is unassigned from Issue Auto Resolution

An incident is unassigned from Issue Auto Resolution and is routed to an agent when any of the following conditions apply:

-   The matched intent doesn't have a matching topic in the same domain as that of the incident.
-   The matched topic doesn't have Issue Auto Resolution enabled.
-   The end user has not subscribed to notifications.
-   The end user declines, ignores, or abandons the Virtual Agent conversation.
-   The matched topic didn't resolve the issue.

## When an incident is assigned from Issue Auto Resolution

An incident is assigned from Issue Auto Resolution and is routed to a Virtual Agent when an intent to topic is matched for the incident.

You must ensure that you check the SLAs and Notifications to see if they trigger the **Assigned to is EMPTY** condition to avoid issues with SLAs and Notifications setup on the instance against the incident table.

Update your SLAs and Notifications trigger condition either to **Assigned to is EMPTY** or ensure that the **Assigned to** field is set to **Virtual Agent**.

## Issue Auto Resolution dashboard

The Issue Auto Resolution dashboard provides metrics for the effectiveness of incident deflection, based on Virtual Agent conversations. This dashboard is only accessible to users with the admin role, the virtual\_agent\_admin role, the chat\_analytics\_viewer role, or the iar\_admin role. The dashboard tracks both the usage of Issue Auto Resolution and the rate of successful incident resolutions. Users can see which tasks are deflected to Issue Auto Resolution and the overall success of Issue Auto Resolution through the following ServiceNow® Performance Analytics KPIs:

-   Number of tasks solved by Issue Auto Resolution
-   Number of notifications ignored by requester.
-   Number of tasks not solved by Issue Auto Resolution to which the requester responded.

To view the dashboard, navigate to **All** &gt; **Conversational Interfaces** &gt; **Conversational Analytics** &gt; **Virtual Agent Dashboard**. Select the **Issue Auto-Resolution** tab to view analytics.

This tab also provides detailed visualizations on intent and topic matching performed for auto-resolution. For more information, see Issue Auto Resolution tab.

## Issue Auto Resolution Intent Analytics dashboard

The Intent Analytics dashboard provides reports on intent prediction efficiency and other metrics that occur before launching the Issue Auto Resolution topic. This dashboard is accessible only to users with the admin, virtual\_agent\_admin, or iar\_admin role. Intent Analytics and Reports are based on context records and are generated from the context data to do the following:

-   Measure the efficiency of the Machine Learning API \(NLU\).​
-   Measure if Issue Auto Resolution successfully resolved the task.

To view the dashboard, navigate to **All** &gt; **Conversational Interfaces** &gt; **Incident Auto-Resolution** &gt; **Intent Analytics**.

## Natural Language Understanding and Issue Auto Resolution

Issue Auto Resolution uses NLU to identify Virtual Agent topics that match intents submitted by users. Intent matching is determined by the **incident Description** and **Short Description** fields. Intents must meet the required minimum confidence threshold to be considered a match.

![Issue Auto Resolution NLU integration process.](../../../administer/virtual-agent/images/MachineLearning.png "Issue Auto Resolution NLU integration")

To view, train, or retrain the NLU model, see Train and test your model in Virtual Agent Designer.

**Note:** Issue Auto Resolution must be activated and ITSM Virtual Agent must be installed to access the NLU models. To learn more, see [Set up Issue Auto Resolution for ITSM Virtual Agent](../task/setup-itsm-ar.md).

## About actionable notifications

Actionable notifications are interactive messages that Virtual Agent sends to the end user on their preferred chat channel. Issue Auto Resolution sends an actionable notification when the machine learning model finds a topic that matches the user's intent and the user is subscribed to notifications. Actionable notifications contain buttons that the user can select. Each button is mapped to an Issue Auto Resolution topic. Based on the user's selections, different aspects of Issue Auto Resolution execute, according to the logic of the matched topic. For more information on how actionable notifications work and how they're delivered to recipients, see Configuring Virtual Agent notifications.

## ITSM Virtual Agent topics for Issue Auto Resolution

Users with the admin or virtual\_agent\_admin role can choose a subset of pre-built topics to be available for Issue Auto Resolution. The following ITSM Virtual Agent intents are supported by Issue Auto Resolution by default and some of the IAR intents are mapped to ITSM topics by default.

|Intents|Mapped topics|
|-------|-------------|
|CollaborationSoftwareIssues|n/a|
|HardwareRequest|n/a|
|HardwareIssues|Hardware Issues \(Template\)|
|LocalAdminAccess|Local Admin Access \(Template\)|
|SoftwareAccessRequest|n/a|
|SoftwareInstall|n/a|
|RSAToken|n/a|
|VPNConnectivity|VPN Connectivity \(Template\)|
|EmailIssues|Email Issues \(Template\)|
|RepositoryAccess|Repository Access \(Template\)|
|PrinterIssues|Printer Issues \(Template\)|
|ManageDistributionList|n/a|
|ResetPassword|Reset Password \(Template\)|
|MACHINE\_GENERATED|n/a|

The default intents and matched topics are listed in the **Auto Resolution Intent Topic Maps** tab. Users with the admin or virtual\_agent\_admin role can create their own custom topics to use, instead of the included pre-built topics. These custom topics must be mapped to a supported intent in the **Auto Resolution Intent Topic Maps** for Auto Resolution Configuration.

## Issue Auto-resolution tuning

Tune the default IAR intents in the NLU Workbench before returning to the Issue Auto Resolution Admin Console and publish them. For more information, see Issue Auto Resolution Tuning in NLU.

-   **[Enabling AI Search in Issue Auto Resolution](enable-ai-search-itsm.md)**  
You can enable AI Search as a fallback mechanism in Issue Auto Resolution when there are no matching intents found for the incident.

**Parent Topic:**[ITSM Virtual Agent pre-built actionable notifications](itsm-actionable-notifications.md)

**Related topics**  


[bundle-convint.auto-resolution-va]

