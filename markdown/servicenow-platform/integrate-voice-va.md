---
title: Integrating ServiceNow Voice with Virtual Agent
description: ServiceNow Voice with Virtual Agent allows you to use the ServiceNow Virtual Agent conversation as an IVR \(Interactive Voice Response\) in phone and to use the existing ServiceNow Advanced Work Assignment to find an agent in case of an escalation and allows agents to work in ServiceNow Workspace to manage the incoming cases on the queue.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating Voice with other applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrating ServiceNow Voice with Virtual Agent

ServiceNow® Voice with Virtual Agent allows you to use the ServiceNow Virtual Agent conversation as an IVR \(Interactive Voice Response\) in phone and to use the existing ServiceNow Advanced Work Assignment to find an agent in case of an escalation and allows agents to work in ServiceNow Workspace to manage the incoming cases on the queue.

The ServiceNow Voice for Virtual Agent application provides seamless interactive voice response \(IVR\) and calling experiences for your customers and agents when integrated with a Contact Center In Australia release, we have Amazon Connect, a pre-built adapter integrating the ServiceNow Voice with Virtual Agent to provide the robust capabilities of the Virtual Agent application.

To use our pre-built adapter connector with ServiceNow Voice with Virtual Agent, install the Virtual Agent API \(sn\_va\_as\_service\) plugin.

## Key features

-   **User experience**
    -   Have Virtual Agent answer calls and interact with end users for automated deflection on the phone channel.
    -   Complete workflow including case lookup, interaction, and task management using Virtual Agent.
    -   Enable agents to interact with users on the phone on workspace in case of any escalations.
    -   Receive calls in inbox that are routed via the Advanced Work Assignment rules.
-   **Calling and routing**
    -   Make outbound calls via click to call or via auto-connecting the Omnichannel Callback feature.

        For more information, see [Configure Conversational IVR with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/configure-va-ivr.md).

    -   Transfer to external phone number using the Amazon Connect Softphone.
    -   Skills-based call assignment using the Advanced Work Assignment.
-   **Artificial intelligence**
    -   Match intent and entity using ServiceNow Virtual Agent.
    -   Analyze sentiments of the utterances.
    -   Real-time transcription and storage of the recording.
-   **User benefits**
    -   Account log in using voice to receive enterprise service.
    -   Callback options.

## Example workflow

The following example workflow shows the use of ServiceNow Voice for Virtual Agent application in resolving a customer issue.

-   A customer is in an IVR call using the ServiceNow Voice for Virtual Agent application.
-   The ServiceNow Voice for Virtual Agent application identifies the customer and starts an interaction.
-   A welcome message is read out to the customer including announcements if any.
-   Based on customer identification, the ServiceNow Voice for Virtual Agent application addresses the call.
    -   If the caller is identified as an existing customer who has a customer contact or consumer record with the phone number details available in the ServiceNow Voice for Virtual Agent application, a personal greeting is read to the caller and the automated interactions with Virtual Agent conversations are made available.
    -   If the caller is not identified, the caller is presented with the guest topics and the live agent topic. The caller can select the live agent topic to route themselves to a live agent.
-   The ServiceNow Voice for Virtual Agent application identifies the customer intent using automated interactions, and the Virtual Agent conversations guide customers to complete the workflow, including changing records, passwords or hearing about a case status.

    **Note:** This step in the flow applies only when the caller is an existing customer.


**Parent Topic:**[Integrating Voice with other applications](integrate-ccc-other-apps.md)

**Related topics**  


[Conversational IVR with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-ivr-voice.md)

