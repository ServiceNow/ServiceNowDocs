---
title: Test your Virtual Agent API configuration
description: Test your Virtual Agent API configuration using API testing tool.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Test your Virtual Agent API configuration

Test your Virtual Agent API configuration using API testing tool.

## Before you begin

Make sure you've setup Postman or Swagger or any other third-party application environment for API testing.

Role required: admin

## About this task

API tests are a way to ensure that your API is behaving as you expect it to. To write a test, do the following:

## Procedure

1.  Select the environment that you've setup and navigate to tab where you can send your first API request.

2.  Configure the payload.

    For example, send the below request:

    ```
    {
        "requestId": "requestid123",
        "userId": "testuser.1",
        "emailId": "admin@example.com",
        "action": "START_CONVERSATION",
        "message": {
            "text": "",
            "typed": true
        },
        "contextVariables": {
            "app_name": "test"
        }
    }
    ```

3.  Click **Send**.

    You can check the response of your payload and your communication status in the response section.

    -   If your instance is on asynchronous mode, you have to check enabling Virtual Agent API logging. See [Common errors in Virtual Agent API](../reference/virtual-agent-common-errors.md) for more information.
    -   If your instance is on synchronous mode, you have to check the Body of the response.

**Parent Topic:**[Configuring Virtual Agent API](../concept/configure-virtual-agent-api.md)

