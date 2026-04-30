---
title: Setup steps for emergency notification
description: Setting up the Emergency Notification feature requires you, as a BCM admin, to configure certain pre-requisite data. The setup steps help you to establish a consistent connection with Everbridge and a successful notification delivery workflow on the Everbridge side.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrating Crisis Management with Everbridge, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Setup steps for emergency notification

Setting up the Emergency Notification feature requires you, as a BCM admin, to configure certain pre-requisite data. The setup steps help you to establish a consistent connection with Everbridge and a successful notification delivery workflow on the Everbridge side.

The following configurations are required to be set up for different users to use the Crisis Management workspace for sending an emergency notification and monitoring the notification workflow:

-   To create a connection and authenticate your credentials with Everbridge, see [Create connection and authenticate credential with Everbridge](../task/setup-connection-everbridge.md).
-   To get the delivery details of the contacts from Everbridge and use them to send notification, see [Import delivery channels from Everbridge](../task/setup-delivery-channel-everbridge.md).
-   To get the details about the type of contacts from Everbridge, see [Import record types from Everbridge](../task/record-types-everbridge.md).
-   To pre-configure a notification template to send an email or SMS to your contacts, see [Define a template for emergency notification](../task/setup-notification-template-bcm.md).
-   To create contacts for sending the notification, see [Create contacts for emergency notifications](../task/create-contact-rules-emergency-notifications.md).
-   To set up rules in filtering the contacts from the user table, see [Create contact import rules](../task/contact-import-sync-rule.md).
-   To create a group of contacts, see [Create a notification contact group](../task/create-notification-contact-group.md).

Here is a flow diagram that shows how the different setup steps are connected for the integration:

![Emergency notification setup flow.](../image/SetupFlowDiagram.png "Emergency notification setup flow")

-   **[Create connection and authenticate credential with Everbridge](../task/setup-connection-everbridge.md)**  
As a first step, establish a connection and authenticate your login credentials with an Everbridge instance to send out a notification using a delivery channel. This connection not only helps you to send but also receive communications.
-   **[Import delivery channels from Everbridge](../task/setup-delivery-channel-everbridge.md)**  
After setting up the connection and credentials with Everbridge, you must import the delivery channels from Everbridge. Sending notifications is made easier through these delivery channels.
-   **[Import record types from Everbridge](../task/record-types-everbridge.md)**  
Import the record types for your organization ID from Everbridge and use them to create contacts.
-   **[Define a template for emergency notification](../task/setup-notification-template-bcm.md)**  
Create a template with pre-defined information that you can use to send notification quickly to your users in an emergency.
-   **[Create contacts for emergency notifications](../task/create-contact-rules-emergency-notifications.md)**  
Use the ServiceNow users list to create contacts manually and synchronize the contacts with Everbridge to send emergency notifications.
-   **[Create a notification contact group](../task/create-notification-contact-group.md)**  
Create a notification contact group using the ServiceNow AI Platform groups. Use the group members as contacts for emergency notification. Synchronize the group members as contacts with Everbridge and track the non-synchronized members as exceptions.

**Parent Topic:**[Integrating Crisis Management with Everbridge](BCM-integration-everbridge.md)

