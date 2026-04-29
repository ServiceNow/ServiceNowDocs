---
title: Setting up a contact as a consumer
description: Set up a contact as a consumer by creating a single, unified profile that supports both the contact and consumer persona in the Customer Service Management \(CSM\) application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring a contact as a consumer, Configuring a Unified User, User management, Set up your environment, Configure, Customer Service Management]
---

# Setting up a contact as a consumer

Set up a contact as a consumer by creating a single, unified profile that supports both the contact and consumer persona in the Customer Service Management \(CSM\) application.

## Overview of unified consumer

A unified consumer is a single user profile that combines both contact and consumer persona within Customer Service Management \(CSM\). This feature eliminates the need to create and manage separate consumer user accounts for individuals who function in both roles.

The following table describes the setup procedure for activating a unified consumer:

|Task|Description|
|----|-----------|
|Update system property|Update the sn\_customerservice.consumer.allowed\_user\_types system property to display the customer\_contact extension records in the reference list. For more information, see [Activate Unified Consumer](../task/activate-unified-consumer.md).|
|Create and associate consumer user|Create and associate a contact with the consumer user. For more information, see [Create and associate a consumer user](create-and-link-a-unified-consumer-user.md).|
|Assign role to a contact|Assign role \(sn\_customerservice.consumer\) to a contact. For more information, see [Assign the consumer role to a contact](assign-the-unified-consumer-role-to-a-contact.md).|

**Related topics**  


[Configuring a contact as a consumer](configuring-a-contact-as-a-unified-consumer.md)

