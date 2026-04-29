---
title: Explore
description: Dynamic Guidance provides an assistance that is proactive and fully embedded within the product, enabling users to access relevant information without navigating away from their Workflow.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2026-03-20"
reading_time_minutes: 1
breadcrumb: [Dynamic Guidance, Adoption services, Configure user experiences]
---

# Explore

Dynamic Guidance provides an assistance that is proactive and fully embedded within the product, enabling users to access relevant information without navigating away from their Workflow.

Explore various features of Dynamic Guidance:

-   Voice and screen share options

    **Note:** User voice or screen share data is not stored. The transcript however, gets logged in the database.

-   Responses are based on ServiceNow® documents from the same family release as that of the instance you're on
-   Front-end component to invoke Dynamic Guidance and end a conversation
-   Option for an unlimited number of users running this simultaneously
-   Enabled to work across the ecosystem of ServiceNow
-   Near real-time experience and minimized latency
-   Browser support: In Firefox, while the entire screen or the app gets shared with screen share, you can choose to share only the desired tab in Google Chrome

    **Note:** Screen share is not supported in Safari.

-   30 minutes of audio and screen share support

    **Note:** You can cancel screen sharing anytime in the course of conversation.

-   Pause and resume conversation at your pace
-   Cross-tab control on pausing and ending the conversation although, the transcript can only be accessed from the launching tab of Dynamic Guidance
-   The floating chat window has a floating feature due to which, you can control the conversation from any other open instance window

## How Dynamic Guidance works

When you ask a question that requires documentation lookup:

1.  User query: You ask a question via voice interface
2.  Gemini decision: Gemini Live API determines if knowledge base search is needed
3.  Tool call: Gemini invokes the knowledge base search tool with the query
4.  RAG API processing: RAG API Handler processes the query and searches XCC
5.  XCC search: XCC searches the crawled ServiceNow Docs content
6.  Results return: RAG API Handler formats and returns relevant documentation snippets
7.  Response Generation: Gemini synthesizes the answer using the retrieved content

