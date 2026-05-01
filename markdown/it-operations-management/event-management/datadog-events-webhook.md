---
title: Integrate Datadog with basic authentication
description: Integrate Datadog with Event Management by adding a standard webhook in the Datadog console.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [Integrate Datadog platform events, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Datadog with basic authentication

Integrate Datadog with Event Management by adding a standard webhook in the Datadog console.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

-   Role required: evt\_mgmt\_integration
-   The Event Management plugin must be installed on the ServiceNow AI Platform instance.
-   Verify Configuration Items for the hosts managed by Datadog exist in ServiceNow. These CIs can be physical or virtual, and can be either manually created or discovered using IP discovery or Cloud discovery.

## About this task

Configure the Event Management environment for the collection of events from Datadog. In your Datadog console, set your ServiceNow AI Platform instance as the rest endpoint using a standard webhook.

## Procedure

1.  In the Datadog console, add cloud provider tags:

    1.  Navigate to **Menu** &gt; **Infrastructure** &gt; **Infrastructure List**

    2.  Click **Inspect** for the VM on which the Datadog agent is installed.

    3.  Click **Edit Tags** and add the cloud\_provider tag.

        The tag should be suffixed with the value of **aws**, **azure**, or **gcp** to identify the AWS, Microsoft Azure, or Google Cloud Platform \(GCP\) provider options. For example: cloud\_provider:aws

    4.  Click **Save Tags** to save the new tag.

        **Note:** Datadog adds the cloud\_provider tag by default when the Azure and Google integration is installed on the Datadog agent. Tags can also be added at the cloud provider level. Datadog collects all the tags defined at the VM level on the cloud.

2.  In the Datadog console, add a webhook:

    1.  Navigate to **Menu** &gt; **Integration** &gt; **Integrations**, and search for webhooks.

    2.  Create a webhook that includes the user ID and password of the ServiceNow user in the endpoint.

        For example, use `https://<username>:<password>@<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=datadog`.

        **Note:** Ensure that the selected user is assigned the evt\_mgmt\_integration role. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

    3.  Add in the following payload structure.

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

3.  In the Datadog console, define rules:

    1.  Navigate to **Menu** &gt; **Monitors** &gt; **Manage Monitors**, and configure rules on when to create a problem from Datadog on the managed hosts.

    2.  In the **Notify your team** section, select the webhook on which the problem should be notified.


## Result

Alerts start flowing from Datadog agents into the Event Management plugin. The plugin extracts information from the original Datadog alert message to populate the required event fields and inserts the event into the database. In your ServiceNow AI Platform instance, navigate to **All Events** to see the events.

**Note:** By default, host binding is enabled for Datadog events for \(AWS/Azure/GCP\) providers. If all hosts in the environment are discovered using Cloud Discovery by providing credentials and discovered resources are in the cmdb\_ci\_vm\_object list, then the VM binding may not occur. To resolve this, you must enable the **Datadog - General** event rule. For further information about Event rules, see [Event rules](../concept/create-event-rules.md).

