---
title: Set up event forwarding
description: Create an event forwarding configuration record to enable events to flow from one ServiceNow instance to another instance. Forwarding events to multiple target instances requires creating separate configuration records for each target instance.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Event forwarding, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Set up event forwarding

Create an event forwarding configuration record to enable events to flow from one ServiceNow instance to another instance. Forwarding events to multiple target instances requires creating separate configuration records for each target instance.

## Before you begin

You must have a credential with the evt\_mgmt\_integration role, which enables you to create events in the target instance. If you don't have this credential, see [Create basic auth server credentials](create-credentials-basic-auth.md) for information on how to create it.

Role required: evt\_mgmt\_admin

## About this task

The source instance, which forwards events to a target instance, must have a user with the evt\_mgmt\_integration role, a password for the credential, and a new event forwarding record. The target instance, which receives events from the source, must have a credential with the same user name and password as the source instance.

The event forwarding record contains details about the target ServiceNow instance URL to which events are to be forwarded along with the credentials to connect it.

You must create a separate configuration record for each target instance to forward events to multiple target instances. Events are then sent to each target instance with an active event forwarding configuration.

## Procedure

1.  On your source instance, navigate to **All** and enter `sn_em_connector_event_sync_configuration.list` in the filter navigator.

2.  On the **Event Sync Configurations** page, select **New**.

3.  On the **Event Sync Configuration** page, in the **Instance url** field, enter the target ServiceNow URL to receive events in the format `https://<your_instance>.service-now.com`.

4.  In the **Credentials** field, provide the credentials for the target instance by either entering them or searching for them.

    -   To enter your credentials, start typing and then select the credential from the drop-down list.
    -   To search for your credentials, select the Lookup using list icon \(![Lookup using list icon](../image/search-icon.png)\) to select your credential from the credentials lookup table.
5.  Select **Save**.

6.  Select **Test Connection** to validate the connection to the target ServiceNow instance.

    -   If the connection succeeded, a confirmation message displays.
    -   If the connection didn't succeed, check your credentials and the instance URL.
7.  When validated, select the **Active** check box to activate the event forwarding to the target instance and select **Submit**.

    The configuration is created and is listed on the **Event Sync Configurations** page.

8.  For multiple targets, repeat the steps for a separate configuration record for each instance.


**Related topics**  


[Periodically run an event forwarding job](configuration-management-job-em.md)

