---
title: Integrating ServiceNow Voice with CSM
description: Access the CSM -specific contact flows and operation handlers when you integrate the ServiceNow Voice application with the Customer Service Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/integrating-ccc-csm.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integrating Voice with other applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrating ServiceNow Voice with CSM

Access the CSM -specific contact flows and operation handlers when you integrate the ServiceNow Voice application with the Customer Service Management application.

The ServiceNow Voice for CSM application provides seamless interactive voice response \(IVR\) and calling experiences for your customers and agents by integrating a cloud contact center provider with the robust capabilities of the Customer Service Management application.

## Overview

The ServiceNow Voice for CSM application provides the following Customer Service capabilities for the integration with a cloud call center provider such as the Amazon Connect service:

-   A bot building framework to automate interactions with consumers and customer contacts.
-   [An inbound contact flow to define the customer experience in an IVR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instld-with-ccc-csm.md).
-   [An outbound contact flow to connect with consumers and customer contacts from the phone number field displayed in any of the ServiceNow application UIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instld-with-ccc-csm.md).
-   [Operation handlers to configure automated interactions for customer service cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instld-with-ccc-csm.md).
-   [A phone PIN setup option for consumers and customer contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/ccc-csm-config-pin.md).
-   [Amazon Connect phone queues for the Workforce Optimization for Customer Service application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integrating-ccc-csm.md).

To get started with the ServiceNow Voice for CSM application, see [Install ServiceNow Voice for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/install-ccc-csm.md).

## Key features

-   **Customer experience**

    Engage via voice-based interactions using a natural language process to do the following:

    -   Create a case
    -   Update and check case status
    -   Speak with an agent
    -   Request a call back from an agent
-   **Agent experience**
    -   Preview caller information displayed in Agent Workspace before accepting an inbound call.
    -   Indicate your presence in the Agent Workspace Inbox with voice as a service channel when the Agent Workspace Inbox is integrated with the Agent softphone.
    -   View real-time transcripts of calls while interacting with a customer. For more information about real-time transcripts, see [Real time transcriptions for ServiceNow Voice for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/using-voice-rtt.md)
    -   Transfer calls to another agent or to a queue, and include transcripts and interaction history with the transfer.
    -   Make outbound calls to connect with a customer and automatically capture interaction details to simplify data entry.
-   **Manager experience**
    -   Review call transcripts, sentiments, and recordings to explore coaching opportunities for agents.
    -   Use call metrics, such as the agent call time, to report on agents.
    -   Monitor real-time phone metrics captured in a unified dashboard by using the Workforce Optimization for Customer Service application.

        **Note:** This feature is available when the Workforce Optimization for Customer Service application is enabled for the Customer Service Management application.


## ServiceNow Voice for CSM user roles

The users with the roles listed in the following table can use the ServiceNow Voice for CSM application.

|Roles|Tasks|
|-----|-----|
|agent\_workspace\_user|Initiate or accept voice calls to understand customer issues and resolve issues.|
|sn\_customerservice\_manager|View details of voice calls using the interaction record of the Phone type.|
|sn\_customerservice.consumer, sn\_customerservice.customer|Initiate or accept voice calls to create and track one's own customer service cases.|

## Example workflow

The following example workflow shows the use of the ServiceNow Voice for CSM application in resolving a customer issue:

1.  A customer is in an IVR call using the ServiceNow Voice for CSM application.
2.  The ServiceNow Voice for CSM application identifies the customer and starts an interaction.
3.  A welcome message is read out to the customer including announcements, if any.
4.  Based on customer identification, the Cloud Call Center for CSM application addresses the call.
    -   If the caller is identified as an existing customer who has a customer contact or consumer record with the phone number details available in the Customer Service Management application, a personal greeting is read to the caller and the automated interactions are made available.
    -   If the caller is not identified, the call is routed to a live agent.
5.  The ServiceNow Voice for CSM application identifies the customer intent using automated interactions, and then based on the interaction responses, either creates or updates a case.

    **Note:** This step in the flow applies only when the caller is an existing customer.


## Workforce Optimization for Customer Service

Integrate Voice with Workforce Optimization for Customer Service to visualize call metrics from the Amazon Connect service. Voice uses the [Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-overview.md) feature to display the call metrics and active calls along with all other Channel metrics in the Manager Workspace. For more information, see [Using Voice with Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configurable-servicenow-voice-cs.md).

\[Omitted image "cloudcallcenter-amazonconnect-wfo-itsm.png"\] Alt text: The Amazon Connect phone queues in the Workforce Optimization for Customer Service application

-   **[Install ServiceNow Voice for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/install-ccc-csm.md)**  
You can install the ServiceNow Voice for CSM application \(sn\_cti\_csm\_cnt\) if you have the admin role. The application installs related ServiceNow® Store applications if they are not already installed.
-   **[Configuring the phone PIN settings for ServiceNow Voice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/ccc-csm-config-pin.md)**  
Use a  PIN-based authentication mechanism for enabling a customer contact or consumer to connect with the ServiceNow Voice for CSM  application. 
-   **[Real time transcriptions for ServiceNow Voice for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/using-voice-rtt.md)**  
Agents can see a transcript of voice calls while interacting with customers. Real time transcription allows agents to better understand customer issues, and allows managers to gain insights into customer trends and agent training gaps.

**Parent Topic:**[Integrating Voice with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integrate-ccc-other-apps.md)

**Related topics**  


[Setting up ServiceNow Voice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/ccc-setup.md)

[Using Voice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/use-ccc.md)

[Components installed with ServiceNow Voice for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instld-with-ccc-csm.md)

