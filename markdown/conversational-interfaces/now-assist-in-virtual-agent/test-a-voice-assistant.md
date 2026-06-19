---
title: Test a voice assistant
description: Test your voice assistant and the AI voice agents assigned to the assistant from the Assistant Designer. You can make browser-based voice calls and view turn-by-turn analysis of AI voice agents invoked, tools executed, and tool execution latency during the conversation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/test-a-voice-assistant.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2026-06-06"
reading_time_minutes: 3
breadcrumb: [View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Test a voice assistant

Test your voice assistant and the AI voice agents assigned to the assistant from the Assistant Designer. You can make browser-based voice calls and view turn-by-turn analysis of AI voice agents invoked, tools executed, and tool execution latency during the conversation.

## Before you begin

The following are required to access the voice testing experience:

-   Conversational Studio v7 or later
-   Zurich Patch 7 or later
-   Microphone enabled on your device
-   Now Assist for Virtual Agent version 19 or later

Roles required: sn\_aia.admin and sn\_voice\_aia.admin

## About this task

Use voice testing to evaluate how your voice assistant handles real conversations before deploying it.

-   Voice mode: Initiate a call, speak to the assistant using your microphone. The assistant responds with synthesized speech.
-   Chat mode: Type messages in a chat interface. This mode follows the same testing experience as chat assistants.

As the conversation progresses, the Analysis tab shows a turn-by-turn breakdown including timestamps, the agent or tool invoked for each utterance, tool execution latency, and tool status, helping you identify gaps and fine-tune behavior.

## Procedure

1.  Navigate to **All** &gt; **Assistant Designer** &gt; **Assistants** tab and select **Test** for the voice assistant you wish to test.

    The voice testing interface opens in a new window. The window displays:

    -   Left panel: A drop down for testing mode with Voice and Chat options. Live transcription of the conversation along with the assistant greeting and input controls.
    -   Right panel: Assistant summary showing the assistant name, telephony provider \(if configured\), language, voice personality, and the Analysis tab.
    \[Omitted image "ai-voice-assistant-test-window.png"\] Alt text: Voice assistant testing window

2.  Test your voice assistant.

    1.  In voice mode, select **Start call** \(green phone button\) to begin voice-based testing.

        Your browser may prompt you to allow microphone access. Click **Allow** to proceed.

        The call connects using WebRTC \(Web Real-Time Communication\). A voice waveform animation indicates the connection is active.

    2.  Speak to the assistant using your microphone.

        The assistant processes your speech and responds with synthesized voice output. The conversation transcript appears in the left panel.

        \[Omitted image "NAinVA-assistant-designer-analytics-voice-testing-voice-mode.png"\] Alt text: Voice assistant testing in Voice mode

    3.  Continue the conversation to test different scenarios and intents.

    4.  When finished, select **End call** \(red phone button\) to disconnect.

    1.  In chat mode, type your message in the **Reply** field at the bottom of the conversation panel.

        Text-based testing follows the same experience as testing chat assistants. You can view the chat transcription, AI agents invoked and tools executed.

    2.  Select the send button to submit your message.

        The assistant processes your text input and responds in the conversation panel.

        \[Omitted image "NAinVA-assistant-designer-analytics-voice-testing-chat-mode.png"\] Alt text: Voice assistant testing in Chat mode

    3.  Continue the conversation to test different scenarios and intents.

3.  Select the **Analysis** tab in the right panel to view real-time analysis.

    The Analysis tab shows a turn-by-turn breakdown of the conversation. For each user utterance, the following details are displayed where applicable:

    -   **Timestamp** — the date and time of the utterance.
    -   **Agent name** — the name of the AI voice agent invoked, or voice assistant if no agent was invoked.
    -   **Tool name** — the name of the tool invoked, where applicable. Expand a tool name to view:
        -   **Tool inputs**
        -   **Tool execution latency**
        -   **Tool status** \(success or failure\)
        -   **Tool response**
    The Analysis tab displays a turn-by-turn breakdown of AI voice agents invoked, tools executed, and tool execution latency for the conversation.

4.  Select **Restart** to start a new voice conversation or close the browser window to exit testing.

    Selecting **Restart** clears the current conversation and resets the testing session.


## Result

You have tested your voice assistant using the voice testing interface. Use the analysis results to identify issues with agent routing, tool execution, or voice assistant performance, and refine your assistant configuration as needed.

