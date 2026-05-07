---
title: Integrate Dynatrace with basic authentication
description: Integrate Dynatrace with Event Management by adding a standard webhook in the Dynatrace console.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Integrate Dynatrace platform events, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Dynatrace with basic authentication

Integrate Dynatrace with Event Management by adding a standard webhook in the Dynatrace console.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Ensure that configuration items for the hosts managed by Dynatrace exist in the ServiceNow AI Platform instance. These CIs can be physical or virtual and can be either manually created or discovered via IP discovery or Cloud Discovery.

Roles required: evt\_mgmt\_integration and web\_service\_admin

## About this task

Configure the Event Management environment for the collection of events from Dynatrace by authenticating Dynatrace as a data source. In your Dynatrace console, set your ServiceNow AI Platform instance as the rest endpoint using a standard webhook.

## Procedure

1.  In your Dynatrace console, define Host Naming rules:

    1.  Navigate to **Settings** &gt; **Process and contextualize** &gt; **Naming** &gt; **Host Naming**.

    2.  Define the Host Naming rules for each cloud provider \(Azure/AWS/GCP\) to uniquely identify a CI from ServiceNow.

    This ensures the ServiceNow CIs can be uniquely identified from the payload received from Dynatrace.

    **Note:** You do not need to create a Host Naming rule for VMware machines because Dynatrace manages them as physical servers.

2.  Define anomaly detection rules:

    1.  Navigate to **Settings** &gt; **Analyze and alert** &gt; **Alerts** &gt; **Hosts**.

    2.  In the **Hosts** tab, define rules on when to create alerts on the managed hosts.

3.  Define the integration settings:

    1.  Navigate to **Settings** &gt; **Analyze and alert** &gt; **Notifications** &gt; **Problem notifications**.

    2.  In the Set up custom integration form, add the Webhook URL: `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=dynatrace`

        For basic authentication, select **Create basic authorization header**. You can see the username and password fields for the user.

    3.  Enter the user name and password of the relevant user.

        **Note:** Ensure the evt\_mgmt\_integration role is assigned to the selected user. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

    4.  In the Custom payload section, add in the following payload structure for the events that will be generated.

        ```
        { 
          "connectionId": <connections_alias_sys_id>,
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

        **Note:** For the &lt;connections\_alias\_sys\_id&gt;:

        1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connection &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.
        2.  Select to open the connector for which you want to get the &lt;connections\_alias\_sys\_id&gt;.

            ![Dynatrace connection aliases list.](../image/dynatrace-connection-aliases.png)

        3.  Right-click the context menu \(![menu icon](../../../common/image/Form_MenuIcon.png)\) and then select **Copy sys\_id**.

            ![sys_id of the connection.](../image/dynatrace-static-sys-id.png)


## Result

Alerts start flowing from the Dynatrace console into the Event Management plugin. The plugin extracts information from the original Dynatrace alert message to populate the required event fields and inserts the event into the database. In your ServiceNow AI Platform instance, navigate to **All Events** to see the events.

**Note:** By default, host binding is enabled for Dynatrace events for all providers \(Azure/AWS/Google\). If all hosts in the environment are discovered using Cloud Discovery by providing credentials and discovered resources are in the cmdb\_ci\_vm\_object list, then the VM binding may not occur. To resolve this, you must enable the **Dynatrace - General** event rule. For further information about Event rules, see [Event rules](../concept/create-event-rules.md).

