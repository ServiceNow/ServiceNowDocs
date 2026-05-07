---
title: Install the Google Chrome extension for adaptive desktop actions
description: Download and install the ServiceNow Web Automation chrome extension to the Google Chrome browser. The browser extension enables AI agents to interact with web applications or websites opened in the browser during task execution.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-09-05"
reading_time_minutes: 2
breadcrumb: [Adaptive desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# Install the Google Chrome extension for adaptive desktop actions

Download and install the ServiceNow Web Automation chrome extension to the Google Chrome browser. The browser extension enables AI agents to interact with web applications or websites opened in the browser during task execution.

## Before you begin

-   Verify that you have at least one AI agent that uses one or more adaptive desktop actions in the ServiceNow® instance you plan to connect to.
-   You must be connected to the ServiceNow® instance.
-   You must have permissions to download and install browser extensions in your Google Chrome browser.
-   Role required: none

## About this task

This procedure enables you to download and install the extension from the Google Chrome webstore. Install the Google Chrome browser extension on each system where you want to invoke an AI agent to automate tasks.

Using the ServiceNow Web Automation browser extension, an AI agent opens a browser tab to navigate to web applications or websites.

When you log out of the ServiceNow® instance, the message **Disconnected** appears in the browser extension. This message also appears when any browser window to your instance is inactive. The extension must be connected for AI agents to interact with the web applications.

**Note:** Verify that you open only one tab with active ServiceNow® instance.

## Procedure

1.  Download the Google Chrome browser extension from the Google Chrome webstore by navigating to [https://chromewebstore.google.com/detail/servicenow-rpa-chrome-ext/bnaofpgjajbimmicdiipemhmheafhgkb](https://chromewebstore.google.com/detail/servicenow-rpa-chrome-ext/bnaofpgjajbimmicdiipemhmheafhgkb).

2.  Select **Add to Chrome**.

3.  In the Add ServiceNow Web Automation confirmation modal, select **Add extension**.

4.  In your Google Chrome browser address bar, enter `chrome://extensions/`.

5.  Select **Details** on the **ServiceNow Web Automation** card and select the **Pin to toolbar** option.

    The extension is now added to the browser.

6.  Select the **ServiceNow Web Automation** extension icon ![](../image/ad-web-automation-pinned-icon.png) on the browser.

7.  In the **Enter your instance URL** field, enter the ServiceNow instance you want to connect to, in the format `https://<instance-name>.service-now.com/`.

    The confirmation message appears in the browser extension: **Connected**.

    ![The browser extension, installed and connected to a ServiceNow instance.](../../../administer/now-assist-web-agents/image/na-ai-wa-install-browser-extension-connectedZ.png "Connected browser extension")

    Verify that you're connected to the ServiceNow® instance that has at least one AI agent that uses one or more adaptive desktop actions.

    **Note:** If any browser windows were already open with the instance, you must reload the windows to connect successfully to the browser extension.

8.  Select **Save**.


## What to do next

After installing the browser extension, configure websites that AI agents can access for automating web tasks. For detailed instructions, see [Configure allowed websites for adaptive desktop actions](na-ai-wa-configure-allowed-websites.md).

**Parent Topic:**[Configuration for adaptive path desktop actions](../concept/ad-adaptive-path-da.md)

