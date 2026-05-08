---
title: Configure a webhook
description: Integrate with a webhook to connect to an external event source and push event information to your ServiceNow instance.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure a webhook

Integrate with a webhook to connect to an external event source and push event information to your ServiceNow instance.

## Before you begin

The plugins listed in the following table must be installed.

|Plugin|Plugin ID|Plugin description|
|------|---------|------------------|
|TSOM Event Management Connectors|sn\_tsom\_em\_connectors|TSOM Assurance Connectors for events and metrics|
|TSOM Event Management Core|sn\_tsom\_em\_core|TSOM Assurance Core features|

Role required: TSOM Assurance admin

## Procedure

1.  Navigate to &gt; **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation pane, select the Integrations Launchpad icon ![](../images/integrations_launchpad_icon.png).

3.  Select the **Browse Integrations** tab

4.  Search for the desired integration \(for example, Meraki or Fortinet\).

5.  Select the integration tile labeled **Events**.

6.  On the Provide details page, provide details about the connector type.

    1.  In the **Connector name** field, enter a unique name for the connector type.

    2.  In the **Tags** field, enter tags to help locate and identify connectors of this type on the Express List.

    3.  Add additional tags.

        1.  Select the plus sign next to the **Tags** field.
        2.  In the Add tags window, provide the tag key and tag value.
        3.  Select **Add**.
    4.  In the **Description** field, enter information to help identify this connector type.

    5.  Verify that the vendor name in the **Source** field is correct.

    6.  From the **Assignment group** drop-down list, select the group or team that is responsible for managing and maintaining the Push connector.

    7.  Select **Next**.

7.  On the Set-up push connector page, copy the auto-generated URL parameter value to the clipboard by selecting **Copy to clipboard** in the **URL parameter value** field.

    This URL is automatically generated.

8.  Follow the instructions on the page to integrate your third-party connector with Event Management.

9.  Select **Activate**.

10. In the confirmation message, select **OK**.

11. In the **Details** tab, view the connector details.

    The connector is saved and a notification is sent after the connector is active.

12. After you receive a notification that the connector is active, confirm the successful configuration of the push connector and the flow of events into the system by selecting the **Events** tab.

    Incoming events might take a few minutes to appear in the dashboard.


**Parent Topic:**[Configure Telecom Assurance](../concept/set-up-fault-management.md)

**Related topics**  


[Exploring Event Management](https://www.servicenow.com/docs/access?context=exploring-event-management&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

