---
title: Configure webhooks
description: Configure a webhook to subscribe to events in Threat Intelligence Security Center.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Working with Webhooks, Administer, Threat Intelligence Security Center, Security Operations]
---

# Configure webhooks

Configure a webhook to subscribe to events in Threat Intelligence Security Center.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

TISC webhooks provides the capability to integrate with security tools such as SIEM. Users can then subscribe to various events related to different artifacts such as observables or indicators or malware or threat actors. TISC notifies security tools \(such as SIEM\) when a new threat intelligence is available or any existing threat intelligence data is updated or deleted in TISC.

For example, whenever a new observable is added in threat intelligence then a payload request is sent to the webhook URL configuration. This payload request usually collects the observable information and provides it as additional information to security tools \(such as SIEM\).

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Webhooks Configurations** &gt; **Webhooks**.

    The Webhooks page displays.

3.  Click **New**.

<table id="choicetable_cfv_dkn_zbc"><thead><tr><th align="left" id="d44108e102">

Field

</th><th align="left" id="d44108e105">

Description

</th></tr></thead><tbody><tr><td id="d44108e111">

**Name**

</td><td>

Enter a webhook name.

</td></tr><tr><td id="d44108e120">

**Description**

</td><td>

Add the description of the webhook.

</td></tr><tr><td id="d44108e129">

**Configuration Details**

</td><td>

 

</td></tr><tr><td id="d44108e137">

**Use REST message**

</td><td>

Select **Use REST Message** check box if you need to use REST Message/REST Method functionality that is provided by ServiceNow AI Platform.If this check box is not selected, then the application uses the endpoint provided in Webhook URL to send the event information. For more information, see [Outbound REST web service](https://servicenow.com/docs/bundle/vancouver-api-reference/page/integrate/outbound-rest/concept/c_OutboundRESTWebService.html) on ServiceNow AI Platform documentation.

</td></tr><tr><td id="d44108e162">

**REST message**

</td><td>

Select the REST Message record from the list of REST message records which are already configured in the instance. For more information, see [Outbound REST web service](https://servicenow.com/docs/bundle/vancouver-api-reference/page/integrate/outbound-rest/concept/c_OutboundRESTWebService.html) on the ServiceNow AI Platform documentation.

**Note:** The REST message and REST method fields are mandatory when you select the REST message.

</td></tr><tr><td id="d44108e183">

**REST method**

</td><td>

Select REST Method from the list of available REST Methods configured for the selected REST Message. For more information, see [Outbound REST web service](https://servicenow.com/docs/bundle/vancouver-api-reference/page/integrate/outbound-rest/concept/c_OutboundRESTWebService.html) on the ServiceNow AI Platform documentation.**Note:** Only POST Rest methods are supported for webhooks.

</td></tr><tr><td id="d44108e201">

**Webhook URL**

</td><td>

A webhook endpoint is a URL that receives webhook event notifications.

</td></tr><tr><td id="d44108e210">

**Authentication Required**

</td><td>

Select this check box if the authentication is required.**Note:** This is only applicable when Webhook URL is being used to retrieve the data.

</td></tr><tr><td id="d44108e221">

**Authentication Type**

</td><td>

The authentication type for the webhook.**Note:** As of now, only Basic authentication type is supported.

</td></tr><tr><td id="d44108e232">

**Username**

</td><td>

Provide a username to your authentication type.

</td></tr><tr><td id="d44108e242">

**Password**

</td><td>

Provide a password to your authentication type.

</td></tr><tr><td id="d44108e251">

**Headers to be passed with request**

</td><td>

Any headers to be passed with the requests can be provided in Request Header Mapping. Header should be provided in key-value pair separated by colon\(':'\). Each header key value pair should be provided in a new line. For providing authentication parameters as header values, enclose the required Authentication Label with '$\{' and '\}$'. For example, username:$\{Username\}$.

</td></tr></tbody>
</table>4.  Click **Validate and Save**.

    In case if your configuration details are incorrect then the system will automatically validate the connection if configuration details are changed and then the application will prompt a warning message that the validation of the webhook is failed and you need to check the configuration details and modify it accordingly.

    **Note:**

    -   For the validation of webhook, empty request payload is sent to the endpoint and the user needs to ensure that the endpoint sends successful response code \(200\) when the empty request is passed to the configured webhook endpoint.
    -   By default, any webhook that is created will be in disabled state, you need to enable the webhook and activate it. A sample webhook is provisioned in the base system as a reference to the users.

-   **[Subscribe Triggers](subscribe-triggers.md)**  
View the list of all the subscribed webhook triggers for the current webhook.
-   **[View webhook error logs](tisc-error-logs.md)**  
Use this error logs section to view all the audit entries which are marked as error in the status for a particular webhook.
-   **[View webhook batches](../task/tisc-webhook-batch.md)**  
A webhook batch record is created for each webhook execution.

**Parent Topic:**[Working with Webhooks](tisc-webhooks.md)

**Related topics**  


[System properties for Webhooks](tisc-sysprops-retry.md)

[Webhook Triggers](tisc-triggers.md)

