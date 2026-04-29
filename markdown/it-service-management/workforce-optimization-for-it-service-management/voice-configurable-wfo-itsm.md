---
title: Using Voice with Workforce Optimization for ITSM
description: Use Voice to deflect incidents away from your human agents using bots. You can record phone interactions when agents resolve issues. Also, you can monitor those interactions to evaluate and improve the quality of incident resolutions.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Routing work items, Channels, Workforce Optimization for ITSM, IT Service Management]
---

# Using Voice with Workforce Optimization for ITSM

Use Voice to deflect incidents away from your human agents using bots. You can record phone interactions when agents resolve issues. Also, you can monitor those interactions to evaluate and improve the quality of incident resolutions.

This video provides an overview of the Voice application:Cloud Call Center Overview

With the Voice application, you can:

-   Enable your workforce to use the voice channel and get call recordings, call transcripts, and reports of sentiment analysis when agents interact with callers. You can visualize all of this information within the Channels application in Workforce Optimization for ITSM.
-   Analyze the call transcripts and sentiments of users after an interaction is complete so that you can create assessments and provide feedback and training for agents.
-   Synchronize agent presence within the queue.

**Note:** You can integrate any third-party telephony service with the [ServiceNow Voice Center application](https://www.servicenow.com/docs/access?context=cloud-call-center-overview&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US). By default, the Voice provides you with the ability to integrate with the Amazon Connect application.

You can visualize the metrics from the Amazon Connect phone queues that are routed through Voice using the Channels application in Workforce Optimization for ITSM.The Voice application uses [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) to report data from the Amazon Connect queues.

## Voice Amazon Connect integration workflow

Here's how the Voice integrates with Amazon Connect:

![Amazon Connect Integration.](../image/amazon-connect-integration.png)

## Benefits of using Voice with Workforce Optimization for ITSM

As a manager, you can:

-   Monitor your agent's calls as they resolve customer issues.
-   View synchronized [agent presence states](https://www.servicenow.com/docs/access?context=agent-experience&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) within the Channels application in Workforce Optimization for ITSM.
-   Assess your agents by reviewing recordings of the agent interaction and call transcripts.
-   Analyze sentiments from the call transcripts and use that information to coach and train your agents.

As an agent, you can:

-   Get information about the caller before you answer an incoming call.
-   Analyze call transcripts and listen to recordings after you complete an interaction.
-   Place outbound calls using automated outbound dialing.

-   **[Associate Amazon Connect queues for ITSM to a ServiceNow instance](../../itsm-manager-workspace/task/setup-cloudcallcenter-itsm-configurable-workspace.md)**  
Set up phone queues for Amazon Connect to gain visibility into the queues using Workforce Optimization for ITSM.
-   **[Listen in to an agent call](../../itsm-manager-workspace/task/listen-in-to-agent-call-configurable-workspace.md)**  
Monitor agent calls when they are resolving issues for external callers by using Workforce Optimization for ITSM.
-   **[Analyze transcripts and sentiments for the Amazon Connect phone channel](../../itsm-manager-workspace/task/analyze-transcripts-sentiments-wfo-itsm-confgurable-workspace.md)**  
Analyze your agent's call recordings, transcripts, and sentiment reports. With this information, you can assess the call quality and train your agents to handle calls better in the future.

**Parent Topic:**[Routing work items using Channels in Workforce Optimization for ITSM](configurable-channels-workforce-optimization-itsm.md)

