---
title: Integrate Instana with OAuth authentication
description: Integrate Instana with Event Management with ServiceNow using OAuth authentication.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Integrate Instana events, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Instana with OAuth authentication

Integrate Instana with Event Management with ServiceNow using OAuth authentication.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Role required: evt\_mgmt\_admin

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
2.  In the Instana console, navigate to **Settings** &gt; **Events &amp; Alerts** &gt; **Alert Channels**.

3.  Open the **Add Alert Channel** drop-down list and select the **Generic Webhook** option.

4.  In the **Webhook URLs** field, create an alert channel by entering the following URL:

    `https://<instance>.service-now.com/api/sn_em_connector/em/inbound_event?source=instana`.

5.  Enable the **Enable OAuth** toggle switch to authenticate the ServiceNow URL.

    1.  In the **Client ID** field, provide the client id value of the OAuth Entity Client created in ServiceNow instance.
    2.  In the **Client Secret** field, provide the client secret value of the OAuth Entity Client created in ServiceNow instance.
    3.  In the **Token URL** field, enter `https://<instance_name>.servicenow.com/oauth_token.do`
    4.  To test the integration, select **Test channel**
    5.  Select **Save**.
6.  Configure Instana to create alerts for event types or events.

    1.  Navigate to **Settings** &gt; **Events &amp; Alerts** &gt; **Alerts**.

    2.  Select **New Alert**.

    3.  In the **Events** section, select one of the following:

        -   Alert on Event Type\(s\)
        -   Alert on Event\(s\)
    4.  When creating alerts for event types:

        1.  Select the type of events for which you want alerts to be created, such as **Critical Issues**, **All Incidents**, **Warning issues**, and so forth.
        2.  In the **Alerting** section, select the **servicenow** alert channel.
    5.  When creating alerts for events:

        1.  Select the events for which you want alerts to be created.
        2.  In the **Alerting** section, select the **servicenow** alert channel.
    When Instana creates an alert, the alert is sent to the ServiceNow instance. Alerts created for the host entity are bound to the Server \(cmdb\_ci\_server\) table, and alerts created for the website entity are bound to the HTTP\(S\) \(cmdb\_ci\_endpoint\_http\) table.

    Add other entity types in the Instana - ci\_type Event Field Mapping table to ensure that the entity binds with the correct CI in the ServiceNow instance.

7.  To view the event in the Instana source system, you can access it from a ServiceNow instance:

    1.  Navigate to **All** &gt; **Event Management** &gt; **Service Operations Workspace**.

    2.  Select **All Alerts**.

    3.  Select the relevant alert.

    4.  On the **Details** tab, locate the **Actions** section on the right side of the page and in the **Show Event on Instana UI** cell, select **Launch app**.


**Parent Topic:**[Integrate Instana events](../concept/instana-integration.md)

