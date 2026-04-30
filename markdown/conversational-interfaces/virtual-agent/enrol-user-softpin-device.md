---
title: Enroll user Soft PIN and Device in ServiceNow instance
description: Enroll the user Soft PIN and Device in your ServiceNow instance to setup callback authentication.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Conversational IVR with Amazon Connect, Configuring Conversational IVR with Amazon Connect, Conversational IVR with Amazon Connect, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Enroll user Soft PIN and Device in ServiceNow instance

Enroll the user Soft PIN and Device in your ServiceNow instance to setup callback authentication.

## Before you begin

Role required: admin

## Procedure

1.  Log in to your ServiceNow instance.

2.  Impersonate the user whose Soft PIN and Device must be authenticated.

3.  Navigate to **Password Reset** &gt; **Enroll**.

4.  In the SoftPin Verification for Amazon Connect tab, provide the soft Pin in the **Enter the SoftPIN** field and click **Submit**.

5.  In the SMS Verification for Amazon Connect tab, authorize the user device.

    1.  Select **Add Device**.

    2.  On the form, fill in the details.

        |Field|Description|
        |-----|-----------|
        |Device name|Name of the device that you are authenticating.|
        |Phone number|Phone number of the user that you want to authenticate.|
        |Service provider|Name of the service provider that you want to authenticate the device with.|

    3.  Click **Submit**.


## What to do next

After adding the phone number, verify the device. An OTP is sent to the user's phone number.

**Parent Topic:**[Configure Conversational IVR with Amazon Connect](configure-va-ivr.md)

