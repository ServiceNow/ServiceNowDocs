---
title: Use deep link for HR Service Delivery Integration with Cornerstone OnDemand
description: Use the deep link prefix to pull learning objects from the Cornerstone OnDemand system during run time.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up HR Service Delivery Integration with Cornerstone OnDemand, HR Service Delivery Integration with Cornerstone OnDemand, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Use deep link for HR Service Delivery Integration with Cornerstone OnDemand

Use the deep link prefix to pull learning objects from the Cornerstone OnDemand system during run time.

## Before you begin

Role required: sn\_hr\_cornerstone.admin

## Procedure

1.  Login to the Cornerstone OnDemand application and generate deep links.

    For more information, refer to the [documentation](https://help.csod.com/help/csod_0/Content/Deep_Linking/Deep_Link_Generator_Tab.htm) of Cornerstone OnDemand system.

    **Note:** Ensure that you have selected **LO Details** in **Page URL** list in the **Deep link Generator** tab.

2.  Copy the URL prefix.

3.  Navigate to **HR Cornerstone Integrations** &gt; **Source**.

4.  Click **Cornerstone**.

5.  In **Properties**, append the copied value in **url\_prefix**.


