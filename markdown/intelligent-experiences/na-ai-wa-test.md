---
title: Test an AI agent or agentic workflow for adaptive desktop actions
description: Test an AI agent or agentic workflow that uses adaptive desktop actions in AI Agent Studio to evaluate its performance.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-09-07"
reading_time_minutes: 7
breadcrumb: [Add adaptive desktop action for web, Create AI agents, AI Desktop Actions, Enable AI experiences]
---

# Test an AI agent or agentic workflow for adaptive desktop actions

Test an AI agent or agentic workflow that uses adaptive desktop actions in AI Agent Studio to evaluate its performance.

## Before you begin

-   Confirm that the **ServiceNow Web Automation** Google Chrome extension is installed and connected to your ServiceNow® instance. For more information, see [Install the Google Chrome extension for adaptive desktop actions](na-ai-wa-install-browser-extension.md).
-   Confirm that you're logged in to your ServiceNow instance and it is in the active state in the browser window.
-   Verify that enhanced chat is available in Now Assist panel. The Web view pane is available only when enhanced chat is enabled. For more information see [Enhanced chat](../../../administer/now-assist-platform/concept/now-assist-panel-enhanced.md).
-   The AI agent checks its access to the internet by first opening the main Google website. If you have implemented an allow list, verify that google.com is allowed. For more information, see [Configure allowed websites for adaptive desktop actions](na-ai-wa-configure-allowed-websites.md).
-   Role required: sn\_aia.admin

## About this task

As an AI agent admin, you can run manual tests of AI agents and agentic workflows in the AI Agent Studio by providing a task or request in the testing module. Testing includes the user experience as seen in Now Assist panel, plus extra information for administrators. This information is provided in a split view in the Node map view:

-   AI process map displays a diagram of agent orchestration.
-   AI agent decision logs provide reports on the AI agent's reasoning as it processes your request.

When testing an AI agent or agentic workflow, you can see the AI agent Orchestrator and Communicator working together to organize and manage the AI agents like a team. The AI agent Orchestrator assigns the individual, specialized agents to complete the subtasks. The AI agent Communicator lets the AI agent Orchestrator know the status of each agent.

**Note:** If you don't have the roles necessary to pass the ACLs of the AI agent and all of its tools, you’ll be notified that you don't have the necessary access and the test won't execute.

Your AI agent or agentic workflow starts to execute the test autonomously to resolve the task.

![Testing module showing AI process map displays a diagram of agent orchestration, AI agent decision logs, and execution plan in the chat panel.](../image/ad-aia-test-playground.png "Testing an AI agent or agentic workflow")

Because generative AI is non-deterministic, try several test runs of a task. The AI agent's responses and results may vary from one test run to another. Your test runs are listed in the **Activity** tab of AI Agent Studio.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.

2.  Select **Start manual test**.

    If you want to start an automated test, see [Evaluate an AI agent](../../../administer/now-assist-ai-agents/task/execute-aia-eval.md) for more details on that process.

3.  In the **Choose a test type** drop-down menu, select **AI agent or workflow**.

    If you want to test user access security controls, see [Test AI agent user access](../../../administer/now-assist-ai-agents/task/test-aia-access.md).

4.  Select an agentic workflow or AI agent that you want to test by searching the name of a workflow or choosing from the drop-down menu.

5.  Under **Choose a testing mode**, select the **Standard** testing mode.

    **Note:** The AI-native testing mode is exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard testing playground.

6.  In the Version drop-down list, select the version of the AI agent or agentic workflow you want to test.

    This field automatically fills in the most recent active version of the AI agent or agentic workflow, but you can switch to a different active version from the drop-down list.

    See [Version control for AI agents and agentic workflows](../../../administer/now-assist-ai-agents/concept/version-control.md) for more information about creating and changing versions.

7.  In the **Task** field, provide a concise summary of the task to be achieved.

    Enter a request that is typical of your users and their needs. Example tasks:

    -   Can you find the best coffeemaker on amazon.com?
    -   Can you find the latest invoice from invoiceninja.com?
    -   Navigate to https://www.accuweather.com/. In the Search field, enter "zip code 95054" and search. In the search results, open the first page. Find the current temperature in degrees Fahrenheit and tell me the temperature.
    -   Navigate to en.wikipedia.org. On the main page of wikipedia.org, in the Search field, search for "Santa Clara, California". In the search results, open the first page listed, and read its contents. Summarize the contents of the page in 2 or 3 sentences.
8.  Select **Continue to Test Chat Response**.

    -   A simulated chat experience begins on the Now Assist panel between your invoking user and AI agent.
    -   A diagram shows the tasks and communication of the AI agents that are working together to solve the case.
    -   A decision log records the thought process of each AI agent that is involved in solving the agentic workflow.

        **Note:** You can view the entire decision log by selecting **Download logs**.

9.  Review the proposed plan in the simulated chat experience.

    -   If you're satisfied that the AI agent understood your request, then enter `proceed` or `approve`
    -   If you're not satisfied with the AI agent's plan, try to rephrase your request.
    **Note:** The system may display an error about a setup configuration if the **ServiceNow Web Automation** Google Chrome extension is disconnected. Verify that the browser extension displays **Connected** by refreshing the browser windows that has the ServiceNow instance open.

10. Monitor the AI agent's updates in AI Agent Studio.

    AI agent opens a concurrent browser tab to your target website, labeled "Opened for you".

    ![The separate browser tab which opens to the third-party website. The title of this tab is "Opened for you".](../../../administer/now-assist-web-agents/image/na-ai-wa-test-opened-for-youZ.png)

    You can switch to the **Web view** tab that displays periodic screenshots of how AI agent navigates to the website and perform requested steps.

    ![The web view in the testing module displays screenshots of the target website.](../../../administer/now-assist-web-agents/image/na-ai-wa-test-web-viewZ.png)

11. If a website requires a login, the AI agent prompts you in the simulated chat experience to enter your credentials.

    You can enter the credentials in the chat or open the separate browser tab labeled **Opened for you**. Enter the log in credentials as required, and then return to the testing module.


## Result

When the test is finished:

-   The AI agent displays a summary of the outcome in the simulated chat experience. This is the outcome that is provided to your users when they are in the Now Assist panel.
-   The AI agent closes the separate browser tab to the external website.
-   Web view automatically switches back to **Node map** view, where an **End** node is displayed in AI process map.
-   AI agent decision logs all display **Completed**. You can review reports of the reasoning process by expanding the decision log sections.

## What to do next

View information about your test runs in the **Activity** tab of AI Agent Studio. The most recent test run is located at the top of the list.

![The Activity tab of AI Agent Studio. A row in the list is displayed, showing a recent test run for a workflow associated to a web-based desktop action.](../../../administer/now-assist-web-agents/image/na-ai-wa-test-activity-tabZ.png)

Your users can access your AI agent by using Now Assist panel. For information see [Trigger an AI agent to execute adaptive path desktop actions](na-ai-wa-access-using-nap.md).

**Related topics**  


[Manually test the execution of an agentic workflow](../../../administer/now-assist-ai-agents/task/test-aia-use-case.md)

[Manually test the execution of an AI agent](../../../administer/now-assist-ai-agents/task/test-ai-agent.md)

