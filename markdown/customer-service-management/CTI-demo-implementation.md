---
title: CTI demo implementation
description: Use the CTI demo implementation to test the phone communication channel between customer service agents and external customers in a non-production instance.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating with Computer Telephony Integration \(CTI\), Integrating Customer Service Management with other applications, Customer Service Management]
---

# CTI demo implementation

Use the CTI demo implementation to test the phone communication channel between customer service agents and external customers in a non-production instance.

The CTI Softphone plugin enables softphone functions and call center capabilities. This plugin provides integration between the ServiceNow platform and the Twilio Voice service using the Notify application. This plugin can be activated any time after activating Notify.

The CTI Softphone plugin includes one OpenFrame configuration, called CTI. This configuration specifies the necessary OpenFrame window settings as well as the URL to be launched within OpenFrame.

**Note:** The included CTI configuration does not have the **Default** field enabled. You must enable this field to use the CTI configuration as the default.

