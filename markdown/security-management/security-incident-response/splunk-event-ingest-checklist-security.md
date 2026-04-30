---
title: Checklist for Splunk Enterprise Security Notable Event Ingestion integration
description: Use this checklist to guide you through all the tasks of the integration. The following checklist includes setup and installation tasks and examples of use cases that include expected results for the integration.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Checklist for Splunk Enterprise Security Notable Event Ingestion integration

Use this checklist to guide you through all the tasks of the integration. The following checklist includes setup and installation tasks and examples of use cases that include expected results for the integration.

## Before you begin

Roles required: sn\_si.ingestion\_profile\_admin, admin, sn\_si.admin, sn\_si.analyst, Splunk Enterprise Security administrator

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

Track your progress with the setup, installation, and configuration of the integration with the following table. Complete all the tasks for a step before moving on to the next step. Each row of the table lists tasks and identifies the roles that are required to perform the tasks. Numbered topics of the installation and configuration guide are also referenced.

Roles required for each task are listed with each step in the following table.

## Procedure

1.  Track your progress with the setup, installation, and configuration of the integration.

    Complete all the tasks for a step before moving on to the next step.

2.  Follow the steps in the table in the order that they are presented.

<table id="table_f2c_xn4_sgb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

![Checkbox](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the ServiceNow AI Platform admin role, set up your ServiceNow AI Platform instance.

 -   Assign users with the **sn\_si.ingestion\_profile\_admin** \(or sn\_si.admin\) and sn\_si.analyst roles as required.
-   Install and configure a MID Server if the Splunk server is deployed within your corporate network.
-   Verify that the ServiceNow Security Incident Response plugins are activated for your release of the ServiceNow AI Platform.
-   \(Optional\) If you want to forward events manually from your Splunk Enterprise Security console into your ServiceNow AI Platform instance, verify that you have assigned the \(sn\_sec\_splunkes.api\_account\_access\) role to a user with the Splunk Enterprise Security administrator permission.
 For more information, see [Set up your ServiceNow AI Platform instance for the Splunk Enterprise Security integration](../reference/splunk-event-ingest-setup-sn-security.md).

</td></tr><tr><td>

![Checkbox](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the ServiceNow AI Platform admin role, install and configure the Splunk Enterprise Security application from the ServiceNow Store.

 1.  Download and install the application on your ServiceNow AI Platform instance.
2.  Configure the application and connect to your Splunk Enterprise Security console.
 For more information, see [Install and configure Splunk Enterprise Security Notable Event Ingestion integration](splunk-event-ingest-install-and-configure-security.md).

</td></tr><tr><td>

![Checkbox](../../vulnerability-response/image/checkbox.png)

</td><td>

\(Optional\) If you intend to export events manually from your Splunk Enterprise Security console to your ServiceNow AI Platform instance, perform the following tasks:

 -   As a Splunk Enterprise Security administrator, install, set up, and enable the ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security from splunkbase in your Splunk Enterprise Security console.
-   As a Splunk Enterprise Security administrator, if not already configured, save searches as notable events in your Splunk Enterprise Security console.


</td></tr><tr><td>

![Checkbox](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the ServiceNow AI Platform **sn\_si.ingestion\_profile\_admin** role, create and name an event profile.

 Select the profile type from the choice list. Options are a scheduled alert profile that you use to ingest sample data, or, an event profile that you use to export attachment data manually from your Splunk Enterprise Security console.

 -   For a scheduled alert, select an available alert.
-   For profile for manually exported data, create a new map or copy an existing map.
 For more information, see [Create and name an event profile for the Splunk Enterprise Security event ingestion integration](splunk-event-ingest-create-profile-security.md).

</td></tr><tr><td>

![Checkbox](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the ServiceNow AI Platform **sn\_si.ingestion\_profile\_admin** role, map values ingested or attachment data that is exported from Splunk Enterprise Security to ServiceNow AI Platform security incidents.

 1.  Fetch sample data for a scheduled alert.
2.  \(Optional\) Export attachment data manually from Splunk Enterprise Security for an event.
3.  Edit the default mapping configuration.
4.  Optionally add filtering criteria, append an alert to an existing security incident, and use the script editor.
 For more information, see [Explore Mapping](../concept/splunk-event-ingest_mapping-security.md) and [Map notable events](splunk-event-ingest-map-alerts-security.md).

</td></tr><tr><td>

![Checkbox](../../vulnerability-response/image/checkbox.png)

</td><td>

-   As a user with the ServiceNow AI Platform **sn\_si.ingestion\_profile\_admin** role, preview the data from Splunk Enterprise that is displayed on a ServiceNow AI Platform security incident.
-   Fix any errors or add any missing data so that no error messages are displayed.
 For more information, see [Preview security incident](splunk-event-ingest-preview-security.md).

</td></tr><tr><td>

![Checkbox](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the ServiceNow AI Platform **sn\_si.ingestion\_profile\_admin** role, schedule alert retrieval for a profile with a scheduled alert.

 For more information, see [Schedule and retrieve notable events](splunk-event-ingest-schedule-security.md).

</td></tr></tbody>
</table>    You have successfully completed the set up steps and verified expected results for the integration.


