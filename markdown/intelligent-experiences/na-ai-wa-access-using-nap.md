---
title: Trigger an AI agent to execute adaptive path desktop actions
description: Trigger an AI agent that uses adaptive desktop actions from the Now Assist panel. These desktop actions perform tasks on an external website or web application.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-09-06"
reading_time_minutes: 5
keywords: [AI Agents, Agentic AI]
breadcrumb: [Execute desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Trigger an AI agent to execute adaptive path desktop actions

Trigger an AI agent that uses adaptive desktop actions from the Now Assist panel. These desktop actions perform tasks on an external website or web application.

## Before you begin

-   Confirm that the **ServiceNow Web Automation** Google Chrome extension is installed and connected to your ServiceNow® instance. For more information, see [Install the Google Chrome extension for adaptive desktop actions](na-ai-wa-install-browser-extension.md).
-   Confirm that you're logged in to your ServiceNow instance and it is in the active state in the browser window.
-   Verify that enhanced chat is available in Now Assist panel. The Web view pane is available only when enhanced chat is enabled. For more information see [Enhanced chat](../../../administer/now-assist-platform/concept/now-assist-panel-enhanced.md).

Role required: now\_assist\_panel\_user

## About this task

AI agents using adaptive desktop actions perform tasks for you on a website or web application. The AI agent opens the website in a separate browser tab in the background, and reports its actions to you in the Now Assist panel. During the process, the website may require credentials for a login or acceptance of terms. In such cases, the AI agent prompts you to provide credentials in the chat or switch to the website's browser window temporarily so you can enter the required information.

Here are tips for writing successful requests for the LLM:

-   Be sure to provide the URL to your target website, using the format `https://www.example.com` or `example.com`.
-   Make your request clear and specify your goal.
-   List steps to achieve the goal, if possible.

## Procedure

1.  On your ServiceNow instance, open the Now Assist panel by using the Now Assist ![Now Assist icon.](../../../administer/now-assist-platform/images/wwna-icon.png) icon.

    Use the same instance that the **ServiceNow Web Automation** extension is connected to and has at least one AI agent that uses adaptive desktop actions.

2.  Type your request.

    Now Assist panel asks for details about your request.

    ![Under View AI Agent Processing Steps, the agent asks for specifics. The Reply to Now Assist text box is highlighted.](../../../administer/now-assist-web-agents/image/na-ai-wa-access-using-nap-specifyZ.png)

3.  Enter details about the task you want the AI agent to execute for you.

    Examples of tasks you can request:

    -   Can you find the best coffeemaker on amazon.com?
    -   Can you find the latest invoice from invoiceninja.com?
    -   Navigate to https://www.accuweather.com/. In the Search field, enter "zip code 95054" and search. In the search results, open the first page. Find the current temperature in degrees Fahrenheit and tell me the temperature.
    -   Navigate to en.wikipedia.org. On the main page of wikipedia.org, in the Search field, search for "Santa Clara, California". In the search results, open the first page listed, and read its contents. Summarize the contents of the page in 2 or 3 sentences.
    In your conversations with AI agents, the actual wording of the questions and answers may be different from the given examples. For more information about Now Assist panel, see [Now Assist panel](../../../administer/now-assist-platform/concept/now-assist-panel-overview.md).

4.  Review the execution plan proposed by the AI agent and confirm your approval.

    -   If you're satisfied that the AI agent understood your request, then enter `proceed` or `approve`
    -   If you're not satisfied with the AI agent's plan, try to rephrase your request.
    After you indicate approval, the AI agent begins to execute its plan. It provides updates on its process in the Now Assist panel.

    **Note:** The system may display an error about a setup configuration if the **ServiceNow Web Automation** Google Chrome extension is disconnected. Verify that the browser extension displays **Connected** by refreshing the browser windows that has the ServiceNow instance open.

5.  Monitor the AI agent's updates in Now Assist panel.

    You can see the following:

    -   AI agent opens a concurrent browser tab to your target website, labeled "Opened for you".![The browser tab opened by the Now Assist AI agent, with the message "Opened for you."](../../../administer/now-assist-web-agents/image/na-ai-wa-test-opened-for-youZ.png)
    -   The **Web view** tab displays periodic screenshots of how AI agent navigates to the website and perform requested steps.

        You can switch to the Web view by selecting the **Web view** tab or by selecting the **Walkthrough of AI agents on the web** card in Now Assist panel.

        ![Under View AI Agent Processing Steps, at Walkthrough of AI agents on the web, the Show button is highlighted.](../../../administer/now-assist-web-agents/image/na-ai-wa-access-using-nap-show-web-viewZ.png)

6.  If the AI agent prompts you that the website requires a login or terms agreement, respond in the chat or switch to the **Opened for you** browser tab to enter the information directly.

    ![In chat in Now Assist panel, the AI agent requests the user to complete the required action on the website and then confirm once finished.](../../../administer/now-assist-web-agents/image/na-ai-wa-access-request-to-userZ.png)

    Return to the Now Assist panel in your instance when you have finished the login. Confirm that you're ready to continue.

7.  When the AI agent returns satisfactory results in the Now Assist panel chat, enter a closing such as `Thank you` to signal to the AI agent that the task is finished.

    If the AI agent doesn't take the expected steps, you can take over and complete them manually.


## Result

The AI agent closes the separate browser tab to the external website. Your chat is moved to the Completed section of Now Assist panel.

## What to do next

You can delete the chat log in Now Assist panel if any sensitive information was captured. For detailed instructions, see [Delete an AI agent chat log](na-ai-wa-delete-chat-log.md).

-   **[Delete an AI agent chat log](na-ai-wa-delete-chat-log.md)**  
After you close an AI agent session, you can delete its chat if any sensitive information was captured. Deleting your chat log permanently erases the chat history of that session, including screenshots.

**Parent Topic:**[Examples of executing desktop actions using AI agents](../concept/use-agentic-desktop.md)

