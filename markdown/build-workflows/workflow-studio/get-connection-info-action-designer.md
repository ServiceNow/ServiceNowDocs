---
title: Get Connection Info step
description: Provide the connection and credential details from another step, such as a REST step, to other steps in your action.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Get Connection Info step

Provide the connection and credential details from another step, such as a REST step, to other steps in your action.

**Note:** The Get Connection Info step is not available in the base system and requires the subscription to Integration Hub Starter Pack Installer \(com.glide.hub.integrations\) or later. For more information about the ServiceNow® Integration Hub subscription packages, see [Integration Hub usage and subscription](https://www.servicenow.com/docs/access?context=subscription-usage&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US). After the required plugin is activated, the step is visible under Integrations.

## Roles and availability

After setting up your Integration Hub Starter subscription, the Get Connection Info step is available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with the Get Connection Info step.

## Inputs

Provide a value for each input that your step needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

<table id="table_hzr_ngz_lnb"><thead><tr><th>

Input

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Choice

</td><td>

Choose from:-   Connection Alias - Associates to connection information required to connect to the remote system.
-   Credential Alias - Associates to credential data required to connect to the remote system.

Depending on which option you choose, the following input requires that you choose the appropriate Connection Alias or Credential Alias.

</td></tr></tbody>
</table>## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your action.

|Output|Data type|Description|
|------|---------|-----------|
|Runtime Alias ID|String|Sys ID of the Connection Alias or Credential Alias record used to connect to the remote system.|
|Connection ID|String|Sys ID of the Connection record used to connect to the remote system.|
|Connection URL|String|URL used to connect to the remote system.|
|Credential ID|String|Sys ID of the Credential record used to connect to the remote system.|
|Credential Value|Password \(2 Way Encrypted\)|2-way encrypted password used to authenticate when connecting to the remote system.|

## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

