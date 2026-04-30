---
title: Add an integration to SRM
description: Add an integration to monitor events and SLO/SLI for your service.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Available SRM integrations, Working with SRM integrations, Add a service to SRM, Working with SRM services, Using Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Add an integration to SRM

Add an integration to monitor events and SLO/SLI for your service.

## Before you begin

Role required: Responder, Manager, or Administrator

## About this task

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You are taken to your SRM homepage.

    **Note:** If you have other SOW applications, and depending on your assigned roles, that homepage may not be the SRM homepage. It is the SOW homepage instead, with SRM alerts and incidents included in your metrics. In that case, to view SRM specific areas, select SRM modules from the left navigation pane.

2.  From the left navigation pane, select the services icon \(![Services icon](../image/icon-sr-services.png)\).

3.  Select a service.

4.  Select the **Integrations** tab.

5.  Select the **Add an integration** button.

6.  Add an available integration or a new integration:

    To add an available integration:

    1.  Select the caret icon to expand the list.

    2.  Select an integration.

    To add a new integration:

    1.  Use the search bar or select a new integration from the list.

    2.  In the integration window, in **Provide details**, fill in the fields on the form, as appropriate.

        |Field|Description|
        |-----|-----------|
        |Integration name|Name for the integration.|
        |Description|Describe the integration. What it's used for.|
        |Source|Auto-populated. \(If it's empty, reload the page.\)|
        |Service|Auto-populated with the service this integration is associated with.|
        |How do you want to connect events?|Directly to the instance. \(Default.\)|
        |Service Description|Description of the overall service that helps others to understand the purpose of the service and other relevant information.|

    3.  Select **Next and save**.

        The integration is in the **Draft** state.

        Follow the instructions in the **Setup 3rd party connector** panel.

        **Note:** These instructions are unique to each vendor. We provide the url to use.

    4.  Once you have completed the third-party instructions, and are notified that it’s active, select the **Activate** button.

    5.  Select **Continue**.

        **Note:** Your integration is active, however, you still need a service user account for authentication. That account needs the `evt_mgmt_integration` role for the third-party application to push events. Contact your administrator and ask them to provide it.

        The integration is **Active** and available in your instance.


**Parent Topic:**[Available SRM integrations](../concept/sr-builtin-integrations.md)

