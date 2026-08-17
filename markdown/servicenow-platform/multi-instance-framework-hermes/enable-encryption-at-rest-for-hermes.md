---
title: Enable encryption at rest for a Hermes topic
description: Enable encryption at rest on a Hermes topic to help protect message data stored on broker disks from unauthorized access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/enable-encryption-at-rest-for-hermes.html
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2026-06-26"
reading_time_minutes: 1
keywords: [encryption at rest, BYOK]
breadcrumb: [Configure, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable encryption at rest for a Hermes topic

Enable encryption at rest on a Hermes topic to help protect message data stored on broker disks from unauthorized access.

## Before you begin

-   The Cloud Encryption plugin must be installed. Because this plugin requires a subscription, contact your ServiceNow® administrator. To verify whether the Cloud Encryption plugin is active, navigate to **All** &gt; **System Plugins**, search for ServiceNow® Cloud Encryption, and confirm that the status is active.
-   At least one service that uses Hermes must be activated, for example, Stream Connect.

Role required: hermes\_admin

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Topics**.

2.  Select the topic name to open the topic record.

3.  Select **Enable Encryption**.

    The selected topic is encrypted and the button changes to **Disable Encryption**.

4.  In the topic record, verify in the Kafka Topic Override Configurations related list that the **snc.hermes.encryption.enable** property value is set to true.


**Parent Topic:**[Configuring Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/configuring-hermes-messaging-service.md)

**Related topics**  


[Activating the Hermes Messaging Service]()

[Set up a secure connection to the Hermes Messaging Service]()

[Revoke a Hermes certificate]()

[Restricting access to Hermes]()

