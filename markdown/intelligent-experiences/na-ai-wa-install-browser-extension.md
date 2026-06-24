---
title: Install the Google Chrome extension for adaptive desktop actions
description: Install the ServiceNow Web Automation Chrome extension to the Google Chrome browser. The browser extension enables AI agents to interact with web applications during task execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/na-ai-wa-install-browser-extension.html
release: zurich
topic_type: task
last_updated: "2025-09-05"
reading_time_minutes: 2
keywords: [Google chrome extension]
breadcrumb: [Adaptive desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# Install the Google Chrome extension for adaptive desktop actions

Install the ServiceNow Web Automation Chrome extension to the Google Chrome browser. The browser extension enables AI agents to interact with web applications during task execution.

## Before you begin

-   At least one AI agent that uses one or more adaptive desktop actions must exist in the ServiceNow® instance you plan to connect to.
-   You must be logged in to your ServiceNow® instance.
-   You must have permissions to install browser extensions in Chrome.

Role required: none

## About this task

Follow the procedure to download and install the extension from the Google Chrome webstore. Install the Google Chrome browser extension on each device where you want to invoke an AI agent to automate tasks.

Using the ServiceNow Web Automation browser extension, an AI agent opens a browser tab to navigate to web applications.

When you log out of the ServiceNow instance, the message `Disconnected` appears in the browser extension. This message also appears when any browser window to your instance is inactive. The extension must be connected for AI agents to interact with the web applications.

**Note:** Verify that you open only one tab with active ServiceNow® instance.

## Procedure

1.  Download the Google Chrome browser extension from the Google Chrome webstore by navigating to:

    [https://chromewebstore.google.com/detail/servicenow-rpa-chrome-ext/bnaofpgjajbimmicdiipemhmheafhgkb](https://chromewebstore.google.com/detail/servicenow-rpa-chrome-ext/bnaofpgjajbimmicdiipemhmheafhgkb)

2.  Select **Add to Chrome**.

3.  In the Add ServiceNow Web Automation dialog, select **Add extension**.

4.  In your Google Chrome browser address bar, enter `chrome://extensions/`.

5.  Select **Details** on the **ServiceNow Web Automation** card, and then select the **Pin to toolbar** option.

    The extension icon appears in the Chrome toolbar.

6.  Select the **ServiceNow Web Automation** extension icon \[Omitted image "ad-web-automation-pinned-icon.png"\] Alt text: in the browser toolbar.

7.  In the **Enter your instance URL** field, enter the ServiceNow instance you want to connect to, in the format `https://<instance-name>.service-now.com/`.

    The confirmation message appears in the browser extension: `Connected`.

    \[Omitted image "na-ai-wa-install-browser-extension-connectedZ.png"\] Alt text: The browser extension, installed and connected to a ServiceNow instance.

    Verify that you're connected to the ServiceNow® instance that has at least one AI agent that uses one or more adaptive desktop actions.

    **Note:** If any browser windows were already open with the instance, you must reload the windows to connect successfully to the browser extension.

8.  In the browser extension panel, select **Save**.


## What to do next

After installing the browser extension, configure websites that AI agents can access for automating web tasks. For detailed instructions, see [Configure allowed websites for adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/na-ai-wa-configure-allowed-websites.md).

**Parent Topic:**[Configuration for adaptive path desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/ad-adaptive-path-da.md)

