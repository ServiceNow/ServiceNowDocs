---
title: Unused resources analysis for Google Cloud
description: Cloud Cost Management uses an optimized Unused resources process for each provider.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Unused resources, Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Unused resources analysis for Google Cloud

Cloud Cost Management uses an optimized Unused resources process for each provider.

## How Unused resources analysis works for Google Cloud

The Google Cloud compute engine generates the recommendations that appear in the Unused resources reports. Cloud Cost Management displays the recommendations that the Google Cloud compute engine generates. Cloud Cost Management updates the reports whenever billing data is updated.

**Note:** The Google Cloud console may show the same resources for both Unused resources and Rightsizing recommendations. If the same resources are displayed, Cloud Cost Management shows the information in Unused resources and excludes it from the Rightsizing recommendations with the reason, `Recommendation already present in unused`.

To get the recommendations from the Google Cloud console and perform start, stop, resize, and delete operations, you must have specific roles and permissions. For detailed information on these permissions, see [Setup roles for Google Cloud billing download](../task/gcp-user-policy-create-cloudin.md).

