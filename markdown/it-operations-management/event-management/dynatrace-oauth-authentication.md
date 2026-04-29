---
title: Integrate Dynatrace with OAuth authentication
description: Integrate Dynatrace with Event Management by authenticating Dynatrace V1 or V2 tokens in the Dynatrace Monitor.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Integrate Dynatrace platform events, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Dynatrace with OAuth authentication

Integrate Dynatrace with Event Management by authenticating Dynatrace V1 or V2 tokens in the Dynatrace Monitor.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

The Event Management plugin must be installed on the ServiceNow AI Platform instance.

Verify Configuration Items for the hosts managed by Dynatrace exist in ServiceNow. These CIs can be physical or virtual, and can be either manually created or discovered using IP discovery or Cloud discovery.

Role required: evt\_mgmt\_integration

## About this task

Dynatrace integration with OAuth authentication is available starting from the Washington DC platform release or later.

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

            The user must have the evt\_mgmt\_integration role that will be used to create the events sent by Dynatrace.

            **Note:** To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

        8.  Set **Default Grant Type** field value to **Client Credentials**.
2.  In the Dynatrace console, define the integration settings.

    1.  Navigate to **Settings** &gt; **Integration** &gt; **Problem notifications** &gt; **Set up notifications**.
    2.  In the Set up custom integration form, webhook URL.

        `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=dynatrace`

    3.  Enable **Use OAuth 2.0 for authentication**.
    4.  In the OAuth 2.0 credentials section, perform the following steps.
        1.  Provide Access token URL as `https://<instance_name>.service-now.com/oauth_token.do`.
        2.  Provide the value for **Client ID** with the client id of the OAuth Entity Client created in ServiceNow instance.
        3.  Provide “Client secret” with the client secret of the OAuth Entity Client created in ServiceNow instance.
        4.  Select **Save**.
    5.  In the Custom payload section, add in the following payload structure for the events that will be generated. Ensure that `ImpactedEntities` and `ProblemDetailsJSONv2` are passed as JSON objects, not strings.

        ```
        { 
          "ImpactedEntities": {ImpactedEntities}, 
          "ImpactedEntity": "{ImpactedEntity}", 
          "PID": "{PID}", 
          "ProblemDetailsHTML": "{ProblemDetailsHTML}", 
          "ProblemDetailsJSONv2": {ProblemDetailsJSONv2},  
          "ProblemDetailsMarkdown": "{ProblemDetailsMarkdown}", 
          "ProblemDetailsText": "{ProblemDetailsText}", 
          "ProblemID": "{ProblemID}", 
          "ProblemImpact": "{ProblemImpact}", 
          "ProblemSeverity": "{ProblemSeverity}", 
          "ProblemTitle": "{ProblemTitle}", 
          "ProblemURL": "{ProblemURL}", 
          "State": "{State}", 
          "Tags": "{Tags}" 
        }
        ```


## Result

Alerts start flowing from Dynatrace agents into the Event Management plugin. The plugin extracts information from the original Dynatrace alert message to populate the required event fields and inserts the event into the database. In your ServiceNow AI Platform instance, navigate to All Events to see the events.

**Note:** By default, host binding is enabled for Dynatrace events for \(AWS/Azure/GCP\) providers. If all hosts in the environment are discovered using Cloud Discovery by providing credentials and discovered resources are in the cmdb\_ci\_vm\_object list, then the VM binding may not occur. To resolve this, you must enable the Dynatrace - General event rule. For further information about Event rules, see [Event rules](../concept/create-event-rules.md).

