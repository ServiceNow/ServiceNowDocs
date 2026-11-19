---
title: Setup for Everbridge notifications
description: The setup steps help you to establish a consistent connection and successful notification delivery workflow with Everbridge notifications system. BCM administrators and application users must configure certain pre-requisite data so that you can set up emergency notifications in BCM UIB Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/setup-steps-for-emergency-notification-uib-ws.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Setup for Everbridge notifications

The setup steps help you to establish a consistent connection and successful notification delivery workflow with Everbridge notifications system. BCM administrators and application users must configure certain pre-requisite data so that you can set up emergency notifications in BCM UIB Workspace.

These pre-requisite configurations must be set up for sending an emergency notification and monitoring the notification workflow:

-   To create a connection and authenticate your credentials with Everbridge, see [Create connections and authenticate their credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-conn-auth-cred-Everbridge-uib-ws.md).
-   To get the delivery details of the contacts from Everbridge and use them to send a notification, see [Import the delivery channels from Everbridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/import-delivery-channels-from-everbridge-uib-ws.md).
-   To get the details about the type of contacts from Everbridge, see [Import record types from Everbridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/import-record-types-from-everbridge-uib-ws.md).
-   To pre-configure a notification template to send an email or SMS to your contacts, see [Create templates for emergency notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/define-template-emergency-noti-uib-ws.md).
-   To create contacts for sending the notification, see [Create contacts for emergency notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-contacts-emergency-noti-uib-ws.md).
-   To set up rules in filtering the contacts from the user table, see [Create the contact import rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-contact-import-rules.md).
-   To create a group of contacts, see [Create notification contact groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-notification-contact-group-uib-ws.md).

Here is a flow diagram that shows how the different setup steps are connected for the integration:

\[Omitted image "SetupFlowDiagram.png"\] Alt text: Setup flow for an emergency notification.

-   **[Create connections and authenticate their credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-conn-auth-cred-Everbridge-uib-ws.md)**  
Establish a connection and authenticate your login credentials with an Everbridge instance. You can then send out a notification using the delivery channel. This connection helps you to send and receive communications with an Everbridge instance.
-   **[Import the delivery channels from Everbridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/import-delivery-channels-from-everbridge-uib-ws.md)**  
Import the delivery channels from the Everbridge instance. You can then easily send the notifications through the delivery channels.
-   **[Import record types from Everbridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/import-record-types-from-everbridge-uib-ws.md)**  
Import the record types for your organization ID from Everbridge and use them to create the contacts for notifications.
-   **[Create templates for emergency notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/define-template-emergency-noti-uib-ws.md)**  
Create a template with pre-defined information. You can then use it to send the notifications to your users in an emergency.
-   **[Create contacts for emergency notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-contacts-emergency-noti-uib-ws.md)**  
Create the contacts manually to send out an emergency notification and synchronize them with the Everbridge instance.
-   **[Create notification contact groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-notification-contact-group-uib-ws.md)**  
Create a notification contact group using the ServiceNow AI Platform groups. Use the group members as the contacts for an emergency notification. Synchronize the group members as the contacts with Everbridge and track the non-synchronized members as exceptions.

**Parent Topic:**[Configuring Business Continuity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configuring-business-continuity-management.md)

