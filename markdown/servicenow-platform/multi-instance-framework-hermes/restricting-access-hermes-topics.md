---
title: Restricting access to Hermes
description: Restrict access to Hermes by IP address.
locale: en-US
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Restricting access to Hermes

Restrict access to Hermes by IP address.

You can filter client access to the Hermes cluster using the IP Address Access Control module. When IP address filtering is enabled, the system only blocks an IP address if a matching Deny rule exists and no matching Allow rule exists. By default, there are no restrictions on access to your instance.

To enable IP address filtering in the Hermes cluster, you must submit a request to Customer Service and Support.

For details on configuring access rules in the IP Address Access Control module, see [IP address access control](https://www.servicenow.com/docs/access?context=t_AccessControl&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **[Create an alert for unauthorized access](../task/create-alert-notification-hermes.md)**  
Receive a notification when an attempt to access Hermes is received from an unauthorized IP address.

**Parent Topic:**[Configuring Hermes Messaging Service](configuring-hermes-messaging-service.md)

**Related topics**  


[Activating the Hermes Messaging Service](hermes-messaging-service-activation.md)

[Set up a secure connection to the Hermes Messaging Service](../task/set-up-secure-connection-to-hermes.md)

[Revoke a Hermes certificate](../task/revoke-certificate.md)

