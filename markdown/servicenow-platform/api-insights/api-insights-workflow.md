---
title: Configuring flows for API actions in API Insights
description: Configure flows in Workflow Studio for automating API actions within API Insights, streamlining processes like API access requests.
locale: en-US
release: zurich
product: API Insights
classification: api-insights
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enterprise architect administrator tasks, Configure, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring flows for API actions in API Insights

Configure flows in Workflow Studio for automating API actions within API Insights, streamlining processes like API access requests.

Configure flows to automate various API actions, such as granting access to APIs or processing API requests. Enterprise architect administrators with the sn\_api\_insights\_ws.api\_mgmt\_architect\_admin role can then select workflows that align with specific API automation tasks when they configure settings for managing APIs. See [Configure settings to manage APIs in API Insights](../task/api-insights-config-settings.md).

## Predefined flow to send reminders for API access

The **API Request Reminder** subflow is available with the API Insights application that sends reminders for approving any API access requests. This flow automatically sends reminder notifications to the ownership groups specified in the flow, prompting them to review and approve pending API access requests.

## Predefined flow to grant API access

The **API Grant/Reject Access Template** subflow is available with the API Insights application that grants access to any APIs. This flow automatically that identifies the API access requests and enables to grant or reject access to any APIs.

## Configuring flow for API access request automation

To manage API access requests through custom flows, it's essential to configure the flow with specific input parameters. These parameters guide the flow's behavior.

To learn about creating flows, see [Getting started with flows](https://www.servicenow.com/docs/access?context=getting-started-flow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

When creating a flow for API access request automation, you must use specific parameters that control how the flow works.

You must include the following input parameters in the flow:

```
Input params:
request (reference from sn_api_insights_ws_request_access_task table) - Required
grant (string) - Required
description (string) - Optional
```

-   **request**

    A required reference to a specific record in the API Requests Access Task \[sn\_api\_insights\_ws\_request\_access\_task\] table that identifies the API access request and facilitates interaction with the API Insights application.

-   **grant**

    A required string input that specifies the action to be taken, such as granting or denying access.

-   **description**

    An optional string input to provide additional details or context about the API access request.


