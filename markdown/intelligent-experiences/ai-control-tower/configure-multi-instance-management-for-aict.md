---
title: Configure multi-instance management for AI Control Tower
description: Configuring Multi-instance management for AI Control Tower.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, AI Control Tower, Enable AI experiences]
---

# Configure multi-instance management for AI Control Tower

Configuring Multi-instance management for AI Control Tower.

## Before you begin

**Note:** The feature is available on Yokohama release onwards.

This feature isn’t supported on Government Community Cloud \(GCC\) and on-premises instances.

Role required: AI steward \[sn\_ai\_governance.ai\_steward\]

## About this task

**Note:** Make sure the plugin com.glide.mif.mtls is active. If it isn’t active, install the plugin com.glide.mif.mtls by submitting a support request with Now support for MIF features.

## Procedure

1.  Log in to all sub-prods and select your prod \(managed\) instance as manager for the AI Control Tower application.

2.  To verify the first step, log in to the prod instance and navigate to the managed instances tab under Multi-instance setup page to view all the sub-prods \(managed\) instances.


## Result

Multi-instance management is configured for the AI Control Tower.

For more information about Trust configuration and Trust configuration management, see [Cross-instance application trust configuration](https://www.servicenow.com/docs/access?context=grant-access-v2&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

For more information about AI asset synchronization process, see [Multi-instance Setup](../concept/multi-instance-management.md) section under Exploring the AI Control Tower configurations.

