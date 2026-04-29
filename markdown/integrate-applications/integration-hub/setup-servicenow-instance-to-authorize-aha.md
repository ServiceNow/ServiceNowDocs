---
title: Set up ServiceNow instance for Aha!
description: Set up your ServiceNow instance to add the Aha! Client ID and Client Secret keys.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Aha! Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up ServiceNow instance for Aha!

Set up your ServiceNow instance to add the Aha! Client ID and Client Secret keys.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Aha! spoke.
-   ServiceNow Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Aha!** and select **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Aha! spoke, select **View Details**.

        ![Connection for the Aha! spoke](../image/aha-spoke-tile.jpg)

    -   To manage more than one Aha! spoke connection records, you should create child alias record by selecting **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you're configuring the spoke for the first time, select **Configure**. Otherwise, select **Edit**.

    ![Initial connection configuration](../image/aha-spoke-configure.jpg)

5.  On the form, fill in the details.

    |Fields|Descriptions|
    |------|------------|
    |Connection Name|Name of the integration profile.|
    |Connection URL|Connection URL for Aha!.|
    |OAuth Client ID|OAuth2 key that you received while creating an OAuth2 authentication from the Aha! site.|
    |OAuth Client Secret|OAuth Client Secret key that you received while creating an OAuth2 authentication from the Aha! site.|
    |OAuth Redirect URL|ServiceNow redirect URL.|

    ![Configure a connection for the Aha! spoke](../image/aha-spoke-edit-connection.jpg)

6.  Select **Save and Get OAuth Token** and then select **Authorize**.


## Result

The Aha! spoke is set up and Aha! account is integrated with your ServiceNow instance.

