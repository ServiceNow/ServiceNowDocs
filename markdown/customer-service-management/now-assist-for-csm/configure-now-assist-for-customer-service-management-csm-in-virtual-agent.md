---
title: Configure Now Assist for Customer Service Management \(CSM\) in Virtual Agent
description: Use Now Assist for CSM in Virtual Agent to provide users a content-driven generative AI experience.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# Configure Now Assist for Customer Service Management \(CSM\) in Virtual Agent

Use Now Assist for CSM in Virtual Agent to provide users a content-driven generative AI experience.

## Before you begin

Role required: admin

To ensure LLM-based appointment booking works in Customer Service Management, the following apps are required:

## About this task

There are 6 main steps to configure Now Assist for CSM in Virtual Agent:

1.  [Activate Virtual Agent for Customer Service Management \(CSM\).](../task/activate-virtual-agent-csm.md)
2.  [Configure Now Assist in Virtual Agent.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md)
3.  [Install Conversational Appointment Booking.](../task/conv_appt_booking_install.md)
4.  [Enable Walk-up Experience Appointment Booking.](csm-walkup-appt-booking.md)
5.  [Configure API credentials for OpenAI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/configure-api-credentials-for-openai.md).
6.  Enable Schedule a Walk-up Appointment topic in the Virtual Agent.

## Procedure

1.  Navigate to **All** &gt; **Conversational interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Locate and select **Schedule a Walk-up Appointment** topic under Now LLM.

3.  Select the **Properties** tab.

4.  Locate the check box labeled Now Assist for Virtual Agent under Select LLM assistant to make topic available.

5.  Select **Save**.

6.  Select **Publish**.


## Result

The topic is available and active in the chat window.

