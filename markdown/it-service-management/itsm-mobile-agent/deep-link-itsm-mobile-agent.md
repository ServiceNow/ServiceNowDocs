---
title: Add deep linking support to ITSM Mobile Agent
description: Deep linking enables instances to support direct communication to a messaging application from a particular record in the system.
locale: en-US
release: zurich
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Collaboration Services for ITSM Mobile Agent, Explore, ITSM Mobile Agent, IT Service Management]
---

# Add deep linking support to ITSM Mobile Agent

Deep linking enables instances to support direct communication to a messaging application from a particular record in the system.

## Before you begin

Role required: itil, itil\_admin, or admin

## About this task

You need to assign the deep linking support on the Mobile Studio.

## Procedure

1.  Log in to your instance.

2.  In the Navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

3.  Open the record for **glide.sg.allowed\_external\_deeplinks**.

4.  In the form, match the following values:

    |Field|Value|
    |-----|-----|
    |Name|glide.sg.allowed\_external\_deeplinks|
    |Type|String|
    |Value|Slack,Teams|

5.  Click **Save**.


