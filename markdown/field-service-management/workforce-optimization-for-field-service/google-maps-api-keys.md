---
title: Configuring Google Maps API keys
description: Google Maps API keys are essential for accessing and utilizing the features provided by the Google Maps Platform in Field Service Management.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up workforce, Configure, Field Service Management]
---

# Configuring Google Maps API keys

Google Maps API keys are essential for accessing and utilizing the features provided by the Google Maps Platform in Field Service Management.

As an administrator, you can set up Google Maps API keys for the FSM features.

To control map usage and manage costs effectively, enable usage limits on the account to turn off the API when the limit is reached.

If API keys are already set up, navigate to **All** &gt; **System Properties** &gt; **Google maps** to enter the API keys.

**Note:**

Google designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. For more information see, [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).

You can’t generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

If you create new Google API keys after March 1, 2025, you must enable the new APIs from Google Console and upgrade to a supported release version to ensure compatibility. For more information on the affected versions, resolution, and compatible versions, see [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf) and [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026).

## Configuration overview

The steps for setting up Google Maps API keys are:

1.  [Setting up system properties](../task/configuring-google-maps-in-fsm.md)

    Field Service Management requires Google Maps configuration for users to view maps and operate location features properly.

2.  [Setting client and server API keys](../../work-management/reference/google-maps-apis-and-fsm-capabilities.md)

    Field Service requires Google Maps API configuration for users to operate location features properly.


