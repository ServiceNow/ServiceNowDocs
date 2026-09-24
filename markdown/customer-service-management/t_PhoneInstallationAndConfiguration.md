---
title: Configure the CTI demo
description: Activate and configure the Notify, CTI Softphone, Customer Service Management, and OpenFrame plugins to use the phone communication channel. These plugins must be activated and configured before the phone communication channel between customer service agents and external customers can be used. You must also set up a Twilio Voice account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/t\_PhoneInstallationAndConfiguration.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [CTI demo implementation, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Configure the CTI demo

Activate and configure the Notify, CTI Softphone, Customer Service Management, and OpenFrame plugins to use the phone communication channel. These plugins must be activated and configured before the phone communication channel between customer service agents and external customers can be used. You must also set up a Twilio Voice account.

## Before you begin

Role required: admin

## Procedure

1.  [Activate Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/t_ActivateNotify.md) \(com.snc.notify\).

2.  Set up a Twilio Voice account.

    You can create an account at `https://www.twilio.com`.

3.  [Configure Notify with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/t_ConfigureNotifyWithTwilio.md).

4.  Activate the CTI Softphone plugin \(com.snc.cti\).

    If you want to load the demo data for CTI Softphone, you must also activate the Customer Service CTI Demo Data plugin \(com.snc.customerservice\_cti\_demo\). This demo data includes sample workflows.

5.  [Activate the Case Management Core plugin \(com.sn\_customerservice\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/t_ActivateCustomerService.md).

6.  Activate the Openframe plugin \(com.sn\_openframe\).

    Activating the Customer Service Management plugin automatically activates the Openframe plugin.

7.  Create an [OpenFrame configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/t_CreateAnOpenFrameConfiguration.md) or use the default CTI configuration by enabling the **Default** field.


