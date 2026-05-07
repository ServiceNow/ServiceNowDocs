---
title: Using Voice with Workforce Optimization for Customer Service
description: Use Voice to deflect cases away from your human agents using bots. You can record phone interactions when agents resolve issues. Also, you can monitor those interactions to evaluate and improve the quality of case resolutions.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Channel Management, Use, Workforce Optimization for Customer Service, Customer Service Management]
---

# Using Voice with Workforce Optimization for Customer Service

Use Voice to deflect cases away from your human agents using bots. You can record phone interactions when agents resolve issues. Also, you can monitor those interactions to evaluate and improve the quality of case resolutions.

With the Voice application, you can:

-   Enable your workforce to work using the voice channel and get call recordings, call transcripts, and reports of sentiment analysis when agents interact with callers. You can visualize all of this information within the Channel Management application in Workforce Optimization for Customer Service.
-   Analyze the call transcripts and sentiments of users after an interaction is complete so that you can create assessments, provide feedback, and training for agents.
-   Synchronize agent presence within the queue.
-   View the Amazon Connect channel on Channel Management. You can view the performance metrics and [reports](../reference/components-installed-configurable-wfo-cs.md) of the agents using the voice channel. To access the reports, your application administrator must install [Amazon Connect Spoke](https://www.servicenow.com/docs/access?context=amazon-connect-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

    **Note:** The following reports on the Amazon Connect channel are chargeable:

    -   Contacts in ACW State
    -   Oldest Contact Age
    -   Average Abandon Time
    These reports are collected from Amazon Connect using GetMetricData and GetCurrentMetricData APIs. For more information on the prices of these reports, see [Amazon CloudWatch Pricing](https://aws.amazon.com/cloudwatch/pricing/).


**Note:** You can integrate any third-party telephony service with the [ServiceNowVoice](https://www.servicenow.com/docs/access?context=cloud-call-center-overview&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) application. By default, ServiceNowVoice provides you with the ability to integrate with the Amazon Connect application.

You can visualise the metrics from the Amazon Connect phone queues that are routed through Voice using the Channel Management application in Workforce Optimization for Customer Service. The Voice application uses [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) to report data from the Amazon Connect queues.

## Benefits of using Voice with Workforce Optimization for Customer Service

As a manager, you can:

-   Monitor your agent's calls as they resolve customer issues.
-   View synchronized [agent presence states](https://www.servicenow.com/docs/access?context=agent-experience&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) within the Channel Management application in Workforce Optimization for Customer Service.
-   Assess your agents by reviewing recordings of agent interaction and call transcripts.
-   Analyze sentiments from the call transcripts and use that to coach and train your agents.

As an agent, you can:

-   Get information about the caller before you answer an incoming call.
-   Analyze call transcripts and listen to recordings after you complete an interaction.
-   Place outbound calls using automated outbound dialing.

-   **[Associate Amazon Connect queues for CSM to a ServiceNow instance](../task/setup-amazonconnect-configurable-csm.md)**  
Set up phone queues for Amazon Connect to gain visibility into the queues using Workforce Optimization for Customer Service.
-   **[Listen, Monitor or Barge in to an agent call](../task/listen-agent-call-configurable-wfo-cs.md)**  
Monitor your customer service agents' calls when they are resolving issues for external callers by using Workforce Optimization for Customer Service.
-   **[Analyze transcripts and sentiments for the Amazon Connect phone channel](../task/analyze-transcripts-sentiments-configurable-wfo-cs.md)**  
Analyze your agent's call recordings, transcripts, and sentiment reports. With this information, you can assess the call quality and train your agents to handle calls better in the future.

**Parent Topic:**[Channel Management in Workforce Optimization for Customer Service](configurable-channels-wfo-cs.md)

