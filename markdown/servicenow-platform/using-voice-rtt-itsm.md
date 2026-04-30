---
title: Real time transcriptions for ServiceNow Voice for IT Service Management
description: Agents can see a transcript of voice calls while interacting with customers. Real time transcription allows agents to better understand caller issues, and allows managers to gain insights into caller trends and agent training gaps.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating ServiceNow Voice with ITSM, Integrating with applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Real time transcriptions for ServiceNow Voice for IT Service Management

Agents can see a transcript of voice calls while interacting with customers. Real time transcription allows agents to better understand caller issues, and allows managers to gain insights into caller trends and agent training gaps.

## Inbound call example flow for customers and agents

The below examples illustrate common scenarios for using real-time transcriptions for inbound calls. The caller calls in and requests to speak to an agent. As soon as the call begins, the agent can see the transcript of the call in chat panel as they work with the caller. The real time transcript is not visible to the caller, however, the transcript can help the agent better understand the caller issue and refer back to the conversation for clarification.

Personas:

-   Agent
-   Caller

Example Caller flow for inbound calls.

1.  Customer dials an Amazon Connect customer service number.
2.  Confirm the approval for recording \(press 1\#\).
3.  Give instruction: “Speak to a live agent”.
4.  Provide a subject for the customer service agent: “Router Issue”.
5.  Confirm the subject and wait for the agent to pick up the call.

Example Agent flow for inbound calls.

1.  Log in to your ServiceNow instance and open the Configurable Workspace
2.  Log in to Amazon Connect.
3.  Set status to **Online**.
4.  Wait for a call alert and answer the call.
5.  A new interaction with the subject and chat panel opens with the real time transcript.

## Outbound call example flow for agents

The below example illustrates a common scenario for using real-time transcriptions in outbound calls. The agent contacts the caller, and as soon as the call starts, the agent can see the transcript of the call in chat panel as they work with the caller. The real time transcript is not visible to the caller, however, the transcript can help the agent better understand the caller issue and refer back to the conversation for clarification.

Persona: Agent.

1.  Log in and open the Configurable Workspace.
2.  Log in to Amazon Connect.
3.  Set status to **Online**.

An interaction is created with the subject “outbound call to `<customer name>`”, and a chat panel opens with the transcript.

**Parent Topic:**[Integrating ServiceNow Voice with ITSM](integrate-ccc-itsm.md)

