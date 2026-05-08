---
title: Integrate Grafana with OAuth authentication
description: Integrate Grafana with Event Management with ServiceNow using OAuth authentication.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 3
breadcrumb: [Integrate Grafana events, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Grafana with OAuth authentication

Integrate Grafana with Event Management with ServiceNow using OAuth authentication.

## Before you begin

-   Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.
-   The Event Management plugin must be installed on the ServiceNow AI Platform instance.
-   The CI binding happens through the IP, instances should be discovered as servers to initiate the binding. CIs discovered through cloud or CIs in **cmdb\_ci\_vm\_object** don’t get bounded as Grafana doesn't provide any information for object IDs.
-   Role required: evt\_mgmt\_integration

## About this task

Configure the Event Management environment for the collection of events from Grafana. In your Grafana console, set your ServiceNow AI Platform instance as the rest endpoint using a standard webhook.

Perform the following steps for Grafana v9.3.2 to send event to ServiceNow.

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

            The user must have the evt\_mgmt\_integration role that will be used to create the events sent by Grafana.

            **Note:** To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

        8.  Set **Default Grant Type** field value to **Client Credentials**.
2.  In the Grafana console, create a contact point.

    1.  Navigate to **Alerts &amp;IRM** &gt; **Alerting** &gt; **Contact Points**.

    2.  Select **New Contact Point**, enter a name, and select the type as **Webhook**.

    3.  Enter a URL.

        For example, use `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=grafana`.

    4.  In the **Optional WebHook** settings, set the HTTP Method as **POST**.

    5.  In **HTTP Config**, select **+Add**.

    6.  In **OAuth2**, select **+Add**.

    7.  Provide token URL as: `https://<instance_name>.servicenow.com/oauth_token.do`.

    8.  Provide the value for **Client ID** with the client id of the OAuth Entity Client created in ServiceNow instance.

    9.  Provide **Client secret** with the client secret of the OAuth Entity Client created in ServiceNow instance.

    10. Select **Save Contact point**.

3.  In the Grafana console, create a notification policy.

    1.  Navigate to **Alerting** &gt; **Notification Policies**.

    2.  Select **New Policy**, add matchers.

        Matchers are labels that direct alert rules to the contact point.

    3.  Select your contact point.

    4.  Select **Save Policy**.

4.  In the Grafana console, create alert rules.

    1.  Navigate to **Alerting** &gt; **Alert Rule**.

    2.  Select **New Rule**.

    3.  Set the Query and Alert Condition.

    4.  Set the data source, metrics, and the necessary filters.

    5.  Set the alert evaluation behavior.

    6.  Enter the rule name.

    7.  In the summary and annotations section, add a summary or a description.

    8.  From the scroll down, select **+Add New**.

    9.  Enter the node, resource, and metric information.

        This information is required for the node, resource, and metric\_name fields for the event.

        **Note:** Use the value string to pass these values. For example, a node can be \{\{ $values.C0.Labels.instance \}\}.

    10. Under custom labels, provide the required labels to direct your notifications to the appropriate contact point.

        **Note:** You can also pass the severity under custom labels. The same is used for events. The available severity options are: critical, major, minor, warning.

    11. Click **Save**.


## Result

Alerts start flowing from Grafana into the Event Management plugin. The plugin extracts information from the original Grafana alert message to populate the required event fields and inserts the event into the database. In your ServiceNow AI Platform instance, navigate to **All Events** to see the events.

A severity parameter is added which is used only for Grafana 8 and above. The provided value is used as a severity for an event if the severity isn’t passed in custom labels.

**Parent Topic:**[Integrate Grafana events](../concept/grafana-integration.md)

