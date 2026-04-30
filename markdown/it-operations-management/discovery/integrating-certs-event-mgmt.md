---
title: Integrate Event Management with Certificate Inventory and Management
description: In Certificate Inventory and Management version 1.2.0 and later, Event Management can create events and alerts for both expiring and expired certificates, enhancing the system's monitoring capabilities.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Certificate integrations and notifications, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Integrate Event Management with Certificate Inventory and Management

In Certificate Inventory and Management version 1.2.0 and later, Event Management can create events and alerts for both expiring and expired certificates, enhancing the system's monitoring capabilities.

## Before you begin

Ensure the Event Management Store application is installed.

Role required: admin

## About this task

The integration leverages the Workflow Studio feature to initiate events. It utilizes a pre-existing daily Discovery schedule designed to identify expired or expiring certificates, activating a subflow. Upon subflow activation, it verifies the installation of the Event Management Store application. If the application is installed, the subflow generates an event for expiring or expired certificates.

## Procedure

1.  To view all the generated alerts or events, navigate to **All** &gt; **Event Management** &gt; **All Alerts** or **All** &gt; **Event Management** &gt; **All Events**.

2.  To exclude specific Certificate events and prevent alert triggers, navigate to **Event Management** &gt; **Rules** &gt; **Event Rules** and perform the following steps.

    1.  Select the **Certificate Expired/Expiring Events** rule.

    2.  Select the **Event Filter** tab.

    3.  Select **Ignore events that match this filter**.

    4.  Add any other necessary details as needed.

    5.  Select **Save**.


**Parent Topic:**[Certificate integrations and notifications](../concept/cert-inventory-mgmt-workflow.md)

