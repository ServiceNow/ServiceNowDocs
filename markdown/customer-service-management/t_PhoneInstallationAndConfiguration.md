---
title: Configure the CTI demo
description: Before the phone communication channel between customer service agents and external customers can be used, the Notify, CTI Softphone, Customer Service Management, and Openframe plugins must be activated and configured, and a Twilio Voice account must be set up.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/t\_PhoneInstallationAndConfiguration.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CTI demo implementation, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Configure the CTI demo

Before the phone communication channel between customer service agents and external customers can be used, the Notify, CTI Softphone, Customer Service Management, and Openframe plugins must be activated and configured, and a Twilio Voice account must be set up.

## Before you begin

Role required: admin

## Procedure

1.  Activate Notify \(com.snc.notify\).

2.  Set up a Twilio Voice account.

    You can create an account at `https://www.twilio.com`.

3.  Configure Notify with Twilio.

4.  [Activate the CTI Softphone plugin \(com.snc.cti\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/r_CustServMgmtAddtlPluginsTable.md).

    If you want to load the demo data for CTI Softphone, you must also activate the Customer Service CTI Demo Data plugin \(com.snc.customerservice\_cti\_demo\). This demo data includes sample workflows.

5.  [Activate the Customer Service plugin \(com.sn\_customerservice\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_ActivateCustomerService.md).

6.  Activate the Openframe plugin \(com.sn\_openframe\).

    Activating the Customer Service Management plugin automatically activates the Openframe plugin.

7.  Create an [OpenFrame configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_CreateAnOpenFrameConfiguration.md) or use the default CTI configuration by enabling the **Default** field.


