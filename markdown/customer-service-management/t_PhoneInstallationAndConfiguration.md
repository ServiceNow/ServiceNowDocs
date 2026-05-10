---
title: Configure the CTI demo
description: Before the phone communication channel between customer service agents and external customers can be used, the Notify, CTI Softphone, Customer Service Management, and Openframe plugins must be activated and configured, and a Twilio Voice account must be set up.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CTI demo implementation, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Configure the CTI demo

Before the phone communication channel between customer service agents and external customers can be used, the Notify, CTI Softphone, Customer Service Management, and Openframe plugins must be activated and configured, and a Twilio Voice account must be set up.

## Before you begin

Role required: admin

## Procedure

1.  [Activate Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/t_ActivateNotify.md) \(com.snc.notify\).

2.  Set up a Twilio Voice account.

    You can create an account at `https://www.twilio.com`.

3.  [Configure Notify with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/t_ConfigureNotifyWithTwilio.md).

4.  [Activate the CTI Softphone plugin \(com.snc.cti\)](../reference/r_CustServMgmtAddtlPluginsTable.md).

    If you want to load the demo data for CTI Softphone, you must also activate the Customer Service CTI Demo Data plugin \(com.snc.customerservice\_cti\_demo\). This demo data includes sample workflows.

5.  [Activate the Customer Service plugin \(com.sn\_customerservice\)](t_ActivateCustomerService.md).

6.  Activate the Openframe plugin \(com.sn\_openframe\).

    Activating the Customer Service Management plugin automatically activates the Openframe plugin.

7.  Create an [OpenFrame configuration](t_CreateAnOpenFrameConfiguration.md) or use the default CTI configuration by enabling the **Default** field.


