---
title: Add deep linking support to ITSM Mobile Agent
description: Add deep linking support so that users can communicate through a messaging application directly from a record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/deep-link-itsm-mobile-agent.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Collaboration services for ITSM Mobile Agent, Exploring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# Add deep linking support to ITSM Mobile Agent

Add deep linking support so that users can communicate through a messaging application directly from a record.

## Before you begin

Role required: itil, itil\_admin, or admin

## About this task

You need to assign the deep linking support on the Mobile Studio.

## Procedure

1.  Log in to your instance.

2.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

3.  Open the record for **glide.sg.allowed\_external\_deeplinks**.

4.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|glide.sg.allowed\_external\_deeplinks|
    |Type|String|
    |Value|Slack,Teams|

5.  Select **Save**.


