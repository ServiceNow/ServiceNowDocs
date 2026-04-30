---
title: CTI demo implementation
description: Use the CTI demo implementation to test the phone communication channel between customer service agents and external customers in a non-production instance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# CTI demo implementation

Use the CTI demo implementation to test the phone communication channel between customer service agents and external customers in a non-production instance.

Starting with the Zurich release, the Computer Telephony Integration \(CTI\) plugin is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

The CTI Softphone plugin enables softphone functions and call center capabilities. This plugin provides integration between the ServiceNow platform and the Twilio Voice service using the Notify application. This plugin can be activated any time after activating Notify.

The CTI Softphone plugin includes one OpenFrame configuration, called CTI. This configuration specifies the necessary OpenFrame window settings as well as the URL to be launched within OpenFrame.

**Note:** The included CTI configuration does not have the **Default** field enabled. You must enable this field to use the CTI configuration as the default.

