---
title: Set up Real-Time Transcription for ServiceNow Voice for IT Service Management
description: Set up the properties in the Amazon Connect integration in order to enable Real-Time Transcription for IT Service Management.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Real Time Transcription for ServiceNow Voice for IT Service Management, Setting up ServiceNow Voice, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up Real-Time Transcription for ServiceNow Voice for IT Service Management

Set up the properties in the Amazon Connect integration in order to enable Real-Time Transcription for IT Service Management.

## Before you begin

Role required: admin

## About this task

For new deployments, the Real-Time Transcription feature is enabled during the guided setup for ServiceNow Voice.

If you have already deployed ServiceNow Voice and are upgrading, go through all of the steps for [Setting up ServiceNow Voice](../concept/ccc-setup.md), and the steps in this procedure, before completing the setup on Amazon Connect.

## Procedure

1.  Add the system property `sn_cti_itsm_cnt.enable_ims_update` and set it to **true**.

    For more information on adding a new system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

2.  Navigate to **All** &gt; **Amazon Connect integration** &gt; **View instances**.

3.  Choose your instance, and click on the **Setup guide** related link.

4.  Select the checkbox at the top of the setup guide to enable Real Time Transcription setup.

    Once you select the Real Time Transcription checkbox, agents can see the conversation panel in their workpace.

5.  Proceed through the setup guide.

    Even if you have already set up your Amazon Connect integration, you must complete the setup tasks again, due to changes in the Lambda Cloudformation Template and contact flow.

6.  In the **Setup Authentication** step, create a user with "Web Service Only access".

    This user is intended only for communication between ServiceNow and Amazon Connect.

    1.  Go to the **Roles** related list.

    2.  Edit the user, and add the role `interaction_integration_user`.

    3.  Click **OK**.


## What to do next

Proceed with the setup tasks on your Amazon Connect instance detailed in the setup guide.

**Parent Topic:**[Configure Real Time Transcription for ServiceNow Voice for IT Service Management](configure-rtt-sn-voice-itsm.md)

