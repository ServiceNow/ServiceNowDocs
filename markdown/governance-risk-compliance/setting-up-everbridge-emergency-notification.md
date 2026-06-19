---
title: Setup steps for emergency notification
description: Setting up the Emergency Notification feature requires you, as a BCM admin, to configure certain pre-requisite data. The setup steps help you to establish a consistent connection with Everbridge and a successful notification delivery workflow on the Everbridge side.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/setting-up-everbridge-emergency-notification.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrating Crisis Management with Everbridge, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Setup steps for emergency notification

Setting up the Emergency Notification feature requires you, as a BCM admin, to configure certain pre-requisite data. The setup steps help you to establish a consistent connection with Everbridge and a successful notification delivery workflow on the Everbridge side.

These configurations are required to be set up for different users to use the Crisis Management workspace for sending an emergency notification and monitoring the notification workflow:

-   To create a connection and authenticate your credentials with Everbridge, see [Create connection and authenticate credential with Everbridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/setup-connection-everbridge.md).
-   To get the delivery details of the contacts from Everbridge and use them to send notification, see [Import delivery channels from Everbridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/setup-delivery-channel-everbridge.md).
-   To get the details about the type of contacts from Everbridge, see [Import record types from Everbridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/record-types-everbridge.md).
-   To pre-configure a notification template to send an email or SMS to your contacts, see [Define a template for emergency notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/setup-notification-template-bcm.md).
-   To create contacts for sending the notification, see [Create contacts for emergency notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-contact-rules-emergency-notifications.md).
-   To set up rules in filtering the contacts from the user table, see [Create contact import rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/contact-import-sync-rule.md).
-   To create a group of contacts, see [Create a notification contact group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-notification-contact-group.md).

Here is a flow diagram that shows how the different setup steps are connected for the integration:

\[Omitted image "SetupFlowDiagram.png"\] Alt text: Emergency notification setup flow.

