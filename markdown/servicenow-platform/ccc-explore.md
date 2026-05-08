---
title: Exploring ServiceNow Voice
description: Use ServiceNow Voice to facilitate inbound and outbound telephone calls by integrating your ServiceNow instance with a third-party phone system such as Amazon Connect.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Exploring ServiceNow Voice

Use ServiceNow Voice to facilitate inbound and outbound telephone calls by integrating your ServiceNow instance with a third-party phone system such as Amazon Connect.

## Key features

-   **Integrate a third-party phone system with Voice in the ServiceNow instance**

    Provide a seamless inbound and outbound voice call experience for your callers and agents using third-party systems. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/search?listingtype=allintegrations&q=voice&searchDetail&pagetype=integration) for a full list of integrations.

    ![Integrate third-party phone system](../image/integrate-third-party-phone-app.png "Integrate third-party phone system")

-   **Display relevant data for an agent at the right time**

    Display relevant data in an interaction for an agent to help a customer during a call.

    ![Route calls to agents](../image/route-calls-agent.png "Route calls to agents")

-   **Analyze recording and call metrics of interactions**

    Within your ServiceNow instance, access recordings, call metrics, and call transcripts of agents to analyze interactions.

    ![Review and analyze call transcripts](../image/review-analyze-call-transcripts.png "Review and analyze call transcripts")


As an admin, you can:

-   Use pre-built instructions and templates to integrate your ServiceNow instance with a third-party phone system such as Amazon Connect.
-   Use pre-built operation handlers that invoke interactions to fulfill requests between a third-party phone system and Voice.

As a manager, you can:

-   View the call transcript and recording for coaching.
-   View call metrics \(for example, agent call time\) for reporting.
-   Analyze agent conversations and provide feedback for quality assurance.

As an agent, you can:

-   Get calls routed to your assigned queues and accept or reject the calls via the integrated softphone from within the ServiceNow instance.
-   Transfer a call to another agent or to a queue using **Quick connect**.
-   Get the context of caller information before accepting a call.
-   View real-time transcripts of calls while interacting with a customer. For more information about real-time transcripts, see
-   Collaborate with managers who can analyze your conversations and provide feedback for quality assurance.
-   Manage presence states within the ServiceNow instance. For information about the presence states of an agent, see Agent Inbox controls.
-   Access and use your softphone directly from within the ServiceNow interface using the OpenFrame integration. For information about OpenFrame, see OpenFrame overview.

As a caller, you can:

-   Create a task using voice-based interactions. For example, create an incident or a case, or unlock your account.
-   Get your requests fulfilled within the integrated ServiceNow instance through bot interactions using the voice or dual-tone multi-frequency \(DTMF\) inputs. These bot interactions are defined in contact flows in the third-party phone system.
-   Speak to an agent who can help fulfill a request.

## Inbound call workflow for the integration of Voice with Amazon Connect

When a caller contacts the call center, using the voice or dual-tone multi-frequency \(DTMF\) inputs from a caller, a contact flow is invoked in the Amazon Connect instance based on the caller context such as language. An interaction record is created for this call.

-   The caller request will invoke an operation handler in the ServiceNow instance.
-   The request can be resolved by an automated interaction with a bot. If the caller request is not resolved by an automated interaction with bot, then the call is queued for the next available agent. An agent then receives the call and interaction, and resolves the request.

Here is an example workflow.

![Amazon Connect Integration](../image/amazon-connect-integration.png "Amazon Connect Integration")

**Parent Topic:**[ServiceNow Voice](cloud-call-center-overview.md)

