---
title: Tracking controls and data collection behavior
description: Understand what happens when you opt out of the consent pop-up in the Usage Insights UI
locale: en-US
release: australia
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2026-04-27"
reading_time_minutes: 1
breadcrumb: [Types of tracking consent policies, User privacy, tracking, and consent, Configuring Usage Insights, Usage Insights, Platform Analytics]
---

# Tracking controls and data collection behavior

Understand what happens when you opt out of the consent pop-up in the Usage Insights UI

When an end-user opts out of data collection via the consent pop-up in their Usage Insights UI, their individual session timeline and interaction details are no longer visible in the Usage Insights dashboard. However, their hashed user ID and session data continue to be collected and included in aggregate metrics \(such as Active Users, Sessions, and Average Session Duration\) so that these counts remain accurate. This is called Basic Tracking.

The consent pop-up remains a transparency and compliance tool. Customers can configure the consent message language and link to their own privacy policy. The pop-up is not required by default but can be enabled per the customer's compliance requirements.

When an admin disables Usage Insights on the instance \(via the glide.analytics.enabled system property\), the Usage Insights dashboard is no longer accessible and no analytics data is displayed. The behavior is functionally the same as opting out via the consent pop-up: underlying data is still collected to support aggregate metric calculations.

**Note:** To fully disable all Usage Insights data collection for an instance, contact ServiceNow® Support by creating a case through Now Support \(support.servicenow.com\). Note that fully disabling data collection means the instance will no longer contribute to aggregated usage metrics used to monitor service health, facilitate feature delivery, and help customers benefit from the latest platform capabilities.

**Parent Topic:**[Types of tracking consent policies in Usage Insights](../reference/uxa-tracking-types.md)

