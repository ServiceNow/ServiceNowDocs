---
title: Configure Real Time Transcription for ServiceNow Voice for IT Service Management
description: Configure settings in your Amazon Connect instance, and in your ServiceNow instance to allow agents to see a real time transcription of voice calls with customers.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up ServiceNow Voice, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Real Time Transcription for ServiceNow Voice for IT Service Management

Configure settings in your Amazon Connect instance, and in your ServiceNow instance to allow agents to see a real time transcription of voice calls with customers.

## Before you begin

-   An Amazon Connect instance set up using the guided setup.
-   Real Time Transcription is only available for ServiceNow Voice for Customer Service Management
-   Role required: admin


## About this task

For new deployments, the Real-Time Transcription feature is enabled during the guided setup for Voice for IT Service Management.

If you have already deployed Voice for IT Service Management and are upgrading, go through all of the steps for [Setting up ServiceNow Voice](../concept/ccc-setup.md), and [Set up Real-Time Transcription for ServiceNow Voice](set-up-rtt.md) before completing the setup on Amazon Connect.

## Procedure

1.  Go to your Amazon Connect instance.

2.  Enable Contact Lens in the Amazon Connect instance.

    See the [Amazon documentation](https://docs.aws.amazon.com/connect/latest/adminguide/enable-analytics.html) for full instructions. Also refer to the [Contact Lens documentation](https://docs.aws.amazon.com/connect/latest/adminguide/contact-lens.html) for more information about Contact Lens for Amazon Connect.

    1.  On the "Set recording and analytics behavior block", enable Contact Lens.

    2.  Enable speech analytics with real-time and post-call analytics.

3.  Go to the **Setup Guide** for Amazon Connect.

4.  Complete the instructions in the Real Time Transcription section.


-   **[Set up Real-Time Transcription for ServiceNow Voice for IT Service Management](set-up-rtt-itsm.md)**  
Set up the properties in the Amazon Connect integration in order to enable Real-Time Transcription for IT Service Management.

**Parent Topic:**[Setting up ServiceNow Voice](../concept/ccc-setup.md)

