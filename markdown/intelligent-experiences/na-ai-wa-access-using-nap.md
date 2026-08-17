---
title: Trigger an AI agent to execute adaptive path desktop actions
description: Trigger an AI agent that uses adaptive desktop actions from the ServiceNow Otto panel. These desktop actions perform tasks on an external website or web application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/na-ai-wa-access-using-nap.html
release: zurich
topic_type: task
last_updated: "2025-09-06"
reading_time_minutes: 5
keywords: [AI Agents, Agentic AI]
breadcrumb: [Execute desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Trigger an AI agent to execute adaptive path desktop actions

Trigger an AI agent that uses adaptive desktop actions from the ServiceNow Otto panel. These desktop actions perform tasks on an external website or web application.

## Before you begin

-   Confirm that the **ServiceNow Web Automation** Google Chrome extension is installed and connected to your ServiceNow® instance. For more information, see [Install the Google Chrome extension for adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/na-ai-wa-install-browser-extension.md).
-   Confirm that you're logged in to your ServiceNow instance and it is in the active state in the browser window.
-   Verify that enhanced chat is available in ServiceNow Otto panel. The Web view pane is available only when enhanced chat is enabled. For more information see [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-panel-enhanced.md).
-   Adaptive desktop actions can handle a broader range of user interactions beyond custom UI, such as triple-click, double-click, right-click, native prompts, dialogues, and alerts.

Role required: now\_assist\_panel\_user for the user and sn\_naa.web\_agent\_runtime for the service account the agent runs as

## About this task

AI agents using adaptive desktop actions perform tasks for you on a website or web application. The AI agent opens the website in a separate browser tab in the background, and reports its actions to you in the ServiceNow Otto panel. During the process, the website might require credentials for a login or acceptance of terms.

You can preserve the context across long-running sessions by summarizing older step history instead of discarding it. When history exceeds the configured window, older steps are automatically summarized instead of being discarded, preserving context about earlier actions, failed approaches, and application state.

There are three system properties that handle this:

-   sn\_naa.web\_agent.compaction\_enabled
-   sn\_naa.web\_agent.compaction\_history\_limit
-   sn\_naa.web\_agent.summarization\_batch\_size

For detailed information about the system properties, see [Components installed with AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/components-installed-with-agentic-desktop.md).

Here are tips for writing successful requests for the LLM:

-   Be sure to provide the URL to your target website, using the format `https://www.example.com` or `example.com`.
-   Make your request clear and specify your goal.
-   List steps to achieve the goal, if possible.

## Procedure

1.  On your ServiceNow instance, open the ServiceNow Otto panel by using the ServiceNow Otto \[Omitted image "otto-icon.png"\] Alt text: ServiceNow Otto icon. icon.

    Use the same instance that the **ServiceNow Web Automation** extension is connected to and has at least one AI agent that uses adaptive desktop actions.

2.  Type your request.

    ServiceNow Otto panel asks for details about your request.

    \[Omitted image "chat-panel.png"\] Alt text: ServiceNow Otto panel

3.  Enter details about the task you want the AI agent to execute for you.

    Examples of tasks you can request:

    -   Can you find the best coffeemaker on amazon.com?
    -   Can you find the latest invoice from invoiceninja.com?
    -   Navigate to https://www.accuweather.com/. In the Search field, enter "zip code 95054" and search. In the search results, open the first page. Find the current temperature in degrees Fahrenheit and tell me the temperature.
    -   Navigate to en.wikipedia.org. On the main page of wikipedia.org, in the Search field, search for "Santa Clara, California". In the search results, open the first page listed, and read its contents. Summarize the contents of the page in 2 or 3 sentences.
    In your conversations with AI agents, the actual wording of the questions and answers may be different from the given examples. For more information about ServiceNow Otto panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-panel-overview.md).

4.  Review the execution plan proposed by the AI agent and confirm your approval.

    -   If you're satisfied that the AI agent understood your request, then enter `proceed` or `approve`
    -   If you're not satisfied with the AI agent's plan, try to rephrase your request.
    After you indicate approval, the AI agent begins to execute its plan. It provides updates on its process in the ServiceNow Otto panel.

    **Note:** The system may display an error about a setup configuration if the **ServiceNow Web Automation** Google Chrome extension is disconnected. Verify that the browser extension displays **Connected** by refreshing the browser windows that has the ServiceNow instance open.

5.  Monitor the AI agent's updates in ServiceNow Otto panel.

    You can see the following:

    -   AI agent opens a concurrent browser tab to your target website, labeled "Opened for you".\[Omitted image "na-ai-wa-test-opened-for-youZ.png"\] Alt text: The browser tab opened by the AI agent, with the message "Opened for you."
    -   The **Web view** tab displays periodic screenshots of how AI agent navigates to the website and perform requested steps.

        You can switch to the Web view by selecting the **Web view** tab or by selecting the **Walkthrough of AI agents on the web** card in ServiceNow Otto panel.

        \[Omitted image "da-show-button.png"\] Alt text: The Show button is highlighted for Walkthrough of AI agents on the web.

6.  When the AI agent returns satisfactory results in the ServiceNow Otto panel chat, enter a closing such as `Thank you` to signal to the AI agent that the task is finished.

    If the AI agent doesn't take the expected steps, you can take over and complete them manually.


## Result

The browser tabs opened during goal execution in adaptive desktop actions stay open after the goal completes. Use the `keep_tab_open` system property to turn this behavior on or off. The property is turned on by default.

## What to do next

You can delete the chat log in ServiceNow Otto panel if any sensitive information was captured. For detailed instructions, see [Delete an AI agent chat log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/na-ai-wa-delete-chat-log.md).

-   **[Delete an AI agent chat log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/na-ai-wa-delete-chat-log.md)**  
After you close an AI agent session, you can delete its chat if any sensitive information was captured. Deleting your chat log permanently erases the chat history of that session, including screenshots.

**Parent Topic:**[Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/use-agentic-desktop.md)

