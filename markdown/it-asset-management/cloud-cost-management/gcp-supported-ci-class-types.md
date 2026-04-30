---
title: Supported CI class types for Google Cloud services
description: Supported CI class types for Google Cloud enable assigning cost and usage data correctly using the CI placement process. Some CI class types are placed immediately. The CI placement process places a subset of CIs into corresponding CI tables that are used in the recommendation generation process for Cloud Cost Management.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2025-04-04"
reading_time_minutes: 1
breadcrumb: [Cloud Cost Management reference, Cloud Cost Management, IT Asset Management]
---

# Supported CI class types for Google Cloud services

Supported CI class types for Google Cloud enable assigning cost and usage data correctly using the CI placement process. Some CI class types are placed immediately. The CI placement process places a subset of CIs into corresponding CI tables that are used in the recommendation generation process for Cloud Cost Management.

**Note:** All the supported CI class types are placed after the Cumulus Unsupported CI Placement scheduled job runs daily. Some of the CI class types are placed immediately after Billing Download job execution.

|All supported CI class types|CI class types that are placed immediately after job execution|
|----------------------------|--------------------------------------------------------------|
|cmdb\_ci\_instance\_scale\_set|cmdb\_ci\_vm\_instance|
|cmdb\_ci\_vm\_instance|cmdb\_ci\_cloud\_database|
|cmdb\_ci\_cloud\_database|cmdb\_ci\_database|
|cmdb\_ci\_kubernetes\_cluster|cmdb\_ci\_storage\_volume|
|cmdb\_ci\_cloud\_load\_balancer|cmdb\_ci\_storage\_vol\_snapshot|
|cmdb\_ci\_database| |
|cmdb\_ci\_network| |
|cmdb\_ci\_storage\_vol\_snapshot| |
|cmdb\_ci\_cloud\_storage\_account| |
|cmdb\_ci\_storage\_volume| |

**Parent Topic:**[Cloud Cost Management reference](../concept/reference-cloudinsights.md)

