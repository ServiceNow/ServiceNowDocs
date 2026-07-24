---
title: Configure Conversational Appointment Booking
description: Install and set up the Conversational Appointment Booking application to enable customers to book, reschedule, or cancel an appointment with a Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-self-service-and-omnichannel-engagement/conv-appt-booking-config.html
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

**Note:** A Now Assist for CSM license must be active on your instance.

## About this task

This procedure provides general steps to set up the Conversational Appointment Booking application so that your customers can book appointments on your ServiceNow instance with a Virtual Agent.

## Procedure

1.  Install the Conversational Appointment Booking application.

    For more information, see [Install Conversational Appointment Booking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/conv_appt_booking_install.md).

2.  Navigate to **Virtual Agent** &gt; **Designer**.

3.  Publish the following topics:

    -   Walk-up Appointment Scheduling - LLM
    -   Reschedule a Walk-up Appointment
    -   Cancel a Walk-up Appointment
    For more information, see Publish a Virtual Agent topic.

    These topics are read-only by default. To add custom controls.

    duplicate the topics.

    **Note:** Translation for custom controls is currently unavailable. You can manually add the translation in the ServiceNow® Walk-up Experience appointment booking application. See [Walk-up Experience appointment booking configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/csm-walkup-appt-booking-config.md) for more information.

4.  Confirm that the **Appointment Booking** custom control is published.

5.  Confirm that the **Book or Update Appointment** and **Get Walk-up Location** topic blocks are published.

6.  Test the topics.

    See Test Virtual Agent topics for more information.


