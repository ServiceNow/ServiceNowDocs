---
title: Credential and dynamic parameter management
description: Logs in automatically when a goal references stored credentials configured for a website, without exposing sensitive values in chat or asking you to provide the input.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/credential-storage.html
release: australia
topic_type: concept
last_updated: "2026-08-31"
reading_time_minutes: 2
keywords: [stored credentials, web agent, login, desktop action parameters]
breadcrumb: [Adaptive desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# Credential and dynamic parameter management

Logs in automatically when a goal references stored credentials configured for a website, without exposing sensitive values in chat or asking you to provide the input.

## Key benefits

This functionality provides the following benefits:

-   Skips manual login steps for websites that already have stored credentials configured.
-   Keeps sensitive values, such as passwords, out of the chat and out of the agent's plan.
-   Falls back to manual login when credentials aren't configured, so the task can continue.

## How it works

If your goal doesn't reference stored credentials, or references credentials that aren't defined for the website, the agent asks you to log in manually:

1.  The agent prompts you to log in.
2.  Switch to the website's browser window and log in.
3.  Confirm in chat so the agent can continue.

If your goal references stored credentials, the agent logs in automatically with dynamic parameters already configured for that website:

1.  The agent retrieves the corresponding values from the stored credentials.
2.  The agent enters the values on the website's login page. You don't need to provide anything in chat.

## Sensitive value handling

-   Values marked as sensitive in the stored credentials are never displayed, in chat or elsewhere.
-   Non-sensitive values, such as a username, might appear as part of the agent's plan.

## Considerations

-   To use stored credentials, an administrator must first define them as desktop action parameters. For more information, see [Enable AI agents to securely access parameters in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-parameter-record-ad.md).
-   To trigger automatic login, phrase your goal in such a way that it explicitly references the stored parameter names, as shown in the following examples.
    -   Go to https://www.example.com/ and authenticate using parameter 'user\_name' and parameter 'password'.
    -   Open https://www.example.org/ and log in with stored 'user\_name' and stored 'password', then select Transactions.
    -   Open https://www.example.net/ and log in using username from reference 'user\_name' and password from reference 'password'. Then navigate to 'Task List', remove any filters, choose Pending status, and select Save.

**Parent Topic:**[Configuration for adaptive path desktop actions for web](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ad-adaptive-path-da.md)

**Related topics**  


[Enable AI agents to securely access parameters in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-parameter-record-ad.md)

