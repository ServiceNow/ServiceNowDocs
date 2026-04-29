---
title: Configure Conversational Appointment Booking
description: Install and set up the Conversational Appointment Booking application to enable customers to book, reschedule, or cancel an appointment with a Virtual Agent.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up self-service, Configure, Customer Service Management]
---

# Configure Conversational Appointment Booking

Install and set up the Conversational Appointment Booking application to enable customers to book, reschedule, or cancel an appointment with a Virtual Agent.

## Before you begin

Role required: va\_admin

## About this task

This procedure provides general steps to set up the Conversational Appointment Booking application so that your customers can book appointments on your ServiceNow instance with a Virtual Agent.

## Procedure

1.  Install the Conversational Appointment Booking application.

    For more information, see [Install Conversational Appointment Booking](conv_appt_booking_install.md).

2.  Navigate to **Virtual Agent** &gt; **Designer**.

3.  Publish the following topics:

    -   Schedule a Walk-up Appointment
    -   Reschedule a Walk-up Appointment
    -   Cancel a Walk-up Appointment
    For more information, see [Publish a Virtual Agent topic](https://www.servicenow.com/docs/access?context=publish-virtual-agent-topic&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

    These topics are read-only by default. To add custom controls.

    [duplicate the topics](https://www.servicenow.com/docs/access?context=duplicate-virtual-agent-topic&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

    **Note:** Translation for custom controls is currently unavailable. You can manually add the translation in the ServiceNow® Walk-up Experience appointment booking application. See [Walk-up Experience appointment booking configuration](../concept/csm-walkup-appt-booking-config.md) for more information.

4.  Confirm that the **Appointment Booking** custom control is published.

5.  Confirm that the **Book or Update Appointment** and **Get Walk-up Location** topic blocks are published.

6.  Test the topics.

    See [Test Virtual Agent topics](https://www.servicenow.com/docs/access?context=va-designer-testing&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) for more information.


