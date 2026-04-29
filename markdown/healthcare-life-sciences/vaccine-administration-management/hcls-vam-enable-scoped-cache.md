---
title: Configure VAM property to enable scoped caching
description: Use a scoped cache instead of a global cache in Vaccine Administration Management to improve application performance.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure VAM property to enable scoped caching

Use a scoped cache instead of a global cache in Vaccine Administration Management to improve application performance.

## Before you begin

Role required: admin

## About this task

Prior to the Tokyo release, the VAM application used a global cache. Existing users using a global cache who want to improve application performance by using a scoped cache must first enable it by configuring a system property.

**Note:** For new users in the Tokyo release, scoped caching is enabled by default.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  Search for `sn_vaccine_sm.enable_cache`.

3.  In the **Value** field, enter `true` to enable scoped caching.

4.  Click **Update**.


**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

