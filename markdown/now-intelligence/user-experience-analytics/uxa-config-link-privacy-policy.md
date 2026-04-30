---
title: Configure link to your privacy policy
description: When User Experience Analytics is enabled, the ServiceNow Services Privacy Statement is linked by default. However, administrators can update the link to point to the organization privacy policy.
locale: en-US
release: zurich
product: User Experience Analytics
classification: user-experience-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [How users consent to tracking in User Experience Analytics, User privacy, tracking, and consent, Configure, User Experience Analytics, Platform Analytics]
---

# Configure link to your privacy policy

When User Experience Analytics is enabled, the ServiceNow Services Privacy Statement is linked by default. However, administrators can update the link to point to the organization privacy policy.

## Before you begin

Role required: admin

Users can choose to enable or turn off tracking in their settings. To learn more about enabling tracking, see [How users consent to tracking in User Experience Analytics](user-exp-analytics-user-set.md).

To learn more about the default privacy statement, see the [ServiceNow Services Statement](https://www.servicenow.com/service-privacy.html).

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Find the system property **glide.analytics.privacy.link**.

3.  Select **glide.analytics.privacy.link**.

4.  In the **Value** field, replace the existing URL with the URL of your company's privacy statement.

5.  Select **Update**.


**Parent Topic:**[How users consent to tracking in User Experience Analytics](user-exp-analytics-user-set.md)

