---
title: Configure rate limiting for providers
description: Configure rate limiting to control the traffic flow to the one\_extend request by restricting the number of requests that can be made within a certain time frame.
locale: en-US
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure rate limiting for providers

Configure rate limiting to control the traffic flow to the one\_extend request by restricting the number of requests that can be made within a certain time frame.

## Before you begin

Role required: admin

## About this task

To rate limit the one\_extend request, you must define the rate limit rules for the incoming requests. You can create your own rule in the One Extend Rate Limit Rules table.

## Procedure

1.  On your ServiceNow instance, navigate to the One Extend Rate Limit Rules \[sys\_one\_extend\_rate\_limit\_rules\] table and select **New**.

2.  On the form, fill in the fields.

<table id="table_tyy_fmk_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the rate limit rule. Identify the rate limit rule with a name.

</td></tr><tr><td>

Application

</td><td>

Application scope that must be set to Global.

</td></tr><tr><td>

Resource

</td><td>

Resources to select for your rate limit rule.Use one of the following resources for your rate limit rule:

-   **LLM Provider**: For the LLM Provider, select the generative AI provider mapping.
-   **Capability Definition**: For the Capability Definition, select the One Extend Capability Definition.
-   **All Capabilities**: Applies to all providers and all capability definitions.


</td></tr><tr><td>

Rule Type

</td><td>

Rule type for the rate limit rule.Define the rule type using the following options:

-   **Instance**: Accumulates data from all the users of that instance.
-   **User**: Keeps the count of the requests per user.


</td></tr><tr><td>

Request limit per hour

</td><td>

Maximum number of requests to be received per hour.

</td></tr><tr><td>

Active

</td><td>

Status of the rate limit rule.

</td></tr></tbody>
</table>3.  Select **Submit**.


