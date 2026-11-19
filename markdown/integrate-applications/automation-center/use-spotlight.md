---
title: Working with ServiceNow Spotlight
description: Use the spotlight feature to auto-calculate the score of an automation request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/integrate-applications/automation-center/use-spotlight.html
release: yokohama
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Working with ServiceNow Spotlight feature, Configuring Automation Center, Automation Center, Data and Automation]
---

# Working with ServiceNow Spotlight

Use the spotlight feature to auto-calculate the score of an automation request.

ServiceNow Spotlight calculates scores when an automation request is created or updated. It's calculated only when the automation request is in the **New** or **Deferred** state.

If there’s any special need to have a different score than the auto-computed score, you can manually update the **Score** field. When you do that:

-   The flag **Score manually altered** is turned on.
-   The Spotlight score is computed and calculated in the **Score auto calculated** field.

You can switch over to using computed score by emptying the **Score** field or setting it to 0. After you save the request record, the system will populate the Spotlight score \(if any\) in the **Score** field.

**Parent Topic:**[Working with ServiceNow Spotlight feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/automation-center/spotlight-ac.md)

