---
title: Integrate Datadog with OAuth authentication
description: Integrate Datadog with Event Management by authenticating Datadog V1 or V2 tokens in the Datadog Monitor.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Integrate Datadog platform events, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Datadog with OAuth authentication

Integrate Datadog with Event Management by authenticating Datadog V1 or V2 tokens in the Datadog Monitor.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

The Event Management plugin must be installed on the ServiceNow AI Platform instance.

Verify Configuration Items for the hosts managed by Datadog exist in ServiceNow. These CIs can be physical or virtual, and can be either manually created or discovered using IP discovery or Cloud discovery.

Role required: evt\_mgmt\_integration

## About this task

Datadog integration with OAuth authentication is available starting from the Washington DC platform release or later.

## Procedure

1.  Configuration on the ServiceNow instance.

    1.  Create **glide.oauth.inbound.client.credential.grant\_type.enabled** system property to use Client Credentials grant type for OAuth inbound integrations.

        -   Type: true\|false
        -   Value: true
        **Note:** An administrator must create this system property because the evt\_mgmt\_admin role lacks permission to do so.

    2.  Create an OAuth Entity endpoint for clients to access the instance.
        1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and then select **New**.
        2.  On the interceptor page, select **Create an OAuth API endpoint for external clients** and then fill in the form.
        3.  To create an OAuth client record, select **Submit**.
    3.  Add the OAuth Application User and the Default Grant Type to the created OAuth client record.
        1.  On the OAuth Entity form, add the **OAuth Application User** and the **Default Grant Type** fields to use the Client Credentials grant type for OAuth inbound integrations.
        2.  Open the created OAuth client record.
        3.  From the page header, select the **More** options icon.
        4.  Select **Configure** &gt; **Form Layout**
        5.  On the Form Layout page, add **OAuth Application User and Default Grant Type** from the list of fields.
        6.  **Save** or **Update** the form.
        7.  For the **OAuth Application User** field, select the user.

            The user must have the evt\_mgmt\_integration role that will be used to create the events sent by Datadog.

            **Note:** To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

        8.  Set **Default Grant Type** field value to **Client Credentials**.
2.  In the Datadog console, add cloud provider tags.

    1.  Navigate to **Menu** &gt; **Infrastructure** &gt; **Infrastructure List**.
    2.  Select **Inspect** for the VM on which the Datadog agent is installed.
    3.  Select **Edit Tags** and add the cloud\_provider tag.

        The tag must be suffixed with the value of aws, azure, or gcp to identify the AWS, Microsoft Azure, or Google Cloud Platform \(GCP\) provider options. For example: cloud\_provider:aws.

    4.  Select **Save Tags**.

        **Note:** Datadog adds the cloud\_provider tag by default when the Azure and Google integration is installed on the Datadog agent. Tags can also be added at the cloud provider level. Datadog collects all the tags defined at the VM level on the cloud.

3.  In the Datadog console, add a webhook.

    1.  Navigate to **Menu** &gt; **Integration** &gt; **Integrations** and search for webhooks.
    2.  On the webhook tile, select **Configure**.
    3.  Select the **Auth Methods** tab and then select **New Auth Method**.
    4.  Enter the name and select the protocol as **OAuth 2.0 Client Credentials**.
    5.  Provide Access token URL as `https://<instance_name>.service-now.com/oauth_token.do`.
    6.  Provide the value for **Client ID** with the client id of the OAuth Entity Client created in ServiceNow instance.
    7.  Provide “Client secret” with the client secret of the OAuth Entity Client created in ServiceNow instance.
    8.  Select **Save**.
    9.  Create webhook URL as

        `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=datadog`

    10. Select the OAuth Method created in the previous steps in AuthMethod dropdown.
    11. Add in the following payload structure.

        ```
        { 
            "body": "$EVENT_MSG", 
            "last_updated": "$LAST_UPDATED", 
            "event_type": "$EVENT_TYPE", 
            "title": "$EVENT_TITLE", 
            "date": "$DATE", 
            "org": { 
                "id": "$ORG_ID", 
                "name": "$ORG_NAME" 
            }, 
            "id": "$ID", 
            "alert_id": "$ALERT_ID", 
            "alert_metric": "$ALERT_METRIC", 
            "metric_namespace": "$METRIC_NAMESPACE",
            "alert_priority": "$ALERT_PRIORITY", 
            "alert_transition": "$ALERT_TRANSITION", 
            "alert_status": "$ALERT_STATUS", 
            "alert_title": "$ALERT_TITLE", 
            "alert_type": "$ALERT_TYPE", 
            "host_name": "$HOSTNAME", 
            "priority": "$PRIORITY", 
            "tags": "$TAGS", 
            "alert_scope": "$ALERT_SCOPE" 
        }  
        
        ```


## Result

Alerts start flowing from Datadog agents into the Event Management plugin. The plugin extracts information from the original Datadog alert message to populate the required event fields and inserts the event into the database. In your ServiceNow AI Platform instance, navigate to All Events to see the events.

**Note:** By default, host binding is enabled for Datadog events for \(AWS/Azure/GCP\) providers. If all hosts in the environment are discovered using Cloud Discovery by providing credentials and discovered resources are in the cmdb\_ci\_vm\_object list, then the VM binding may not occur. To resolve this, you must enable the Datadog - General event rule. For further information about Event rules, see [Event rules](../concept/create-event-rules.md).

