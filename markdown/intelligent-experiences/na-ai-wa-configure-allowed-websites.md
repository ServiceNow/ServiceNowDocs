---
title: Configure allowed websites for adaptive desktop actions
description: Specify a list of websites that AI agents configured with adaptive desktop actions are permitted to open and perform tasks.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-08-28"
reading_time_minutes: 2
breadcrumb: [Adaptive desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# Configure allowed websites for adaptive desktop actions

Specify a list of websites that AI agents configured with adaptive desktop actions are permitted to open and perform tasks.

## Before you begin

Set your application scope to Now Assist AI web agent.

Role required: admin

## About this task

AI agents configured with adaptive desktop actions perform tasks on web applications or websites. You can control the websites that AI agents access by updating a system property, sn\_naa.allowed\_websites. This system property permits access to all websites, with a single asterisk \(\*\) as the default value. When you enter a list of allowed sites, the AI agents are restricted to only the sites in the list.

**Note:** AI agents operate through the browser extension, which means they can only access content within the browser and are unable to interact with desktop applications or other local files, except for downloading files. The AI agents can't access the downloaded files as well from the desktop. Use defined desktop actions for uploading data from the local system.

When configuring an allow list, include your organization's websites. Work with your stakeholders to determine which websites to include. If an AI agent tries to access a website not on the allow list, the system stops the request and displays an error message. An AI agent can open websites defined in tool actions that aren't on the allow list. However, the AI agent can't perform any actions on those websites.

**Note:** The AI agent checks its access to the internet by first opening the Google website. If the AI agent isn't allowed to open the Google website, it can't proceed with its task. Be sure to include `google.com` or `*.google.com` in the allowed list.

## Procedure

1.  Navigate to **All**.

2.  In the filter navigator, enter `sys_properties.list`.

3.  In the System Properties table, search and select the **sn\_naa.allowed\_websites** property.

    The System Properties form opens.

4.  In the **Value** field, delete the single asterisk \(\*\) and enter the websites that you want to allow for AI agents to access.

    The following guidance apply:

    -   Separate the websites using commas \(comma-separated list\).
    -   Enter websites as hostnames without protocols, such as `example.com`.
    -   Allow all subdomains on a website by using an asterisk. The format `*.example.com` allows abc.example.com, xyz.example.com, and so forth.
    -   Be sure to include access to Google website by entering `google.com` or `*.google.com`.
    ![The webform for the sys property sn_naa.allowed_websites, with two example websites in the Value field. The websites are separated by a comma.](../../../administer/now-assist-web-agents/image/na-ai-wa-configure-allowed-websites1Z.png)

5.  Select **Update** to save your changes.


## What to do next

-   [Create an AI agent](../concept/create-ai-agents-ad.md)
-   [Add an adaptive desktop action tool to an AI agent for web-based tasks](../concept/create-web-actions.md)
-   [Create an agentic workflow for automating web tasks](na-ai-wa-configure-workflow.md)

**Parent Topic:**[Configuration for adaptive path desktop actions](../concept/ad-adaptive-path-da.md)

