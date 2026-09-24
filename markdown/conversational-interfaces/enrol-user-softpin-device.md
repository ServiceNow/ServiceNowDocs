---
title: \(Legacy\) Enroll user Soft PIN and Device in ServiceNow instance
description: Enroll the user Soft PIN and Device in your ServiceNow instance to setup callback authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/enrol-user-softpin-device.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure Conversational IVR, Configure, Conversational IVR with Amazon Connect, Integrate VA for NLU with voice channels, Virtual Agent channel integrations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Enroll user Soft PIN and Device in ServiceNow instance

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

**Parent Topic:**[\(Legacy\) Configure Conversational IVR with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-va-ivr.md)

